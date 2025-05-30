# Field Reference Guide

Complete reference for all InSPIRE Metadata Schema fields.

---

##  **Section 1: Identification & Overview**

### **title** *(required)*
- **Type:** String
- **Description:** Concise dataset name
- **Standards:** DDI, ISO 19115
- **Example:** "Hurricane Harvey Social Media Response Dataset"
- **Guidelines:** Keep under 200 characters; be descriptive but concise

### **abstract** *(required)*
- **Type:** String  
- **Description:** Summary of dataset content, purpose, and scope
- **Standards:** DDI, ISO 19115
- **Example:** "Analysis of social media responses during Hurricane Harvey, focusing on community resilience and information sharing patterns"
- **Guidelines:** 2-4 sentences; include what, where, when, why

### **purpose**
- **Type:** String
- **Description:** Explanation of why the dataset was collected
- **Standards:** DDI
- **Example:** "To understand how communities use social media during disasters for coordination and support"
- **Guidelines:** Focus on the research question or practical application

### **creator** *(required)*
- **Type:** String
- **Description:** Name(s) of the individual(s) or organization(s) who created the dataset
- **Standards:** DDI
- **Example:** "Dr. Jane Smith, University of Texas at Austin"
- **Guidelines:** Include affiliation; use format "LastName, FirstName, Institution"

### **unique_identifier**
- **Type:** String
- **Description:** Persistent, citable reference (DOI, handle, etc.)
- **Standards:** DDI, ISO 19115
- **Example:** "10.5555/harvey-social-2017"
- **Guidelines:** Use DOI when available; otherwise use institutional handle

### **version**
- **Type:** String
- **Description:** Dataset version and update history
- **Standards:** DDI
- **Example:** "1.2"
- **Guidelines:** Use semantic versioning (major.minor.patch)

