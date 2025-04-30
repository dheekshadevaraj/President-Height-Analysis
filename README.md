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
![image](https://github.com/user-attachments/assets/41886b10-e245-49b7-80f7-1aae8fa26558)

---

## 📈 Histogram Kernel Density Estimate

sns.set_style("darkgrid")  # Makes it visually cleaner

plt.figure(facecolor='black')
ax = plt.gca()
ax.set_facecolor('black')

sns.histplot(height, kde=True, color='yellow', edgecolor='black', bins=10)

plt.title("Height Distribution of Presidents of USA", color='white')
plt.xlabel("Height (cm)", color='white')
plt.ylabel("Frequency", color='white')
ax.tick_params(colors='white')
plt.show()

---     

## 📈 Histogram with Key Statistics

plt.figure(facecolor='black')
ax = plt.gca()
ax.set_facecolor('black')

plt.hist(height, color='purple', edgecolor='black', bins=10)


plt.axvline(height.mean(), color='cyan', linestyle='--', label=f"Mean: {height.mean():.2f} cm")
plt.axvline(np.median(height), color='lime', linestyle='--', label=f"Median: {np.median(height):.2f} cm")
plt.axvline(np.percentile(height, 25), color='orange', linestyle=':', label='25th Percentile')
plt.axvline(np.percentile(height, 75), color='red', linestyle=':', label='75th Percentile')

plt.title("Height Distribution of Presidents of USA", color='white')
plt.xlabel("Height (cm)", color='white')
plt.ylabel("Number", color='white')
ax.tick_params(colors='white')

plt.legend(facecolor='black', labelcolor='white', frameon=True)
plt.show()

---     
