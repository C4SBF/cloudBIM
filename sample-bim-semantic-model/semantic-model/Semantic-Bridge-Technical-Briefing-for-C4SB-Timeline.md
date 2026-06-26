[↑ Back](README.md)

# Appendix A \- C4SB, Semantic Buildings, cloudBIM, Timeline

### **Track A: PAE Living Building Activation into a Digital Twin and Semantic Model**

The PAE Living Building journey represents a transition from fragmented, static data to a continuously updated, living semantic model. Below is the timeline of the development, integration, and refinement of the PAE digital twin from early 2025 to the present.

#### **Phase 1: Discovery & Digital Foundation (Early 2025 – Summer 2025\)**

* **Feb 2025:** Pilot initiated at the AHR Expo / C4SB sessions; PAE agrees to test the digital twin workflow.  
* **Mar 2025:** Initial Data Ingestion: All available fragmented data (Revit, PDFs, spreadsheets, reports) consolidated into the ONUMA System (cloudBIM) to establish unique asset and spatial IDs.  
* **Aug 2025:** SkyCentrics IBB (Super SkyBox) installed; 100,000+ sensor endpoints discovered via BACnet and integrated into the cloudBIM backbone.  
* **Sept 2025:** First live operational dashboard; PAE achieves a unified view of live sensor data (PV/Battery/Energy) overlaid with spatial cloudBIM context.  
* **Sept 2025:** SkyCentrics API opened to cloudBIM ONUMA System to generate graphs from live time series data at building, space and asset level

#### **Phase 2: Semantic Alignment & Model Refinement (Fall 2025 – Winter 2025\)**

* **Oct 2025:** Pacific Northwest National Lap (PNNL) begins Revit model updates (BIM2RDF enablement) to enhance MEP system relationships and ensure IFC/GUID consistency.  
* **Nov 2025:** Identification of the "semantic gap"; the Onuma team establishes that existing tools lack the ability to maintain RDF/ASHRAE 223P semantic models alongside evolving cloudBIM spatial data.  
* **Dec 2025:** Onuma Semantic Bridge Reference Implementation: A working environment is demonstrated, enabling live semantic maintenance where ASHRAE 223P-aligned relationships are preserved through operational changes.

#### **Phase 3: Operational Testing & Expansion (2026 – Present)**

* **Feb 2026:** AHR/ASHRAE Expo 2026: Live demonstrations prove the "Data-to-Context-to-Action" workflow (e.g., triggering work orders from live sensor thresholds from SkyCentrics to BIMgenie CMMS).  
* **May 2026:** Digital Twin Maturity Assessment: Implementation of a new framework to formally measure PAE’s semantic completeness, temporal continuity, and operational trust.  
* **Late June 2026:** **(Upcoming):** Technical Dissemination & Scalability:  
  * Release of the *Semantic Bridge Technical Briefing*, which outlines the federated architecture.

### **Track B: ASHRAE 223PM and Semantic Bridge**

This milestone timeline tracks the convergence of the cloudBIM, ASHRAE 223P implementation, and the development of the Semantic Bridge over the past year.

#### **Phase 1: Semantic Foundation & Operational Discovery (May – Sept 2025\)**

* **May 16, 2025:** Weekly Semantic Building group (C4SB) meetings begin to focus on ASHRAE 223P and RDF as the primary interoperability languages.  
* **Aug 1, 2025:** Formal ASHRAE 223P \+ RDF development initiates, leveraging the RE1 reference model to establish a path toward what would become the Semantic Bridge App.  
* **Aug 5, 2025:** Sensor endpoint curation begins; thousands of siloed points are reduced to \~400 meaningful signals (PV, battery, occupancy).  
* **Aug 11, 2025:** Proof of activation: Battery thresholds are successfully linked to BIMGenie CMMS to trigger automated work orders, proving "data to context to action".  
* **Aug 28, 2025:** PNNL joins the effort, launching the BIM2RDF track to prototype Revit-to-RDF workflows in parallel to the cloudBIM track.  
* **Sept 5, 2025:** Strategy shift: The RE1 model is proposed as a small, simplified sandbox to reduce friction for multi-party testing.

#### **Phase 2: Tooling & Open Infrastructure (Oct 2025 – Dec 2025\)**

