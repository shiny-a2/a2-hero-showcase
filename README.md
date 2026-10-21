# A2 Hero — Android reliability showcase

A private Android application for user-configured monitoring and request handling.
This repository contains sanitized engineering notes only. Production source,
device identifiers, account details, request content, and diagnostics are excluded.

## 1.1.0 — 2026-10-21

The update makes active monitoring coexist with the phone's normal secure lock.
An unlocked foreground session keeps the screen awake; leaving the app or stopping
monitoring releases it. A manually locked device stays locked.

Outcome handling now distinguishes explicit allocation, a submitted proposal,
a lost request, a quota limit, and an unconfirmed result. Loading or navigation
alone is no longer reported as success. Submission waits are bounded and use
fresh UI controls, with interruption checks for lock, stop, or app changes.

These changes improve truthful reporting and session reliability. They do not
guarantee priority over other users or remove upstream/network latency.

## Validation

- 25 JVM regression tests passed, including 6 acceptance-result tests.
- Debug APK build, XML parsing, shell syntax and whitespace checks passed.
- Physical Android 14 device: foreground display retention and release on app exit verified.
- Android Lint could not run because the required Google Maven artifact was unavailable.
- No real customer request was submitted solely for testing.

Detailed validation and release notes remain in the private repository.
