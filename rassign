vehicles_data <- read.csv("programming/vehicles.csv")

# Display the first few rows of the dataset for an initial inspection
head(vehicles_data)

# Obtain summary statistics to highlight potential data issues
summary(vehicles_data)
print("Column names in the dataset are: ")
print(colnames(vehicles_data))
# ==========================================
# DATA CLEANING
# ==========================================
# Handle duplicates
vehicles_data <- unique(vehicles_data)

# Handle missing values by omitting them
vehicles_data <- na.omit(vehicles_data)

# Display the structure of the cleaned data
str(vehicles_data)

hist(vehicles_data$UHighway, main="Histogram of Original Data", xlab="Value", border="blue", col="lightgray")

if(all(vehicles_data$UHighway > 0)) {
  vehicles_data$log_transformed <- log(vehicles_data$UHighway)
  hist(vehicles_data$log_transformed, main="Histogram of Log Transformed Data", xlab="Log(Value)", border="red", col="lightcyan")
} else {
  cat("Log transformation cannot be applied due to non-positive values in the dataset.\n")
}

# ---- Square Root Transformation ----
vehicles_data$sqrt_transformed <- sqrt(vehicles_data$UHighway)
hist(vehicles_data$sqrt_transformed, main="Histogram of Square Root Transformed Data", xlab="Sqrt(Value)", border="green", col="lightyellow")
