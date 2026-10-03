# insta_studio: image host for the Insta Studio pipeline

This repository exists only to **host generated quote-card images** for the [Insta Studio](https://github.com/virajchikhale/insta_studio_codebase) content pipeline (a private project).

## Why it is public

The pipeline renders an image, uploads it here through the GitHub API, and then gives Instagram's Graph API a `https://raw.githubusercontent.com/<repo>/<branch>/<path>` URL to fetch. Instagram can only fetch that URL if the repository is public, so **do not make this repository private** or posting will stop working.

## What is in it

- `test` branch: the generated images (`CodeConnection/quote_NNNN.jpg`, one commit per image) written by the pipeline. The branch is the one configured in the account settings of the pipeline.
- `main`: this README and placeholder files only.

**Do not commit anything private here:** every file is world-readable.

## Maintenance notes

- One commit per image makes the history grow quickly (hundreds of commits so far). If clone size becomes a problem, archive old images and squash the branch; the pipeline only needs the URLs of images that have not been posted yet.
- Credentials for uploading live in the private pipeline's account settings (a GitHub token with access to this repository only), never here.
