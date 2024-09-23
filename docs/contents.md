| [Home](../README.md) |
| -------------------- |

# Contents

The **OT - Asset Management** solution pack contains the following resources.

## Connectors

| Name                | Version        | Description                                                                                                                                                                                                                                                |
| :------------------ | :------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CSV Data Management | 1.2.0 or later | CSV Data management can perform different operations on CSV files like reading files, performing deduplication, merging two CSV files, joining two CSV files, concatenation of two CSV files, and returning a well-formatted dataset                       |
| Fortinet FortiEDR   | 1.3.0 or later | FortiEDR protects endpoints pre and post-infection, stopping data breaches in real-time and automatically orchestrating incident investigation and response. This connector facilitates automated operations related to events, forensics, and collectors. |
| Fortinet FortiGate  | 5.2.1 or later | Fortinet FortiGate enterprise firewall provides high performance, consolidated advanced security, and granular visibility for broad protection across the entire digital attack surface.                                                                   |
| ServiceNow          | 3.2.0 or later | ServiceNow connector provides functionality to create, read, update, and delete records of Table and Catalog type                                                                                                                                          |
| Qualys              | 1.0.1 or later | Qualys provides cloud security, compliance, and protection of IT assets and web applications. This connector facilitates automated operations for vulnerability management, policy compliance, and asset management.                                       |

## Widgets

| Name                | Description                                                                                                                                                                                                                                                                                                         |
| :------------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Record Distribution | Ability to visualize items/records and their correlations in different levels based on a given grouping context. A very good example of the widget's utility is the OT view, where assets are visualized across different Purdue Levels and highlight any existing relations with other assets at different levels. |
 
## Roles

| Name                       | Description                                                                                                                         |
|:---------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| Full App Permissions       | *Create*, *Read*, *Update*, and *Delete* permission for module **Asset Resources** and **Asset Change Activity**                    |
| SOC Manager <sup>New</sup> | *Create*, *Read*, *Update*, and *Delete* permission for module **Asset Resources** and **Asset Change Activity**                    |
| SOC Analyst <sup>New</sup> | *Read* permission for module **Asset Resources**; *Create*, *Read*, and *Update* permission for module **Asset Change Activity**    |

## Dashboards

| Name                           | Description                                                                                                                |
| :----------------------------- | :------------------------------------------------------------------------------------------------------------------------- |
| Asset Change Activity Tracking | Track the activity over asset change                                                                                       |
| Asset Overview                 | This dashboard displays Assets By Level, By Zone, By Vendor By Category, By Level By State, By Type, By Vendor, By MEF Tag |
| Asset Risk Overview            | Displays the alerts over assets By Zone, By Criticality, and Recent Alerts                                                 |

## Reports

| Name                                 | Description                                   |
| :----------------------------------- | :-------------------------------------------- |
| Asset Change Activity Summary Report | Provide the report over asset change activity |

## System View

| Name                        |
| :-------------------------- |
| Navigation Menu - Resources |

## Module Schemas

| Name                  | Description                                                                     |
|:----------------------|:--------------------------------------------------------------------------------|
| Asset                 | A new field `Asset Icon` under the **Asset Resources** module of type *Lookup*. |
| Asset Resources       | A Module that contains the icons of assets                                      |
| Asset Change Activity | A module that monitors asset changes on various baselines.                      |

## Scenario Record Set

| Name                                | Description                                                                                                                                                                                                                                              |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| OT - Add Sample Assets              | Generates 87 IT/OT assets as per the Purdue model based on various criticality levels, types, and other asset categorizations as sample data.                                                                                                            |
| OT - Add Sample Alerts              | Generates 12 well-populated alerts associated with assets, generated in the *OT - Add Sample Assets* scenario, as sample data.                                                                                                                           |
| OT - Stuxnet Attack Scenario        | Demonstrates the *Stuxnet Incident* to observe how FortiSOAR&trade; behaves when encountering a real cyber attack. Although Stuxnet is a dated piece of malware, it represents the complexity of real targeted attacks and is infamous for many reasons. |
| OT - Asset Change Activity Scenario | Demonstrates the process of conducting an *Asset Change Activity* for an asset. The sample Asset Change Activity records have a tag, `Sample`, for easy identification.                                                                                  |

## Asset Resources Record Set

