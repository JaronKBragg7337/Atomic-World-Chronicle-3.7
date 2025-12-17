Atomic World Chronicle v3.7

**A world you want — or a world of worlds.**

Atomic Chronicle v4.0 is an **append-only execution and memory substrate** that records actions, state transitions, and outcomes across time. It hosts multiple independent "worlds" (simulations, robotics, economies, games) that can interact while preserving perfect historical fidelity.

> *It preserves what happened, not why it should have happened.*

## ✨ Features

- **Multi-World Architecture**: Run games, robots, energy systems, DAOs simultaneously
- **Inter-World Causality**: GameControl → RobotWorld → RewardWorld pipelines
- **Transparency Economy**: Rewards discovery of unknown entities
- **Physical Integration**: Serial control for real robots/vehicles
- **VR/Gamepad Ready**: Human input → structured commands
- **FastAPI/WebSocket**: Live control and streaming
- **Offline-Capable**: Single file, no external dependencies required
- **Feature Toggles**: Enable/disable worlds via config/CLI/API

## 🏗️ Architecture Overview

```
GameControlWorld ──→ RobotWorld ──→ RewardWorld
     ↓                    ↓              ↓
EnergyHarvester ──→ FlywheelPlant     OmniWorld (Meta-Control)
     ↓
PublicCommons ←→ PrivateConsortium ← TransparencyEconomy
     ↓
     └─→ Atomic Chronicle Core (Blocks + RUS Validation)
```

## 🚀 Quick Start

### Prerequisites
- Python 3.7+
- (Optional) `pygame`, `pyserial`, `fastapi[all]` for full features

## 🎮 Demo: Game → Robot → Reward Pipeline

1. **Player plays Asteroids** (or sends gamepad input)
2. **GameControlWorld** translates to robot commands
3. **RobotWorld** executes (simulated or real hardware via serial)
4. **RewardWorld** pays player tokens on success

```python
# Example: Send game command
game_control.step({"action": "move_forward", "distance": 1.0})

# Carrier automatically routes: Game → Robot → Reward
```

## 🌍 Available Worlds

| World | Domain | Purpose |
|-------|--------|---------|
| `EnergyHarvesterWorld` | Energy | Log harvested energy (solar/wind/piezo) |
| `FlywheelPlantWorld` | Storage | Mechanical energy storage (RPM/kWh) |
| `WindupGeneratorWorld` | Mechanics | Spring-based generator simulation |
| `AsteroidsGameWorld` | Gaming | Classic asteroids with score/leveling |
| `GameControlWorld` | Control | Gamepad → robot command translation |
| `RobotWorld` | Robotics | Serial control for real hardware |
| `RewardWorld` | Economy | Token rewards for completed jobs |
| `MysteryTechnologyWorld` | Research | Unknown tech discovery mechanics |
| `PublicCommonsWorld` | Social | Open knowledge sharing |
| `PrivateConsortiumWorld` | DAO | Private proposals/voting |
| `OmniWorld` | Meta | Route/toggle any world |

## 💰 Transparency Economy

- **Register entities** (tech, robots, data) as `public`/`private`/`unknown`
- **Discovery rewards**: Reveal mysteries → earn tokens
- **Commercial rights**: Public entities generate license fees
- **Reputation system**: Transparency = earning multiplier

```python
# Register mystery tech
te = TransparencyEconomy()
reg = te.transparency.register_entity("mystery_device", "unknown")

# Attempt reveal for rewards
result = te.reveal_entity("mystery_device", "researcher", evidence={"scan_data": "..."})
```

## 🔧 Configuration

Create `atomic_chronicle_config.json`:
```json
{
  "enable_robot_world": true,
  "enable_fastapi_server": true,
  "enable_omni_world": true
}
```

CLI overrides:
```bash
python atomic_chronicle_v4.py --set-feature enable_game_world=false --no-server
```

## 📖 API Endpoints (FastAPI)

| Endpoint | Description |
|----------|-------------|
| `GET /` | System status + world list |
| `POST /world/{name}/step` | Execute action in specific world |
| `GET /world/{name}/chain` | Retrieve world blockchain |
| `WS /ws` | Live block stream |
| `POST /omni/route` | OmniWorld command routing |

## 🧪 Development

```bash
# Run tests
python -m pytest tests/

# Lint
flake8 atomic_chronicle_v4.py

# Generate docs
pydoc-markdown atomic_chronicle_v4.py > API.md
```

## 🤖 Hardware Integration

Connect real robot:
```bash
# Edit RobotWorld port
python atomic_chronicle_v4.py --set-feature enable_robot_world=true
```

Supported: Serial (USB), future: Network, CAN bus, ROS2

## 📚 Philosophy

Atomic Chronicle embodies **existential equality**:
> *I am not higher or below any other entity. We create equal opportunity.*

- **Neutral substrate**: No moral judgment of actions
- **Perfect memory**: Every outcome preserved forever
- **Rediscoverable**: Future civilizations can reconstruct history
- **Multi-reality**: Each world defines its own physics/economics

## 🛤️ Roadmap

- [x] Core block ledger + RUS validation
- [x] Multi-world architecture + Carrier
- [x] Game→Robot→Reward pipeline
- [x] Transparency Economy
- [x] FastAPI/WebSocket interface
- [ ] VR/AR integration
- [ ] Distributed carrier (P2P)
- [ ] Hardware wallet integration
- [ ] Mobile app controller

## 🤝 Contributing

1. Fork the repo
2. Create feature branch (`git checkout -b feature/AmazingWorld`)
3. Commit changes (`git commit -m 'Add AmazingWorld'`)
4. Push (`git push origin feature/AmazingWorld`)
5. Open Pull Request

See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

## 📄 License

MIT License - see [LICENSE](LICENSE) file.

## 🙏 Acknowledgments

- Built for long-term continuity and rediscoverability
- Inspired by blockchain immutability + simulation theory
- Designed for physical-digital convergence

## 🧑‍💻 Author

**Jaron Kyler Bragg**  
[GitHub](https://github.com/jaronkbragg7337) | [LinkedIn](https://linkedin.com/in/YOUR_PROFILE)
https://jaronkbragg7337.github.io/persistent-memory-substrate/
***
4.0 is OLD version USE 3.7 (yes backwards) (https://github.com/JaronKBragg7337/ATOMIC-CHRONICLE-v4.0-A-World-You-Want-Or-a-World-of-Worlds)
A-World-You-Want-Or-a-World-of-Worlds
*⭐ Star this repo if you find it useful!*

***

**Made with ❤️ for the future**  
`atomic_chronicle_v4.py` — *A world you want, or a world of worlds.
