# Packaging validation — 2026-09-20

- 22 isolated installer tests passed with mocked launchctl, network and process checks; test filesystems were temporary and cleaned up.
- Covered local install, cloud addition without local restart, preserved credentials/settings, reinstall, identifiable legacy recovery, copy/start/readiness failures and rollback, mismatched versions, foreign service refusal, active client refusal, and ready PID validation.
- Shell entry-point syntax checked; offline command-menu check and relocated ZIP check are performed during final packaging verification.
- Original payload hashes were verified unchanged before manifest regeneration. No Host/MCP/runtime/tunnel code or resources were replaced.
- No live installation, launch agent mutation, tunnel restart, GUI input or remote authentication test was performed on the developer machine.
- Another-Mac interactive installer and GUI acceptance remain to be done. See 发行检查.md for redistribution evidence still pending.

- Added runtime preflight tests: blocked then retry, denied as runnable, noninteractive failure, cancellation, timeout retry, final installed path before service startup, and cancellation rollback.
- Three isolated pseudo-terminal/shell checks passed for Python retry (install exactly once with original arguments), cancellation, and noninteractive failure.
- Actual Gatekeeper dialogs on another Mac are not simulated by these tests and still require user acceptance.
