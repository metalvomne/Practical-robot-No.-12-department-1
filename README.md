import pandas as pd

# Завантаження даних з CSV
df = pd.read_csv('data.csv')

# Перегляд перших рядків
print(df.head())

# Основні статистичні показники
print(df.describe())

# Фільтрація даних
filtered = df[df['Age'] > 30]
print(filtered)

# Групування та підрахунок середнього значення
grouped = df.groupby('Department')['Salary'].mean()
print(grouped)
