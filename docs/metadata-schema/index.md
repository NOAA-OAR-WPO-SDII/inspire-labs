# InSPIRE Metadata Schema

**Comprehensive metadata schema for social science datasets related to weather and climate**

[![Schema Version](https://img.shields.io/badge/Version-1.0-blue)](schema/inspire-schema.json)
[![Standards](https://img.shields.io/badge/Standards-DDI%20|%20ISO%2019115%20|%20DataCite-green)](field-reference.html#standards-compliance)
[![License](https://img.shields.io/badge/License-MIT-orange.svg)](../LICENSE)

[⬅️ Back to InSPIRE Labs](../)

---

##  **Overview**

The InSPIRE Metadata Schema bridges the gap between meteorological data standards and social science research needs, ensuring your datasets are discoverable, citable, and interoperable. It organizes metadata into **7 logical sections** with **34+ fields** and built-in controlled vocabularies.

---

##  **Quick Start**

<div class="quick-start-section">
  <div class="quick-option">
    <h3> Get Templates</h3>
    <p>Download ready-to-use templates</p>
    <a href="templates/inspire-template.csv" class="btn btn-primary">CSV Template</a>
    <a href="schema/inspire-schema.json" class="btn btn-secondary">JSON Schema</a>
  </div>
  
  <div class="quick-option">
    <h3> Validate Data</h3>
    <p>Test your metadata</p>
    <a href="tools/validator.html" class="btn btn-primary">Online Validator</a>
  </div>
  
  <div class="quick-option">
    <h3> See Examples</h3>
    <p>Real-world datasets</p>
    <a href="examples/" class="btn btn-primary">Browse Examples</a>
  </div>
</div>

---

##  **Schema Structure**

The schema organizes metadata into **7 logical sections**:

### **1.  Identification & Overview**
Core dataset information including title, creators, funding, and licensing.
- **Key Fields:** `title`, `abstract`, `creator`, `license`, `citation_recommendation`
- **Focus:** Who created what, when, and how to cite it

### **2.  Subject Classification & Keywords** 
Domain classification and discoverability using controlled vocabularies.
- **Key Fields:** `subject_category`, `keywords_controlled`, `keywords_other`
- **Focus:** What domain and topics does this dataset cover

### **3.  Geographic & Temporal Information**
Spatial and temporal coverage with flexible location specification.
- **Key Fields:** `geographic_coverage_controlled`, `temporal_coverage_start`, `spatial_resolution`
- **Focus:** Where and when the data represents

### **4.  Data Characteristics & Methods**
Collection methodology, data types, and processing history.
- **Key Fields:** `data_type`, `collection_methodology`, `uncertainty_quantification`
- **Focus:** How the data was collected and processed

### **5.  Decision-Support Attributes**
Intended applications and integration capabilities.
- **Key Fields:** `use_cases`, `integration_with_other_data`
- **Focus:** How the data can be used for decisions

### **6.  Community Engagement & Ethics**
Community involvement and ethical considerations.
- **Key Fields:** `community_engagement`, `equity_accessibility`
- **Focus:** Was the community involved and are there equity considerations

### **7.  Technical Details & Access**
Access methods, file formats, and technical requirements.
- **Key Fields:** `data_access_url`, `api_endpoint`, `software_dependencies`
- **Focus:** How to access and use the data technically

---

##  **Downloads & Resources**

| Resource | Format | Best For | Download |
|----------|--------|----------|----------|
| **CSV Template** | CSV | Quick data entry, pilot testing | [📄 Download](templates/inspire-template.csv) |
| **JSON Schema** | JSON | Validation, tool development | [📄 Download](schema/inspire-schema.json) |
| **XML Schema** | XSD | Legacy systems, formal validation | [📄 Download](schema/inspire-schema.xsd) |
| **YAML Documentation** | YAML | Human-readable specification | [📄 Download](schema/inspire-schema.yaml) |

---

##  **Examples**

Real-world examples showing the schema in action:

### 🌀 **Hurricane Harvey Social Media Dataset**
Emergency management research using social media data during a major hurricane event.
- **Domain:** Emergency Management
- **Location:** Gulf Coast, Urban Areas  
- **Data Type:** Text Analysis
- [📄 View Complete Example](examples/hurricane-harvey-example.json)

### 🌾 **Midwest Drought Perception Study**
Risk perception research among rural farming communities during drought conditions.
- **Domain:** Risk Perception
- **Location:** Midwest, Rural Communities
- **Data Type:** Survey Data
- [📄 View Complete Example](examples/drought-perception-example.json)

### 🏙️ **Urban Heat Island Social Vulnerability**
Geospatial analysis of social vulnerability to extreme heat in urban environments.
- **Domain:** Social Vulnerability
- **Location:** Urban Areas
- **Data Type:** Geospatial Data
- [📄 View Complete Example](examples/urban-heat-example.json)

---

##  **Validation & Tools**

### **Online Validator**
Test your metadata against the InSPIRE schema with our interactive validation tool.

**Features:**
- ✅ JSON and CSV input support
- ✅ Real-time validation feedback
- ✅ Completeness scoring
- ✅ Controlled vocabulary checking

[🔧 **Try the Validator →**](tools/validator.html)

### **Validation Checklist**

**Required Fields (Must Have):**
- `title` - Dataset name
- `abstract` - Description 
- `creator` - Who made it
- `subject_category` - Domain classification
- `geographic_coverage_controlled` - Location
- `temporal_coverage_start` - Time period

**Recommended Fields (Should Have):**
- `license` - Usage terms
- `unique_identifier` - DOI or persistent ID
- `keywords_controlled` - Standardized tags

---

## 📖 **Documentation**

### **Complete References**
- [ **Field Reference**](field-reference.html) - Detailed description of every field
- [ **Controlled Vocabularies**](controlled-vocabularies.html) - All standardized terms and options
- [ **Implementation Guide**](implementation-guide.html) - Technical integration details
- [ **FAQ**](faq.html) - Common questions and answers

### **Standards Compliance**
- [ **Standards Mapping**](standards-compliance.html) - How InSPIRE maps to DDI, ISO 19115, DataCite
- [ **Crosswalks**](crosswalks.html) - Field mappings between standards
- [ **Best Practices**](best-practices.html) - Recommended usage patterns

---

##  **Getting Started Guide**

### **For Researchers**
1. **Download** the [CSV template](templates/inspire-template.csv)
2. **Fill out** your dataset metadata section by section
3. **Validate** using our [online tool](tools/validator.html)
4. **Export** to JSON for repository submission

### **For Data Managers**
1. **Review** the [JSON Schema](schema/inspire-schema.json) 
2. **Test** integration with your repository software
3. **Configure** field mappings for automated ingestion
4. **Implement** validation in your data submission workflow

### **For Tool Developers**
1. **Examine** the [schema structure](schema/inspire-schema.json)
2. **Use** the JSON Schema for validation
3. **Implement** section-based form interfaces using the `x-sections` metadata
4. **Contribute** improvements via [GitHub issues](https://github.com/inspirelabs/inspire-labs/issues)

---

##  **Key Features**

### **Built for Social Science**
- Community engagement tracking
- Equity and accessibility considerations
- Flexible geographic specification
- Decision-support use cases

### **Standards Compliant**
- Compatible with DDI, ISO 19115, DataCite
- Follows metadata best practices
- Enables institutional repository integration

### **Practical & Flexible**
- Flat data structure for tool compatibility
- Controlled vocabularies for consistency
- Optional fields for different use cases
- Multiple format support (JSON, XML, CSV)

---

##  **Community & Support**

### **Get Involved**
- ** Schema Discussions:** [GitHub Discussions](https://github.com/mettakyle/inspire-labs/discussions)
- ** Report Issues:** [GitHub Issues](https://github.com/mettakyle/inspirelabs/inspire-labs/issues)
- ** Schema Questions:** [kyle.metta@noaa.gov](mailto:kyle.metta@noaa.gov)

### **Contributing**
We welcome contributions to improve the schema:
- Suggest new controlled vocabulary terms
- Propose additional fields
- Share implementation examples
- Improve documentation

See our [Contributing Guide](../CONTRIBUTING.md) for details.

### **Citing the Schema**
```
InSPIRE Labs. (2025). InSPIRE Metadata Schema for Social Science Weather Data. 
Version 1.0. https://inspirelabs.github.io/inspire-labs/metadata-schema/
```

---

<div class="next-steps-banner">
  <h3>🚀 Ready to Start?</h3>
  <p>Download the <a href="templates/inspire-template.csv">CSV template</a>, check out our <a href="examples/">examples</a>, or <a href="tools/validator.html">validate your existing data</a>.</p>
  <p><a href="../">← Back to InSPIRE Labs</a> | <a href="field-reference.html">Field Reference →</a></p>
</div>

<style>
.quick-start-section {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  margin: 30px 0;
}

.quick-option {
  background: #f8f9fa;
  padding: 20px;
  border-radius: 8px;
  text-align: center;
  border-left: 4px solid #007bff;
}

.quick-option h3 {
  margin-top: 0;
  color: #007bff;
}

.btn {
  display: inline-block;
  padding: 8px 16px;
  margin: 5px;
  text-decoration: none;
  border-radius: 5px;
  font-weight: bold;
  font-size: 14px;
}

.btn-primary {
  background-color: #007bff;
  color: white;
}

.btn-secondary {
  background-color: #28a745;
  color: white;
}

.next-steps-banner {
  background: linear-gradient(135deg, #007bff, #0056b3);
  color: white;
  padding: 25px;
  border-radius: 8px;
  text-align: center;
  margin-top: 40px;
}

.next-steps-banner a {
  color: #b3d9ff;
  font-weight: bold;
}

.next-steps-banner a:hover {
  color: white;
}

table {
  width: 100%;
  border-collapse: collapse;
  margin: 20px 0;
}

table th, table td {
  border: 1px solid #ddd;
  padding: 12px;
  text-align: left;
}

table th {
  background-color: #f2f2f2;
  font-weight: bold;
}

@media (max-width: 768px) {
  .quick-start-section {
    grid-template-columns: 1fr;
  }
}
</style>
