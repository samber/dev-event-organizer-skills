# Capacity, session length and network evidence

Contents: the three ceilings · the demand-vote mechanic · every published session length · density ratios and what they are not · the named live-failure causes · the venue's written network questions · what this reference deliberately does not give you.

## The three ceilings

Capacity is not a preference. It is the lowest of three numbers, and which one binds is the useful output - state it, because it is also the thing to fix if you want a bigger room next time.

- **Room ceiling.** Seats, with the furniture the exercise actually needs. A workshop layout packs looser than theatre rows, and power at the seats is a separate question from seats. The carried band for a technical event's breakout rooms is a mix holding 10-20 and 20-40, with chairs that can form a circle - recorded in `samber/dev-event-organizer-skills@event-venue-sourcing`'s space program, which attributes it to the DevOpsDays organizing guide.

  Two rooms in a published 2017 workshop-day grid were named _Small Room_ and _Workspace_, which is a reminder that a venue's own room names carry no capacity information at all.

- **Coverage ceiling.** How many people the instructor plus whatever the facilitator menu bought can reach before someone quietly gives up. **There is no number to look up.** It depends on the exercise's failure density more than on headcount, and the honest way to state it is with the sizing logic attached.

- **Exercise-throughput ceiling.** How many people can get real hands-on time given what is genuinely finite: boards, cables, licence seats, per-participant logins, physical stations, or a shared cluster's capacity. This is the ceiling most often missed, because it is invisible on the registration page and appears only when the twenty-first person needs the ninth device.

  MLH's hardware guidance implies it throughout - dedicated stations for fabrication, assembly, testing and specialised electronics, each with its own equipment list - without ever converting it into a headcount.

## The one published capacity-setting mechanic

A published 2017 workshop day put four parallel workshops in each of two blocks and asked attendees to choose before the day: _"Please vote for your favorite workshops!"_, with the stated purpose _"This will help us determine which rooms to place them in."_ The 2025-2026 DevOpsDays chapter pages for Graz, Zurich, London, Portland, Lima and Istanbul document no such pre-event workshop-room vote. Their closest current mechanic is Open Spaces: same-day, real-time self-selection into breakout topics on sticky notes or a board. That serves a different moment - on-site unconference agenda-setting, not pre-event workshop-room sizing. Treat the pre-event vote as historical and unconfirmed at any current edition, not as standing practice.

That is demand-driven room assignment, and it inverts the usual order. Instead of guessing a capacity and hoping the right number of people want it, collect expressed interest and match the sessions to the rooms you have. It costs one question in whatever pre-event mail already goes out, and it is the only method here that produces a capacity number from evidence rather than from a guess.

Its limit is worth naming: a vote ranks demand, it does not lift any of the three ceilings. A workshop that wins the vote and needs one device per participant is still capped by devices.

## Every published session length

Report these as instances. There is no average here, and computing one across four events, three formats and two decades would be false precision.

| Instance                                                  | Length                   | What it was                                                                                                          |
| --------------------------------------------------------- | ------------------------ | -------------------------------------------------------------------------------------------------------------------- |
| DevOpsDays Amsterdam 2017, workshop-day morning block     | 09:00-11:30 (150 min)    | Four parallel workshops, hands-on technical                                                                          |
| DevOpsDays Amsterdam 2017, workshop-day afternoon block   | 12:00-14:30 (150 min)    | Four parallel workshops, after a catered lunch                                                                       |
| DevOpsDays Singapore 2025, Team Topologies workshop       | 180 min                  | Published as _"Agenda (180 minutes)"_, structured as _"four 45-minute segments"_                                     |
| DevOpsDays pre-event workshop day, published slot options | 45 / 90 / 120 / 180 min  | Carried from `samber/dev-event-organizer-skills@event-format-selection`'s precedents reference                       |
| PyCon US tutorials                                        | 3 hours, separately paid | Carried from the same reference                                                                                      |
| MLH, team-formation workshop                              | under an hour            | _"Team formation workshops generally don't last over an hour."_ Not a technical hands-on session - a social mechanic |

Two patterns, stated as observation:

