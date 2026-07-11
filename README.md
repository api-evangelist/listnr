# Listnr (listnr)

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