* **Oct 1, 2025**: Search for Open RDF editor and gap identified; motivates the creation of the dedicated Semantic Bridge App within the ONUMA System.  
* **Oct 7, 2025:** GUID alignment established; PNNL agrees to add IFC GUID properties to Revit models, ensuring stable identifiers across cross-tool workflows.  
* **Nov 1, 2025:** Community declaration: Plan announced to publish the RE1 sandbox model openly on the C4SB GitHub.  
* **Dec 1, 2025:** IP hygiene: A six-week process begins to remove proprietary asset data from the RE1 model, ensuring the semantic intent is preserved while allowing open sharing.

#### **Phase 3: Semantic Bridge Realization & Convergence (Jan 2026 – June 2026\)**

* **Jan 9, 2026:** Semantic Bridge App developed, linking cloudBIM geometry (persistent IDs) with 223P/RDF semantics; RE1 model is published to GitHub as a shared baseline.  
* **Feb 2026:** AHR/ASHRAE Expo 2026: The team provides live demonstrations of the working integration, publicly proving the "data to context to action" workflow.  
* **Feb 18, 2026:** Phase 2 workflow established: All parties adopt the open RE1 sandbox to standardize the 223P mapping process on 2–3 assets before re-applying it to the full PAE building model.  
* **June 2026:** Expansion: BDNS (Building Device and Asset Naming Standards) integration begins, enabling a mapping between BIM/IFC, BDNS asset types, and semantic ontologies (223P/Brick/REC), allowing for the automated generation of RDF Turtle files.

#### **Rensselaer Polytechnic Institute (RPI) / Georgia Tech / IFC-LD Collaboration**

* **Jan 2026:** Dennis Shelden and Devon Sparks presented IFC modernization and IFC-LD work to the C4SB Semantic Buildings group.  
* **Feb–Mar 2026:** RPI and ONUMA teams explored IFC-LD, RDF generation, SHACL-based transformations, and semantic workflows using the RE1 reference model as a common discussion framework.  
* **Apr–Jun 2026:**  Follow-up discussions focused on lessons learned, RDF generation, semantic interoperability, and potential alignment with buildingSMART, ASHRAE 223P, and BDNS efforts.  
* **June 2026:** Public IFC-LD resources and repositories were identified and reviewed as part of the broader Semantic Bridge alignment effort.

### **Track C: C4SB CyberSecurity Pilot**

**May 2026**

* **May 5 – 6:** David Holmberg (NIST) initiates a cybersecurity review of the PAE building, while Kimon emphasizes linking security governance to BIM contexts like the RE1 model.  
* **May 14:** The team establishes a research scope focused on a knowledge graph that maps IT/OT access rules directly to physical building assets in the RE1 model.  
* **May 18 – 20:** Kimon develops the "ALN cloudBIMStorm \#2" scenario, creating a cyber-physical framework where security governance is intrinsically tied to object models.  
* **May 27 – 28:** NIST intern joins the project, with the team aligning the research effort to focus on tangible building context rather than abstract IT security.

**June 2026**

* **June 2 – 4:** NIST gains access to PAE data via the ONUMA System/Semantic Bridge to evaluate cyber-physical use cases for maintenance and emergency conditions.  
* **June 16 – 19:** The team defines the distinction between the "Semantic Bridge" (data meaning) and "Operational Trust/Governance" (data access) layers within the IBB workflow.  
* **June 19:** The architecture is finalized, establishing a three-layer model—Source Systems, Semantic Bridge, and Operational Trust—to align with broader industry standards.

### **Track D: BuildingSmart and BDNS IFC**

