# 🦥 SlerfSwap V2 - Decentralized Exchange Protocol

> A community-driven AMM DEX on X-Layer with reduced fees and enhanced features

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Network: X-Layer](https://img.shields.io/badge/Network-X--Layer-green.svg)](https://www.okx.com/xlayer)
[![Fee: 0.2%](https://img.shields.io/badge/Swap%20Fee-0.2%25-orange.svg)]()

## 🌟 Features

### 💰 Lower Fees
- **Swap Fee**: 0.2% (vs 0.30% standard)
- **Reduced Trading Costs**: Save 33% on every trade
- **LP Friendly**: More competitive returns for liquidity providers

### 🚀 X-Layer Optimized
- **Native Integration**: Built specifically for X-Layer blockchain
- **Low Gas Costs**: Benefit from X-Layer's efficient infrastructure
- **OKB Support**: Native support for wrapped OKB (WOKB)

### 🔧 Enhanced Features
- **Standalone Contracts**: No external dependencies
- **Hash Verification**: Built-in INIT_CODE_PAIR_HASH() function
- **GPL-3.0 Compliant**: Fully open source and legally compliant

## 📋 Contract Addresses

### Mainnet (X-Layer)
```
Factory: [0x702758afEDBD000A982D5A9845b0B0b32916d97b]
Router:  [0x04aE0E6364635f307A7c81Bee1F8612C14d19917]
WOKB:    [0xe538905cf8410324e03A5A23C1c177a474D59b2b]
```

### Testnet (X-Layer)
```
Factory: [To be deployed]
Router:  [To be deployed]
WOKB:    [To be deployed]
```

## 🏗️ Architecture

### Core Contracts
- **SlerfSwapV2Factory**: Creates and manages trading pairs
- **SlerfSwapV2Pair**: Individual trading pair implementation
- **SlerfSwapV2ERC20**: LP token standard implementation

### Periphery Contracts
- **SlerfSwapV2Router02**: User-facing trading interface
- **SlerfSwapV2Library**: Mathematical calculations and utilities
- **TransferHelper**: Safe token transfer utilities

## 🛠️ Development

### Prerequisites
- Node.js 16+
- Hardhat or Remix IDE
- MetaMask wallet
- X-Layer network configuration

### Deployment
1. **Deploy Factory**:
   ```solidity
   constructor(address _feeToSetter)
   ```

2. **Get INIT_CODE_PAIR_HASH**:
   ```solidity
   factory.INIT_CODE_PAIR_HASH()
   ```

3. **Update Router Library**:
   - Update hash in SlerfSwapV2Library
   - Recompile Router contract

4. **Deploy Router**:
   ```solidity
   constructor(address _factory, address _WETH)
   ```

### Testing
```bash
# Run tests
npm test

# Deploy to testnet
npm run deploy:testnet

# Deploy to mainnet
npm run deploy:mainnet
```

## 📊 Fee Structure

### Trading Fees
- **Total Swap Fee**: 0.2% per trade
- **LP Share**: 0.16% (80% of total fee)
- **Protocol Share**: 0.04% (20% of total fee)

### Fee Distribution
```
User Trade (0.2%) → LP Rewards (0.16%) + Protocol (0.04%)
```

### Fee Breakdown
- **Liquidity Providers**: Receive 80% of all trading fees
- **Platform**: Receives 20% of trading fees for development and maintenance
- **Competitive Advantage**: 33% lower fees than standard 0.3% DEXs

## 🔒 Security

### Auditing Status
- **Code Review**: Internal security review completed
- **Open Source**: All code publicly available
- **Battle Tested**: Based on proven Uniswap V2 architecture

### Security Features
- **Reentrancy Protection**: Lock modifiers on critical functions
- **Overflow Protection**: SafeMath library usage
- **Access Control**: Proper permission management

## ⚖️ Legal Compliance

### Open Source License
- **License**: GNU General Public License v3.0
- **Base Code**: Uniswap V2 (GPL-3.0-or-later)
- **Compliance**: Fully compliant with GPL-3.0 requirements

### Attribution
This project is based on Uniswap V2:
- **Original Authors**: Uniswap Labs and contributors
- **Modifications**: SlerfSwap Team
- **License**: GPL-3.0-or-later

## 🤝 Contributing

We welcome contributions from the community!

### How to Contribute
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

### Development Guidelines
- Follow Solidity best practices
- Maintain GPL-3.0 license compatibility
- Document all changes
- Include comprehensive tests

## 📞 Community

### Official Links
- **Website**: [slerfswap.com](http://slerfswap.com/)
- **Documentation**: [docs.slerfswap.com](https://docs.slerfswap.com/)
- **GitHub**: [SlerfSwap](https://github.com/SlerfSwap)
- **Twitter**: [@SlerfTools](https://twitter.com/SlerfTools)
- **Telegram**: [SlerfTools](https://t.me/SlerfTools)
- **TG Channel**: [SlerfTools_Official](https://t.me/SlerfTools_Official)

### Support
- **Technical Issues**: GitHub Issues
- **Community Support**: [Telegram](https://t.me/SlerfTools)
- **Official Email**: [official@slerfswap.com](mailto:official@slerfswap.com)

## ⚠️ Disclaimer

- **No Financial Advice**: This software is provided for informational purposes only
- **Use at Own Risk**: Users are responsible for their own due diligence
- **No Warranty**: Software provided "AS IS" without warranty of any kind
- **Regulatory Compliance**: Users must comply with local regulations

## 📜 License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details.

Based on Uniswap V2, which is also licensed under GPL-3.0-or-later.

---

**Built with ❤️ by the SlerfSwap Community**