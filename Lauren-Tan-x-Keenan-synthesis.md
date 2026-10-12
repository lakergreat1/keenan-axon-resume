# Lauren Tan (@poteto) × Keenan Keeling: what they have that most engineering orgs do not yet have
Sources: X thread (Mike → Lauren, Oct 8–9 2026), Lauren's 38-min talk "i shipped 2000 (good) PRs last month" (Sep 21 2026, 3.7M views; transcript + Gemini watch saved alongside), Keenan's essay "How I build with agent fleets" (Oct 2026).

## The thread
Mike asked Lauren how she would rewrite her resume for a less savvy VP of Engineering to explain the 10x/100x/1000x gains, mentioning a Senior Director friend "building Michelin Kitchens." Lauren: "my talk is probably the closest thing to a compressed form of these ideas."

## Lauren's talk in one paragraph
Shipping 2,000 good PRs a month is not about typing faster. It is about trust, built in layers so agents produce quality work when she is not there. Her kitchen metaphor: engineers no longer cook each dish, but they design the kitchen, train the line, choose the equipment, and own the final plate. The specific layers: (1) verification skills so the agent can run the real app and collect empirical proof (Control Glass CLI + a feature map of how every feature is reached); (2) skills that teach agents to work like senior engineers (pstack); (3) architecture that makes bad code impossible (Dune: five nouns, process boundaries enforced by the import graph, comments banned because agents copy workarounds); (4) the correction hierarchy, codebase > static analysis > rules > skills > style guide, so a correction becomes a lint rule, never a review comment; (5) gardeners who delete tech debt, keep one paved path, and lint against anti-patterns; (6) an outer loop (Sentry/Datadog/Slack → cloud agent → reproduction video → PR).

## Where Lauren and Keenan are the same person
| Lauren | Keenan |
|---|---|
| "I am the bottleneck" | "I don't write code anymore; I set direction and check results the way a user would" |
| Trust curve: 1–5 agents is the trap; 100 needs a system | Fleet: commander, designer, 3 workers, reviewer, verifier; "idle seats with an unfinished goal is a commander failure" |
| The agent verifies its own work with a CLI + feature map, empirical traces | The author never grades its own work; a fresh verifier walks a real browser; "liveness is not success" |
| Correction → lint rule, never a style guide | Correction → dated rule in the standing brief, in the engineer's exact words |
| Codebase is memory; one paved path; ban comments | Truth lives in files, not conversations: ideal state, work graph, git, evidence |
| Gardeners | Template reports flow back into Wheelhouse; fleets file tooling defects instead of working around them |
| Outer loop: Sentry → cloud agent → PR with video | Sentinel: production errors → bug + work item; herald wakes the commander |
| 2,000 PRs/month, 5,000 in six months | 505 PRs in 30 days, 3,100 since Sep 2025, zero reverts |

## The difference from a strong, conventional engineer (stated without putting anyone down)
A strong conventional engineer makes themselves better. Lauren and Keenan make the system better, so every engineer and every agent after them is better by default. Concretely, the shift is in where effort goes:
1. **From writing code to writing "done."** They define outcomes and checks before a build and treat a hedge ("should work") as a fail.
2. **From reviewing to encoding.** A correction becomes a lint rule, a type, a bench check, or a dated rule. It never has to be made twice.
3. **From trusting people to trusting evidence.** Nothing counts on the author's word; a different mind re-runs the proof.
4. **From a personal workflow to a transferable system.** Lauren's skills repo and framework; Keenan's public MIT template and seven-stage path. Both have teammates using it without them.
5. **From activity to throughput you can audit.** Both publish the numbers and how they were measured, and both pair volume with a safety record.

## The one-line version for a VP
"Most engineers ship their own work. Keenan ships the system that lets a whole squad ship like a department, and the controls that keep a CJIS-grade product safe while it does."
