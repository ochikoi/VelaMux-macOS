# Third-party components and notices

VelaMux's own license does not replace any third-party license. Original notices remain in the payload; additional license copies are in `licenses/`. Retrieval URLs, dates and SHA-256 values are recorded in `licenses/SOURCES.json`.

| Component | Included evidence | Scope / remaining verification |
|---|---|---|
| Python 3.12 runtime | `licenses/Python-LICENSE.txt`, identical to the runtime's own LICENSE.txt | Retains the PSF and historical licenses supplied with this runtime. This alone is not an exhaustive notice inventory for all native libraries statically included in its distributor's build. |
| tunnel-client 0.0.11+8d55683eeef80bc5e360d95abf4692454fafc615 | LICENSE (Apache 2.0) and NOTICE fetched from that exact upstream commit, copied verbatim | Upstream: https://github.com/openai/tunnel-client . The local binary was copied unchanged. Commit-matched top-level terms do not establish an exhaustive transitive dependency license inventory or independently prove reproducible binary provenance. |
| Tcl / Tk 9.0 | `Tcl-license.terms`, `Tk-license.terms` from upstream core-9-0-branch | Version family matches bundled library names; exact distributor build revision still needs confirmation. |
| Itcl 4.3.8 | `Itcl-license.terms` from upstream itcl-4-3-8 tag | Corresponds to bundled directory version; preserve original embedded notices. |
| Thread 3.0.6 | `Thread-license.terms` from upstream thread-3-0-6 tag | Corresponds to bundled directory version; preserve original embedded notices. |

The Python runtime was relocated from the developer's available runtime, not rebuilt from a fully captured bill of materials. Its linked/static native dependencies and the tunnel client's transitive dependencies require a final distributor-level audit before this complete bundle can be represented as redistribution-cleared. No missing terms have been invented or silently replaced with VelaMux's license.

VelaMux pointer artwork and any other included resources also require confirmation of original ownership or applicable permission by the publisher. This packaging pass did not replace resources or binaries.

This document records evidence and open items; it is not a blanket assertion that every file has completed redistribution review. See `发行检查.md` for release status.
