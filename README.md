# Medora — Vercel deployment

This folder contains the production static export of the Medora frontend demo.
Source revision: `770c283ababbf32c0402dc0a1e2875fdaa081c94`.

## Publish

Deploy this folder to Vercel with the included `vercel.json`. It selects the Other
framework preset, skips dependency installation and building, and serves `public`.
The existing compiled files include every app route and its assets.

With Vercel CLI and an authenticated account:

```sh
vercel deploy --prod
```

Run that command from this folder. Select your account/team and a project when
prompted. No environment variables or backend services are required.

## Routes

- `/` — landing page
- `/login` — demo sign-in
- `/patient` — patient workspace
- `/doctor` — clinician workspace
- `/hospital` — hospital workspace

## Demo credentials

- Patient: `patient@medora.demo`
- Doctor: `doctor@medora.demo`
- Hospital: `hospital@medora.demo`
- Password for all three: `Medora123!`

This is a frontend demonstration. Changes are stored in the current browser;
authentication, AI processing, medical data, messaging and booking are simulated.

## Validation

The source passed its production build, TypeScript validation and 20 feature
checks before packaging. This package checks that all five route exports, React
Server Component navigation payloads, and referenced HTML/JavaScript/CSS assets
are present. Live Vercel smoke checks still require a completed deployment.

Configuration references:
https://vercel.com/docs/project-configuration/vercel-json
https://vercel.com/docs/builds/configure-a-build
