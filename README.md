# mcp-proofspan

MCP server for Proofspan wrapper - Agent evaluation benchmark wrapper.

## Tools

### run_evaluation
Run agent evaluation on a benchmark.

**Parameters:**
- `agent` (string, required): Agent identifier
- `benchmark` (string, required): Benchmark suite name
- `config` (object, optional): Evaluation configuration

### get_results
Get evaluation results.

**Parameters:**
- `eval_id` (string, required): Evaluation ID

### get_trend_report
Get evaluation trend report for an agent.

**Parameters:**
- `agent` (string, required): Agent identifier
- `days` (integer, optional): Days of history (default: 30)

## Installation

```bash
pip install -r requirements.txt
```

## Usage

```bash
python main.py
```

## Connecting to Claude Desktop

Add to your `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "proofspan": {
      "command": "python",
      "args": ["/path/to/mcp-proofspan/main.py"],
      "cwd": "/path/to/mcp-proofspan"
    }
  }
}
```

## License

MIT