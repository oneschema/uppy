---
"@uppy/aws-s3": patch
---

Multipart uploads send up to 6 parts of a file at once again, as in v5. Since 6.0.0, parts were uploaded one at a time, which made large single-file uploads several times slower. Already-uploaded parts are still skipped on resume, and a failed part, pause, or cancel stops the file's other in-flight parts.
