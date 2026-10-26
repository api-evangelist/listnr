# Listnr (listnr)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Listnr AI is a text-to-speech and AI voice platform offering 1,000+ ultra-realistic voices across 142+ languages and accents, used for voiceovers, podcasts, and text-to-video. Listnr is primarily a web application, but it also exposes a **documented public Text-to-Speech API** at base `https://bff.listnr.tech/api/tts/v1`. The API converts SSML text or an article URL into MP3/WAV audio synchronously or asynchronously, lists available voices, and reports async job status. API keys are self-service: generate a personal key in the Listnr dashboard at `voices.listnr.tech` and pass it in an `x-listnr-token` header. Keep the key server-side — never expose it in the browser or front-end code.

The endpoints, parameters, headers, and job-status values below are confirmed from Listnr's public API documentation at [github.com/team-listnr/text-to-speech-api](https://github.com/team-listnr/text-to-speech-api). The OpenAPI and collections in this repository model request/response schemas from those documented fields and should be verified against the live API.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/listnr/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/listnr/refs/heads/main/apis.yml)

## Tags

- AI
- Text to Speech
- TTS
- Voice
- Speech Synthesis
- Audio
- Voiceover

## Timestamps

- **Created:** 2026-07-11
- **Modified:** 2026-07-11

## APIs

### Listnr Text-to-Speech API

Convert SSML text or an article URL into MP3/WAV speech using a chosen voice, voice style, speed, and sample rate. Synchronous endpoints (`/convert-text`, `/convert-url`) return an audio URL directly; asynchronous endpoints (`/convert-text-async`, `/convert-url-async`) return a `jobId` to poll.

- **Human URL:** [https://listnr.ai/text-to-speech-api](https://listnr.ai/text-to-speech-api)
- **Base URL:** `https://bff.listnr.tech/api/tts/v1`

#### Tags

- Text to Speech
- Speech Synthesis
- Audio

#### Properties

- [Documentation](https://listnr.ai/text-to-speech-api)
- [API Reference](https://github.com/team-listnr/text-to-speech-api)
- [OpenAPI](openapi/listnr-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/listnr.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/listnr.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Listnr Voices API

List the voices available on Listnr, optionally filtered by language, gender, and style. Each voice returns its identifier, language, gender, and supported voice styles for use with the Text-to-Speech API.

- **Human URL:** [https://github.com/team-listnr/text-to-speech-api](https://github.com/team-listnr/text-to-speech-api)
- **Base URL:** `https://bff.listnr.tech/api/tts/v1`

#### Tags

- Voices
- Languages
- Catalog

#### Properties

- [API Reference](https://github.com/team-listnr/text-to-speech-api)
- [OpenAPI](openapi/listnr-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/listnr.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/listnr.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Listnr Audio Jobs API

Poll the status of an asynchronous text-to-speech or URL-to-speech job by `jobId`. Returns a status of `PENDING`, `IN_PROGRESS`, `COMPLETED`, or `FAILED`, plus the resulting audio URL and audio key when the job finishes.

- **Human URL:** [https://github.com/team-listnr/text-to-speech-api](https://github.com/team-listnr/text-to-speech-api)
- **Base URL:** `https://bff.listnr.tech/api/tts/v1`

#### Tags

- Jobs
- Async
- Status

#### Properties

- [API Reference](https://github.com/team-listnr/text-to-speech-api)
- [OpenAPI](openapi/listnr-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/listnr.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/listnr.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/listnr)
- [GitHub Organization](https://github.com/team-listnr)
- [Website](https://listnr.ai)
- [Documentation](https://github.com/team-listnr/text-to-speech-api)
- [Sign Up](https://voices.listnr.tech)
- [Plans](plans/listnr-plans-pricing.yml)
- [Rate Limits](rate-limits/listnr-rate-limits.yml)
- [Fin Ops](finops/listnr-finops.yml)

## Authentication

All requests require a personal API key generated in the Listnr dashboard at [voices.listnr.tech](https://voices.listnr.tech), passed in an `x-listnr-token` request header. Do not use the API key in front-end code or the browser.

## Access Model

Listnr is primarily a web application (podcast, voiceover, and text-to-video studio). On top of that, it offers a documented, self-service public Text-to-Speech API whose reference lives in a public GitHub repository. The endpoints in this catalog are confirmed from that documentation; request/response schemas in the OpenAPI and collections are modeled from the documented fields and should be verified against the live API. No public WebSocket API is documented — see `review.yml`.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
