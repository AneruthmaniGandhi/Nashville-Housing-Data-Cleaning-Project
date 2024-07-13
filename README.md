# Nashville Housing Data Cleaning Project

This SQL project focuses on cleaning and standardizing the Nashville Housing dataset within a SQL Server database. The provided script addresses common data quality issues found in real-world datasets, making it more suitable for analysis and further use.

Key Cleaning Steps

Standardize Date Format:

Converts the SaleDate column to a consistent DATE format, ensuring uniformity for temporal analysis.
Creates a new SaleDateConverted column to preserve the original format if needed.

Populate Property Address:

Identifies and fills in missing values in the PropertyAddress column by leveraging the ParcelID to find matching records with complete addresses.

Split Address into Components:

Parses the PropertyAddress and OwnerAddress columns into separate columns for street address, city, and state. This facilitates more granular analysis and filtering based on location.

Standardize 'Sold as Vacant' Field:

Replaces the ambiguous 'Y' and 'N' values in the SoldAsVacant column with more descriptive 'Yes' and 'No' values.

Remove Duplicate Records:

Identifies and eliminates duplicate entries in the dataset based on key property attributes like ParcelID, PropertyAddress, SalePrice, SaleDate, and LegalReference.

Delete Unused Columns:

Removes the original OwnerAddress, TaxDistrict, PropertyAddress, and SaleDate columns as they are either redundant or no longer needed after cleaning.
