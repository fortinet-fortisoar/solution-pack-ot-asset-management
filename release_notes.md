# What's New

## Enhancement

- FortiSOAR Minimum Compatibility - 7.4.1
- Renamed playbook `Set Assets With MEF Tag` to `Tag as Most Essential Function (MEF)` and added manual input to get reason for tagging asset as Most Essential Function (MEF).
- Introduced new **Asset Icon** record, `VOIP Phone`, `Gateway`, `Controller`, `Historian`, and `Printer`
- Introduced new playbook `Set Asset Icon` under collection **02 - Use Case - IT OT Asset Management** which correlate **Asset Icon** with **Asset** as per asset category.
- Dashboard:
  - Configured Record Distribution widget under `Asset Overview` with title as Asset Hostname.
  - Introduced new widget **Top 10 Devices With Vulnerabilities** under **Asset Risk Overview**
  
## Bug Fixes
    
- Dashboard:
    - Added roles for dashboard **Asset Change Activity Tracking**, **Asset Overview**, and **Asset Risk Overview**  
    - Update Query for dashboard **Asset Risk Overview**, under the section "Recent Alerts On Critical Assets" as `Asset Criticality` is eq `Critical` or `Asset Criticality` is eq `Very Critical`

- Changed playbook collection name:
    - **00 - Use Case - Asset Change Activity** to **02 - Use Case - Asset Change Activity**
    - **00 - Use Case - Asset Management** to **02 - Use Case - IT OT Asset Management**

- Changed tag name from `SampleAsset` & `SampleAlert` to `Sample`
- Added connector `Qualys` in Solution Pack.
- Under dashboard **Asset Overview** changed widget name from `MEF Asset` to `Most Essential Function (MEF) Assets`
- Renamed playbook `Links MITRE Matrices To Alert` to `Links Assets To Alert` and removed MITRE Module data correlation as implemented same in **MITRE ATT&CK Enrichment Framework v2.2.0**

## Depreciated

- Moved following fields from Asset from this Solution Pack to **Soar Framework Solution Pack v2.2.0**:
    - Network - Text Field
    - Subnet - Text Field
    - Firmware - Text Field
    - Vendor - Text Field
    - Product - Text Field
    - Asset - ManyToMany
    - Protocol - Picklist
    - ESPZone - Text Fields
    - Facility - Text Fields
    - Level - Picklist
    - Zone - Picklist
    - Asset Type - Picklist
    - Vulnerability Risk Status - Picklist

- Moved following picklist from Asset from this Solution Pack to **Soar Framework Solution Pack v2.2.0**:
    - AssetLevel 
    - AssetProtocol
    - AssetType
    - AssetZone
    - VulnerabilityRiskStatus

- Removed playbook `MITRE ATT&CK > Fetch Latest Data` from collection `02 - Use Case - IT OT Asset Management` as MITRE data can be ingested using data ingestion from MITRE connector.
- Removed playbook `Create Alerts Record`
- Removed playbook `Alert - Escalate To Incident`, `Alert - Escalate to Incident (Link Relations)`, and `Alert - Escalate To Incident (No Trigger)`, as implemented it in **Soar Framework Solution Pack v2.1.1** 
- Moved `MITRE Widget` from dashboard **Asset Risk Overview** to **MITRE ATT&CK Enrichment Framework v2.2.0**