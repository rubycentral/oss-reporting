# RubyGems.org 2023 Q4 Recap

## Significant Events

### Monthly update newsletters

1. https://rubycentral.org/news/october-2023-monthly-update/
2. https://rubycentral.org/news/december-2023-newsletter/
3. https://rubycentral.org/news/january-2023-newsletter/

### Open Source Ecosystems roundtable at Google Austin, hosted by the Google Open Source Security Team

* André and Samuel attended in person
* Josef and Colby attended via Google Meet
* discussed security and sustainability challenges with maintainers from PyPi, Homebrew, Maven, PHP Composer, Google OSS Security, and others

### Full-time AWS Security Engineer Residency

https://rubycentral.org/news/ruby-central-welcomes-new-software-engineer-in-residence-sponsored-by-aws/

* AWS provided funding for 1 full time engineer
* Samuel started full-time on Dec 1
* Smooth transition from contributor to FT
* Already shipped two significant features:

## Shipped Features

### Trusted Publishing (Nov - Dec 2023)

https://blog.rubygems.org/2023/12/14/trusted-publishing.html

* Primarily work by Samuel
* Design significantly assisted by prior art from PyPI
* Trusted Publishing provides security as good as MFA, while allowing automatic build and push from GitHub Actions

### Full OIDC Support (Aug - Oct 2023)

* Arbitrary server-to-server short-term authentication
* GitHub as first supported provider
* Full support for scoped permissions based on repo, user, workflow, and other action attributes

### Webauthn / Passkey support (Sep 2022 - Dec 2023)

https://blog.rubygems.org/2023/08/03/level-up-using-security-devices.html
https://blog.rubygems.org/2023/04/11/security-device-cli-support.html
https://blog.rubygems.org/2022/12/21/introducing-hardware-security-token-and-passkey-support.html

* Passkeys as MFA second factor shipped by Shopify team
* Passkey support for CLI MFA shipped by Shopify team
* Passkeys alternative to email/password shipped by Samuel
* Full support for passkeys as primary, phishing-proof credentials (Dec 2023)

### Updated RubyGems.org to Ruby 3.3

* Fastest Ruby upgrade for RubyGems.org so far

### Talk at RubyConf 2023

https://rubycentral.org/news/state-of-the-ruby-gems/
https://www.youtube.com/watch?v=Hea-x7LHO9Y

### Talk at RubyConf Taiwan 2023

https://speakerdeck.com/segiddins/handling-225k-requests-per-second-to-rubygems-dot-org

* Also met with MRI, JRuby, TruffleRuby maintainers

## Roadmap for the upcoming quarter

These are the upcoming items we want to work on. We plan to work on them using whatever funding we have available, while using these items to demonstrate our plans and goals when soliciting contributors and funding.

### Maintenance

* 24/7 on-call rotation
* Upgrade Kubernetes, Postgres, and OpenSearch, Rails 7.1

### Security

* Significant event audit logs for gems and users
* Repository Service for The Update Framework
* GitHub action for SLSA-compliant gem build + push
* Hosted gem content files for browsing and diffs
* Hosted gem code search for maintenance and analysis
* Hosted gem security analysis to detect malware and adware and etc.

### User experience

* Visual redesign
* UI/UX tooling and design improvements, speeding up security features as well
* Hosted gem documentation (adding each gem to rubyapi.org)

## Project goals for the next year and beyond

How quickly we accomplish these projects depends entirely on the level of funding that Ruby Central is able to secure. With the single AWS residency, we expect to most likely accomplish 2 of these items during 2024, and work on the remaining items in 2025.

### Audit logging & public transparency

Allow developers and security researchers to monitor important gems by storing and publishing signed audit logs and event histories for gem permissions and gem contents.

### Organization ownership

Provide companies and groups a better story around permissions and succession planning, by adding organizations composed of multiple users, with individual permissions for each gem and user.

### Sigstore & The Update Framework

Add verifiable signatures for gems from authors and from RubyGems by implementing the sigstore.dev and theupdateframework.io systems in both the online service and the clients that install gems.

### SLSA & verified provenance

Implement SLSA level 2 (and ideally 3) across the entire RubyGems build, publish, serve, and install process. Create a secure, known build process that allows verifying not just the artifacts but the source used to create the artifacts.

## Updates for the future

* Monthly updates for RubyGems: https://rubycentral.org/news/
* Planned weekly Residency worklog blog posts, similar to Seth’s residency updates for PyPI
* Monthly update call with AWS, 3rd or 4th week of each month