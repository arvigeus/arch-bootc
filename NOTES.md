# Development Notes

## Podman Build Networking
- **Issue**: `just build-containerfile` failed with DNS timeouts when retrieving packages.
- **Fix**: Added `--network host` to the `podman build` command in `Justfile`. This allows the container to share the host's network stack, bypassing potential DNS isolation issues.
