# Sales Data Mart

## Overview
This Sales Data Mart is a comprehensive business intelligence solution designed to consolidate, transform, and analyze sales data from multiple sources. The data mart provides a centralized repository for sales analytics, reporting, and decision-making processes.

## Architecture Overview
The Sales Data Mart follows a multi-layered ETL (Extract, Transform, Load) architecture with the following key components:

### Data Sources
- **Sales Order Header**: Contains master sales order information
- **Sales Order Details**: Detailed line items for each sales order
- **Product Data**: Product catalog and specifications
- **Customer Data**: Customer demographics and information
- **Excel Sources**: Additional business data in Excel format
- **OLE DB Sources**: Various database connections for additional data feeds

### Data Processing Flows

#### Flow 1: Main Sales Processing Pipeline
1. **Data Extraction**: Retrieves data from Sales Order Header and Sales Order Details
2. **Merge Join**: Combines header and detail information
3. **Customer Lookup**: Enriches data with customer information
4. **Product Lookup**: Adds product details and specifications
5. **Territory Lookup**: Incorporates geographical sales territory data
6. **Date Processing**: Handles date dimensions and time-based calculations
7. **Derived Columns**: Creates calculated fields and business metrics
8. **Final Calculations**: Performs aggregations and business rule applications

#### Flow 2: Product Dimension Processing
1. **Product Data Extraction**: Sources product master data
2. **Product Model Lookup**: Links products to their respective models
3. **Product Category Lookup**: Categorizes products for analysis
4. **Derived Columns**: Creates product-specific calculated fields
5. **Slowly Changing Dimension (SCD)**: Manages historical product changes
6. **Data Quality**: Ensures data consistency and accuracy
7. **Union Operations**: Consolidates multiple product data streams

#### Flow 3: Extended Data Processing
1. **OLE DB Source Integration**: Incorporates additional database sources
2. **Lookup Operations**: Cross-references with master data
3. **Slowly Changing Dimension Management**: Handles historical data changes
4. **Multiple SCD Branches**: Manages different types of dimensional changes
5. **Union All**: Combines all processed data streams

#### Flow 4: Excel Integration
1. **Excel Source**: Imports data from Excel files
2. **Data Conversion**: Standardizes data formats and types
3. **Direct Load**: Efficiently loads processed Excel data

#### Flow 5: Lookup Enhancement
1. **OLE DB Source**: Additional data source integration
2. **Lookup Transformation**: Data enrichment and validation
3. **Derived Columns**: Final calculated field creation

## Key Features

### Data Integration
- **Multiple Source Support**: Handles various data sources including databases, Excel files, and OLE DB connections
- **Real-time Processing**: Supports both batch and near real-time data processing
- **Data Quality Assurance**: Built-in validation and cleansing processes

### Business Intelligence Capabilities
- **Customer Analytics**: Comprehensive customer behavior and segmentation analysis
- **Product Performance**: Detailed product sales and profitability metrics
- **Territory Management**: Geographical sales performance tracking
- **Time-based Analysis**: Historical trends and seasonal pattern identification

### Data Management
- **Slowly Changing Dimensions**: Proper handling of historical data changes
- **Data Lineage**: Clear tracking of data transformation processes
- **Error Handling**: Robust error management and data quality reporting

## Technical Specifications

### ETL Components
- **SSIS Package**: Built
