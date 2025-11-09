# NFT Market Analysis Using Covalent API 📊

> **Comprehensive cross-chain NFT market data analysis and visualization toolkit**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Covalent API](https://img.shields.io/badge/Powered%20by-Covalent%20API-brightgreen)](https://www.covalenthq.com/)

## 🎯 Project Overview

This project was created as a submission for the [Gitcoin Bounty: Codeless Con - Build An NFT CryptoSheets Using Covalent API](https://gitcoin.co/issue/covalenthq/covalent-gitcoin-bounties/18/100027635).

It provides a comprehensive analysis of NFT market data across **four major blockchain networks** using the Covalent API, complete with SQL querying capabilities and interactive data visualizations.

## 🚀 Features

- ✅ **Multi-Chain Support**: Analyzes NFT data from Ethereum, Polygon, Avalanche, and Fantom
- ✅ **Real-Time Data**: Fetches live NFT market data using Covalent's powerful API
- ✅ **SQL Analytics**: Built-in SQLite database with 10+ pre-configured analytical queries
- ✅ **Data Visualization**: Beautiful charts and graphs using Matplotlib and Seaborn
- ✅ **Export Capabilities**: Data available in Excel (.xlsx) and SQLite (.db) formats
- ✅ **Comprehensive Analysis**: Market cap rankings, transaction volumes, deployment histories

## 📊 Supported Blockchains

| Blockchain | Chain ID | Icon |
|-----------|----------|------|
| **Ethereum** | 1 | 🔷 |
| **Polygon** | 137 | 🟣 |
| **Avalanche** | 43114 | 🔺 |
| **Fantom** | 250 | 👻 |

## 🛠️ Installation

### Prerequisites

- Python 3.8 or higher
- pip package manager

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/jakobrichert/CovalentAnalaysis.git
   cd CovalentAnalaysis
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook covalentnft_analysis.ipynb
   ```

## 📁 Repository Structure

```
CovalentAnalaysis/
│
├── covalentnft_analysis.ipynb    # Main analysis notebook with visualizations
├── nft_market_data.xlsx           # Excel export of NFT market data
├── nft_market_data.db             # SQLite database for SQL queries
├── requirements.txt                # Python dependencies
├── README.md                       # This file
└── LICENSE                         # MIT License
```

## 💡 Key Insights Uncovered

The analysis reveals fascinating insights about the NFT market:

1. **Market Dominance**: Ethereum hosts ~70% of all NFT collections analyzed
2. **Transaction Leader**: "ZED Horse" (Polygon) has the highest all-time transaction count
3. **Historical Context**: CryptoKitties (2017) was the earliest NFT deployment on Ethereum
4. **Cross-Chain Growth**: Polygon shows significant NFT activity with 3,500+ collections

## 📈 Analytical Queries Included

The notebook includes 10 sophisticated SQL queries:

| # | Query Description |
|---|-------------------|
| 1 | Top 5 Ethereum NFT collections by market cap |
| 2 | Top 5 Polygon NFT collections by market cap |
| 3 | Top 5 Avalanche NFT collections by market cap |
| 4 | Top 5 Fantom NFT collections by market cap |
| 5 | NFT collection distribution across blockchains |
| 6-9 | Earliest NFT contract deployments per chain |
| 10 | Highest transaction volume collection (all chains) |

## 🎨 Visualizations

The notebook generates professional-grade visualizations including:

- **Bar Charts**: Collection counts by blockchain
- **Pie Charts**: Market share distribution
- **Horizontal Bar Charts**: Top collections by market cap per chain
- **Statistical Tables**: Market cap analytics and deployment timelines

## 🔍 Sample Results

### Top Ethereum Collections by Market Cap
1. Rarible
2. Town Star
3. Fantasy Islands - Sandbox
4. Sandbox's LANDs
5. BoredApeYachtClub

### Blockchain Distribution
- **Ethereum**: 9,039 collections (69.8%)
- **Polygon**: 3,545 collections (27.4%)
- **Avalanche**: 308 collections (2.4%)
- **Fantom**: 33 collections (0.3%)

## 🧰 Technologies Used

- **Data Source**: [Covalent API](https://www.covalenthq.com/)
- **Language**: Python 3.8+
- **Data Processing**: Pandas, SQLite3
- **Visualization**: Matplotlib, Seaborn
- **Export Formats**: Excel (openpyxl), SQLite
- **Environment**: Jupyter Notebook

## 📝 Usage Examples

### Loading the Data

```python
import pandas as pd
import sqlite3

# Load from Excel
df = pd.read_excel('nft_market_data.xlsx')

# Or load from SQLite
conn = sqlite3.connect('nft_market_data.db')
df = pd.read_sql('SELECT * FROM nft_collections', conn)
```

### Running Custom Queries

```python
cursor = conn.cursor()

# Example: Find all Ethereum NFTs with market cap > $1M
query = '''
    SELECT collection_name, market_cap_quote
    FROM nft_collections
    WHERE chain_id = 1 AND market_cap_quote > 1000000
    ORDER BY market_cap_quote DESC
'''

results = cursor.execute(query).fetchall()
```

## 🤝 Contributing

Contributions are welcome! Feel free to:

- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

You are free to:
- ✅ Use this code for commercial purposes
- ✅ Modify and distribute
- ✅ Use for academic research
- ✅ Build upon this work

## 🙏 Acknowledgments

- **Covalent** for providing the comprehensive NFT market data API
- **Gitcoin** for hosting the bounty challenge
- The blockchain and NFT communities for continued innovation

## 📫 Contact

**Jakob Richert**
- GitHub: [@jakobrichert](https://github.com/jakobrichert)
- Email: jakobquantum@tuta.io

## 🔗 Links

- [Original Gitcoin Bounty](https://gitcoin.co/issue/covalenthq/covalent-gitcoin-bounties/18/100027635)
- [Covalent API Documentation](https://www.covalenthq.com/docs/api/)
- [Google Colab Version](https://colab.research.google.com/drive/11f_UzU1BA5i-dq2oIK-p9kyqK1cvy4fa?usp=sharing)

---

<div align="center">
Made with ❤️ for the blockchain and NFT community
<br>
<sub>If you found this useful, consider giving it a ⭐!</sub>
</div>