### **contributors**
- **Type:** Array of Objects
- **Description:** People or organizations who contributed to dataset creation
- **Standards:** DDI
- **Required Fields:** name, role
- **Optional Fields:** role_description
- **Controlled Vocabulary:** See [Contributor Roles](#contributor-roles)
- **Example:**
  ```json
  [
    {
      "name": "Dr. John Doe",
      "role": "Co-Investigator"
    },
    {
      "name": "Sarah Johnson", 
      "role": "Data Analyst"
    }
  ]
  ```

### **funding_reference**
- **Type:** Array of Strings
- **Description:** Information about funding sources supporting dataset creation
- **Standards:** DDI
- **Example:** ["NSF Award #1234567", "NOAA Grant ABC123"]
- **Guidelines:** Include grant numbers, agency names, award titles

### **license** *(recommended)*
- **Type:** String (Controlled Vocabulary)
- **Description:** Terms of use for the dataset
- **Standards:** DDI
- **Controlled Vocabulary:** See [License Options](#license-options)
- **Example:** "CC-BY (Attribution 4.0 International)"

### **license_custom_terms**
- **Type:** String
- **Description:** Required if license is 'Other' or 'Proprietary'
- **Example:** "Available for academic use only with written permission"

### **citation_recommendation**
- **Type:** String
- **Description:** Suggested citation format for the dataset
- **Standards:** DataCite
- **Example:** "Smith, J., Doe, J., & Johnson, S. (2017). Hurricane Harvey Social Media Response Dataset. https://doi.org/10.5555/harvey-social-2017"

---

##  **Section 2: Subject Classification & Keywords**

### **subject_category** *(required)*
- **Type:** String (Controlled Vocabulary)
- **Description:** Broad domain classification from controlled vocabulary
- **Standards:** DDI, Domain-Specific
- **Controlled Vocabulary:** See [Subject Categories](#subject-categories)
- **Example:** "Emergency Management"

### **keywords_controlled**
- **Type:** Array of Strings (Controlled Vocabulary)
- **Description:** Specific tags from controlled vocabulary
- **Standards:** DDI, NOAA Glossary
- **Controlled Vocabulary:** See [Controlled Keywords](#controlled-keywords)
- **Example:** ["Hurricane Preparedness", "Social Equity in Disasters"]

### **keywords_other**
- **Type:** Array of Strings
- **Description:** Custom keywords for discoverability
- **Example:** ["Twitter", "Facebook", "Disaster Communication"]
- **Guidelines:** Use specific, searchable terms; avoid duplicating controlled keywords

### **related_datasets**
- **Type:** Array of Strings
- **Description:** Links to datasets that complement this one
- **Standards:** Domain-Specific
- **Example:** ["https://doi.org/10.5555/harvey-weather-2017"]
- **Guidelines:** Provide URLs or DOIs; include brief relationship description

---

##  **Section 3: Geographic & Temporal Information**

### **geographic_coverage_controlled** *(at least one geographic field required)*
- **Type:** Array of Strings (Controlled Vocabulary)
- **Description:** Broad geographic categories
- **Standards:** ISO 19115
- **Controlled Vocabulary:** See [Geographic Coverage](#geographic-coverage)
- **Example:** ["Gulf Coast", "Urban Areas"]

### **geographic_coverage_specific**
- **Type:** String
- **Description:** Exact location description
- **Example:** "Houston Metropolitan Area, Texas"
- **Guidelines:** Be as specific as useful for discovery; include country for international locations

### **coordinate_system**
- **Type:** String
- **Description:** Coordinate system used
- **Standards:** ISO 19115
- **Example:** "WGS84"
- **Guidelines:** Use standard coordinate system names (WGS84, NAD83, etc.)

### **spatial_resolution**
- **Type:** String
- **Description:** Level of detail in spatial data
- **Standards:** ISO 19115
- **Example:** "ZIP code level"
- **Guidelines:** Describe the smallest geographic unit in your data

### **temporal_coverage_start** *(required)*
- **Type:** Date (YYYY-MM-DD format)
- **Description:** Start date of time period covered
- **Standards:** DDI, ISO 19115
- **Example:** "2017-08-25"

### **temporal_coverage_end**
- **Type:** Date (YYYY-MM-DD format)
- **Description:** End date of time period covered
- **Example:** "2017-09-15"
- **Guidelines:** Use same date as start for single-day datasets

### **temporal_resolution**
- **Type:** String
- **Description:** Frequency of data collection
- **Standards:** DDI
- **Example:** "Hourly"
- **Guidelines:** Use standard terms (Hourly, Daily, Weekly, Monthly, Annual, etc.)

---

##  **Section 4: Data Characteristics & Methods**

### **data_type**
- **Type:** String (Controlled Vocabulary)
- **Description:** Nature of the data collected
- **Standards:** DDI
- **Controlled Vocabulary:** See [Data Types](#data-types)
- **Example:** "Text Analysis"

### **data_format**
- **Type:** String
- **Description:** File format for interoperability
- **Standards:** ISO 19115
- **Example:** "JSON, CSV"
- **Guidelines:** List primary formats; include version numbers if relevant

### **collection_methodology**
- **Type:** String
- **Description:** How the data were obtained
- **Standards:** DDI
- **Example:** "API collection from Twitter and Facebook during event period"
- **Guidelines:** Include enough detail for reproducibility

### **uncertainty_quantification**
- **Type:** String
- **Description:** Measures of accuracy, error margins
- **Standards:** Domain-Specific
- **Example:** "95% confidence intervals provided for sentiment analysis scores"
- **Guidelines:** Quantify uncertainty where possible; mention known limitations

### **data_processing**
- **Type:** String
- **Description:** Cleaning, transformations, or analyses applied
- **Standards:** ISO 19115
- **Example:** "Text cleaning, sentiment analysis using VADER, geographic geocoding"
- **Guidelines:** List major processing steps; mention software/methods used

### **provenance**
- **Type:** String
- **Description:** Documentation of changes made over time
- **Standards:** DataCite, ISO 19115
- **Example:** "Raw data collected hourly, processed weekly, final analysis completed 2018-01-15"
- **Guidelines:** Include dates and reasons for major changes

---

##  **Section 5: Decision-Support Attributes**

### **use_cases**
- **Type:** String (Controlled Vocabulary)
- **Description:** Intended applications of the data
- **Standards:** Domain-Specific
- **Controlled Vocabulary:** See [Use Cases](#use-cases)
- **Example:** "Public Risk Communication"

### **integration_with_other_data**
- **Type:** String
- **Description:** How this dataset links to others
- **Standards:** Domain-Specific
- **Example:** "Links to NOAA weather data via temporal and spatial joins"
- **Guidelines:** Describe technical integration possibilities

---

##  **Section 6: Community Engagement & Ethics**

### **community_engagement**
- **Type:** Boolean (true/false)
- **Description:** Whether local knowledge was incorporated
- **Standards:** Domain-Specific
- **Example:** true
- **Guidelines:** True if community members participated in design, collection, or validation

### **equity_accessibility**
- **Type:** Boolean (true/false)
- **Description:** Considerations for vulnerable communities
- **Standards:** Domain-Specific
- **Example:** true
- **Guidelines:** True if dataset considers or addresses equity issues

---

## 🔧 **Section 7: Technical Details & Access**

### **data_access_url**
- **Type:** URL
- **Description:** Link to dataset
- **Standards:** ISO 19115
- **Example:** "https://example.com/dataset/harvey-social"
- **Guidelines:** Provide direct link to data download or landing page

### **api_endpoint**
- **Type:** URL
- **Description:** URL for automated access
- **Standards:** Domain-Specific
- **Example:** "https://api.example.com/harvey-social/v1"
- **Guidelines:** Include API documentation link if available

### **file_size**
- **Type:** String
- **Description:** Total dataset size
- **Standards:** ISO 19115
- **Example:** "2.3 GB"
- **Guidelines:** Use appropriate units (KB, MB, GB, TB)

### **software_dependencies**
- **Type:** String
- **Description:** Required tools for use
- **Standards:** ISO 19115
- **Example:** "Python 3.7+, pandas, nltk"
- **Guidelines:** List critical software and minimum versions

### **access_restrictions**
- **Type:** String
- **Description:** Any limitations on dataset access
- **Standards:** DDI, ISO 19115
- **Example:** "None"
- **Guidelines:** Mention embargos, registration requirements, geographic restrictions

### **data_sensitivity**
- **Type:** Boolean (true/false)
- **Description:** Does data contain sensitive information
- **Standards:** DDI, IRB Guidelines
- **Example:** false
- **Guidelines:** True if data contains PII, private information, or sensitive content

### **retention_policy**
- **Type:** String
- **Description:** Long-term availability and storage duration
- **Standards:** ISO 19115
- **Example:** "Available indefinitely through university repository"
- **Guidelines:** Include expected availability timeline and preservation commitments

---

##  **Controlled Vocabularies**

### **Subject Categories** {#subject-categories}
- Risk Perception
- Emergency Management
- Climate Adaptation
- Impact-Based Forecasting
- Social Vulnerability
- Weather Communication
- Hydrometeorology
- Economic Impacts
- Public Health & Weather

### **Controlled Keywords** {#controlled-keywords}
- Flood Risk
- Hurricane Preparedness
- Wildfire Impact
- Tornado Forecasting
- Power Outages
- Social Equity in Disasters
- GIS Mapping
- Crowd-Sourced Observations

### **Geographic Coverage** {#geographic-coverage}
- United States
- Coastal Regions
- Midwest
- Gulf Coast
- Urban Areas
- Rural Communities
- River Basins

### **Data Types** {#data-types}
- Survey Data
- Satellite Observations
- Model Simulations
- Text Analysis
- Geospatial Data
- Sensor Networks
- Administrative Data
- Other

### **Use Cases** {#use-cases}
- Evacuation Planning
- Hazard Mitigation
- Public Risk Communication
- Climate Resilience Research
- Infrastructure Risk Assessment
- Policy Development
- Economic Risk Modeling
- Other

### **Contributor Roles** {#contributor-roles}
- Principal Investigator (PI)
- Co-Investigator
- Data Manager
- Field Data Collector
- Metadata Curator
- Software Developer
- Modeler
- Data Analyst
- Community Partner
- Other

### **License Options** {#license-options}
- CC0 (Public Domain Dedication)
- CC-BY (Attribution 4.0 International)
- CC-BY-SA (Attribution-ShareAlike 4.0 International)
- CC-BY-NC (Attribution-NonCommercial 4.0 International)
- CC-BY-ND (Attribution-NoDerivs 4.0 International)
- Open Data Commons Open Database License (ODbL)
- Proprietary
- Government Public Data (U.S. Federal Only)
- Other

---

##  **Field Validation Rules**

### **Required Fields**
All datasets must include:
- title
- abstract
- creator
- subject_category
- geographic_coverage_controlled OR geographic_coverage_specific
- temporal_coverage_start

### **Conditional Requirements**
- **license_custom_terms**: Required if license is "Other" or "Proprietary"
- **role_description**: Required if contributor role is "Other"
- **temporal_coverage_end**: Recommended for datasets covering multiple time points

### **Format Requirements**
- **Dates**: Use ISO 8601 format (YYYY-MM-DD)
- **URLs**: Must be valid HTTP/HTTPS URLs
- **Email**: Must be valid email format

---

*For questions about specific fields or validation, see our [FAQ](faq.html) or [contact us](mailto:inspire-schema@yourlabs.org).*
