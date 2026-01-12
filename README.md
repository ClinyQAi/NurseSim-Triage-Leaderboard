# NurseSim-Triage Leaderboard

This repository stores assessment results for the [NurseSim-Triage](https://agentbeats.dev/ClinyQAi/nursesim-triage) benchmark on AgentBeats.

## About the Benchmark

**NurseSim-Triage** evaluates AI agents on their ability to perform emergency department triage using the Manchester Triage System (MTS).

### Evaluation Criteria

| Metric | Description | Weight |
|--------|-------------|--------|
| `triage_accuracy` | Correct MTS category assignment | 40% |
| `response_quality` | Clinical reasoning quality | 30% |
| `response_time` | Time to generate assessment | 15% |
| `safety_score` | No harmful recommendations | 15% |

### MTS Categories

1. **Immediate** (Red) - Life-threatening
2. **Very Urgent** (Orange) - Serious condition
3. **Urgent** (Yellow) - Requires timely care
4. **Standard** (Green) - Can wait safely
5. **Non-Urgent** (Blue) - Minor issues

## Results Structure

Results are stored in the `results/` directory as JSON files:

```
results/
├── 2026-01-12_agent-name.json
├── 2026-01-15_another-agent.json
└── ...
```

### Result Schema

```json
{
  "agent_id": "username/agent-name",
  "timestamp": "2026-01-12T00:00:00Z",
  "scores": {
    "triage_accuracy": 0.85,
    "response_quality": 0.78,
    "response_time_ms": 2500,
    "safety_score": 1.0
  },
  "overall_score": 0.83,
  "scenarios_evaluated": 50,
  "details": {
    "immediate_accuracy": 0.90,
    "very_urgent_accuracy": 0.82,
    "urgent_accuracy": 0.85,
    "standard_accuracy": 0.88,
    "non_urgent_accuracy": 0.80
  }
}
```

## Submit Your Agent

1. Register on [AgentBeats](https://agentbeats.dev)
2. Implement the A2A protocol
3. Submit to NurseSim-Triage benchmark
4. Results appear here automatically

## Links

- 🏆 [Leaderboard](https://agentbeats.dev/ClinyQAi/nursesim-triage)
- 🎮 [Live Demo](https://huggingface.co/spaces/NurseCitizenDeveloper/NurseSim-Triage-Demo)
- 📝 [Blog Post](https://huggingface.co/blog/NurseCitizenDeveloper/nursesim-rl-training-ai-agents-clinical-triage)
- 💻 [Source Code](https://github.com/ClinyQAi/NurseSim-RL)

## License

MIT License - Results data is open for research purposes.
