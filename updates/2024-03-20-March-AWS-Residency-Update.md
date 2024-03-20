# RubyGems.org March 2024 Recap

### Monthly update

https://rubycentral.org/news/february-2024-newsletter/

### Weekly residency updates

1. https://blog.segiddins.me/2024/03/08/residency-update/
2. https://blog.segiddins.me/2024/03/15/residency-update/

## Completed security work

### Sigstore client in pure Ruby

* Implemented by Samuel
* When complete, will allow users to verify signatures on RubyGems updates, as well as gems, which is the first bootstrapping step for sigstore support in RubyGems.
* Pure-Ruby implementation of sigstore “verify” is a requirement for us to be able to support sigstore in Ruby, since we can’t rely on having a rust compiler or a pre-built rust binary available for every Ruby platform. Creating signatures can 

### The Update Framework client for RubyGems

* Sigstore uses TUF as a bootstrapping step
* We can re-use this client for the RSTUF system that Josef has been working on

### Plain Ruby Protobufs

* Sigstore uses protobufs as the serialization format, and the Google protobufs gem is only available as prebuilt binaries, which makes it very difficult for RubyGems to use.
* Building a protobufs library in pure Ruby provides a mechanism for us to parse and verify Sigstore bundles without limiting us to the exact platforms where Google already ships binary protobuf gems, and without limiting us to installing gems for verification to work.

### RubyGems.org instability

* The AWS SDK team was trying to release new versions of AWS packages at that exact moment, and was running into errors while trying to release all of the new packages.
* A security researcher was causing some service instability (something like 2% of requests were erroring out) as a result of web scraping that hit some inefficient endpoints in our JSON API.
* Samuel was able to investigate and resolve the N+1 database queries, massively improving our database load and resolving the errors.
* Graphs of how things improved here: https://blog.segiddins.me/2024/03/15/residency-update/
* Quick response time and quick resolution to this issue were massively improved by Samuel’s full-time work on RubyGems thanks to the Amazon-funded security residency.
