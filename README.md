
# 🚗 Intelligent Parkinglot Price Prediction System

A real-time parking analytics pipeline using the **Pathway** streaming engine to compute dynamic parking prices and predict demand, based on occupancy, capacity, and additional context features like traffic and vehicle type.

---

## 🔧 Tech Stack Used

| Tool / Library     | Purpose                                      |
|--------------------|----------------------------------------------|
| `Python`           | Core programming language                    |
| `Pathway`          | Real-time streaming data processing engine   |
| `Pandas` / `NumPy` | Data manipulation and preprocessing          |
| `Bokeh`            | Interactive data visualization               |
| `Panel`            | Dashboard layout wrapper                     |
| `Matplotlib`       | Basic static plotting                        |

---

## 🧠 Architecture Overview

### 🧩 Model 1 Architecture
 ![Untitled diagram _ Mermaid Chart-2025-07-07-132305](https://github.com/user-attachments/assets/ac5571ac-58df-40bc-a69c-c80bedf4d810)

### ⚙️ Model 2 Architecture (Enhanced)
  ![Untitled diagram _ Mermaid Chart-2025-07-07-133658](https://github.com/user-attachments/assets/b289d116-2474-4e67-b5c6-b059a312ad8d)


## 📊 Comparison Table

| Feature                         | Model 1                         | Model 2                              |
|----------------------------------|----------------------------------|---------------------------------------|
| Aggregation Window              | Daily                           | Hourly                                |
| Demand Factors                  | Occupancy only                  | QueueLength, Traffic, VehicleType     |
| Prediction Formula              | Fixed (based on max occupancy)  | Tunable weighted formula              |
| Dynamic Features                | ❌                              | ✅                                     |
| Traffic & Special Day Aware     | ❌                              | ✅                                     |
| Vehicle Type Consideration      | ❌                              | ✅                                     |
| Data Windowing Granularity      | Coarse (1 day)                  | Fine (1 hour)                         |

---

## ✅ Benefits of Model 2 over Model 1

1. **Higher Granularity**: Model 2 uses hourly windows, enabling more timely pricing and analysis.
2. **Multivariate Demand Model**: Instead of relying solely on occupancy, it considers traffic conditions, queue length, special days, and vehicle types.
3. **Better Personalization**: Pricing logic adapts based on the type of vehicle and contextual factors.
4. **Scalability**: Designed to be more extensible with tunable weights for domain-specific optimization.
5. **Real-time Responsiveness**: Faster windowing allows for live dashboards with greater situational awareness.
6. **Data-Driven Pricing**: Enables better alignment of supply-demand using advanced features.

---

## ▶️ How to Run

### 1. Install dependencies

```bash
pip install pathway bokeh panel
```

### 2. Launch either model notebook

```bash
# For Model 1
Run: Model1.ipynb

# For Model 2
Run: best Model 2.ipynb
```

Ensure your dataset is named `dataset.csv` and is available in the current directory.

---

## 📁 Project Structure

```
📦parking-price-predictor
 ┣ 📜 Model1.ipynb
 ┣ 📜 best Model 2.ipynb
 ┣ 📜 dataset.csv
 ┣ 📜 README.md
```
