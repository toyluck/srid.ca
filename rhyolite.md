---
title: Rhyolite
---

{.ui .warning .message}
Rhyolite is **neither recommended nor officially** supported by [Obsidian Systems](https://obsidian.systems/), who is working on a new project called "Incremental View" that will supercede it; Incremental View will be much more appropriate for general use.

[Rhyolite](https://github.com/obsidiansystems/rhyolite) provides a bunch of functionality useful in complex SPAs. It is normally used with [[obelisk]]. Use [obelisk-rhyolite-template](https://github.com/srid/obelisk-rhyolite-template) to bootstrap an Obelisk+Rhyolite project.

## Real-time view

When using rhyolite your frontend can "listen" on some time-varying data stored in postgres on the backend.  Rhyolite uses websocket for the communication between frontend and backend, as well as PostgreSQL NOTIFY/LISTEN for communicating updates from the database.

Your app will define a `ViewSelector` that the frontend will use to define what kind of data it needs to render its view. The rhyolite backend will in response push the resultant `View` down the websocket which gets reflected in a `Dynamic` in the frontend.
