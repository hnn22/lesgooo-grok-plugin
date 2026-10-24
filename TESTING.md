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
