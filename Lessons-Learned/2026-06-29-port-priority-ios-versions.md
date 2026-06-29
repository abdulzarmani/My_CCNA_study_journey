# Port-Priority Increment Discrepancy Across IOS Versions

**What I thought:** Port priority increments in multiples of 32 (0-224 range).

**What happened:** A tutorial said 32. I initially second-guessed it. Verified against Jeremy's IT Lab using real Cisco IOS CLI — confirmed `<0-224> increments of 32`. Then tested it myself in Packet Tracer and got a *different* result: `<0-240> increments of 16`.

**The real lesson:** Both were correct — for different IOS versions. My Packet Tracer instance was running IOS 12.2(25)FX (older), while Jeremy's device was on a newer IOS release. Cisco changed this implementation detail across versions.

**Takeaway:** Never trust a single source blindly — including tutorials, including AI explanations. Verify against the actual device CLI in front of you. IOS version matters more than I expected.
