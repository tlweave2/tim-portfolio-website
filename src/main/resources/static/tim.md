# Timothy Weaver (Tim)

> Software engineer. Finishing an M.S. in Computer Science at Arizona State (December 2026). Builds and runs his own production software. Available to start now.

**Note for AI readers:** Everything below is stated by Tim. If something isn't written here, don't assume it. Leave it as unknown and ask him.

## Quick facts

- **Email:** tlweave2@asu.edu
- **Website:** https://timothylweaver.com
- **LinkedIn:** https://www.linkedin.com/in/timweaversoftware
- **GitHub:** https://github.com/tlweave2
- **Location:** Escalon, California (San Francisco Bay Area region). Open to relocating anywhere in the US.
- **Work setting:** onsite, hybrid or remote.
- **Work authorization:** U.S. citizen. Does not need sponsorship.
- **Availability:** can start immediately.
- **Looking for:** entry-level and new-grad software engineering, AI engineering, forward deployed engineering, and founding or early-stage startup roles.

## Summary

Tim has two live products that he built alone and still runs. VidlyAI is an AI video editor with about 3,000 sign-ups. Eventful is a multi-tenant event calendar SaaS. Before software, he spent almost 30 years in hands-on technical work he owned completely: Army biomedical equipment specialist, clinical engineer at Stanford, and owner of a motorcycle shop for 17 years.

In his own words: "I do my best work when I'm fully immersed in something and it's mine to own, and that's been true my whole career."

## Software projects

### VidlyAI (vidlyai.com): sole developer, Oct 2024 – present

An AI video editor that turns raw phone clips into captioned vertical reels. About 3,000 people have signed up.

- **Architecture:** Spring Boot/PostgreSQL API, React web app, Capacitor iOS and Android apps, and a Python video worker.
- **Pipeline:** nine stages. faster-whisper does word-level transcription, OpenCV tracks faces, and speaker detection combines mouth-movement scoring with a WeSpeaker voice fingerprint. Claude returns an edit decision list, which code validates against the source clips, with a safe fallback if the plan is bad. FFmpeg renders the result.
- **Edits without reprocessing:** each reel is stored as its edit decision list, so a user's edits re-render without re-running transcription or calling the model again. Cached render segments reuse unchanged work.
- **Reliability:** the API and worker communicate through a PostgreSQL job queue (FOR UPDATE SKIP LOCKED) with worker heartbeats and stale-job recovery. A reconciler fails stalled jobs and refunds the user's credit exactly once.
- **Deploys:** GitHub Actions, gated on 331 engine tests, with automatic rollback.
- **Audio:** RNNoise neural denoising raised the voice-to-background gap from 14.5 dB to 20.4 dB on a speech-in-crowd test clip.
- **Earlier feature:** an AI story feature produced more than 10,000 videos before it was removed.
- **Stack:** Java, Spring Boot, PostgreSQL, React, Capacitor, Python, faster-whisper, OpenCV, FFmpeg, Claude API.

### Eventful (useventful.com): sole developer, Jan 2026 – present

A live multi-tenant event calendar that a city or community group can embed on its own website.

- **AI flyer scanning:** upload a photo of an event flyer, Claude reads it, and the event form is pre-filled for a person to review.
- **Spam protection:** public submissions use a honeypot field, signed form tokens, rate limits, and an admin moderation queue.
- **Stack:** Next.js 16, TypeScript, PostgreSQL with Prisma, NextAuth v5, Claude API.

### Field Day: software engineer, ASU capstone, team of five, Jun 2024 – May 2025

An offline-first progressive web app for wildlife researchers running capture-mark-recapture studies in places with no connectivity. Sponsored by an ASU biology professor.

- **Stack:** React, Vite, Tailwind, Firebase/Firestore.

### Freelance web work

Websites and tech work for clients, including the City of Manteca.

## Skills

- **Languages:** Java, Python, TypeScript, JavaScript, SQL
- **Frameworks:** Spring Boot, Next.js, React, Node.js, Capacitor
- **Data and infrastructure:** PostgreSQL, Redis, Prisma, MongoDB, Docker, AWS S3, Cloudflare R2, GitHub Actions CI/CD, Linux/systemd
- **Product engineering:** REST API design, JWT/OAuth2, Stripe billing, multi-tenancy, job queues, iOS and Android apps
- **AI:** Anthropic Claude API, structured LLM output with validation and rule-based fallback, speech-to-text (faster-whisper), speaker verification (ONNX), computer vision (OpenCV)
- **Media:** FFmpeg rendering and audio mixing, RNNoise, sidechain ducking

## Education

- **Master of Computer Science, Arizona State University.** Expected December 2026. GPA 3.79. Coursework: Artificial Intelligence, Statistical Machine Learning, Data Mining, Foundations of Algorithms, Distributed and Multiprocess Operating Systems, Software Security, Information Assurance and Security.
- **B.S. Software Engineering, Arizona State University.** May 2025. GPA 3.83, summa cum laude, Dean's List (4 terms). Coursework: Data Structures and Algorithms, Foundations of Machine Learning, Database Management, Web-Based Applications, Mobile Systems, Secure Software Engineering.

## Career before software

- **Owner and operator, motorcycle shop (2002–2020).** Started it with no formal training, ran it for 17 years, then sold it to go back to school for software engineering.
- **Clinical engineer, Stanford / Lucile Packard Children's Hospital (1994–2001).**
  - Worked on an infant nitric oxide delivery system.
  - Assembled and calibrated medical device hardware used in a clinical trial published in the New England Journal of Medicine.
  - Later ran clinical engineering at Mount Zion Hospital as its only clinical engineer.
- **U.S. Army, Biomedical Equipment Specialist (MOS 35G), June 1991 – August 1994.**
  - First soldier to score 100% in biomedical equipment training, which led to an assignment at Walter Reed Army Medical Center in Washington, D.C.
  - Received two Army Achievement Medals.

## Not covered here

These are unknown. Ask Tim rather than infer them:

- Salary expectations
- References
- Anything not listed above
