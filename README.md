# opnlocal model catalog

The list of AI models the [opnlocal](https://github.com/MilanDanilovic) app knows how to run.

- `catalog.json`: the models, each pinned to an exact Hugging Face commit with its file size and sha256.
- `catalog.json.sig`: ed25519 signature of `catalog.json` (base64). The app only accepts a catalog
  whose signature matches the public key built into it, and only if its `version` is newer than
  what it already has. A copy is also built into the app, so it works offline.

The app fetches these two files at most once a day (users can turn this off). The request carries
no information about the user or the device.

Models are downloaded by the app directly from Hugging Face; nothing is redistributed here.
Each model keeps its own license, shown in the app before download.
