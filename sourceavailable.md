# Why We Believe in Source-Available

In our proposal, all controllers except those sold by Nintendo are required to disclose all running source code that relates to reading user inputs, communication via Gamecube controller protocol, and everything that interacts with the data in between, to be permitted for use at Melee tournaments that abide by this controller ruleset.

While this may seem like a burden to makers of controllers, we feel this is necessary to be able to verifiably audit controller behavior for compliance.

# Past Occurrences of Rule-Breaking

In late 2022, it was revealed via decompilation of firmware blobs that the Goomwave DX controller had processing that clearly violated existing rulesets that prohibited macros, as well as demonstrating other behaviors that would be prohibited in this proposed ruleset.
It had been widely believed that the device was not being entirely above-the-board but it took efforts of enterprising community members to definitively show the problems.

This became a dilemma because these controllers have been available for several years and players had invested hundreds of dollars in a device without being made aware of how it was doing what it was advertising—and the legality repercussions thereof.

# Why We Choose to Require Source Available

To prevent this from ever happening again, we stipulate that all firmware code pertaining to the function of the controller as a controller for a Gamecube be available at request for *anyone* to audit.

We do not want code to be hidden behind non-disclosure agreements for several reasons:

1. Signing a non-disclosure agreement is a risk for whoever audits the code. The people in this community are not obligated to put themselves at risk of a lawsuit just to verify functionality.
2. This concentrates responsibility in a small number of people, who could be biased or bribed by any number of parties.
3. It relies on the technical ability of the auditor(s) to detect underhanded code. The more people who get to see the code, the lower the likelihood that rule-breaking code goes unnoticed.

The risk and responsibility being placed in a few individuals makes this option a non-starter.

Additionally, even without the ability to compile the full firmware code, having the source available for the pertinent parts of the firmware makes it easier to verify that actual devices exhibit compliant behavior.

# Why We Limit Our Requirements

There are two notable limitations on what we require of the source:

1. We do not require any code unrelated to core functionality as a controller to be open.
2. We do not require the code to be open-source licensed for reuse.

These are concessions to makers of proprietary controllers who want to offer software features that differentiate them from other makers.

One example is that we do not require USB or other console functionality to be open-sourced if the maker does not want to.

Other features that are permitted to remain closed-source would include proprietary methods for updating or cosmetic features such as lighting, as long as their code is cleanly isolated.

If there is novel but legal controller-related processing that the maker wishes to keep proprietary, this rule exists to protect them from code theft as all competing devices will have to also have their code open or be excluded from Melee tournaments.

# How We Plan to Roll Out Enforccement

Existing devices will, after approval of the ruleset, have N months to prepare compliant firmware and provide source code.
Once they do, the code will be inspected by members of the ruleset team and the wider Melee community, and any concerns brought up.

New devices will be permitted on an experimental basis with explicit permission of tournament operators, but must provide pertinent code within...
