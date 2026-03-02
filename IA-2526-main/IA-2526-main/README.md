<div align="center">

# 🚖 TaxiGreen - AI Fleet Management

### *Smart Autonomous Taxi Fleet Simulation for the City of Braga*

[![Python](https://img.shields.io/badge/Python-3.13-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![AI](https://img.shields.io/badge/AI-Pathfinding-orange.svg)]()
[![Status](https://img.shields.io/badge/Status-Active-success.svg)]()

---

**TaxiGreen** is an advanced simulation and fleet management system for autonomous smart taxis. Leveraging **Artificial Intelligence algorithms**, it optimizes routes, manages energy consumption, and efficiently allocates vehicles to passenger requests in dynamic urban environments.

[Features](#-key-features) • [Installation](#️-installation) • [Usage](#-usage) • [Documentation](#-documentation) • [Authors](#-authors)

---

</div>

## ✨ Key Features

<table>
<tr>
<td width="50%">

### 🗺️ Real City Graph
- Authentic mapping of **Braga city** using real OpenStreetMap data
- Nodes and edges represent actual streets and intersections
- Dynamic traffic simulation

</td>
<td width="50%">

### ⚡ Energy Management
- Realistic fuel/battery consumption simulation
- Support for both Gas and Electric vehicles
- Strategic charging station placement

</td>
</tr>
<tr>
<td width="50%">

### 🧭 Intelligent Pathfinding
- Advanced algorithms (**A***, **Dijkstra**)
- Distance and traffic-aware routing
- Real-time route optimization

</td>
<td width="50%">

### 🌐 Client-Server Architecture
- Distributed simulation design
- Server manages world state
- Agents interact via socket communication

</td>
</tr>
<tr>
<td colspan="2">

### 📊 Real-Time Visualization
- Live graphical interface for fleet monitoring
- Performance metrics and analytics dashboard
- Visual representation of taxi movements and requests

</td>
</tr>
</table>

---

## 🛠️ Installation

### Prerequisites

- **Python 3.13** or higher
- Git

### Quick Start

1. **Clone the repository:**

```bash
git clone https://github.com/your-repo/IA-2526.git
cd IA-2526
```

2. **Create a Virtual Environment** *(Recommended):*

```bash
# Linux/Mac
python -m venv .venv
source .venv/bin/activate

# Windows
python -m venv .venv
.venv\Scripts\activate
```

3. **Install Dependencies:**

```bash
pip install -r requirements.txt
```

Or simply use:

```bash
make install
```

---

## 🚀 Usage

### Using Makefile (Recommended)

The project includes a `Makefile` for easy automation:

| Command | Description |
|---------|-------------|
| `make help` | Display all available commands with descriptions |
| `make install` | Install all dependencies from requirements.txt |
| `make server` | Start the TaxiGreen simulation server |
| `make client` | Start the TaxiGreen client (open in a new terminal) |
| `make doc` | Generate complete Sphinx documentation (HTML) |
| `make doc-open` | Open the generated documentation in browser |
| `make docclean` | Clean only the documentation build folder |
| `make clean` | Remove all cache, logs, docs build, and temporary files |

> **Note:** On Windows without `make`, install [GnuWin32](http://gnuwin32.sourceforge.net/packages/make.htm) or use [WSL](https://docs.microsoft.com/en-us/windows/wsl/).

### Manual Execution

If you prefer not to use the Makefile, follow these steps:

#### 1️⃣ Generate Map Data *(Optional)*

If you need to regenerate Braga's OpenStreetMap data and create CSV files:

```bash
python -m src.utils.Graph_Generator
```

#### 2️⃣ Run the Server

Start the simulation server to manage world state:

```bash
python -m src.server
# or use: make server
```

#### 3️⃣ Run the Client *(In a new terminal)*

Launch the agent logic and visualization interface:

```bash
python -m src.client
# or use: make client
```

> **💡 Tip:** You need to run the server first, then open a new terminal window to run the client.

---

## 📚 Documentation

Technical documentation is automatically generated using **Sphinx** with the **Read the Docs** theme.

### 📖 Generate Documentation

```bash
make doc
```

This will generate fresh HTML documentation in `docs/_build/html`.

### 🌐 View Documentation

You can open the documentation automatically:

```bash
make doc-open
```

Or manually open this file in your browser:

```
docs/_build/html/index.html
```

### 🧹 Clean Documentation

To remove only the documentation build:

```bash
make docclean
```

### 📋 Documentation Contents

- **Core Models:** Cars, Fuel Stations, Graphs, Nodes, Edges
- **Simulation:** Environment logic, data loading, report generation
- **Utilities:** Helper tools, interfaces, and generators
- **Visualization:** Real-time monitoring and analytics

---

## 📂 Project Structure

```
IA-2526/
├── 📁 data/                  # CSV datasets (nodes, edges, cars)
├── 📁 docs/                  # Sphinx documentation
│   ├── conf.py
│   ├── index.rst
│   └── _build/              # Generated HTML docs
├── 📁 src/                   # Source code
│   ├── 📁 models/           # Core classes (Car, Graph, Node, etc.)
│   ├── 📁 simulation/       # Simulation logic and visualization
│   ├── 📁 utils/            # Utility scripts and generators
│   ├── client.py            # 🎮 Client entry point
│   └── server.py            # 🖥️  Server entry point
├── 📄 Makefile              # Task automation
├── 📄 requirements.txt      # Python dependencies
├── 📄 LICENSE               # License information
└── 📄 README.md             # This file
```

---

## 👥 Authors

**Group 6** - *Artificial Intelligence Course (2025)*

<table>
<tr>
<td align="center">
<a href="https://github.com/DelgadoDevT">
<img src="https://github.com/DelgadoDevT.png" width="100px;" alt="DelgadoDevT"/><br />
<sub><b>DelgadoDevT</b></sub>
</a>
</td>
<td align="center">
<a href="https://github.com/PaoComPlanta">
<img src="https://github.com/PaoComPlanta.png" width="100px;" alt="PaoComPlanta"/><br />
<sub><b>PaoComPlanta</b></sub>
</a>
</td>
<td align="center">
<a href="https://github.com/SirLordNelson">
<img src="https://github.com/SirLordNelson.png" width="100px;" alt="SirLordNelson"/><br />
<sub><b>SirLordNelson</b></sub>
</a>
</td>
<td align="center">
<a href="https://github.com/M4chad0">
<img src="https://github.com/M4chad0.png" width="100px;" alt="M4chad0"/><br />
<sub><b>M4chad0</b></sub>
</a>
</td>
</tr>
</table>

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

*University of Minho • 2025*

</div>
