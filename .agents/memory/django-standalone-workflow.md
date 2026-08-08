---
name: Django standalone workflow
description: Environment note for running a Django app alongside the preconfigured workspace services.
---

Use a dedicated fixed-port workflow for standalone Django apps when the workflow does not inject `PORT`; binding to `$PORT` can result in an empty value and prevent Django from starting.

**Why:** The managed JavaScript artifact services receive their port through artifact routing, but a custom workflow may not receive that variable.

**How to apply:** Configure the Django command with an explicit supported port such as `8000`, then verify the app on that port rather than assuming the shared root proxy belongs to it.