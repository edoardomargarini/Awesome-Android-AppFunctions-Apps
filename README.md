# Awesome Android App Functions Apps

A community-driven list of Android apps that support App Functions.

Goal: become the reference repository for mapping the emerging App Functions ecosystem and the evolution of agentic AI on smartphones.

## What Are App Functions

In plain terms: App Functions are a new Android capability that lets apps expose specific features as invokable actions for trusted agents.

According to official Android documentation (package `android.app.appfunctions`):

- An app function is a discrete piece of functionality made available to "trusted, system-privileged applications" (agents).
- Agents can discover available functions, read structured metadata, and execute them.
- The framework enables cross-app orchestration (official examples include `createNote` in a notes app and `playSong` in a music app).

Mental model:

- App = function provider.
- Agent = orchestrator that discovers, evaluates runtime state, and executes.

### Why It Is Different From Classic Intents

App Functions are designed for a more semantic and structured interaction model:

- Explicit function metadata (id, parameters, return type, scope).
- Native flow: discovery -> state retrieval -> execution.
- Design oriented to tool-calling and multi-app orchestration.

### Current Limits (Important)

Official sources make it clear that today the ecosystem is controlled:

- `EXECUTE_APP_FUNCTIONS` (API 36) has protection level `internal|privileged` and is currently granted only to privileged system apps.
- Services that expose functions must require `BIND_APP_FUNCTION_SERVICE` (signature), so only the system can bind.
- The feature is marked as beta/experimental preview in Android reference docs.

Implication: this is still an early-stage ecosystem. This repo does not document a mature ecosystem yet; it helps it emerge.

## Why This Repo Exists

This list aims to be:

- A public map of the App Functions ecosystem.
- A reference point for developers, researchers, and the Android community.
- An open dataset to track adoption, patterns, and agentic use cases.

## How This List Works (Community-Driven)

This is an awesome-style list. It grows via:

- Pull Requests
- Issues
- Collaborative updates and fixes

It is normal to have very few entries at the beginning. Quality matters more than quantity.

## Inclusion Criteria

Each entry must include:

- A real, identifiable app.
- Plausible evidence of App Functions support.
- A verifiable source (see evidence levels below).
- A short and clear description.

Rejected entries:

- Spam or promotion without evidence.
- Duplicates.
- Non-verifiable claims.

## Evidence Levels

We use trust levels for transparency:

- `A - Official`: official documentation, official release notes, official vendor communication.
- `B - Strong`: credible technical demo, talk, or authoritative technical post with implementation details.
- `C - Community`: reverse engineering, APK analysis, reproducible community testing.
- `D - Rumor`: not included in the main list (can be discussed in issues).

## Entry Format

Use this format for each app:

| App | Developer | Play Store | Exposed Functions (if known) | Evidence | Level |
| --- | --- | --- | --- | --- | --- |
| Example App | Example Dev | https://play.google.com/... | createNote, searchNotes | https://example.com/proof | A |

## App List

No entries yet. Contribute the first one.

## How To Contribute

1. Open an issue or a PR.
2. Use the table format above.
3. Add at least one verifiable source.
4. Explain in one line why App Functions support is credible.
5. If possible, include test date and app/OS version.

## Vision

We believe agentic AI on smartphones will grow around reliable interfaces between apps.
App Functions can become one of those key layers.

This repository aims to be the open reference point for tracking that transition while it is being built.

## Official Sources

Android documentation (core references):

- Android App Functions package summary:
	https://developer.android.com/reference/android/app/appfunctions/package-summary
- `AppFunctionService`:
	https://developer.android.com/reference/android/app/appfunctions/AppFunctionService
- `Manifest.permission.BIND_APP_FUNCTION_SERVICE`:
	https://developer.android.com/reference/android/Manifest.permission#BIND_APP_FUNCTION_SERVICE
- `Manifest.permission.EXECUTE_APP_FUNCTIONS`:
	https://developer.android.com/reference/android/Manifest.permission#EXECUTE_APP_FUNCTIONS
- Manifest permissions reference (permissions/protection levels context):
	https://developer.android.com/reference/android/Manifest.permission

Android platform and permission policy context:

- Android permissions (AOSP):
	https://source.android.com/docs/core/permissions

Official Android and Google update channels:

- Android Developers News:
	https://developer.android.com/news
- Android Developers Blog:
	https://android-developers.googleblog.com/
- Google Android News (The Keyword):
	https://blog.google/products/android/

## Disclaimer

- This repository is not officially affiliated with Google.
- Details may change quickly because the feature is currently in preview.
- If you find outdated information or mistakes, please open an issue.