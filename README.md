# Python-program-113
13. EXERCISES TO PERFORM DATA HANDLING USING DATA FRAMES (CREATION, INSPECTION,SORTING, FILTERING, MERGING AND GROUPING)
pip install pandasimport pandas as pddf = pd.DataFrame({'Name': ['Alice', 'Bob', 'David'],'Age': [25, 32, 47],'City': ['NY', 'LA', 'NY'],'Salary': [70000, 90000, 120000]})
print(df)
print(df.head(), df.shape)
print(df.sort_values('Age'))
print(df[df['Age'] > 30])dept = pd.
DataFrame({'Name': ['Alice', 'Bob', 'David'],'Dept': ['HR', 'Eng', 'Eng']
merged = pd.merge(df, dept, on='Name')
print(merged)print(df.groupby('City')['Salary'].mean())

Output:Name Age City Salary0 Alice 25 NY 700001 Bob 32 LA 900002 David 47 NY 120000Name Age City Salary0 Alice 25 NY 700001 Bob 32 LA 900002 David 47 NY 120000 (3, 4)Name Age City Salary0 Alice 25 NY 700001 Bob 32 LA 900002 David 47 NY 120000Name Age City Salary1 Bob 32 LA 900002 David 47 NY 120000Name Age City Salary Dept0 Alice 25 NY 70000 HR1 Bob 32 LA 90000 Eng2 David 47 NY 120000 EngCityLA 90000.0NY 95000.0Name: Salary, dtype: float64
