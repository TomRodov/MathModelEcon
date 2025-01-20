# Bond Yield Curve Analysis Implementation

## Overview
This project attempts to implement the bond pricing model from the paper "Retractable and Extendible Bonds" using modern market data. The implementation focuses on calculating and visualizing yield curves for government bonds.

## Original Paper Reference
The model is based on equations from "Retractable and Extendible Bonds", which provides a framework for understanding the relationship between interest rates and bond yields across different maturities. The paper originally used data from 1959-1977.

## Key Components

### Data
- Uses Canadian government bond data (1-year and 10-year bonds)
- Data fetched using the FRED API through R
- Focus on simplified version without tax considerations

### Core Equations
The implementation is based on three fundamental equations:
1. Bond price with continuous coupon (Equation 10)
2. Pure discount bond price (Equation A-1)
3. Yield to maturity calculation (Equation 12)

## Implementation Details

### Required R Packages
```r
library(quantmod)
library(dplyr)
library(ggplot2)
```

### Main Functions
- `get_canadian_bond_data()`: Fetches bond data from FRED
- `calculate_yield()`: Implements yield calculations
- `run_analysis()`: Performs the complete analysis and generates plots

## Results
The current implementation shows some limitations:
- Single convergent line instead of multiple curves
- Yield values not matching expected patterns
- Numerical stability issues in calculations


## Known Issues
- Numerical instability in parameter estimation
- Challenges with modern low interest rate environment
- Divergence from original paper's results

## Future Improvements
- Enhanced numerical stability
- Better parameter estimation methods
- Additional validation techniques
- Incorporation of modern market features

## Contributing
Feel free to contribute by:
- Improving numerical stability
- Adding test cases
- Enhancing documentation
- Implementing suggested improvements

