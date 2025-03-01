### Plan of read teaming SAES
Red Teaming SAEs: 1-Page How-To

Target the Weak Spots

SAEs often create “AND” features or split features unnaturally.
Suspect L1 regularization as the main culprit.
Test in Mini Models

Build or use a tiny Transformer/MLP.
Inject known features or compositional patterns, see if the SAE groups them wrongly.
Try simple changes (e.g. log penalty instead of L1) to see if that prevents misbehavior.
Scale to a Real Model

Pick a medium model (e.g. GPT-2 Small).
Check for suspicious or combined features (“biology-AND-math”).
Quantify how often the SAE lumps or splits features.
Attack with Adversarial Inputs

Push weird prompts to trigger bizarre SAE features.
See if your penalty changes or architecture tweaks help.
Document & Fix

Summarize which penalty approaches or architectures fail and which work better.
Create a short best-practices guide (e.g. “Use log penalty for better feature separation”).
Demonstrate improved interpretability on real text tasks.
