import pandas as pd
from sklearn.impute import SimpleImputer
from sklearn.preprocessing import MinMaxScaler, StandardScaler, OneHotEncoder

# Sample Dataset
data = {
    'Age': [20, 25, None, 30, 35],
    'Salary': [25000, 30000, 35000, 40000, 100000],
    'Gender': ['Male', 'Female', 'Female', 'Male', 'Female']
}

df = pd.DataFrame(data)

print("Original Dataset")
print(df)

# Handling Missing Values
imputer = SimpleImputer(strategy='mean')
df['Age'] = imputer.fit_transform(df[['Age']])

# Normalization
minmax_scaler = MinMaxScaler()
df['Salary_Normalized'] = minmax_scaler.fit_transform(df[['Salary']])

# Standardization
standard_scaler = StandardScaler()
df['Salary_Standardized'] = standard_scaler.fit_transform(df[['Salary']])

# One-Hot Encoding
encoder = OneHotEncoder(sparse_output=False)
encoded = encoder.fit_transform(df[['Gender']])

encoded_df = pd.DataFrame(
    encoded,
    columns=encoder.get_feature_names_out(['Gender'])
)

final_df = pd.concat([df, encoded_df], axis=1)

print("\nTransformed Dataset")
print(final_df)