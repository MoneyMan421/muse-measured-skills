---
name: guide-store-publishing
description: Sequence a guide launch across two or more online stores so daily caps, approval windows, payout status, and test mode are checked first and every listing is verified live before it is counted as sellable. Use when the same guide or product set is being published to multiple stores; for single-store catalog work, use the Store Operations skill instead — the boundary between the two is stated in this skill's amendment section.
---

# Publish guides across multiple stores

Part of Measured Skills for Muse, by Collin. A measurement record, not a warranty.

## Stay inside the Store Operations boundary

- Follow Muse's Store Operations skill for single-store catalog, inventory, order, refund and fulfillment work, and use this skill only for sequencing a guide launch across two or more stores.
- Treat the Store Operations rules on reading current state, approval before publishing, trying one item first, and re-reading before a retry as the base rules, and apply this skill only where it adds daily cap, payout, test mode, and approval window checks across stores.

## Check sellability before you count a listing

- Read the live store before a publish run and record its mode, its payout status, and its current product roster.
- Treat a listing in a test or sandbox mode as not sellable, even when the product and price were created and verified there.
- Treat a listing with no payout method connected as not sellable when the product page shows no buy path, and say that plainly instead of counting it as launched.
- Count the items you plan to create against any daily creation cap the platform shows, and name the time the cap lifts before you start.

## Sequence the run around caps and approvals

- Split a launch that exceeds a daily cap into a part that fits today and a part scheduled after the cap lifts, and record the scheduled time with your scheduler (Muse's scheduling, or the platform's).
- Start steps that raise an approval card only while the user can approve within its expiry window, and pause the run instead of letting approvals expire while the user is away or unable to respond.
- Try one listing first when a store or format is new, verify it live, and only then continue with the rest of the set.
- Keep each store as its own run with its own roster, price, and link records, so a block on one store does not stall or contaminate the others.

## Resume an interrupted run without duplicates

- Re-read the live roster first when a publish or upload session ends early, times out, or is left unverified.
- Match what is already live against the planned set by title and price, and create only the items the live roster does not show.
- Stop and report the exact unverified state when the live roster cannot be read, instead of re-running the whole upload and risking duplicates.

## Verify each store live and report its state

- Open each published product page after the run and confirm the title, the price, the visibility, and the buy path from the page itself.
- Report each store separately as live and sellable, live but not sellable, scheduled, paused at the user's direction, or unverified, with the reason for any state that is not sellable.
- Save the product and price IDs from the verified live read in a run file beside the launch records, and name that file in the report.
- Leave two recommendations that make the next launch easier, naming the next cap, approval, or payout step the user will face.

## Tools this skill uses

- If your Muse has store connections (for example Gumroad or Stripe), use them to read products, sales, payouts, and balances, and to check whether products and prices sit in a test account or a live account before publishing.
- The checks in this skill are written against the live store pages themselves, so they apply whether or not a connection is available: when in doubt, the product page is the source of truth.

## Alternatives for better results

- Publish to the one store that is fully sellable first and hold the rest, rather than spreading a launch across stores that cannot yet take payment.
- Use a scheduled run for the overflow after a cap lifts, instead of staying in session waiting for the reset.
- Ask the user to connect payouts or confirm live mode before the publish session, so the session itself is spent creating and verifying listings.

## Amendment — the boundary with Store Operations (folded in)

*This section is the author's standing amendment to the Store Operations skill, folded into this skill rather than published separately, because its whole content is the boundary between the two skills.*

- Keep the base Store Operations skill as the governing skill for single-store catalog, inventory, order, refund, and fulfillment work.
- Use this skill (Publish guides across multiple stores) only when a guide launch spans two or more stores and needs daily cap, payout, test mode, and approval window sequencing across those stores.
- Treat this amendment as the boundary between the two skills, so the general Store Operations rules are not restated as a competing method in the guide launch skill.
- Alternative: stay with the base Store Operations skill alone for a single-store change, rather than adding multi-store sequencing that the task does not need.

## Verification

How this skill's output is checked: a listing counts only after its live product page has been opened and the title, price, visibility, and buy path confirmed from the page itself. Each store is reported separately in one of the stated states — live and sellable, live but not sellable, scheduled, paused at the user's direction, or unverified — with the reason for any state that is not sellable, and the product and price IDs from that verified live read are saved in a run file named in the report. A listing in test mode, or with no payout path, is reported as not sellable no matter how completely it was created. If the live roster cannot be read, the run stops and reports the unverified state rather than re-running and risking duplicates.

Status: In regular use in the author's own Muse workspace. First public verification run: pending — this skill has not yet been re-verified in this repo's cadence, and it will not be described as verified here until a dated Proof Record is published in records/.
