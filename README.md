# Afghanistan Provinces, Districts, and Villages

A comprehensive dataset of Afghanistan's administrative divisions, including all provinces, districts, and villages with geographical coordinates and multi-language support.

## 📊 Statistics

- **Provinces**: 34
- **Districts**: 492
- **Villages**: 8,892
- **Languages**: English, Dari (Farsi), Pashto
- **Data Points**: Geographic coordinates (latitude/longitude) for all locations

## 📁 File Information

### JSON Format
The repository contains two main JSON files:

#### 1. `JSON/provinces-and-districts.json`
- **Structure**: Hierarchical nested JSON
- **Size**: ~34 provinces with nested districts
- **Fields per Province**:
  - `id`: Unique identifier
  - `name`: Province name (English)
  - `nameFa`: Province name (Dari/Farsi - فارسی)
  - `namePa`: Province name (Pashto - پښتو)
  - `latitude`: Geographic latitude
  - `longitude`: Geographic longitude
  - `districts`: Array of district objects

- **Fields per District**:
  - `id`: Unique identifier
  - `name`: District name (English)
  - `nameFa`: District name (Dari/Farsi)
  - `namePa`: District name (Pashto)
  - `latitude`: Geographic latitude
  - `longitude`: Geographic longitude

#### 2. `JSON/villages.json`
- **Structure**: Flat JSON array
- **Size**: 8,892 village records
- **Fields per Village**:
  - `No`: Sequential number
  - `Province`: Province name (English)
  - `District`: District name (English)
  - `Village Name`: Village name
  - `Latitude`: Geographic latitude
  - `Longitude`: Geographic longitude
  - `Area(Square Meter)`: Village area in square meters
  - `Hectares`: Village area in hectares
  - `Shape Length`: Perimeter measurement

### SQL Format
The repository includes SQL dump files for easy database import:

- `SQL/provinces.sql` - Province data table
- `SQL/districts.sql` - District data table
- `SQL/villages.sql` - Village data table

**Database Format**: MySQL/MariaDB compatible SQL dumps (phpMyAdmin export)

## 📝 Summary

This dataset provides a complete administrative hierarchy of Afghanistan, from provinces down to individual villages. Each location includes:

- **Multi-language support**: Names in English, Dari (Farsi), and Pashto
- **Geographic positioning**: Precise latitude and longitude coordinates
- **Spatial data**: Village area measurements and shape information
- **Relational structure**: Clear province → district → village hierarchy

The data is provided in both JSON (for web applications and APIs) and SQL (for database applications) formats, making it versatile for various use cases.

## 🔑 Details & Key Points

### Usage Considerations

1. **Language Support**
   - English names for international applications
   - Dari (Farsi) and Pashto for local language support
   - UTF-8 encoding ensures proper display of native scripts

2. **Data Accuracy**
   - Geographic coordinates provided for mapping applications
   - Village area measurements included for spatial analysis (note: verify hectare calculations as they may require recalculation)
   - Hierarchical relationships maintained between administrative levels

3. **Format Options**
   - **JSON**: Ideal for web APIs, JavaScript applications, and modern frameworks
   - **SQL**: Ready for direct import into MySQL/MariaDB databases
   - Both formats contain the same core data with appropriate structure

4. **Practical Applications**
   - Geographic Information Systems (GIS)
   - Location-based services and applications
   - Administrative and demographic analysis
   - Educational and research purposes
   - Government and NGO planning tools

5. **Data Relationships**
   - Each province contains multiple districts
   - Each district belongs to exactly one province
   - Villages are associated with specific districts and provinces
   - Clear hierarchical structure: Province → District → Village

### Important Notes

- The villages dataset includes geometric data (area and perimeter)
- **Data Quality Note**: The `Hectares` field in villages.json appears to contain values that are 100x larger than expected based on standard conversion (1 hectare = 10,000 square meters). Users should verify and recalculate this field if precise area measurements are needed.
- All geographic coordinates use standard decimal degree format
- Province and district data includes hierarchical nesting for easy traversal
- Village data is flattened for simpler querying and analysis

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions, corrections, and improvements are welcome! Please feel free to submit issues or pull requests.

## 📧 Contact

For questions or suggestions, please open an issue in the repository.
