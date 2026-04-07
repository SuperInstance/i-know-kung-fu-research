# I Know Kung Fu: Claude Code Research

Sometimes you add a small file to your project and Claude Code's behavior changes. This tool helps you observe and test those changes in a controlled environment.

✅ Live test bed: https://the-fleet.casey-digennaro.workers.dev

## Quick Start
1. **Fork this repo first** – you run your own isolated tests. No account required.
2. Deploy directly to Cloudflare Workers. Zero dependencies, zero build steps.
3. Edit one file in `/skills/`. Run the test. Watch how Claude's output shifts.

You can observe changes in token ordering, context loading, and rule activation. No black box.

## Why This Exists
When using Claude Code, you might notice that adding a small file sometimes improves performance. Official documentation doesn't explain this. We built this to test and document what actually happens, with reproducible results you can verify yourself.

## Features
- Trace which lines Claude prioritizes when scanning your project
- Run side-by-side tests to measure behavior changes per line added to a Skill
- Verify which rules persist between chat sessions
- Observe when Claude delegates work to a subagent and what triggers it
- Inject controlled failures to map system limits
- Tests run against real production wifi driver code, not trivial examples
- Every observation is marked with Claude version for tracking changes

## What Makes This Different
1. No hype – this isn't a product. We share test results.
2. Test-driven – every claim has a runnable test you can execute.
3. Transparent – we document how the system works, not "secrets" or "hacks."

## Limitations
One specific limitation: the test bed currently only supports one codebase (a production wifi driver) for consistency. You cannot test against your own arbitrary codebase without modifying the project.

## License
MIT. Use, break, and improve this however you want.

Research by Superinstance and Lucineer (DiGennaro et al.)

<div style="text-align:center;padding:16px;color:#64748b;font-size:.8rem"><a href="https://the-fleet.casey-digennaro.workers.dev" style="color:#64748b">The Fleet</a> · <a href="https://cocapn.ai" style="color:#64748b">Cocapn</a></div>