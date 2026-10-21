# RUNBOOK

## daily

### Start deamon

```bash
uv run kama-core
```

 `Ctrl+C`  -- exit

### verify

```bash
uv run kama ping
# → pong server=0.0.1 uptime=12ms latency=2ms
```

### End deamon

```bash
kill $(pgrep -f kama-core)
```

---

## config

优先级（低 → 高）：**内建默认值 → `~/.kama/config.toml` → `.env` → 系统环境变量**。

### `~/.kama/config.toml`

```toml
[core]
host = "127.0.0.1"
port = 7437

[logging]
level  = "INFO"
file   = "~/.kama/logs/core.log"
format = "text"    # "text" | "json"
```

### `.env`

```bash
cp .env.example .env
```

---

## development

```bash
uv run ruff check src tests scripts   # lint
uv run mypy src                       
uv run pytest tests/ -v               
uv run pytest tests/unit/ -v         # without deamaon

make docs                             
make verify-s0                        
```

---

## log

```bash
tail -f ~/.kama/logs/core.log
```

