# opencode-trace

This opencode plugin lets you see the raw json requests made to the LLM, and the responses.
* Example: https://ljw1004.github.io/opencode-trace/example.html

## Installation

Choose one of the following methods.

### Option 1: Copy the folder (recommended for forks)

```bash
git clone https://github.com/PiyiHan/opencode-trace.git ~/.config/opencode/plugins/opencode-trace
```

Restart OpenCode and you'll see each transcript stored in `~/opencode-trace`.

### Option 2: npm (original)

Add the package to your OpenCode config:

```json
{
  "$schema": "https://opencode.ai/config.json",
  "plugin": ["@ljw1004/opencode-trace"]
}
```

Restart OpenCode and you'll see each transcript stored in `~/opencode-trace`.

That installation path by default uses `@latest`, which opencode currently does't refresh when latest changes. You can force a refresh with `rm -rf ~/.cache/opencode/packages/@ljw1004/opencode-trace@latest`

## Viewing traces

Open any `.html` file in `~/opencode-trace` directly in a browser. The viewer is self-contained — no server needed.
