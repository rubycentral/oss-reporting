# RubyGems.org May 2024 Recap

### Monthly update

https://rubycentral.org/news/may-2024-newsletter/

### Weekly residency updates

1. https://blog.segiddins.me/2024/04/19/residency-update/
2. https://blog.segiddins.me/2024/04/26/residency-update/
3. https://blog.segiddins.me/2024/05/03/residency-update/
4. https://blog.segiddins.me/2024/05/10/residency-update/
5. https://blog.segiddins.me/2024/05/17/residency-update/
 
## Completed security work

### Make trusted publishing automatable via API

* Enabled short lived API keys with expirations - API keys with less than a 15 minute expiration are allowed to skip MFA during usage since they were already MFA’d on creation.
* Trusted publishing API key scopes
* Wrote rubygems plugin to use the API used for setting up trusted publishing for an existing gem.
* Real popular gems are now using Trusted Publishing, set up via the new rubygems plugin at railsconf hack day (including Pundit and net-imap, which is the first ruby stdlib gem to use it)
* (Note, also spoke with AWS SDK team about trusted publishing requirements)

### Plain Ruby Protos

* Now working on TruffleRuby and JRuby.
* Started optimizing performance in YJIT.
* Cut initial gem releases

### SigStore

* Fixes and improvements, including finding lots of bugs and improvements necessary in related libraries like JRuby and Ruby openssl libraries.
* Coordinating with sigstore TSC about moving my sigstore implementation into the sigstore organization
* Begin implementing dsse/in-toto support, needed to be able to verify sigstore bundles produced by github’s new attestation action
* SCT verification
* RFC3161 timestamp verification beginnings, blocked by issues with ruby/openssl
* Contributions to nascent tuf conformance suite

### RubyGems Research Project

* Reimaged and reconfigured the machine using docker/k8s to make deploy more consistent and reliable.

### Ruby Developer Meeting

* Long-awaited change merged into Zlib that should help RubyGems and RubyGems.org be able to read gem files much more efficiently

### RubyKaigi

* Presented a talk about Ruby’s Marshal implementation
* Met with contributors from around the world

### Next

* Continue working with AWS-SDK to enable trusted publishing
* Continue work on SigStore