| Name                      | Description                        |
|:--------------------------|:-----------------------------------|
| PLC                       | PLC icon                           |
| WorkStation               | WorkStation icon                   |
| Laptop, Desktop, Endpoint | Laptop, Desktop, and Endpoint icon |
| Switch                    | Switch icon                        |
| Server                    | Server icon                        |
| Network                   | Network icon                       |
| Router                    | Router icon                        |
| HMI                       | HMI icon                           |
| Firewall                  | Firewall icon                      |
| Storage<sup>New<sup>      | Storage icon                       |
| VOIP Phone<sup>New<sup>   | VOIP Phone icon                    |
| Gateway<sup>New<sup>      | Gateway icon                       |
| Controller<sup>New<sup>   | Controller icon                    |
| Historian<sup>New<sup>    | Historian icon                     |
| Printer<sup>New<sup>      | Printer icon                       |

## Picklist

| Name            | Description                                |
| :-------------- | :----------------------------------------- |
| ActivityStatus  | Contains the Asset Change Activity status. |
| AssetChangeType | Contains the Asset Change Activity type.   |
| AssetCategory   | Contains the OT-related asset values.      |

## Playbook Collection

| 02 - Use Case - Asset Change Activity |
|:--------------------------------------|

| Playbook Name                         | Description                                                                                        |
| :------------------------------------ | :------------------------------------------------------------------------------------------------- |
| Scenario - OT - Asset Change Activity | Generate an Asset Change Activity record for type Add New Asset and Medium Impact Baseline Change. |
| Medium Impact Baseline Change         | Baseline Change Workflow for Medium Impact Cyber Assets                                            |
| High Impact Baseline Change           | Baseline Change Workflow for High Impact Cyber Assets                                              |
| Add Cyber Asset                       | Baseline Change Workflow for Add Cyber Asset                                                       |
| Remove Cyber Asset                    | Baseline Change Workflow for Remove Cyber Asset                                                    |
| Replace Cyber Asset                   | Baseline Change Workflow for Replace Cyber Assets                                                  |
| Modify Cyber Asset                    | Baseline Change Workflow for Modify Cyber Asset                                                    |
| Add New Task                          | New task for Asset Change Activity                                                                 |
| Manage Asset Change Activity Closure  | Update the *Closed On* field with the current date and time if the status is Closed.               |
| Generate Asset Change Summary Report  | Generate report by manual trigger in FortiSOAR                                                     |
| Generate Report                       | Generates Report and Link to Incidents                                                             |

| 02 - Use Case - IT OT Asset Management |
|:---------------------------------------|

| Playbook Name                           | Description                                                                                     |
|:----------------------------------------|:------------------------------------------------------------------------------------------------|
| Set Asset Icon<sup>New<sup>             | Correlates asset with Icon (If found in Asset Resources) as per their category.                 |
| Scenario - OT - Create Assets Record    | Playbook reads a CSV file and creates Assets records.                                           |
| > Create Assets Record                  | This will generate an Alert record.                                                             |
| Tag as Most Essential Function (MEF)    | Playbook tags asset as Most Essential Function(MEF)                                             |
| Scenario - OT - Create Alerts Record    | Playbook reads CSV file and creates Alerts records.                                             |
| Scenario - OT - Stuxnet Attack Scenario | Generate Alert for Stuxnet worm that targets Siemens S7 PLCs connected to Engineering Stations. |
| Links Assets To Alert                   | Playbook correlates Assets on the basis of Source and Destination IP found in Alert.            |
| Find Assets Related To Alert            | Finds the asset based on the IP address provided.                                               |
| Quarantine Asset and Raise Ticket       | Playbook quarantine assets in FortiEDR and raise ticket in Service Now.                         |
| Isolate and Comment Assets              | Playbook update the assets as Isolate and add a comment.                                        |
| Update Firewall Policy                  | Update Firewall Policies To Restrict Communications.                                            |
| Scan All Assets Involved                | Initiate a quick scan of all assets related to the incident.                                    |
| Isolate Devices From Network            | Isolate Selected Devices From Network Based On Criticality and Risk.                            |

>**Warning:** We recommend that you clone these playbooks before customizing to avoid loss of information while upgrading the solution pack.

| [Installation](./setup.md#installation) | [Configuration](./setup.md#configuration) | [Usage](./usage.md) |
|-----------------------------------------|-------------------------------------------|---------------------|