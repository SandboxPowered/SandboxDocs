---
description: >-
  The resource manifest is a file named manifest.toml placed in a resource
  folder on the server.
---

# Resource Manifest

## Example

An example resource manifest for a hypothetical resource looks as follows:

{% code title="manifest.toml" %}
```csharp
# Defines version this resource uses
#
# cantankerous | In Development API
manifest_version = "cantankerous"

# Adds a data file of a specified type to the game extra content system.
#
# This directive supports globbing in the filename field.
files = [
    "resources/**/*.*"
]

# Defines a script to be loaded on both sides. The extension determines which script loader will handle the file.
#
# Extension | Loader     | Type                   | Side        | Environments
# .js       | JavaScript | JavaScript source code | Both Sides  | All environments support
# .py       | Python     | Python source code     | Both Sides  | All environments support
# .lua      | Lua        | Lua source code        | Both Sides  | All environments support
# .jar      | JVM        | Compiled JVM code      | Server Only | Not all environments support
scripts = []

# Requires the specified resource to load before the current resource.
dependencies = ["chat"]

[server]
# Defines a script to be loaded on the server side. The extension determines which script loader will handle the file as described in scripts.
scripts = ["server.js"]

# Marks the resource as being server-only. This stops clients from downloading anything of this resource.
# If all resources are marked as server-only the server will accept vanilla connections.
server_only = false

[client]
# Defines a script to be loaded on the client side. The extension determines which script loader will handle the file as described in scripts.
scripts = ["client.js"]
```
{% endcode %}

## Globbing

Some entry types may support globbing for multiple files. These take a pattern syntax as follows:

| Example | Matches |
| :--- | :--- |
| `*.js` |  `a.js`, `b.js` \(non-recursively\) |
| `dir/*.js` |  `dir/a.js`, `dir/b.js` \(non-recursively\) |
| `**/*.js` |  `dir1/a.js`, `dir2/b.js`, `dir1/dir2/c.js` |
| `**.js` | Same as `**/*.js` |
| `**/cl_*.js` | `dir/cl_a.js`, etc |

Support for globbing is specified under each entry type.

