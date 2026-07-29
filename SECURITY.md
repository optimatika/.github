# Security Policy

This policy covers all Optimatika open source projects, including ojAlgo and its extensions.

## Reporting a vulnerability

Please do not open a public issue for a security vulnerability. Use GitHub's private reporting instead: open the Security tab of the repository concerned and choose Report a vulnerability. That creates an advisory visible only to you and the maintainers. If private reporting is not enabled on that repository, use the contact form at www.optimatika.se/contact and say only that you have a security report, without the details.

Tell us which version you were using, what the problem is, and how to reproduce it. A minimal test case is worth more than a long description.

We aim to acknowledge a report within a week, and we will tell you whether we consider it a vulnerability. If we do, we agree a disclosure date with you, and credit you in the advisory unless you would rather we did not.

## Supported versions

Fixes go into the next release. Only the most recent release published to Maven Central is supported. There are no maintenance branches for older versions, so the remedy for a confirmed vulnerability is to upgrade.

## What belongs here, and what does not

ojAlgo is pure Java with no external runtime dependencies, so a report concerns our own code rather than something inherited from a dependency. Numerical inaccuracy, non-convergence, slow solve times and the like are ordinary bugs, not vulnerabilities. Open a normal issue for those.
