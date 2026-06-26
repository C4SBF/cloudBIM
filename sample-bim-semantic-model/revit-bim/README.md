[↑ Back](../README.md)

# Revit BIM

## Model Overview

**Revit R25** model covering four disciplines: Architectural, Mechanical, Electrical, and Plumbing.

The three MEP models (Mechanical, Electrical, Plumbing) are linked from the Architectural model. Besides the IfcGUID carried through all stages and models, all assets carry a unique value for the instance parameter **`Mark`**, which follows the BDNS naming standard (see below) and which serves as the identifier in schedules, tags, and the labels in the Semantic Model.

---

## Model Versions

### v2026-06-23 — BDNS Naming & Asset Schedules *(current)*

- Revit model updated to follow the [BDNS standard for Device/Asset role names (`asset.name`)](https://theodi.github.io/BDNS/BDNS_Specification_naming_syntax.html#deviceasset-role-name-asset.name).
- The Semantic Class included as a paramter is derivedd from the [BDNS-Semantic Ontology Crosswalk](https://docs.google.com/spreadsheets/d/1q-WDK43twUAN_64i6BG_JsI5yuX3Smi9t2coR8eTQcU/edit?gid=180246182#gid=180246182). It is used in the Semantic Bridge converting the BIM to a Semantic Model.
- Plumbing assets enriched with attributes for connection counting and directional connection identification. These attributes were written to Revit parameters via a **Dynamo script** and are reflected in the asset Excel files below.
- The previous `RE1_Electrical_Schedule.xlsx` has been archived and replaced by three discipline-specific asset files:

| File | Contents |
|---|---|
| `Mechanical Assets.xlsx` | Mechanical assets with BDNS naming, Semantic Class, MasterFormat, System/Connection parameters |
| `Electrical Assets.xlsx` | Electrical assets with BDNS naming, Semantic Class, MasterFormat, Panel Connection parameters |
| `Plumbing Assets.xlsx` | Plumbing assets with BDNS naming, Semantic Class, MasterFormat, System/Connection parameters |

📦 **Download:** [RE1 Revit 2025 — 2026-06-23](../revit-bim/RE1-Revit-2025_2026-06-23.zip)

---

### v2026-03-12 — Mechanical Room Relationships Cleaned Up

- Relationships between all elements in the Mechanical Room have been clarified.
- All elements are modeled as **panels**; upstream relationships are captured via the Revit parameter **`Supply From`**, populated with the upstream panel's value.

![Mechanical Room downstream relations](MechanicalRoom_downstream_relations.png)

---

### v2026-02-21 — Mechanical Room & Semantic Classes Added

- New **Mechanical Room** added, including Transformer, Meter, and Panels.
- All assets now carry a type parameter **`Semantic Class`** containing either the [s223](https://open223.info/) or [Brick](https://brickschema.org/) class, simplifying conversion to a Semantic Model.

![Electrical Diagram](Electrical.png)