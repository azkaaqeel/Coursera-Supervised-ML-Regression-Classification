
from sklearn.preprocessing import MinMaxScaler, StandardScaler, RobustScaler

# Assuming you have your features in X_imputed_df

# Min-Max Scaling
min_max_scaler = MinMaxScaler()
X_min_max_scaled = min_max_scaler.fit_transform(X_imputed_df)

# Standardization
standard_scaler = StandardScaler()
X_standardized = standard_scaler.fit_transform(X_imputed_df)

# Robust Scaling
robust_scaler = RobustScaler()
X_robust_scaled = robust_scaler.fit_transform(X_imputed_df)
