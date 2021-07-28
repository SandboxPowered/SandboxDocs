# Introduction to Resources

Servers run on a collection of resources. A resource is a collection of files - such as client scripts, server scripts, and assets - that can be started, stopped and restarted at any time.

## Resource Directories

In the server, resources are loaded from a folder called `resources/` in the server data directory. Any folder in the `resources/` folder is parsed as a resource, except folders between `[brackets]` which are categories, which can contain multiple resource folders.

Each resource folder also has to contain a [resource manifest reference](resource-manifest.md) called `manifest.toml` to be correctly parsed as a resource.

See this example directory tree:

```text
server
└── resources
    ├── [category]
    │   ├── [another]
    │   │   └── resource-2
    │   │       └── manifest.toml
    │   └── resource-1
    │       └── manifest.toml
    └── main
        └── manifest.toml
```

In this tree, the following resources exist:

* main
* resource-1
* resource-2

{% page-ref page="resource-manifest.md" %}

{% page-ref page="first-script-javascript.md" %}

