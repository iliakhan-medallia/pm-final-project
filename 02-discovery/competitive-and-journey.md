# Competitive Analysis & Journey Map

> **Module 2 · Lab 2 — ★ Deliverable 2.** Repo file `02-discovery/competitive-and-journey.md` — part of your submission.
> Do the lab in the **Module 2 · Exercise 2 Guide** (linked from the Module 2 deck), then click **⬇ Download .md** — it saves as this exact file. Commit it here.
> It becomes the **Competitive Analysis & Journey Map** slide of your Module 6 final deck. Builds on your `ai-synthesis.md` and your Module 1 `problem-hook.md`.

## Responses

- **Role, who are you solving for?:** Persona 1: Fleet Dispatcher (Night-Shift Coordinator). A dispatcher at a mid-size 3PL who reassigns routes and monitors driver progress, often on night shift.
- **Goal, what is this user ultimately trying to achieve?:** Keep route changes and stop statuses accurate so the drivers in the field and the dispatch board show the same reality.
- **Friction, the main barrier (moment of misery) stopping them:** "I reassign a route and the driver doesn't see it for ten, fifteen minutes. By then they've driven the wrong way. We keep a WhatsApp group as the real system." (UXR-02; BUG-2044, Critical). The board compounds this: "A stop shows 'in progress' when it was delivered an hour ago. I can't trust the board." (UXR-09; BUG-2072, Medium)
- **External tools the user is forced to use:** The RouteLogic platform for reassignments and the dispatch board, plus a WhatsApp group that serves as the real system of record for driver communication (UXR-02).
- **The process, the 3–5 manual steps they take:**
  1. Reassign the route in the platform (UXR-02).
  2. Rely on the WhatsApp group to reach the driver, since the group is where the change actually lands (UXR-02).
  3. Message the driver directly when the change is urgent, because the app sends no push notification on route change (BUG-2044). *Inferred; validate in interviews.*
  4. Wait 10–15 minutes for the driver to see the change in the app, while drivers may already be on the wrong route (UXR-02).
  5. Check the dashboard for stop status, then cross-check it against driver messages before trusting it (UXR-09; BUG-2072). Take status updates by text and re-enter them by hand (UXR-01). *Inferred; validate in interviews.*
- **Core frustration, where the process feels most "broken":** Double entry. Every change is made in the platform and then repeated in WhatsApp, so the same work is done twice. Latency runs both ways: reassignments take 8–15 minutes to reach drivers, and status lags 20–60 minutes on the board, so the dispatcher works from information that is already stale. Errors compound on the road, since a driver who receives a change late can complete several stops on the wrong route before the dispatcher knows.
- **The evidence, a quote or behavior from the research:** The regional manager values the admin reporting: "The admin reporting is genuinely powerful, that's why we bought it." (UXR-10). That reporting depends on accurate status data, and the dispatcher reports that the board cannot be trusted: "I can't trust the board." (UXR-09). The enterprise account evaluating a leaner routing product (UXR-04) is a single account, not a general churn trend.
- **Journey map, a shareable link or the map file you committed:** [journey-map.html](journey-map.html) (`02-discovery/journey-map.html`). Four-stage future-state timeline: reassign with confirmation, driver acknowledges, monitor the live board, exceptions and close-out. Not yet committed.
