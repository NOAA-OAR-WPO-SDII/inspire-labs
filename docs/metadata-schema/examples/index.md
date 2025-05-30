# Example Datasets

**Real-world examples demonstrating the InSPIRE Metadata Schema in practice**

[⬅️ Back to Metadata Schema](../) | [🏠 InSPIRE Labs Home](../../)

---

These examples show how the InSPIRE schema captures metadata for different types of social science weather research. Each example demonstrates the schema's flexibility while maintaining consistency across different domains and methodologies.

## 📚 **Complete Examples**

### 🌀 **Emergency Management**
**[Hurricane Harvey Social Media Response Dataset](hurricane-harvey-example.json)**
- **Domain:** Emergency Management  
- **Data Type:** Text Analysis
- **Location:** Gulf Coast, Urban Areas
- **Community Focus:** Social media coordination during disaster response
- **Key Features:** Community engagement, real-time data collection, sentiment analysis

---

### 🌾 **Risk Perception**
**[Farmer Risk Perception During 2019 Midwest Drought](drought-perception-example.json)**
- **Domain:** Risk Perception
- **Data Type:** Survey Data  
- **Location:** Midwest, Rural Communities
- **Community Focus:** Agricultural producers' drought preparedness
- **Key Features:** Community partnerships, agricultural extension collaboration, equity considerations

---

### 🏙️ **Social Vulnerability**
**[Social Vulnerability to Urban Heat Islands in Phoenix](urban-heat-example.json)**
- **Domain:** Social Vulnerability
- **Data Type:** Geospatial Data
- **Location:** Urban Areas
- **Community Focus:** Environmental justice and heat exposure
- **Key Features:** Multi-source data integration, vulnerability mapping, health outcomes

---

### 📡 **Weather Communication**
**[Impact-Based Tornado Warning Communication Effectiveness](tornado-communication-example.json)**
- **Domain:** Weather Communication
- **Data Type:** Survey Data
- **Location:** United States, Midwest  
- **Community Focus:** Public understanding of weather warnings
- **Key Features:** Mixed methods, government partnership, behavioral observation

---

## 🎯 **What These Examples Show**

### **Schema Flexibility**
- **Multiple data types:** Survey, geospatial, text analysis, sensor data
- **Various scales:** Household to metropolitan to multi-state
- **Different methodologies:** Quantitative, qualitative, mixed methods
- **Diverse partnerships:** Academic, government, community organizations

### **Consistent Structure**
- **Standard fields** used across all domains
- **Controlled vocabularies** ensuring discoverability
- **Clear documentation** of methods and limitations
- **Proper attribution** and citation guidance

### **Community Integration**
- **Community engagement** documented for participatory research
- **Equity considerations** highlighted where relevant
- **Local partnerships** acknowledged in contributor roles
- **Real-world applications** clearly described

---

## 🔍 **Browse by Domain**

| Domain | Example | Data Type | Key Focus |
|--------|---------|-----------|-----------|
| **Emergency Management** | [Hurricane Harvey](hurricane-harvey-example.json) | Text Analysis | Disaster response coordination |
| **Risk Perception** | [Midwest Drought](drought-perception-example.json) | Survey Data | Agricultural decision-making |
| **Social Vulnerability** | [Phoenix Heat](urban-heat-example.json) | Geospatial Data | Environmental justice |
| **Weather Communication** | [Tornado Warnings](tornado-communication-example.json) | Survey Data | Warning effectiveness |

---

## 🔍 **Browse by Data Type**

| Data Type | Examples | Common Features |
|-----------|----------|-----------------|
| **Survey Data** | [Drought Perception](drought-perception-example.json), [Tornado Communication](tornado-communication-example.json) | Response rates, weighting, demographic analysis |
| **Text Analysis** | [Hurricane Harvey](hurricane-harvey-example.json) | Sentiment analysis, social media APIs, natural language processing |
| **Geospatial Data** | [Phoenix Heat](urban-heat-example.json) | Coordinate systems, spatial resolution, mapping integration |

---

## 📝 **Using These Examples**

### **For Researchers**
- **Copy and adapt** field examples for your own datasets
- **See required vs. optional** field usage patterns
- **Learn controlled vocabulary** application in context
- **Understand community engagement** documentation

### **For Data Managers** 
- **Test repository integration** with realistic metadata
- **Validate import/export** workflows with complete examples
- **Configure field mappings** based on common patterns
- **Design user interfaces** informed by real use cases

### **For Tool Developers**
- **Test validation logic** against complete datasets
- **Design form interfaces** with realistic field combinations
- **Build search functionality** using controlled vocabularies
- **Create data visualization** features with sample data

---

## 🛠️ **Validate Your Own Data**

Ready to create metadata for your dataset? 

<div class="action-buttons">
  <a href="../tools/validator.html" class="btn btn-primary">🔍 Test with Validator</a>
  <a href="../templates/inspire-template.csv" class="btn btn-secondary">📥 Download Template</a>
  <a href="../field-reference.html" class="btn btn-outline">📖 Field Reference</a>
</div>

---

## 💡 **Contributing Examples**

Have a dataset that would make a good example? We'd love to include more examples showing:

- **International research** (non-US locations)
- **Indigenous knowledge** integration
- **Longitudinal studies** with multiple time periods  
- **Multi-institutional collaborations**
- **Sensor network data** and IoT applications
- **Economic impact** assessments

**Contact us:** [schema@inspirelabs.org](mailto:schema@inspirelabs.org)

---

<div class="next-steps">
  <h3>🚀 Next Steps</h3>
  <p>Explore the <a href="../field-reference.html">complete field reference</a>, try the <a href="../tools/validator.html">online validator</a>, or return to the <a href="../">metadata schema homepage</a>.</p>
</div>

<style>
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

.action-buttons {
  display: flex;
  gap: 10px;
  margin: 20px 0;
  flex-wrap: wrap;
}

.btn {
  display: inline-block;
  padding: 10px 20px;
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

.next-steps {
  background: #f8f9fa;
  padding: 20px;
  border-radius: 8px;
  border-left: 4px solid #007bff;
  margin-top: 30px;
}

@media (max-width: 768px) {
  .action-buttons {
    flex-direction: column;
  }
  
  .btn {
    text-align: center;
  }
}
</style>
