# 🚀 Meme Core - Advanced Meme Token Bundler - User friendly

<div align="center">

<img src="docs/meme-core.png" alt="Meme Core Logo" width="20%">
</div>

<div align="center">

[![Rust](https://img.shields.io/badge/rust-%23000000.svg?style=for-the-badge&logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)](https://reactjs.org/)
[![Tauri](https://img.shields.io/badge/tauri-%2324C8DB.svg?style=for-the-badge&logo=tauri&logoColor=%23FFFFFF)](https://tauri.app/)
[![Solana](https://img.shields.io/badge/Solana-black?style=for-the-badge&logo=Solana&logoColor=blueviolet)](https://solana.com/)

_The ultimate desktop application for creating, managing, and bundling meme tokens on Solana_ 🎯

[Features](#-features) • [Quick Start](#-quick-start) • [Installation](#-installation) • [Usage](#-usage) • [API](#-api) • [Contributing](#-contributing)

</div>

---

<div align="center">

**📱 Telegram: [@vladmeer](https://t.me/vladmeer67)**

</div>

# Video

---

![Wallets Config View](docs/create_token.gif)

<br>

# Screenshots

---

![Bundler View](docs/view-bundler2.png)

<br>

![Wallets Config View](docs/view-wallets-config2.png)

## 📋 Table of Contents

- [About](#-about)
- [Features](#-features)
- [Architecture](#-architecture)
- [Quick Start](#-quick-start)
- [Installation](#-installation)
- [Configuration](#-configuration)
- [Usage](#-usage)
- [API Reference](#-api-reference)
- [Contributing](#-contributing)
- [License](#-license)

## 🎭 About

**Meme Core** is a sophisticated desktop application built with **Rust** and **React** that empowers users to create, deploy, and manage meme tokens on the Solana blockchain with unprecedented ease and efficiency. Whether you're launching the next viral meme coin or managing a portfolio of tokens, Meme Core provides the tools you need.

### Why Meme Core? 🤔

- 🏃‍♂️ **Blazing Fast**: Built with Rust for maximum performance
- 🎨 **Beautiful UI**: Modern React interface with Tailwind CSS
- 🔧 **Powerful Tools**: Advanced bundling and wallet management
- 🛡️ **Secure**: Desktop-first approach with local key management
- 🌐 **Solana Native**: Deep integration with Solana ecosystem
- 📦 **All-in-One**: Token creation, buying, selling, and management

## ✨ Features

### 🪙 Token Creation & Management

- **One-Click Token Deployment** on Pump.fun
- **Custom Token Metadata** with IPFS integration
- **Bulk Token Operations** for efficient management
- **Real-time Price Tracking** and portfolio monitoring

### 💼 Advanced Wallet Management

- **Multi-Wallet Support** with hierarchical organization
- **Secure Key Storage** with local encryption
- **Bulk Wallet Generation** for advanced strategies
- **Balance Monitoring** across all wallets
- **SOL Distribution** tools for wallet funding

### 🚀 Automated Trading Features

- **Auto-Buy Functionality** with customizable triggers
- **Smart Bundling** for coordinated purchases
- **Slippage Protection** and MEV resistance
- **Priority Fee Management** for faster execution

### 🎯 Bundler Capabilities

- **Coordinated Token Launches** across multiple wallets
- **Volume Generation** for market making
- **Anti-Detection Measures** with randomized timing
- **Profit Distribution** tools

### 🔧 Developer Tools

- **Pump.fun SDK Integration** (`pumpfun-rs`)
- **Comprehensive API** for custom integrations
- **Logging & Analytics** for operation tracking
- **Configuration Management** for different strategies

## 🏗️ Architecture

```
meme-core/
├── 🦀 back/                    # Rust Backend (Tauri)
│   ├── src/
│   │   ├── config.rs          # Configuration management
│   │   ├── jobs.rs            # Background task management
│   │   ├── services/          # Core business logic
│   │   │   ├── create_meme_token.rs    # Token creation
│   │   │   ├── distribute_sol.rs       # SOL distribution
│   │   │   ├── close_accounts.rs       # Account cleanup
│   │   │   └── refund_wallets.rs       # Wallet management
│   │   └── solana/            # Solana blockchain integration
│   │       ├── buy.rs         # Token purchasing
│   │       ├── sell.rs        # Token selling
│   │       ├── create.rs      # Token creation
│   │       ├── price.rs       # Price feeds
│   │       └── tokens.rs      # Token utilities
│   └── tauri.conf.json        # Tauri configuration
├── ⚛️ front/                   # React Frontend
│   ├── src/
│   │   ├── components/        # Reusable UI components
│   │   ├── views/             # Main application views
│   │   ├── context/           # React context providers
│   │   ├── hooks/             # Custom React hooks
│   │   └── lib/               # Utility libraries
│   └── package.json
└── 📦 pumpfun-rs/             # Pump.fun SDK
    └── src/                   # Solana program integration
```

## 🚀 Quick Start

### Prerequisites

- **Windows 10/11** (Primary support)
- **Node.js 18+** and **npm**
- **Rust 1.70+** and **Cargo**
- **Visual Studio Build Tools** (C++)
- **Git**

### One-Line Installation

```powershell
# Clone and setup in one command
git clone https://github.com/vladmeer/pumpfun-bundler-rust.git && cd pumpfun-bundler && npm run setup
```

## 🛠️ Installation

### Step 1: Environment Setup (Windows)

Install **vcpkg** for dependency management:

```powershell
git clone https://github.com/microsoft/vcpkg C:\vcpkg
C:\vcpkg\bootstrap-vcpkg.bat
C:\vcpkg\vcpkg.exe install openssl:x64-windows
```

### Step 2: Environment Variables

Set up required environment variables:

```powershell
$env:VCPKG_ROOT="C:\vcpkg"
$env:OPENSSL_DIR="C:\vcpkg\installed\x64-windows"
$env:OPENSSL_LIB_DIR="$env:OPENSSL_DIR\lib"
$env:OPENSSL_INCLUDE_DIR="$env:OPENSSL_DIR\include"
$env:VCPKGRS_DYNAMIC="1"
$env:RUST_LOG="info"
```

### Step 3: Project Setup

```powershell
# Clone the repository
git clone https://github.com/vladmeer/pumpfun-bundler-rust.git
cd pumpfun-bundler-rust

# Install frontend dependencies
cd front
npm install
cd ..

# Build the Rust workspace
cargo clean
cargo build
```

### Step 4: Development Server

```powershell
# Start the development environment
cd back
cargo tauri dev
```

This will automatically:

- Start the React development server on `http://localhost:5173`
- Launch the Tauri desktop application
- Enable hot-reload for both frontend and backend

## 📸 Screenshots

Get a glimpse of the powerful interface and professional design:

### 🚀 Token Creator & Bundler Interface

_Create meme tokens and execute coordinated bundling operations_

![Bundler View](docs/view-bundler.png)

### ⚙️ Advanced Settings Panel

_Configure RPC endpoints, trading parameters, and automation settings_

![Settings View](docs/view-settings.png)

### 💼 Professional Wallet Management

_Manage multiple wallet groups with real-time balance tracking_

![Wallets Configuration](docs/view-wallets-config.png)

## ⚙️ Configuration

### Environment Configuration

Create a `.env` file in the `back/` directory:

```env
# Solana RPC Configuration
SOLANA_RPC_URL=https://api.mainnet-beta.solana.com
SOLANA_WS_URL=wss://api.mainnet-beta.solana.com

# Default Trading Parameters
DEFAULT_SLIPPAGE_BPS=500
DEFAULT_PRIORITY_FEE=100000
MAX_RETRIES=3

# Logging
RUST_LOG=info
```

### Wallet Configuration

Import your wallets using a CSV file format for better security and bulk management:

**Create a `wallets.csv` file:**

```csv
publicKey,privateKey
4CkQJBxhU8EZ2UjhigbtdaTESVV1xdJ4oMjY9JbY5R8WdQs6,2CkQJBxhU8EZ2UjhigbtdaTESVV1xdJ4oMjY9JbY5R8W...
7GkNJBxhU8EZ2UjhigbtdaTESVV1xdJ4oMjY9JbY5R8WaPs3,5GkNJBxhU8EZ2UjhigbtdaTESVV1xdJ4oMjY9JbY5R8W...
9FkQJBxhU8EZ2UjhigbtdaTESVV1xdJ4oMjY9JbY5R8WbKs1,8FkQJBxhU8EZ2UjhigbtdaTESVV1xdJ4oMjY9JbY5R8W...
```

**Import via the application:**

1. Open **Wallet Manager**
2. Click **"Import Wallets"** button
3. Select your `wallets.csv` file
4. Choose wallet group name
5. All wallets will be automatically loaded and organized

**CSV Format Requirements:**

- First line must be the header: `publicKey,privateKey`
- Each subsequent line contains one wallet
- Private keys should be in base58 format
- Public keys are automatically derived but can be included for validation

## 🎮 Usage

### Creating a Meme Token 🪙

1. **Navigate to Pumpfun bundler**

   - Open the application
   - Select "Pumpfun bundler" from the sidebar

2. **Configure Token Details**

   ```
   Name: My Awesome Meme
   Symbol: MEME
   Description: The most epic meme token ever!
   Supply: 1,000,000,000
   ```

3. **Set Launch Parameters**

   - Initial SOL amount for development
   - Slippage tolerance
   - Priority fees

4. **Deploy** 🚀
   - Click "Create Token"
   - Monitor transaction status
   - Get your token mint address

### Auto-Buy Configuration 🤖

1. **Access Auto-Buy Panel**
2. **Set Trigger Conditions**

   - Price thresholds
   - Volume triggers
   - Time-based conditions

3. **Configure Wallets**
   - Select participating wallets
   - Set individual buy amounts
   - Configure timing randomization

### Bundler Operations 📦

1. **Select Target Token**
2. **Configure Bundle Parameters**

   - Number of participating wallets
   - Individual purchase amounts
   - Timing strategy
   - Multiple groups of wallets with configurable strategies for each

3. **Execute Bundle**
   - Monitor real-time execution
   - Track success rates
   - Analyze results

## 📊 API Reference

### Token Creation API

```rust
pub struct CreateTokenReq {
    pub name: String,
    pub symbol: String,
    pub decimals: f64,
    pub supply_human: u64,
    pub dev_sol_amount: f64,
    pub slippage_bps: u64,
    // ... additional fields
}
```

### Wallet Management API

```rust
// Distribute SOL to multiple wallets
distribute_sol(wallets: Vec<WalletInfo>, amount: f64) -> Result<Vec<TxResult>>

// Generate new wallets
generate_wallets(count: u32, group: String) -> Result<Vec<Wallet>>

// Refund wallets to main wallet
refund_wallets(wallets: Vec<String>) -> Result<Vec<TxResult>>
```

### Trading API

```rust
// Buy tokens
buy_token(mint: String, amount: f64, wallet: String) -> Result<TxResult>

// Sell tokens
sell_token(mint: String, percentage: f64, wallet: String) -> Result<TxResult>
```

## 🎨 UI Components

### Main Views

- **🏠 Dashboard**: Overview and statistics
- **🪙 Pumpfun bundler**: Create and deploy new tokens
- **💼 Wallet Manager**: Manage multiple wallets
- **🚀 Bundler**: Execute coordinated operations
- **⚙️ Settings**: Application configuration

### Key Features

- **Real-time Updates** with WebSocket integration
- **Responsive Design** with Tailwind CSS
- **Dark Theme** optimized for trading
- **Toast Notifications** for operation feedback
- **Modal Dialogs** for configuration

## 🔧 Development

### Project Structure

The project follows a **Cargo workspace** architecture:

```
trading_corps/
 ├─ Cargo.toml        ← Workspace root (Rust)
 ├─ front/            ← React frontend (npm/yarn/pnpm)
 │   └─ package.json
 └─ back/             ← Rust binary + Tauri
     └─ Cargo.toml
```

### Development Workflow

1. **Install frontend dependencies:**

```powershell
cd trading_corps/front
npm install
```

2. **Launch Tauri (from `back/`):**

```powershell
cd trading_corps/back
cargo tauri dev
```

The `beforeDevCommand` will start `npm run dev` in `../front`, and Tauri will load `http://localhost:5173`.

### Building for Production

```powershell
# Build optimized release
cargo tauri build

# The installer will be created in:
# back/target/release/bundle/
```

### Testing

```powershell
# Run Rust tests
cargo test

# Run frontend tests
cd front
npm test
```

### Development Guidelines

- Follow Rust conventions and clippy recommendations
- Use TypeScript for new frontend components
- Add tests for new functionality
- Update documentation as needed
- **Cargo workspace** manages all Rust crates (`back`, `pumpfun-rs`, etc.)
- **package.json only in `front/`** - JS doesn't need to be in the Rust workspace
- Everything stays clean: `cargo build` manages Rust crates, `npm run dev` manages frontend, and Tauri bridges them

## � Get the Full Version

**Interested in this project and want to see the complete version?**

This repository contains only a documentation showcasing the core architecture and features. For access to the **full production-ready version** with advanced features, enhanced security, and complete functionality:

📱 **Contact me on Telegram: [@vladmeer](https://t.me/vladmeer67)**

### Full Version Includes:

- 🔒 **Advanced Security Features**
- 🎯 **Professional Trading Algorithms**
- 📊 **Enhanced Analytics Dashboard**
- 📈 **Advanced Bundling Strategies**
- 🎮 **Premium UI/UX Experience**
- 📞 **Priority Support & Updates**

---

<div align="center">

**📱 Telegram: [@vladmeer](https://t.me/vladmeer67)**
**📱 Twitter: [@vladmeer](https://x.com/vladmeer67)**

</div>
