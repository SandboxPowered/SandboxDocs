# Release Policy

## API Releases

### Versioning

 API releases are categorised as major, minor or patch using standard [semantic versioning](http://semver.org/) \(`major.minor.patch`\):

* **Major** releases \(X.y.z\) include new features and breaking changes for previously warned deprecations.

  For major releases, we provide an upgrade guide as well as release notes.

* **Minor** releases \(x.Y.z\) include new features and no breaking changes.

  Minor releases don’t require an upgrade guide, but we provide release notes.

* **Patch** releases \(x.y.Z\) contain only bug fixes and no breaking changes.

  Patch releases don’t require an upgrade guide. We typically provide release notes.

{% hint style="info" %}
### Breaking Changes

Though we try not to, we may have to make out-of-policy releases, deprecations, or breaking changes due to issues such as security risks, or fixes with exceptional technical burden.
{% endhint %}

## API Stages

* **Internal**: APIs in this state will have the annotation **`@Internal`**. In some cases the term `internal` also appears in their namespace, comments, or as a prefix to each method name. Does not adhere to our bug fixing or breaking change policies. **Should never be used outside of the API or Implementations**
* **Pre-Alpha**: Feature incomplete. Unknown if will become stable. APIs in this state will have the annotation **`@PreAlpha`**. In some cases the term `prealpha` also appears in their namespace, comments, or as a prefix to each method name. Does not adhere to our bug fixing or breaking change policies. Available for testing and development, but **not recommended** for public releases.
* **Alpha**: Feature incomplete and may have some significant bugs. Planned to become stable. APIs in this state will have the annotation **`@Alpha`**. In some cases the term `alpha` also appears in their namespace, comments, or as a prefix to each method name. Does not adhere to our bug fixing or breaking change policies. Available for testing and development, but **not recommended** for public releases.
* **Beta**: Feature complete and potentially with some performance optimisation, but may still be slightly unstable. APIs in this state will have the annotation **`@Beta`**. In some cases the term `beta` also appears in their namespace, comments, or as a prefix to each method name.

  Does not adhere to our bug fixing or breaking change policies. Available for development, but **not recommended** for public releases.

* **Stable**: A complete feature that meets the needs of a set of users for publicly released addons. We plan to continue working on this.
* **Deprecated**: Not currently working on or planning to work on features or fixes. Could be removed permanently with notice.

  Not recommended for public releases.