* **Pre-June 1:** buildingSMART USA Webinar: Addressed PAE/C4SB, establishing key global interest.  
* **June 4:** buildingSMART International/Japan: Aligned on IFC/IoT ontology mapping and Semantic Bridge efforts.  
* **June 8:** buildingSMART USA Chapter: Strategized interoperability and Semantic Bridge alignment.  
* **June 11:** [Semantic Bridge BDNS → Semantic Ontology Crosswalk](https://docs.google.com/spreadsheets/d/1q-WDK43twUAN_64i6BG_JsI5yuX3Smi9t2coR8eTQcU/edit?usp=sharing) draft created and posted for comment  
* **June 12:** Working Group Session: Reviewed BDNS mapping concepts relative to C4SB workflows.  
* **June 17:** International Collaborative Meeting: Advanced discussions on BDNS, IFC, and digital twins with global stakeholders.  
* **June 22:** BDNS data added to C4SB cloudBIM RE1 Model  
* **June 25:** **(Upcoming)** Semantic Bridge used to create TTL file of RE1 with BDNS data  
* **June 26 (Upcoming):** Semantic Buildings Working Group: Scheduled BDNS and C4SB presentation.

### **Track E: Events and Conferences**

This timeline captures key events, conferences, and presentations for the Coalition for Smarter Buildings (C4SB) and related industry collaborations from 2025 through June 2026.2025: Foundation & Working Groups

### **2026**

* **February 2026:** AHR/ASHRAE Expo 2026: The team provided live demonstrations of the integrated "Data-to-Context-to-Action" workflow.  
* **April 27–30, 2026:** **Asset Leadership Network (ALN) Global Asset Management Summit (Washington, D.C.): (Rayburn House Office Building):** Featured C4SB and PAE Living Building as a case study for AI in Federal facilities.  
* **May 2026:** **SimBuild Conference:** Presentation on C4SB, cloudBIM, and interoperability workflows.  
* **June 5, 2026:** Collaborative meeting with buildingSMART Japan/UK groups regarding IFC to Smart Building ontologies.  
* **June 17, 2026:** **U.S. Green Building Council (USGBC) Webinar:** "Ensuring Trust in AI for Building Operations," featuring a panel from C4SB, the Linux Foundation, and SkyCentrics.  
* **June 26, 2026 (Upcoming):** **Semantic Buildings Working Group:** Scheduled show-and-tell presentation regarding BDNS (Building Device and Asset Naming Specification) and its mapping to semantic ontologies.  
* **October 20, 2026 (Planned):** **GreenBuild International Convention (NYC):** Collaborative presentation on digital twins and interoperability.  
* **October 2026 (Planned):** **buildingSMART International Summit (Tokyo):** Ongoing alignment on the buildingSMART position paper and collaborative demonstrations.

* **January 31 – February 4, 2026:** **AHR Expo & ASHRAE Winter Conference (Las Vegas):**  
  * **February 1:** BACnet group gathering.  
  * **February 2–4:** C4SB Booth \#C743 activities: Demonstrations of "Data-to-Context-to-Action," PAE Living Building sessions, and "Super SkyBox" connectivity  
  * **February 2:** ASHRAE Conference Session: "From Models to Meaning"  
  * **February 3:** AHR Session: "Software Platform Wars"  
* **February 9, 2026:** **Monday Live\!:** Debrief and review session of AHR/ASHRAE events.  
* **February 27, 2026:** **Webinar Presentation:** Kimon Onuma presentation on PAE and Microgrids.  
* **Early 2025: AHR Expo & ASHRAE Winter Conference:** Initial C4SB presentations and industry outreach, serving as the foundational public push for the coalition.  
* **April 9, 2025:** C4SB Semantic Buildings group meeting on "ontologies," featuring a 5-minute presentation on Minimum BIM and Connection Profiles.  
* **April 2025:** C4SB "Semantic Tiger Team" kickoff.  
* **May 2025:** Weekly Semantic Building Group meetings begin (recurring Friday sessions).  
* **Summer 2025:** Joining the recurring "Monday Live\!" sessions, providing a platform for cloudBIM, interoperability, and coalition strategy.  
* **August 10–28, 2025:** Collaboration with PNNL on BIM2RDF and semantic modeling workflows.

### **Related Conferences**

* **June 17, 2026:** **U.S. Green Building Council (USGBC) Webinar:** "Ensuring Trust in AI for Building Operations."  
* **October 20, 2026 (Planned):** **GreenBuild International Convention (NYC):** Digital twins and interoperability presentation.  
* **October 2026 (Planned):** **buildingSMART International Summit (Tokyo):** Global collaborative alignment.

### **Expanding Use Cases**

### **2026**

* cloudBIMStorm \#1: Emergency Response and Resilience  
* cloudBIMStorm \#2: Cybersecurity and Governance (NIST collaboration)  
* cloudBIMStorm \#3: Sustainability, Performance, and AI Readiness (USGBC Greenbuild)

Each initiative applies the same cloudBIM → Semantic Bridge → RDF workflow to a different domain, demonstrating that shared identity, context, and semantic relationships can support multiple owner outcomes without requiring separate information models.  
