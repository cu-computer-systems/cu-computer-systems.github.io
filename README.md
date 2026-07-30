# CU Computer Systems Lab Website

Source for the Computer Systems Research Lab site at the University of Colorado Boulder — **[systems.cs.colorado.edu](https://systems.cs.colorado.edu)**.

Built with [Jekyll](https://jekyllrb.com/) and hosted on GitHub Pages.

## Updating the Site

To request an update to any page on this site, contact **Yueqi Chen** ([yueqi.chen@colorado.edu](mailto:yueqi.chen@colorado.edu)).

If you have write access and want to make the change yourself, see [Making Changes](#making-changes) below.

## How the Site Is Built

The live site is a **single page** — `index.html` — with four anchor sections:

| Section | Anchor | Content comes from |
| --- | --- | --- |
| About | `#about` | Text written directly in `index.html` |
| Faculty | `#faculty` | `_data/faculty.yml` |
| Research Areas | `#research-areas` | `_data/researchAreas.yml`, rendered by `_includes/area.html` |
| Gallery | `#gallery` | `_data/gallery.yml` |

Nearly all content lives in the YAML files under `_data/` — you rarely need to touch HTML.

## Making Changes

### Add or edit a faculty member

Edit `_data/faculty.yml`. Entries are sorted alphabetically by last name:

```yaml
- name: Joshua Viszlai (Joining Aug 2027)
  image_url: /assets/img/faculty/jviszlai.png
  areas:
    - Quantum Computing
  website: https://jviszlai.github.io/
```

Put the photo in `assets/img/faculty/`. Only `name` is required; `image_url`, `areas`, and `website` are optional. Without `image_url` the card falls back to `assets/img/faculty/default.jpg`.

Appointment status goes in the `name` field as a parenthetical — `(Prof. Emeritus)`, `(On-Leave)`, `(Joining Aug 2027)`. The card has no separate field for titles or affiliations, and keeping every card to the same shape (photo, name, website, areas) is deliberate.

**`areas` values must exactly match a `title:` in `_data/researchAreas.yml`.** That string match is what places someone under a research area in the Research Areas section. Anything that does not match still shows on the person's card but groups them nowhere. (The `tags:` field in `researchAreas.yml` is not used by any template.)

### Edit a research area

Edit `_data/researchAreas.yml`:

```yaml
- title: Networking, Wireless & Mobile Systems
  caption: Networking, Wireless & Mobile Systems
  tags:
    - Networks
    - Wireless
  description: |
    - Markdown bullet points describing the area.
```

`title` is what faculty entries reference in their `areas:` list, so renaming a title means updating every `_data/faculty.yml` entry that used the old name. `caption` is the heading shown on the page and `description` is markdown. `tags` is unused by the templates — it is left over from an earlier version.

### Add gallery photos

Put the images in `assets/img/gallery/`, then add an entry to `_data/gallery.yml`:

```yaml
- title: Retirement BBQ
  description: The lab gave a retirement party with barbeque.
  image_url:
  - /assets/img/gallery/bbq-2.jpg
  - /assets/img/gallery/bbq-7.jpg
```

### Edit the About text or the banner

The About copy is plain HTML in `index.html`. The banner image is `assets/img/banner.jpg`.

### Site-wide settings

`_config.yml` holds the site title, description, URL, and department address. Jekyll does **not** reload this file automatically — restart the local server after editing it.

## Local Preview

Requires Ruby 3.1+ and Bundler.

```bash
bundle install
bundle exec jekyll serve
```

The site is then at <http://localhost:4000>.

If you would rather not install Ruby, you can use Docker:

```bash
docker run --rm -it -v "$PWD":/app -w /app -p 4000:4000 ruby:3.3 \
  bash -c "bundle install && bundle exec jekyll serve --host 0.0.0.0"
```

## Deployment

Pushing to **`master`** publishes the site — GitHub Pages rebuilds it automatically, usually within a minute or two. There is no separate deploy branch and no GitHub Actions workflow.

Because the build uses GitHub's own server-side Jekyll toolchain, the committed `Gemfile.lock` does **not** affect the published site. It only pins versions for local previews and is what Dependabot scans, so it is still worth keeping current:

```bash
bundle lock --update
```

The custom domain is set by the `CNAME` file (`systems.cs.colorado.edu`).

## Repository Layout

```
index.html            The live site (single page)
_config.yml           Jekyll and site settings
_data/                Site content — faculty, research areas, gallery
_includes/            Reusable template fragments
_layouts/             Page templates
assets/               CSS, JS, images
CNAME                 Custom domain
```

### Legacy files

The repo still carries material from an earlier multi-page version of the site: `about.html`, `blog.html`, `contact.html`, `projects.html`, `team.html`, the `people/` directory, and everything under `collections/`. **None of it is linked from the live site.** Some of those pages also render empty, because the collections they loop over (`site.alumni`, `site.postdocs`, `site.projects`) are not declared in `_config.yml`.

Treat these as inactive. If you want one of them back, it needs to be wired up in `_config.yml` and linked from `index.html` — editing the file alone will not make it appear.

## Credits

The design is based on the [Business Jekyll Theme](https://business-jekyll-theme.github.io) by [Melvin Ch'ng](http://melvinchng.github.io), itself a Jekyll port of the [Office](https://github.com/technext/office) template by [Technext](https://github.com/technext/).
