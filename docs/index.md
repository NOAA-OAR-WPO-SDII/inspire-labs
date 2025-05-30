# InSPIRE Labs

**Development space social science and datasets related to extreme weather**

[![GitHub](https://img.shields.io/badge/GitHub-Repository-blue)](https://github.com/inspirelabs/inspire-labs)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Version](https://img.shields.io/badge/Version-1.0-orange.svg)](CHANGELOG.md)

---


*InSPIRE Labs** is the development space for the Integrated Societal-data Platform for Interdisciplinary Research and Evaluation — or InSPIRE for short. This platform is a core product of the Societal Data Insights Initiative (SDII) within NOAA's Social Science Program (SSP) at the Weather Program Office (WPO).

We’re building InSPIRE as a cloud-native platform on **Amazon Web Services (AWS)** to support the future of integrated weather and social science research. Our goal is to enable more thoughtful coordination and evaluation by bringing together diverse data sources and disciplinary perspectives.

### Why Labs?

This space is for **experiments, feedback, and iteration**. You’ll find:

- Prototypes of InSPIRE features  
- Tutorials and cookbooks  
- Metadata schema discussions  
- Ongoing design artifacts

## InSPIRE Metadata Schema

## ⚡ **Quick Start**

<div class="quick-start-buttons">
  <a href="#download-templates" class="btn btn-primary">📥 Download Templates</a>
  <a href="#validate-data" class="btn btn-secondary">✅ Validate Your Data</a>
  <a href="#examples" class="btn btn-outline">📚 See Examples</a>
</div>

---

## 📋 **Schema Overview**

The InSPIRE schema organizes metadata into **7 logical sections**:

### **1. 🆔 Identification & Overview**
Core dataset information including title, creators, funding, and licensing.

**Key Fields:** `title`, `abstract`, `creator`, `license`, `citation_recommendation`

### **2. 🏷️ Subject Classification & Keywords** 
Domain classification and discoverability tags using controlled vocabularies.

**Key Fields:** `subject_category`, `keywords_controlled`, `keywords_other`

### **3. 🌍 Geographic & Temporal Information**
Spatial and temporal coverage with flexible location specification.

**Key Fields:** `geographic_coverage_controlled`, `temporal_coverage_start`, `spatial_resolution`

### **4. 📊 Data Characteristics & Methods**
Collection methodology, data types, and processing history.

**Key Fields:** `data_type`, `collection_methodology`, `uncertainty_quantification`

### **5. 🎯 Decision-Support Attributes**
Intended applications and integration capabilities.

**Key Fields:** `use_cases`, `integration_with_other_data`

### **6. 🤝 Community Engagement & Ethics**
Community involvement and ethical considerations.

**Key Fields:** `community_engagement`, `equity_accessibility`

### **7. 🔧 Technical Details & Access**
Access methods, file formats, and technical requirements.

**Key Fields:** `data_access_url`, `api_endpoint`, `software_dependencies`

---

## 📥 **Download Templates** {#download-templates}

Choose your preferred format to get started:

| Format | Best For | Download |
|--------|----------|----------|
| **CSV Template** | Quick data entry, pilot testing | [📄 CSV Template](templates/inspire-template.csv) |
| **JSON Schema** | Validation, tool development | [📄 JSON Schema](schema/inspire-schema.json) |
| **XML Schema** | Legacy systems, formal validation | [📄 XML Schema](schema/inspire-schema.xsd) |
| **YAML Documentation** | Human-readable specification | [📄 YAML Docs](schema/inspire-schema.yaml) |

---

## ✅ **Validate Your Data** {#validate-data}

Test your metadata against the InSPIRE schema:

<div class="validator-section">
  <p><strong>🔧 Online Validator</strong> - <a href="tools/validator.html">Validate your JSON/CSV data</a></p>
  <p><strong>📋 Checklist</strong> - <a href="validation-checklist.html">Manual validation checklist</a></p>
  <p><strong>⚡ Quick Check</strong> - Required fields: title, abstract, creator, subject_category, geographic_coverage_controlled, temporal_coverage_start</p>
</div>

---

## 📚 **Examples** {#examples}

Real-world examples showing the schema in action:

### 🌀 **Hurricane Harvey Social Media Dataset**
```json
{
  "title": "Hurricane Harvey Social Media Response Dataset",
  "subject_category": "Emergency Management",
  "geographic_coverage_controlled": ["Gulf Coast", "Urban Areas"],
  "geographic_coverage_specific": "Houston Metropolitan Area, Texas",
  "data_type": "Text Analysis",
  "use_cases": "Public Risk Communication"
}
```
[📄 View Complete Example](examples/hurricane-harvey-example.json)

### 🌾 **Midwest Drought Perception Study**
```json
{
  "title": "Farmer Risk Perception During 2019 Midwest Drought",
  "subject_category": "Risk Perception", 
  "geographic_coverage_controlled": ["Midwest", "Rural Communities"],
  "data_type": "Survey Data",
  "community_engagement": true
}
```
[📄 View Complete Example](examples/drought-perception-example.json)

### 🏙️ **Urban Heat Island Social Vulnerability**
```json
{
  "title": "Social Vulnerability to Urban Heat Islands in Phoenix",
  "subject_category": "Social Vulnerability",
  "geographic_coverage_controlled": ["Urban Areas"],
  "data_type": "Geospatial Data",
  "equity_accessibility": true
}
```
[📄 View Complete Example](examples/urban-heat-example.json)

---

## 🎓 **Getting Started Guide**

### **For Researchers**
1. **Download** the [CSV template](templates/inspire-template.csv)
2. **Fill out** your dataset metadata
3. **Validate** using our [online tool](tools/validator.html)
4. **Export** to JSON for repository submission

### **For Data Managers**
1. **Review** the [JSON Schema](schema/inspire-schema.json)
2. **Test** integration with your repository software
3. **Configure** field mappings for automated ingestion
4. **Implement** validation in your data submission workflow

### **For Tool Developers**
1. **Examine** the [schema structure](schema-documentation.html)
2. **Use** the JSON Schema for validation
3. **Implement** section-based form interfaces
4. **Contribute** improvements via GitHub issues

---

## 📖 **Documentation**

| Resource | Description |
|----------|-------------|
| [📚 Complete Field Reference](field-reference.html) | Detailed description of every field |
| [📝 Controlled Vocabularies](controlled-vocabularies.html) | All standardized terms and enums |
| [🔧 Implementation Guide](implementation-guide.html) | Technical integration details |
| [❓ FAQ](faq.html) | Common questions and answers |
| [📊 Standards Compliance](standards-compliance.html) | Mapping to DDI, ISO 19115, DataCite |

---

## 🤝 **Community & Support**

### **Get Involved**
- **💬 Discussions:** [GitHub Discussions](https://github.com/inspirelabs/inspire-metadata-schema/discussions)
- **🐛 Issues:** [Report bugs or request features](https://github.com/inspirelabs/inspire-metadata-schema/issues)
- **📧 Contact:** [inspire-schema@yourlabs.org](mailto:inspire-schema@yourlabs.org)

### **Contributing**
We welcome contributions! See our [Contributing Guide](CONTRIBUTING.md) for details.

### **Citing InSPIRE**
```
InSPIRE Labs. (2025). InSPIRE Metadata Schema for Social Science Weather Data. 
Version 1.0. https://inspirelabs.github.io/inspire-metadata-schema/
```

---

## 📄 **License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div class="footer-note">
<p><strong>InSPIRE Labs</strong> | Bridging Social Science and Weather Data</p>
<p>Created with ❤️ for the research community</p>
</div>

<style>
.quick-start-buttons {
  margin: 20px 0;
}

.btn {
  display: inline-block;
  padding: 10px 20px;
  margin: 5px;
  text-decoration: none;
  border-radius: 5px;
  font-weight: bold;
}

.btn-primary {
  background-color: #007bff;
  color: white;
}

.btn-secondary {
  background-color: #28a745;
  color: white;
}

.btn-outline {
  background-color: transparent;
  color: #007bff;
  border: 2px solid #007bff;
}

.validator-section {
  background-color: #f8f9fa;
  padding: 15px;
  border-radius: 5px;
  margin: 15px 0;
}

.footer-note {
  text-align: center;
  margin-top: 40px;
  padding-top: 20px;
  border-top: 1px solid #eee;
  color: #666;
}

table {
  width: 100%;
  border-collapse: collapse;
  margin: 15px 0;
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
</style>
