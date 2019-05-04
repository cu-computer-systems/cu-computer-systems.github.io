---
layout: headlines_layout
title: THIS IS YOUR PRESIDENT SPEAKING
caption: Spoofing Presidental Alerts
image_url: /assets/img/slider/lab-bench.png
image_alt: LTE Software Radio
targeturl: /headlines/cmas.html
url: /headlines/cmas.html
order_number: 1000
output: true
---

Our research shows that it is possible for a physically-proximate
attacker to spoof Wireless Emergency Alerts, including Presidential
alerts, AMBER alerts, and other imminent threat alerts to cell phones
within range. This attack can be done with commercially-available
software-defined radios costing less than $1,000, and a few
modifications to open source software. While AMBER and imminent threat
alerts can be disabled by users, Presidential Alerts cannot be turned
off by end users, making spoofed alerts a significant threat for
abuse.

While these problems have already been discussed in a 3GPP study group
previously[cite], we believe we are the first to publicly demonstrate
a practical working attack. While we release the details of our
attack, we are not releasing the code or modifications we developed to
carry out this attack. It is our hope that our demonstration of this
attack prompts carriers and manufacturers to find ways to ultimately
fix the problem.

We have disclosed our findings to cell carriers, government agencies,
and cell phone manufacturers in January 2019, and are currently in the
process of working with these groups to address this
vulnerability. Fixing this problem will require a coordinated effort
between standards bodies, cell phone makers, and carriers, and may
take years to fully roll out.

---

## Demonstration Video

---

## Paper

---

## FAQ

### Should I still trust emergency alerts?

Yes. While this attack allows nefarious attackers to spoof alerts if
they are physically close, it does not allow country-wide spoofed
alerts. Alerts can be verified through other channels, such as local
radio, TV, or the Internet.

How close does an attacker have to be to spoof alerts? What is the
range of the attack?  Our analysis shows that an attacker with a
modest 1 Watt transmitter can spoof alerts to the vast majority of
cell phones within a 1km range.

### What carriers or devices are vulnerable?

All of the devices and carrier combinations we tested were vulnerable
to this attack. Our tests involved 9 phones from 5 manufacturers
(including both iPhone/iOS and Android operating systems), and we
believe all LTE-compatible phones and carriers are currently
vulnerable to spoofed alerts.

### Why can alerts be spoofed?

Wireless Emergency Alerts are not authenticated or encrypted, and are
sent on broadcast channels in LTE, allowing an attacker to send
messages to phones within range.

### Why aren’t emergency alerts authenticated?

Specification designers chose to allow phones that had not yet
established to a network, or were roaming on an unknown carrier to
still receive alerts, without authenticating to the network. In
addition, as many alerts are sent from local municipalities, a
centralized key infrastructure would be difficult to maintain. This
design emphasizes availability at the cost of authenticity, allowing
attackers to spoof alerts.

### What can I do to stop spoofed alerts?

Unfortunately, end-users cannot disable Presidential Alerts, leaving
this as a problem that cell phone software maintainers and cell
carriers must ultimately fix. We suggest several countermeasures that
can be implemented: Signed presidential alerts - while other alerts
can be disabled and are sent from many distributed sources,
presidential alerts should only come from a single or small set of
well-defined sources, allowing simple key management procedures to be
used.  Only show messages when established - Cell phone software could
be modified to only display (presidential) alerts when connected and
authenticated to a trusted carrier.  Provide trusted URLs in alerts -
Alerts could contain an HTTPS URL to a trusted site, providing more
information and allowing users to validate the contents of the
messages.

### Is it illegal to spoof emergency alerts?

Yes. We performed our tests in realistic lab environments that were
radio isolated and shielded from outside signals to prevent our tests
from interfering with legitimate services. Conducting these attacks
against real users violates federal law and is subject to FCC fines
and criminal penalties in the United States.

### Does 5G fix this problem?

No.
