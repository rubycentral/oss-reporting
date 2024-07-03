# Update 2024-06

## Organizations

* Our designer created some initial flows just to investigate what creating an Org will look like.
* We have refactored a large portion of our authorization system, using rails best practices (a gem known as "Pundit").
* We are continuing to work on the API authorization system, which adds an extra layer but is not blocking yet.
* In the meantime, we have devised [a roadmap for the upcoming features for Organizations][1].

Next steps:

* Create the Organization database models and user interface.
* Potentially re-use our existing gem ownership transfer system to support adding gems to organizations.
* Continue defining and writng the maintainer role.
* Onboarding flow will likely allow people to name their organization, choosing the namespace in the process.
* We will onboard initial beta testors without the creation flow at first to test out permissions, adding and removing projects and people, etc.

## Audit

* SoW with Trail of Bits (ToB) is signed and paid.
* We met with our ToB project manager and talked about next steps and scheduling.
* They estimated that their engineer(s) would be available to start in late July.

Next steps:

* Awaiting our project kick-off meeting to onboard ToB team and begin work.

**This update was originally published in the [alpha-omega reporting project](https://github.com/ossf/alpha-omega/blob/main/alpha/engagements/2024/RubyCentral/update-2024-06.md) on GitHub.** 

[1]: https://docs.google.com/document/d/1YTNNiqxORDik5_cuIkK-3VsKuBafGLXN3gSUFZr9kV4/edit?usp=sharing