- The granularity is 45 minutes almost everywhere, and a genuine hands-on technical session in this record lands at 150-180 minutes.
- The one sub-hour figure is attached to a format with no exercise in it, so do not read it as the short end of a range that includes the others.

MLH names two placement constraints for a workshop running inside a larger event rather than on its own day:

- _"Limit the number of workshops during an event as they consume valuable building time."_ - an argument for the do-nothing rung.
- _"Schedule them earlier in the event when hackers are most likely to need guidance."_ - a real scheduling input to hand to `samber/dev-event-organizer-skills@event-schedule-design`.

## Density ratios, and what they are not

The carried per-attendee figures - roughly four devices and at least two and a half outlets per attendee - come from a hackathon organizer guide, recorded in `samber/dev-event-organizer-skills@event-venue-sourcing`'s space program with that pole stated. They describe a room of people building for a weekend.

**There is no per-seat bandwidth or power figure specific to a workshop room.** A workshop room is plausibly denser than a talk room and plausibly less demanding than a hackathon floor, and that intuition does not convert into a number. Borrow the hackathon figure as an upper bound and say that is what you are doing, exactly as `samber/dev-event-organizer-skills@event-venue-sourcing` instructs - never present a workshop-specific ratio.

What the guidance does give, on power, is a shape rather than a ratio: check that the venue's outlets actually work, and _"Provide sufficient surge-protected power strips at every station."_ Power strips are the cheap fix for a room whose outlets are on the walls and whose participants are in the middle.

## The named live-failure causes

The named causes are unusually specific, and none of them is bandwidth.

- **The venue blocks device classes.** _"Work with venue infrastructure to ensure the network allows IoT and other devices, as these are often blocked by standard university networks."_ Written for hardware, true for anything unusual on the wire.
- **The venue blocks protocols.** A published workshop's own prerequisites depend on it: participants need an RDP client and, in the page's parenthesis, _"(RDP protocol allowed)"_.
- **The participant's own VPN.** _"Turn off VPN (we use websockets extensively)"_ - published by the workshop author as a known failure of a browser-based lab.
- **The participant's ad-blocker.** From the same note: _"pause AdBlock for the lab domain (there are no ads)"_.
- **A burst of simultaneous cold installs.** The published mitigation is the pre-download ask, with its reason attached: _"Encourage hackers to pre-download software drivers and IDEs ahead of time to reduce network load during the event."_
- **Peak load that is not the download.** _"Secure robust, high-speed Wi-Fi and plan for peak usage (uploads, documentation, data streaming)."_

And one participant-side fallback, published by the workshop rather than the organizer: a session requiring internet access to a remote lab tells participants to _"(Use Wi-Fi or your own data)"_. Naming a fallback in the prerequisites is cheaper than any organizer-side remedy and it is the only one that survives the venue failing entirely.

## What to put to the venue in writing

`samber/dev-event-organizer-skills@event-venue-sourcing` already asks venues to answer in writing what sustained bandwidth a room can guarantee, on what circuit, with what fallback. For a workshop room, add three questions that the failures above make necessary:

1. How many simultaneous devices does this room's access point hold, and what happens at the limit?
2. Which protocols and ports are blocked, and can they be opened for a day?
3. Are unusual device classes blocked by default, and who can grant an exception on the day?

If the venue will not answer these, that is the promotion condition for removing the live dependency - the answer being unavailable _is_ the evidence.

## What this reference deliberately does not give you

Five numbers and conventions you will look for here and will not find. Derive each one for your own session rather than borrowing a figure that will read as measured once it is written down.

- **A participant ceiling for a hands-on workshop.** Not a number, not a band - take the lowest of the three ceilings above.
- **A facilitator-to-participant ratio.** The coverage reference makes the same refusal from the other side.
- **A per-seat bandwidth or power figure specific to a workshop room.** Borrow the hackathon figure as an upper bound and say that is what you are doing.
- **A relationship between session length and capacity**, though the two obviously interact through the throughput ceiling.
- **A convention for what to do mid-session when the network fails anyway.** Every mitigation above is preventive and lives before the day. The live response belongs to `samber/dev-event-organizer-skills@event-run-of-show`; agree it with that plan rather than improvising a protocol on the day.
