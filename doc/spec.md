# Model Directory Structure

```
<modelname-version>
|-- assets
|   |-- labels.txt
|   `-- <optional-config-files>
|-- LICENSE    # optional currently
|-- meta.json
`-- model.pb
```

# Metadata Format of Model Package

Metadata, `meta.json`, describes all the details in a model package.

Metadata format v1.1.0:

```
# Example of meta.json
# Note: model directory name is fight-detection-1.0.0
{
    "name": "fight-detection",
    "version": "1.0.0",
    "inference-engine": "tensorflow",
    "model": "model.pb",
    "label": "assets/labels.txt",
    # optional configs
    "config": {
        "<optional-key>": "<optional-value>",
        "<optional-key>": "<optional-value>",
        ...
    },
    "checksums-sha256": {
        "model.pb": "<sha256sum>",
        "assets/labels.txt": "<sha256sum>",
        "<optional-file-path>": "<sha256sum>",
        ...
    }
}
```
