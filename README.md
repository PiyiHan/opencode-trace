# opencode-trace

Captures raw LLM request/response payloads as interactive HTML files in `~/opencode-trace/`.

Example: https://ljw1004.github.io/opencode-trace/example.html

## Installation

### Copy files (recommended for forks)

```bash
git clone https://github.com/PiyiHan/opencode-trace.git /tmp/opencode-trace
cp /tmp/opencode-trace/opencode-trace.ts /tmp/opencode-trace/viewer.js /tmp/opencode-trace/package.json ~/.config/opencode/plugins/
rm -rf /tmp/opencode-trace
```

The `package.json` tells Node.js the plugin uses ES modules (`"type": "module"`). All 3 files are required.

### Symlink (for development)

```bash
git clone https://github.com/PiyiHan/opencode-trace.git ~/Codes/opencode-trace
ln -s ~/Codes/opencode-trace/opencode-trace.ts ~/.config/opencode/plugins/
ln -s ~/Codes/opencode-trace/viewer.js ~/.config/opencode/plugins/
cp ~/Codes/opencode-trace/package.json ~/.config/opencode/plugins/
```

Edits to `~/Codes/opencode-trace/` take effect immediately after restarting opencode.

### npm (original upstream)

```json
{
  "$schema": "https://opencode.ai/config.json",
  "plugin": ["@ljw1004/opencode-trace"]
}
```

Restart OpenCode. To force a refresh after changes: `rm -rf ~/.cache/opencode/packages/@ljw1004/opencode-trace@latest`

## Viewing traces

Open any `.html` file in `~/opencode-trace` directly in a browser. The viewer is self-contained — no server needed.
