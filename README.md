# A2 Hero — Android reliability showcase

A private Android application for user-configured monitoring and request handling.
This repository contains sanitized engineering notes only. Production source,
device identifiers, account details, request content, and diagnostics are excluded.

## 1.5.8-preview — 2026-10-24

Fixed ambiguous request diagnostics by separating account, detail and submission routes.
A bounded sanitized event history preserves context without identifiers or credentials.

178 JVM tests and offline build passed. Installed; bounded account/history/detail reads
succeeded with the existing session. A historical access-denied error did not reproduce,
so its root cause remains unproven. No login or order mutation was performed.

## 1.5.7-preview — 2026-10-24

Added typed diagnostic facts for pricing qualification while preserving the strict
submission guard. Reports distinguish absent data from special pricing without storing
raw values. 175 JVM tests and offline build passed. A session rejection during follow-up
requires isolated-session validation; direct acceptance remains disabled.
A fresh isolated session subsequently passed discovery and a short background smoke
test. Empty lists prevented live pricing and acceptance qualification; long-term session
stability remains unproven.

## 1.5.6-preview — 2026-10-24

Corrected an unconditional discovery restriction that could hide candidates before local
policy evaluation. Local acceptance filters and disabled direct writes remain unchanged.
A live discrepancy motivated the fix, but causality for that individual event is unproven.
Post-install observation received one item and recorded its structural report; local
policy rejected it and the standard-pricing check did not pass. No write was attempted.

## 1.5.5-preview — 2026-10-24

Automatic observation reports now retain fixed policy decision codes and display clear
rejection explanations. Reasons are whitelisted and legacy reports remain unknown;
customer content cannot enter this diagnostic field. Eligibility and traffic are unchanged.

Validation: 170 JVM tests and offline build passed. Real nonempty reports remain pending;
automatic API acceptance remains compiled off.

## 1.5.4-preview — 2026-10-24

Corrected list-arrival instrumentation to collect all exposed explicit identities before
selection and filtering. In-app list timing is the primary comparator; notification
timing remains separate secondary evidence. No additional network traffic was added.

Validation: 168 JVM tests and offline build passed. Real matched-job timing remains
pending; this does not establish faster delivery or guaranteed acceptance.

## 1.5.3-preview — 2026-10-24

Added passive channel-arrival comparisons without additional network traffic. Anonymous
timing differences are retained only for matching identity candidates; identifiers stay
in bounded expiring process memory. Duplicate observations do not manufacture samples.

Validation: 164 JVM tests and offline build passed. Real identity mapping and matched-job
timing remain unqualified; no claim of earlier server delivery or guaranteed acceptance.

## 1.5.2-preview — 2026-10-24

Added explicitly enabled automatic read-only observation alongside the existing screen
acceptance owner. Bounded sanitized reports retain structural facts and filter results
without customer values. Request serialization, pacing and backoff remain intact.

Validation: 157 JVM tests and offline build passed; installed and successful empty-list
observation was checked on device. Direct acceptance remains compiled off. Nonempty
contract semantics, live allocation and provider-equivalent traffic remain unverified.

## 1.5.1-preview — 2026-10-24

Added an explicit bounded contract probe: one list page and at most one detail, with
manual cooldown and fixed-label diagnostic facts that exclude customer values.
This helps identify missing contract evidence without enabling automatic acceptance.

Validation: 153 JVM tests and offline build passed; installed and exercised on device.
The live list was empty, so real detail and acceptance remain unverified. Accessibility
binding was checked after installation. Direct automatic acceptance remains compiled off.

## 1.5.0-preview — 2026-10-24

Added a priority queue that preserves request pacing and server backoff, monotonic
preparation deadlines, separate queue/network timings and bounded submission-result
follow-up. Exact matching evidence is retained without inventing a loss from a missing
row or replaying an ambiguous write. Reconciled history no longer permanently blocks
return to the existing screen engine.

Validation: 147 JVM tests and the offline debug build passed. Installed in place;
one explicit connection check succeeded and the empty review state was exercised.
Real acceptance timing, full allocation semantics, independent push enrollment,
authoritative calendar synchronization and sustained-session validation remain open.
Automatic direct acceptance remains compiled off; this is not a final release.

## 1.4.4-preview — 2026-10-24

Corrected expert-account role recognition using authenticated response evidence and
added a bounded on-device qualification runner with explicit network opt-in and
redacted output. Unknown and corporate account states remain excluded.

All 132 JVM tests and offline builds passed; the updated preview was installed.
A rejected session required one explicit sign-in; the new session passed a bounded
read with no incoming jobs. Long-term session stability and live direct acceptance
remain unqualified. No direct job submission or independent push enrollment occurred.
The short observer run was stopped afterward, and the existing screen service was
rebound and verified following instrumentation cleanup.

## Push feasibility review — 2026-10-24

Read-only review identified an additional persistent messaging transport beyond the
existing REST polling design. A background service was present on the target device;
this does not establish delivery latency or an independently authorized integration.
Documented registration isolation, duplicate suppression, authoritative detail checks
and deadline scheduling as prerequisites. No credentials, push registration changes
or live submissions were used. The independent acceptance release remains unqualified.

## Device validation follow-up — 2026-10-24

Verified an existing session through a bounded read, exercised observer stop and
return-to-screen controls, and inspected key portrait screens at the device's large
text setting. Accessibility was confirmed enabled and bound at the end. No incoming
job was available; account qualification and live allocation remain unresolved.
No direct acceptance was performed. This is still a preview, not final certification.

## 1.4.3-preview — 2026-10-24

Prioritized front-page analysis before pagination I/O while preserving a bounded
read budget and tail coverage. Missing or malformed waiting metadata now remains
ineligible rather than being defaulted. Added ordering, cancellation, duplicate,
transport-failure and strict-field regression coverage.

All 129 JVM tests and the offline debug build passed.
This remains a preview: physical UI and live acceptance qualification are incomplete.
Direct acceptance remains disabled; no fastest-client or zero-defect claim is made.

## 1.4.2-preview — 2026-10-24

Made screen observation event-responsive while preserving timeout fallback, loading
deadlines and action spacing. This removes an avoidable fixed wait after eligible
screen changes without increasing network polling or weakening eligibility checks.

Validation: 121 JVM tests and an offline debug build passed. Live-job latency gains
remain unmeasured; there is no priority guarantee. Direct acceptance remains disabled.

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
