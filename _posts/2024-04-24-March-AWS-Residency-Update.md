# RubyGems.org April 2024 Recap

### Monthly update

https://rubycentral.org/news/march-2024-newsletter/
https://rubycentral.org/news/april-2024-newsletter/

### Weekly residency updates

1. https://blog.segiddins.me/2024/03/29/residency-update/
2. https://blog.segiddins.me/2024/04/05/residency-update/
3. https://blog.segiddins.me/2024/04/12/residency-update/


## Completed security work

### Plain Ruby Protos

* The plain ruby implementation is fully compliant.
* Met with Shopify folks also building a JIT performance focused protobuf implementation
* SigStore uses protobuf
* The google one relies on native extensions so it is not usable inside rubygems.

### liblzma/xz backdoor

* RubyGems Research (expanding and indexing all gems on rubygems.org) proved immediately useful for searching all packages.
* Quickly ruled out the likelihood of packages containing a vulnerable version.
* [RubyGems is not vulnerable to the xz/liblzma backdoor](https://blog.rubygems.org/2024/03/31/rubygems-and-xz.html) by Samuel Giddins
* Funding a security resident meant that he could spend 10 hours evaluating the impact.
* It only took 10 hours because of the time spent on the research project.
* Piggybacking on work by Seth Larson and [a blog post](https://sethmlarson.dev/security-developer-in-residence-weekly-report-16) about PyPI, which inspired the research work.
* Without an engineer on full-time, the deeper triage/blog post/analysis would have been a much slower response (potentially 1-4 weeks to fully check gems in the ecosystem and write up a blog post)

### Documentation for the compact index

* Work with Martin to improve documentation so that deps.dev can implement rubygems integration.
* Deps.dev is really useful for investigating dependencies in packages, finding canonical versions, researching licensing.

### Re-introducing avatars to RubyGems.org

* Removed for privacy reasons (gravatar leaks emails, which resulted in complaints from users on rubygems)
* It caused everything to look anonymous, reducing the trust in rubygems.
* Sam created a solution that proxies the images through rubygems.org now so they remain private but can still be seen on the website.

### Disabling YAML aliases in RubyGems.org

* Patches a theoretical DoS vector in the gem upload endpoint. Disabling resolution of YAML aliases fixes that vector.
* Limiting uploaded gem metadata size
* Patches a potential DoS vector.
* If your entire uploaded gem is maximally compressed, it would use all the memory on the server.
* Put an upper bound on how much metadata we will read.

### Open Source Summit NA

* Roundtable

### Make trusted publishing automatable via API

* Allow adding new api scopes more easily.
* Improve default security of API keys

### MFA requirements / Gem deletion protections

* Prepare for situations similar to left-pad
* Implemented a yank protection policy to prevent disruption to the ecosystem.
* Disruptions make it easy for malicious users to distribute malware via a fork of a gem.
* Attempting to strike a balance between maintainer control and disruption of users.
* We’re aiming to narrow the policy gap with other package ecosystems.

### SigStore Release Plan

* Converging with other package indexes (PyPI)
* What does it mean to “do sigstore”?
* Focusing on what pieces need to be in place first, what will come later.
* Creating a story about what sigstore means.
* Tying in with trusted publishing, still relies on trusting the package index.
* Eventually building towards better controls and policies for devs relying on signatures.
* Tr​​ust on first use - inform when updates don’t match claims that were expected not to change.

### Next

* Improve the rubygems data dumps so “researchers” can have easier access to the rubygems.org data. The goal is to push people to use these to start their data set rather than scraping all the data from the api. (Can all the package repositories use all the same format for exporting packages?)
* SigStore feature plan and rollout.
* Trusted publishing rollout to the AWS SDK (2025Q1?)

