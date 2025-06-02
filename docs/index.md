# InSPIRE Labs

**Development space for social scientists and SBES datasets related to extreme weather**

[![NOAA](https://img.shields.io/badge/NOAA-Social%20Science%20Program-blue)](https://wpo.noaa.gov/social-science/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

---

##  **What is InSPIRE?**

**InSPIRE** is the development space for the **Integrated Societal-data Platform for Interdisciplinary Research and Evaluation** — or InSPIRE for short. This platform is a core product of the **Societal Data Insights Initiative (SDII)** within NOAA's Social Science Program (SSP) at the Weather Program Office (WPO).

We're building InSPIRE as a **cloud-native platform on Amazon Web Services (AWS)** to support the future of integrated weather and social science research. Our goal is to enable more thoughtful coordination and evaluation by bringing together diverse data sources and disciplinary perspectives.

---

##  **Why Labs?**

This space is for **experiments, feedback, and iteration**. You'll find:

  <div>
  <div class="feature-card">
    <h3> Tutorials</h3>
    <p>Step-by-step guides for working with social science and weather data</p>
    <a href="tutorials/" class="btn-link">View Tutorials →</a>
  </div>
  
  <div class="feature-card">
    <h3> Metadata Schema</h3>
    <p>Standardized metadata framework for social science weather datasets</p>
    <a href="metadata-schema/" class="btn-link">Schema Documentation →</a>
  </div>
  
  <div class="feature-card">
    <h3> Design Artifacts</h3>
    <p>User research, wireframes, and design decisions driving platform development</p>
    <a href="design-artifacts/" class="btn-link">Design Resources →</a>
  </div>
</div>

---

## **InSPIRE Metadata Schema**

*Comprehensive metadata framework for social science datasets related to weather and climate*

The InSPIRE Metadata Schema bridges the gap between meteorological data standards and social science research needs, ensuring datasets are discoverable, citable, and interoperable.

### **⚡ Quick Start**

<div class="quick-actions">
  <a href="metadata-schema/templates/inspire-template.csv" class="btn btn-primary"> Download CSV Template</a>
  <a href="metadata-schema/tools/validator.html" class="btn btn-secondary"> Validate Your Data</a>
  <a href="metadata-schema/examples/" class="btn btn-outline"> See Examples</a>
  <a href="metadata-schema/" class="btn btn-outline">📖 Full Documentation</a>
</div>

### ** Schema Highlights**

- **7 logical sections** organizing 34+ metadata fields
- **Controlled vocabularies** for consistency and discoverability  
- **Standards compliance** with DDI, ISO 19115, and DataCite
- **Community engagement** and **equity considerations** built-in
- **Flexible format support** (JSON, XML, CSV)

---

##  **Platform Development**

### **Current Focus Areas**

**Data Integration Pipeline**
- Automated ingestion from multiple social science data sources
- Real-time weather data integration via NOAA APIs
- Quality assurance and validation workflows

**User Interface Design**
- Researcher-friendly data discovery and visualization
- Collaborative analysis tools
- Mobile-responsive design for field research

**Community Features**
- Discussion forums for cross-disciplinary collaboration
- Shared methodology repositories
- Best practices documentation

### **Technology Stack**

- **Cloud Infrastructure:** Amazon Web Services (AWS)
- **Data Storage:** S3,
- **Processing:** Lambda, EC2, SageMaker
- **API:** 
- **Frontend:** Modern web frameworks and graphical user interface

---

## 📖 **Resources**

### **Getting Started**
- [ Platform Overview](overview.html) - High-level introduction to InSPIRE
- [ Technical Architecture](architecture.html) - System design and components (coming soon)
- [ User Personas](personas.html) - Who we're building for


### **For Researchers**
- [ Data Standards](metadata-schema/) - Metadata schema documentation
- [ Use Cases](use-cases.html) - Real-world application examples
- [ Community Guidelines](community.html) - Collaboration expectations (coming soon!)

### **For Developers**
- [ Issue Tracking](https://github.com/inspirelabs/inspire-platform/issues) - Bug reports and feature requests

---

##  **Community & Collaboration**

### **Get Involved**

**Research Community**
- Join our [Data Forum Calls](community/research-calls.html)
- Participate in [user testing sessions](community/user-testing.html)
- Share your [data challenges and needs](community/research-needs.html)



### **Contact & Support**

- ** General Discussion:** [GitHub Discussions](https://github.com/mettakyle/inspire-labs/discussions)
- ** Research Inquiries:** [kyle.metta@noaa.gov](mailto:kyle.metta@noaa.gov)
- ** Bug Reports:** [GitHub Issues](https://github.com/mettakyle/inspirelabs/inspire-platform/issues)

---

## 📅 **Latest Updates**

### **Recent Developments**
- **v1.0 Metadata Schema** - Complete field specification with controlled vocabularies
- **Prototype Data Viewer** - Interactive visualization tool for weather-social data
- **Community Feedback Portal** - Streamlined input collection from researchers
- **AWS Architecture** - Cloud-native infrastructure design completed

### **Coming Soon**
- **Jupyter Integration** - Notebook environment for collaborative analysis
- **Cookbooks** - Binder launchable notebooks and tutorials


---

## **About NOAA's Social Science Program**

The **Social Science Program (SSP)** within NOAA's Weather Program Office advances the integration of social science research with weather and water forecasting to improve societal outcomes and decision-making.

**Key Goals:**
- Enhance forecast communication and public understanding
- Improve decision-support tools for emergency management
- Advance equity and accessibility in weather services
- Foster interdisciplinary research collaborations

Learn more about [NOAA's Social Science Program](https://www.weather.gov/about/social-science-program).

---

##  **Acknowledgments**

InSPIRE Labs is supported by:
- **NOAA Weather Program Office** - Primary funding and institutional support
- **Social Science Program** - Research guidance and community connections
- **Societal Data Insights Initiative** - Strategic direction and oversight
- **Research Community Partners** - Ongoing feedback and collaboration

---

##  **License & Use**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

**Citation:**
```
InSPIRE Labs. (2025). Integrated Societal-data Platform for Interdisciplinary 
Research and Evaluation. NOAA Weather Program Office. 
https://inspirelabs.github.io/inspire-labs/
```

---

<div class="footer-cta">
  <h3>🚀 Ready to Get Started?</h3>
  <p>Explore our <a href="metadata-schema/">metadata schema</a>, try our <a href="prototypes/">prototypes</a>, or <a href="mailto:research@inspirelabs.org">get in touch</a> to learn more about InSPIRE.</p>
</div>

<style>
.feature-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  margin: 30px 0;
}

.feature-card {
  background: #f8f9fa;
  padding: 20px;
  border-radius: 8px;
  border-left: 4px solid #007bff;
}

.feature-card h3 {
  margin-top: 0;
  color: #007bff;
}

.quick-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 20px 0;
}

.btn {
  display: inline-block;
  padding: 10px 20px;
  text-decoration: none;
  border-radius: 5px;
  font-weight: bold;
  text-align: center;
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

.btn-link {
  color: #007bff;
  text-decoration: none;
  font-weight: bold;
}

.btn-link:hover {
  text-decoration: underline;
}

.footer-cta {
  background: linear-gradient(135deg, #007bff, #0056b3);
  color: white;
  padding: 30px;
  border-radius: 10px;
  text-align: center;
  margin-top: 40px;
}

.footer-cta a {
  color: #b3d9ff;
}

.footer-cta a:hover {
  color: white;
}

@media (max-width: 768px) {
  .quick-actions {
    flex-direction: column;
  }
  
  .btn {
    width: 100%;
  }
}
</style>
