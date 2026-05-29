# 🔍 OSINTBox Data

> **Community-driven repository of OSINT tools and resources**  
> Curated collection of Open Source Intelligence tools organized by category

[![Validation](https://img.shields.io/badge/validation-passing-brightgreen)](https://github.com/vixkram/OSINTBox-data/actions)
[![Contributors](https://img.shields.io/badge/contributors-welcome-blue)](#-contribute)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

> 🌐 Explore the live OSINTBox directory at [osintbox.vikk.dev](https://osintbox.vikk.dev/)

---

## 📁 Repository Structure

```
├── 📄 tools.json         # Core categories and tools 
├── ⚙️ widgets.json       # Widget configuration 
└── 📋 schema/            # JSON schemas for validation
    ├── tools.schema.json
    └── widgets.schema.json
```

### 🔧 File Descriptions

| File | Status | Description |
|------|--------|-------------|
| `tools.json` | **Required** | Main database of OSINT tools organized by categories |
| `widgets.json` | *Optional* | Configuration for dashboard widgets (world clock, feeds, etc.) |

---

## 🤝 Contribute

We welcome contributions from the OSINT community! Here's how you can help:

### 📝 Quick Start
1. **Fork** this repository
2. **Edit** `tools.json` (and `widgets.json` if needed)
3. **Open** a Pull Request
4. **Wait** for automated validation to pass

> 💡 **Tip**: All submissions are automatically validated through our CI pipeline

### ✅ Local Validation (Optional)

Want to test your changes before submitting? Follow these steps:

```bash
# 1. Install validation tools
npm i -D ajv-cli@5

# 2. Validate your changes
npx ajv validate -s schema/tools.schema.json -d tools.json --all-errors

# 3. Validate widgets (if modified)
if [ -f widgets.json ]; then 
  npx ajv validate -s schema/widgets.schema.json -d widgets.json --all-errors
fi
```

---

## 📊 Data Schema

### 🛠️ Tool Object
```json
{
  "name": "Tool Name",
  "url": "https://example.com"
  // Optional overrides:
  // "description": "Brief description",
  // "icon": "https://example.com/favicon.ico"
}
```

### 📂 Category Object
```json
{
  "category": "Category Name",
  "tools": [
    // Array of tool objects
  ]
}
```

---

## 💡 Best Practices

### ✏️ Writing Guidelines
- **Descriptions**: Only include if they add clear value beyond the tool name (otherwise omit)
- **Icons**: Usually omit — the UI auto‑generates favicons from the tool domain. Only set `icon` to override.
  - Do not use third‑party proxies; if needed, use a direct image URL (e.g., the site’s real favicon).
- **URLs**: Ensure all links are active and lead to canonical pages; remove tracking params

### 🎯 Quality Standards
- ✅ Verify tool functionality before adding
- ✅ Use clear, descriptive names
- ✅ Categorize appropriately
- ✅ Test all URLs

---

## 🚀 Getting Started

1. **Browse** the `tools.json` file to see existing categories and tools
2. **Identify** gaps or new tools to add
3. **Follow** the schema structure
4. **Submit** your contribution via Pull Request

---

## 💖 Donate

Help keep the OSINTBox data project maintained.

- BTC: _bc1qlz8thfq9k02y86lr49w5mqty2c93dz4ptjz4cn_
- ETH: _0x278881E9Edaa585174b1708447B1C07934530ded_
- LTC: _ltc1q9qr39kdxv3ulmszw48jgp7p8jqq0metdjzxp4m_

## 📞 Support

- 🐛 **Issues**: Report bugs or suggest improvements
- 💬 **Discussions**: Open an issue describing the change you propose

---

## 🙏 Acknowledgments

Thanks to all contributors who help maintain and expand this valuable OSINT resource!

---

<div align="center">

**[⭐ Star this repo](https://github.com/vixkram/OSINTBox-data) | [🍴 Fork it](https://github.com/vixkram/OSINTBox-data/fork) | [📝 Contribute](#-contribute)**

</div>
