# infra
Directory-per-env, not workspaces. Workspaces share one backend config and make it too easy to apply dev to prod. Directories give you explicit, separate state files and separate CI jobs. State backend: S3 with versioning + encryption. Terraform ≥1.10 supports S3 native locking (use_lockfile = true), so DynamoDB is no longer required.
