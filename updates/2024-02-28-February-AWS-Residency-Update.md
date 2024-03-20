# RubyGems.org Feb 2024 Recap

### Monthly update

https://rubycentral.org/news/february-2024-newsletter/

### Weekly residency updates

1. https://blog.segiddins.me/2024/01/26/residency-update/
2. https://blog.segiddins.me/2024/02/02/residency-update/
3. https://blog.segiddins.me/2024/02/09/residency-update/
4. https://blog.segiddins.me/2024/02/23/residency-update/

## Completed security work

### Event / audit logging

* Implemented by Samuel
* Tracks security-relevant events on accounts and gems, like password resets or email address changes

### research.rubygems.info

* A new service for investigating the contents of every gem
* Initially used to investigate a serialization security report from GitHub
* Should be useful for future similar work
* Impact: Able to search gems to find which gems have certain vulnerabilities, or could prevent certain fixes for a vulnerability.
* Determine the impact of security fixes. Dry run a decision.

### In-progress security work

* Sigstore client for RubyGems
* The Update Framework client for RubyGems
