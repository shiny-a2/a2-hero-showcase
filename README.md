# A2 Hero — Android reliability showcase

A private Android application for user-configured monitoring and request handling.
This repository contains sanitized engineering notes only. Production source,
device identifiers, account details, request content, and diagnostics are excluded.

## 1.4.1-preview — 2026-10-24

Refreshed the native dark interface with grouped job cards, collapsible secondary
settings, consistent action styling and confirmation before local sign-out.
This reduces visual clutter without changing eligibility or acceptance behavior.

Validation: 118 JVM regression tests and an offline debug build passed. Installed
in place; physical visual checks remain pending manual device unlock. Light-theme
support is not claimed. Direct acceptance remains disabled.

## 1.4.0-preview — 2026-10-24

Added an independent account dashboard with manually refreshed job lists and an
explicit experimental background observer. Ten specialist reviews informed fixes
to session invalidation, cancellation, strict filtering, transport isolation,
private-data protection and truthful UI state. A durable single-attempt submission
foundation is present, but direct acceptance is compiled off pending live qualification.

Validation: 118 JVM tests and a debug build passed. Authorized physical-device checks
verified account-list reads, short locked-screen observation and process recovery
without repeating sign-in. The preview was installed in place. Long unattended
stability and real direct acceptance are not certified; no test order was submitted.
Current management views are read-only, not financial or full lifecycle controls.

Production source and account evidence remain private. This update makes no claim
of permanent sessions, invisibility or guaranteed response priority.

## Engineering review — 2026-10-24

Reviewed retained field evidence and prepared the implementation/release sequence for
an independent engine. Existing screen-based discovery was still active; rendering
waits and periods of manual mode also affected outcomes. The new design requires
exclusive engine ownership, durable submission records, strict structured eligibility,
bounded network recovery and explicit outcome reconciliation.

This is a feasibility and release-planning update, not a new deployed version.
Independent acceptance, non-empty live contract validation and long unattended session
qualification remain release gates. No account data, raw payloads or provider-specific
implementation details are included here.

## 1.3.0 — 2026-10-22

Added user-initiated independent sign-in with local, fresh-message OTP matching and
encrypted session persistence. Verification is bounded to the active attempt and
cannot silently repeat. Purpose-specific access allows interactive authentication
and a single manual connection check; background polling and direct acceptance
remain disabled while session behavior is investigated.

Validation: 76 JVM tests and a debug build passed. Authorized device checks verified
automatic code entry, encrypted-session restoration and one read-only connection
check. No customer order was submitted. Token permanence, long-term simultaneous
sessions and independent acceptance are not claimed. Sensitive account and message
data remain excluded from this showcase and source history.

## 1.2.1 — 2026-10-22

Suspended experimental direct networking following a reported session issue. The
cause is still unconfirmed. The update removes Internet permission and rejects all
network entry points locally, disables observer restart, and removes experimental
session material. Historical diagnostics remain available. The established on-device
accessibility workflow is preserved.

Four regression tests exercise blocked login, verification, listing and detail calls.
No provider request is needed to test these protections.

## 1.2.0 — 2026-10-21

Added independent, read-only network observation alongside the existing monitoring
workflow. Structured eligibility checks use the user's selected regions, brands and
working hours, with explicit handling of unknown dates and time-zone conversion.
Device-held session credentials are encrypted and excluded from backup storage.
A foreground notification exposes status and a stop control; sequential requests
respect server retry delays and back off on errors.

This is an observation milestone. Independent network acceptance is not implemented
or claimed. Keeping a single existing acceptance writer avoids duplicate actions
while the new path is validated against naturally arriving work.

Validation: 55 JVM tests and the debug build passed. Physical-device authenticated
empty-list reads, background observation and stop/restart were verified. No live
customer request was submitted solely for testing. Non-empty live-data parsing,
long unattended operation and independent acceptance remain unverified.

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

## 1.1.0 validation

- 25 JVM regression tests passed, including 6 acceptance-result tests.
- Debug APK build, XML parsing, shell syntax and whitespace checks passed.
- Physical Android 14 device: foreground display retention and release on app exit verified.
- Android Lint could not run because the required Google Maven artifact was unavailable.
- No real customer request was submitted solely for testing.

Detailed validation and release notes remain in the private repository.
