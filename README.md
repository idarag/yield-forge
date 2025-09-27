# YieldForge Protocol

[![Clarity Version](https://img.shields.io/badge/Clarity-3.2-blue?style=flat-square)](https://docs.stacks.co/clarity)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![Tests](https://img.shields.io/badge/Tests-Vitest-yellow?style=flat-square)](https://vitest.dev/)

## Advanced sBTC Yield Generation Platform on Stacks Layer 2

YieldForge is an innovative DeFi protocol that transforms idle sBTC holdings into productive yield-generating assets through sophisticated time-weighted staking mechanisms and automated reward distribution systems.

## 🎯 Overview

Built on Stacks Layer 2, YieldForge revolutionizes Bitcoin DeFi by offering institutional-grade staking infrastructure with unparalleled flexibility. The protocol features dynamic APY calculations, compound reward mechanisms, and governance-driven parameter optimization to maximize returns while maintaining security.

### Key Benefits

- **Non-custodial staking** with instant reward claiming capabilities
- **Configurable lock periods** that balance liquidity needs with yield optimization
- **Zero-slippage reward claiming** with automatic compounding options
- **Mathematical precision** in reward calculations using time-weighted algorithms
- **Enterprise-ready security** model with multi-layer validation

## 🚀 Core Features

### Yield Generation Engine

- **Time-weighted rewards**: Sophisticated algorithms that calculate yields based on staking duration
- **Compound growth**: Automatic reward accumulation with timestamp-based reset mechanisms
- **Flexible staking**: Support for partial unstaking and position management
- **Dynamic APY**: Real-time yield calculations based on protocol parameters

### Governance & Security

- **Decentralized governance**: Community-driven parameter optimization
- **Multi-layer validation**: Enterprise-grade security framework
- **Rate limiting**: Configurable reward rate caps for protocol stability
- **Minimum commitment periods**: Balanced approach to yield optimization and liquidity

### Analytics & Transparency

- **Comprehensive dashboards**: Real-time protocol health metrics
- **Historical tracking**: Complete audit trail of reward distributions
- **TVL monitoring**: Total Value Locked tracking and reporting
- **APY calculations**: Live yield rate displays for users

## 📊 Protocol Statistics

| Metric | Description |
|--------|-------------|
| **Current APY** | Dynamic yield rate based on reward rate configuration |
| **Total Staked** | Aggregate sBTC locked in the protocol (TVL) |
| **Reward Pool** | Available reserves for yield distribution |
| **Min Stake Period** | Security-focused minimum commitment (blocks) |

## 🏗️ Architecture

### Smart Contract Structure

```text
YieldForge Protocol
├── Core Functions
│   ├── stake(amount)              # Deploy capital into yield position
│   ├── unstake(amount)            # Execute position liquidation
│   └── claim-rewards()            # Harvest accumulated yields
├── Governance
│   ├── set-reward-rate(rate)      # Calibrate yield parameters
│   ├── set-min-stake-period()     # Optimize commitment requirements
│   └── set-contract-owner()       # Execute governance transitions
└── Analytics
    ├── calculate-rewards()        # Time-weighted yield calculations
    ├── get-protocol-stats()       # Comprehensive health metrics
    └── get-stake-info()           # Individual position details
```

### Data Storage Layer

- **Stakes Map**: Primary staking records with timestamp-based tracking
- **Rewards Claimed**: Historical reward distribution for transparency
- **Protocol Variables**: Dynamic configuration parameters

## 🛠️ Development Setup

### Prerequisites

- [Clarinet](https://github.com/hirosystems/clarinet) >= 2.0
- [Node.js](https://nodejs.org/) >= 18
- [Git](https://git-scm.com/)

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/idarag/yield-forge.git
   cd yield-forge
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Verify setup**

   ```bash
   clarinet check
   ```

### Running Tests

```bash
# Run test suite
npm test

# Run tests with coverage and cost analysis
npm run test:report

# Watch mode for development
npm run test:watch
```

### Contract Validation

```bash
# Check contract syntax and analysis
clarinet check

# Format contract code
clarinet fmt --in-place

# Deploy to devnet
clarinet integrate
```

## 🔧 Configuration

### Network Settings

The protocol supports multiple deployment environments:

- **Devnet**: `settings/Devnet.toml`
- **Testnet**: `settings/Testnet.toml`
- **Mainnet**: `settings/Mainnet.toml`

### Protocol Parameters

| Parameter | Default | Description |
|-----------|---------|-------------|
| `reward-rate` | 5 basis points | Dynamic yield rate (0.01% precision) |
| `min-stake-period` | 1440 blocks | Minimum commitment period |
| `reward-pool` | 0 | Available reward distribution reserves |

## 📖 Usage Examples

### Basic Staking

```clarity
;; Stake 1000 sBTC tokens
(contract-call? .yield-forge stake u1000000000)

;; Check your stake information
(contract-call? .yield-forge get-stake-info tx-sender)

;; Calculate pending rewards
(contract-call? .yield-forge calculate-rewards tx-sender)
```

### Reward Management

```clarity
;; Claim accumulated rewards
(contract-call? .yield-forge claim-rewards)

;; Partial unstaking (500 sBTC)
(contract-call? .yield-forge unstake u500000000)

;; View reward history
(contract-call? .yield-forge get-rewards-claimed tx-sender)
```

### Protocol Analytics

```clarity
;; Get comprehensive protocol statistics
(contract-call? .yield-forge get-protocol-stats)

;; Check current APY
(contract-call? .yield-forge get-current-apy)

;; Monitor total value locked
(contract-call? .yield-forge get-total-staked)
```

## 🔐 Security Considerations

### Error Handling

The protocol implements comprehensive error handling with specific error codes:

- `ERR_NOT_AUTHORIZED (100)`: Unauthorized governance action
- `ERR_ZERO_STAKE (101)`: Invalid zero amount operation
- `ERR_NO_STAKE_FOUND (102)`: No active stake position
- `ERR_TOO_EARLY_TO_UNSTAKE (103)`: Minimum period not satisfied
- `ERR_INVALID_REWARD_RATE (104)`: Rate exceeds safety limits
- `ERR_NOT_ENOUGH_REWARDS (105)`: Insufficient reward pool
- `ERR_INVALID_PERIOD (106)`: Invalid staking period
- `ERR_SAME_OWNER (107)`: Redundant ownership transfer

### Best Practices

1. **Always verify transaction parameters** before calling contract functions
2. **Monitor reward pool levels** before claiming rewards
3. **Understand minimum staking periods** before committing capital
4. **Use test environments** for integration development
5. **Follow governance procedures** for parameter changes

## 🤝 Contributing

We welcome contributions from the community! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details on:

- Code style and formatting
- Testing requirements
- Pull request process
- Security disclosure policy

### Development Workflow

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔗 Links & Resources

- **Documentation**: [docs.yieldforge.io](https://docs.yieldforge.io)
- **Stacks Documentation**: [docs.stacks.co](https://docs.stacks.co)
- **Clarity Language**: [clarity-lang.org](https://clarity-lang.org)
- **Clarinet CLI**: [github.com/hirosystems/clarinet](https://github.com/hirosystems/clarinet)

## 💬 Community & Support

- **Discord**: [Join our Discord](https://discord.gg/yieldforge)
- **Twitter**: [@YieldForge](https://twitter.com/yieldforge)
- **GitHub Issues**: [Report bugs and feature requests](https://github.com/idarag/yield-forge/issues)
- **Email**: [support@yieldforge.io](mailto:support@yieldforge.io)

---

**Disclaimer**: This protocol is experimental software. Users should conduct their own research and exercise caution when interacting with smart contracts. Never invest more than you can afford to lose.

Built with ❤️ for the Bitcoin DeFi ecosystem on Stacks
