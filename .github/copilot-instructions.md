# Copilot Instructions

## Project Guidelines
- Never run `git commit` or `git push` on the user's behalf. Make changes in the working tree only, then report what changed and let the user review and check in the changes themselves.

## Kubernetes Manifests
- Keep `imagePullPolicy: IfNotPresent` in this repo's Kubernetes manifests (cloud.yaml, edge.yaml) to support offline scenarios.
- Container updates on running systems should be done via temporary `kubectl` patches, not manifest changes.