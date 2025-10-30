## 1. Feature Freeze Before Tuning
- No micro-optimizing until core features are done.
- Ask: Does the main thing work fully?

## 2. Tiny Comments for Clarity
- One-line comments on non-obvious code.
- Example: `# sets pywal colors in Rofi`

## 3. Confirm Why a Fix Works
- After a fix, recreate the bug in a stripped-down test.
- Lock in the root cause.

## 4. Keep a Clean Baseline Config
- Maintain a minimal version of Neovim, Kitty, Rofi, etc.
- Diff against it when things break.

## 5. Check Dependency Weight
- Before adding a library: Can I do this already? Is there a smaller option?
- Run a bundle diff before committing.

## 6. Quick Mode vs Slow Mode
- Quick mode: get it working.
- Slow mode: later, verify it’s the best approach.

## 7. Scheduled Config Rebuilds
- Once or twice a year, rebuild configs from scratch.
- Drop old tweaks that aren’t worth keeping.
