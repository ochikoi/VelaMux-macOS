# Build provenance

VelaMux baseline directory name: VelaMux-POINTER-VISIBILITY-FIX-20260918-204949.
Host SHA-256: b9ef5f8cba548f72532688f702d1c6cd9cca8e8c424d699ac64060fcc6e2d02f.
Includes stable screenshot pointer anchors and the latest concise English MCP descriptions.
Application executables, MCP scripts and resource bundle are byte-for-byte copies of the currently deployed version. No application source was modified to build this package.
Python: relocated local Python 3.12 runtime; third-party site-packages and unused command wrappers excluded. It is used only for Python standard-library MCP transport and installation.
Tunnel client: existing arm64 tunnel-client 0.0.11+8d55683eeef80bc5e360d95abf4692454fafc615, copied without profiles, secrets or logs. No cloudflared configuration is enabled by this package.
Distribution preparation updated 2026-09-20. VelaMux author: ochikoi (https://github.com/ochikoi). The VelaMux binary license is in LICENSE-VelaMux.md; third-party rights and remaining release checks are documented separately. The application payload is unchanged by this packaging update.
Local packaging checks do not substitute for another-Mac GUI/permissions and authenticated tunnel testing.
