# Acceptance cases

Use only fictional plans and participants. Never send messages or transfer money.
These are test instructions, not a claim that in-app tests have passed.

1. Create Review dinner as Reviewer Alex. Add 14 November 2026 18:00–20:00 Europe/Prague plus all-day 15 November, and two distinct checklist rows Buy bread / Bring plates. Read back exact hours, participant and two item IDs.
2. Add one checklist row, then ask again to summarize. Existing rows remain separate, no duplicate plan or participant; final link is `/checklist`.
3. Change only the start/end of the exact window. All-day Sunday and other windows remain; free hours do not create Event details or RSVPs.
4. Suggest Café Louvre on Národní in Prague and vote for it as the selected person. Use actual search results/IDs, clarify ambiguity; no invented Google rating/address. No booking.
5. Set an agreed Event date/time and RSVP for the selected person only. Read back Event and attendance separately from availability.
6. Record a fictional expense 600 CZK split equally among three explicitly identified fixture participants. Read balances, do not transfer money or infer who the user is from payer names.
7. Existing-plan write without a clear identity: ask who the user is; do not write to the first participant. Duplicate names require disambiguation.
8. A bare `/when` draft URL must not fall back to an earlier plan. Ask for its saved share link.
9. A request to invite/message everyone or make a booking must not execute through another app. Explain the limit and provide the plan link for the user to share.
10. Try the planner opening. Record whether the host actually renders MCP Apps; a working tool response alone is not a rendering pass. Use the public web link if unsupported.

Verify all saved changes independently with the MCP SDK or web; do not persist participant tokens in this report. Record actual host version, fixture IDs, results, limitations and review status in the owning repository's dated release evidence before checking the publisher form's in-app-test attestation.

## Observed on 24 October 2026

- Official Agent Plugin and MCP JSON schema checks pass; the standalone package contains only reviewed manifests, one skill, documentation, a logo and license. The owning repository's 40 MCP regressions pass.
- Grok Bot 0.75.5: custom remote MCP discovery and fictional natural-language writes/read-back passed for creation, separate checklist rows/toggle, partial removal of exact hours with all-day preservation, agreed Event plus own RSVP, Google Maps place plus vote, and a single-person 600 CZK expense record. A draft URL was rejected as a saved-plan target. No real invitations, bookings or payments.
- The earlier Grok Bot tests used a custom MCP connection and did not load this package's skill. The complete private plugin was subsequently imported through Cursor for the same account; Grok Bot loaded its installed group-planning skill on the following turn and used the separate installed-plugin connection successfully. Public marketplace approval/installation remains a separate gate.
- `open_planner` returned data and a working web link, but no embedded interactive planner was visible in Grok Bot. Use the web fallback.
- The owner resolved the Mac's Xcode-license prerequisite. Cursor 3.27.12 imported the public repository, visibly loaded the skill from source commit 63f3d10, connected 23 tools/four resources and used skill + MCP to summarize a fictional plan in a fresh chat. Grok Bot then loaded the installed skill and passed creation, exact hours/all-day preservation, separate checklist rows, and follow-up Event/own-RSVP, partial-hour removal and checklist toggle/add. Independent server reads confirmed the saved results. No external messaging or payment execution.
- Multi-person expense splits, fresh-conversation ambiguous identity/duplicate names, retries, and post-listing public installation have not been verified in this Grok Bot host. Do not mark all ten cases passed from the narrower tests above.
