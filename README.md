# 🇺🇸 President Heights Analysis 📊

This project analyzes the height distribution of Presidents of the United States using Python, NumPy, Pandas, Matplotlib, and Seaborn.

## 📁 Dataset
The dataset used is `president_heights.csv`, containing the heights of U.S. Presidents in centimeters.

---

## 📊 Exploratory Data Analysis (EDA)

### ✅ Basic Statistics:
- **Mean Height**: Computed using `np.mean()`
- **Standard Deviation**: Using `np.std()`
- **Min / Max Height**
- **25th Percentile, Median (50th), 75th Percentile**: via `np.percentile()`

---

## 📈 Histogram Visualization

A histogram displays the distribution of heights with a **black background** for better visual impact.

```python
plt.figure(facecolor='black')  
ax = plt.gca()
ax.set_facecolor('black')

plt.hist(height, color='orange') 
plt.title("Height Distribution of Presidents of USA", color='white')
plt.xlabel("Height (cm)", color='white')
plt.ylabel("Number", color='white')
ax.tick_params(colors='white')

plt.show()
