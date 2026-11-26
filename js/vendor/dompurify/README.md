# DOMPurify

This directory contains the DOMPurify 3.5.0 production browser build used to sanitize
Wordfence preflight notices before they are added to the page.

- Source: https://github.com/cure53/DOMPurify/tree/3.5.0
- Artifact: `dist/purify.min.js`
- License: Apache License 2.0 and Mozilla Public License 2.0. See `LICENSE`.
- SHA-256: `d3785a5d41335ef41a2dc0ef44c740d15bbde9f8b1c0d10a350bfd354895ba3b`

The PHP integration enqueues this required file before the JDITC login script with the
static version `3.5.0`. If the sanitizer cannot run, the login script uses text-only
notices instead of inserting untrusted HTML.

When updating this dependency, replace the production build and license from the same
upstream release, update this version and checksum, and repeat the JavaScript, security,
and login regression checks. Review DOMPurify security releases before distributing an
updated plugin. DOMPurify 3.x supports modern browsers; its upstream documentation lists
2.5.9 as the latest branch for Internet Explorer support.

