- Some data is plotted on different ranges.
- Scaling allows them to be directly compared and used together

## Min-Max Scaling
"Normalization"
- Max value maps to 1
- Min value maps to 0
Formula:
$$\hat{f_i}=\frac{f_i - min(f_i)}{max(f_i)-min(f_i)}$$
Issues:
- Since it's linear, outliers skew the mapping

## Standardization
Formula:
$$\hat{f_i}=\frac{f_i - \mu f_i}{\sigma f_i <TODO>}$$

Issues:
- Assumes gaussianity 

