REXY — PWA OFFLINE SHELL TEST (v1)

This is a separate test package based on the user-confirmed Lawyers resume test copy. The original v7 file and Supabase project were not modified.

WHAT THIS PROTOTYPE DOES
- Adds a web app manifest and install icons.
- Registers a service worker and caches the single-file app shell plus manifest/icons.
- Uses the cached app shell as a fallback when a later page load has no network.
- Attempts to cache Google Fonts after a successful online visit.
- Explicitly excludes Supabase authentication, progress sync, entitlements, and AI/API traffic from the cache.

IMPORTANT LIMITATIONS
- Service workers require HTTPS (or localhost); opening index.html as a local file will not install this PWA.
- This package has not yet been hosted on an HTTPS origin and has not been tested on the user's phone.
- SpeechSynthesis / speech recognition may still require network or device language packs; offline voice is not guaranteed.
- Account login, cloud sync, and AI features need internet. This prototype only targets offline loading of the app shell and its embedded lesson content after one successful online visit.
- Do not clear browser site data when testing progress persistence.

TEST PLAN (after temporary HTTPS hosting)
1. Open the HTTPS address while online and wait for the app to finish loading.
2. Confirm install/add-to-home-screen is available; install if offered.
3. Open the app once online, navigate to a lesson, and confirm content displays.
4. Turn on airplane mode and fully close/reopen the installed app.
5. Confirm the app shell and embedded lessons still load.
6. Do not expect login, cloud sync, AI, or speech recognition to work offline.
7. Reconnect and confirm the app reloads normally.

SOURCE
REXY-v7-LAWYERS-RESUME-TEST-01.html (separate test copy; not original v7).
