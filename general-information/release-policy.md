# Release Policy

## API Releases

### Versioning

 API releases are categorised as major, minor or patch using standard [semantic versioning](http://semver.org/) \(`major.minor.patch`\):

* **Major** releases \(**x**.y.z\) include new features and breaking changes for previously warned deprecations.

  For major releases, we provide an upgrade guide as well as release notes.

* **Minor** releases \(x.**y**.z\) include new features and no breaking changes.

  Minor releases don’t require an upgrade guide, but we provide release notes.

* **Patch** releases \(x.y.**z**\) contain only bug fixes and no breaking changes.

  Patch releases don’t require an upgrade guide. We typically provide release notes.

{% hint style="info" %}
### Breaking Changes

Though we try not to, we may have to make out-of-policy releases, deprecations, or breaking changes due to issues such as security risks, or fixes with exceptional technical burden. In such cases, a release note and upgrade guides will always be provided.
{% endhint %}

## API Stages

API features in sandbox go through some stages before they are marked as Stable. Your plugin should only ever rely on Stable APIs, since they are the only ones that respect the bug fixing and breaking changes policy outlined above. Usage of APIs in other stages is highly discouraged.

All APIs that are in a different stage than Stable are marked with an annotation that indicates their current stage \(e.g. `@Beta` indicates that the API is in Beta stage\). Additionally, the current stage name may be in their package hierarchy, their class name, their method names and/or in comments \(e.g., `InternalBlock` may reside in a package named `internal`\).

| Stage | Meaning | Breaking Changes | Intended usage |
| :--- | :--- | :--- | :--- |
| **Internal** | Restricted to implementations of the Sandbox API | May include breaking changes with no notice or upgrade guide | Should never be used by external addons |
| **Pre-Alpha** | Incomplete and/or extremely buggy features, prone to breaking | May include breaking changes with no notice or upgrade guide | Testing |
| **Alpha** | Incomplete features and/or with high chance of bugs | May include breaking changes with no notice or upgrade guide | Testing and development |
| **Beta** | Feature complete, but potentially in need of optimization or real world usage testing | Will include notice & upgrade guide if breaking changes occur | Testing and development |
| **Stable** | Fully tested features, ready to be used in addons | Will include notice & upgrade guide if breaking changes occur | Public addons and releases |
| **Deprecated** | Potential removal in future releases, with no bug fixing or enhancement in the mean time | Will be completely removed in future update, notice & upgrade guides are given on deprecation and complete removal | Phasing out of old methods: addons should move to new methods as soon as possible |

