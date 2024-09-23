# What's New

> The compatibility of this solution pack has been enhanced to FortiSOAR v7.4.1 and later.

## Playbook Enhancements

- A new playbook **Set Asset Icon** under the collection **02 - Use Case - IT OT Asset Management** correlates *Asset Icon* with *Asset* as per the asset's category.

- The playbook *Set Assets With MEF Tag* has been renamed to **Tag as Most Essential Function (MEF)**.
    - A manual input now asks for a reason when tagging assets as MEF.

- Renamed the playbook *Links MITRE Matrices To Alert* to **Links Assets To Alert**
    - Removed the correlation with MITRE module data as the correlation is now a part of [**MITRE ATT&CK Enrichment Framework**](https://fortisoar.contenthub.fortinet.com//detail.html?entity=mITREATT%26CKEnrichmentFramework&version=2.2.0&type=solutionpack) v2.2.0 and later.

## Record Enhancements

- A new record **Asset Icon** now has icons for following asset categories:
    - VOIP Phone
    - Gateway
    - Controller
    - Historian
    - Printer

## Dashboard Enhancements

- The **Asset Risk Overview** dashboard now appears with following enhancements:

    - A widget titled **Top 10 Devices With Vulnerabilities** displays the top 10 devices with vulnerabilities.

    - A widget titled **Recent Alerts On Critical Assets** now comes with pre-defined filter to list assets based on their criticalities &ndash; *Critical* or *Very Critical*

- The **Asset Overview** dashboard displays *Asset Hostname* as the asset label under **Critical Asset Distribution**.

- Changed the widget name from *MEF Asset* to **Most Essential Function (MEF) Assets** to better describe the asset listing
  
## Other Enhancements

- The tag names `SampleAsset` and `SampleAlert` have been renamed to `Sample` for easy identification.

## Bug Fixes
    
- Users with any of the following roles can now access and manage the dashboards **Asset Change Activity Tracking**, **Asset Overview**, and **Asset Risk Overview**:

    - Full App Permission
    - SOC Manager
    - SOC Analyst

- Following playbook collection names were changed to be inline with other playbook collections in FortiSOAR&trade;:
    - **00 - Use Case - Asset Change Activity** renamed to **02 - Use Case - Asset Change Activity**.
    - **00 - Use Case - Asset Management** renamed to **02 - Use Case - IT OT Asset Management**.

- The connector **Qualys** now installs with this solution pack.

## Deprecations

- Following fields from the **Asset** module in this solution pack are now a part of [**SOAR Framework**](https://fortisoar.contenthub.fortinet.com//detail.html?entity=sOARFramework&version=2.2.0&type=solutionpack) v2.2.0 and later:

    | Field Name                | Input Type  |
    |:--------------------------|:------------|
    | Network                   | Text Field  |
    | Subnet                    | Text Field  |
    | Firmware                  | Text Field  |
    | Vendor                    | Text Field  |
    | Asset                     | ManyToMany  |
    | Protocol                  | Picklist    |
    | ESPZone                   | Text Fields |
    | Facility                  | Text Fields |
    | Level                     | Picklist    |
    | Zone                      | Picklist    |
    | Asset Type                | Picklist    |
    | Vulnerability Risk Status | Picklist    |

- Following picklists from the **Asset** module in this solution pack are now a part of [**SOAR Framework**](https://fortisoar.contenthub.fortinet.com//detail.html?entity=sOARFramework&version=2.2.0&type=solutionpack) v2.2.0 and later:
    - `AssetLevel`
    - `AssetProtocol`
    - `AssetType`
    - `AssetZone`
    - `VulnerabilityRiskStatus`

- The playbook *MITRE ATT&CK > Fetch Latest Data* from the collection **02 - Use Case - IT OT Asset Management** is now deprecated as the MITRE data can be ingested using data ingestion from the MITRE ATT&CK connector.

- The playbook **Create Alerts Record** is now deprecated

- Following playbooks are now deprecated as they are now a part of [**SOAR Framework**](https://fortisoar.contenthub.fortinet.com//detail.html?entity=sOARFramework&version=2.1.1&type=solutionpack) v2.1.1 and later:
    - **Alert - Escalate To Incident**
    - **Alert - Escalate to Incident (Link Relations)**
    - **Alert - Escalate To Incident (No Trigger)**

- The widget **MITRE** under the dashboard **Asset Risk Overview** is now deprecated as it is now a part of [**MITRE ATT&CK Enrichment Framework**](https://fortisoar.contenthub.fortinet.com//detail.html?entity=mITREATT%26CKEnrichmentFramework&version=2.2.0&type=solutionpack) v2.2.0 and later.