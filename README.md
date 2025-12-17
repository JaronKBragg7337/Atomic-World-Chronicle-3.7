# Atomic World Chronicle v3.7

**A world you want — or a world of worlds.** Atomic Chronicle is an append-only execution and memory substrate that records every action, state transition, and outcome with perfect historical fidelity. It hosts multiple independent "worlds" (simulations, robotics, economies, games) that interact seamlessly while preserving immutable history.

## ✨ Features
- **Immutable State Tracking**: Append-only ledger captures all changes across worlds for verifiable history.
- **Cross-World Interactions**: Game outcomes trigger robot actions; economies reward simulations (e.g., game → robot → reward pipeline).
- **Hardware Integration**: Direct robotics control with logged outcomes for real-world prototyping.
- **FastAPI Endpoints**: Query states, transitions, and economies via REST API.
- **Transparency Economy**: Verifiable rewards and transactions across simulations.

## 🏗️ Architecture Overview
Core is a persistent memory substrate (see [persistent-memory-substrate demo](https://jaronkbragg7337.github.io/persistent-memory-substrate/)). Worlds run independently but share atomic logs for interactions. Built for robotics, energy harvesting sims, and AI economies.

## 🚀 Quick Start
### Prerequisites
- Python 3.10+
- `pip install fastapi uvicorn`

### Run
```bash
git clone https://github.com/JaronKBragg7337/Atomic-World-Chronicle-3.7
cd Atomic-World-Chronicle-3.7
python "ATOM Code 3.7"  # Or main script
uvicorn main:app --reload  # For API
```
Access at `http://localhost:8000/docs` for API playground.

## 🎮 Demo: Game → Robot → Reward
1. Start game world: Player scores points.
2. Triggers robot path: Executes hardware move.
3. Logs reward: Transparent economy credits action.
Query: `GET /worlds/game/state` shows full history.

## 🌍 Available Worlds
- **Game World**: Simple physics sim with scoring.
- **Robot World**: GPIO/serial integration for actuators.
- **Economy World**: Token rewards with blockchain-like transparency.

## 💰 Transparency Economy
All rewards are append-only tokens verifiable across worlds. Ideal for energy harvesting prototypes tracking output vs. rewards.

## 🔧 Configuration
Edit `config.yaml`:
```yaml
worlds:
  game: {gravity: 9.8}
  robot: {port: /dev/ttyUSB0}
economy: {reward_rate: 0.01}
```

## 📖 API Endpoints (FastAPI)
| Endpoint | Description | Example |
|----------|-------------|---------|
| `/worlds/{name}/state` | Get world state  | `curl http://localhost:8000/worlds/game/state` |
| `/action` | Execute cross-world action  | POST JSON: `{"from": "game", "to": "robot", "data": {...}}` |
| `/history/{world}` | Query full log | Immutable append-only chain. |

## 🤖 Hardware Integration
Supports Raspberry Pi/Arduino via serial. Example: Piezoelectric energy harvest → robot move → logged reward.

## 🧪 Development
- Add worlds in `worlds/` folder.
- Test: `pytest tests/`
- Contribute: Fork, PR with atomic logs.

## 🛤️ Roadmap
- v3.7: Multi-node clustering.
- Blockchain bridge for economies.
- Soft robotics + energy harvesting worlds.

## 📄 License
MIT License — free to build worlds!

## 🙏 Acknowledgments
Built for inventors prototyping the future. ⭐ Star if useful!

**🧑‍💻 Author**: JaronKBragg7337 (Fort Wayne, IN) — Energy harvesting, robotics, space tech enthusiast.

Atomic-World-Chronicle-3.7 https://github.com/JaronKBragg7337/Atomic-World-Chronicle-3.7


**Jaron Kyler Bragg**  
[GitHub](https://github.com/jaronkbragg7337) | [LinkedIn](https://linkedin.com/in/YOUR_PROFILE)
https://jaronkbragg7337.github.io/persistent-memory-substrate/
***
(https://github.com/JaronKBragg7337/ATOMIC-CHRONICLE-v4.0-A-World-You-Want-Or-a-World-of-Worlds)
*⭐ Star this repo if you find it useful!*

***

**for the future**  
`atomicd_chronicle_v4.py` — *A world you want, or a world of worlds.
