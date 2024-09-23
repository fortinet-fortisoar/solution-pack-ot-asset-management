| [Home](../README.md) |
| -------------------- |

# Usage

Refer to [Simulate Scenario documentation](https://github.com/fortinet-fortisoar/solution-pack-soc-simulator/blob/develop/docs/usage.md) to understand how to simulate and reset scenarios.

To understand the process FortiSOAR follows to respond to **Asset Management**, **Baseline changes over assets** and **Alerts over Assets**, we have included a scenario &mdash; `OT - Add Sample Assets`, `OT - Add Sample Alerts`, `OT - Stuxnet Attack Scenario` and `OT - Asset Change Activity` with this solution pack. 

Refer to the section `OT - Asset Management` to understand how this solution pack automation addresses your needs.

# OT- Asset Management

### Step to be followed after installing SP:

1. Ingest MITRE **Group**, **Tactics**, **Techniques**, **Sub-techniques**, **Mitigations**, **Software**, and **Mitigation** data using `MITRE ATT&CK` connector on `ICS` configuration.

> **NOTE**: On alert creation, IOCs are enriched, and the alerts are correlated with Techniques, Mitigation, and all other records for the MITRE ATT&CK Id available in the alert.

## Simulation mode

The simulation mode has some sample data that helps you get a better understanding of how the solution pack functions. Following steps help you use the solution pack with some included sample data.

1. **OT - Add Sample Assets**

    - Browse to `Simulations` > `OT - Add Sample Assets` scenario and click **Simulate Scenario**.

    - This scenario adds 86 different sample OT Assets (different Levels, Types etc.) for testing dashboards, use case playbooks, reports and other actions.<br>

2. **OT - Add Sample Alerts**

    - Browse to `Simulations` > `OT - Add Sample Alerts` scenario and click **Simulate Scenario**.

    - This scenario adds 12 well populated sample OT Alerts for testing dashboards, use case playbooks, reports and other actions.<br>

3. **OT - Stuxnet Attack Scenario**

    - Make sure the global variable **Demo mode** is set to `true`. 

    - Browse to `Simulations` > `OT - Stuxnet Attack Scenario` scenario and click **Simulate Scenario**.

    - Four Alerts get created each at an interval of 2 seconds:
        - Stuxnet peer to peer communication attempt
        - Anomalous communication between two Windows XP machines
        - Communication between public and private networks
        - STEP7 configuration download command

    - If an asset does not already exist, it is created and added to the record with the following hostname:
        - PLC S7-400-324
        - Dell - 5490-42E6
        - ThinkCentre M910s-1181
        - HP - PB7181

    - Each alert get associated with assets based on the Source and Destination IP.

    - **Group**, **Tactics**, **Technique**, **Sub-Technique**, and **Software** get linked to alert under `Correlations` tab of Alert.
    
    - **Mitigation** get correlated to alert `Recommended ATT&CK Mitigations` tab.

    - Once the alert has been enriched, open the `Stuxnet peer to peer communication attempt` alert and look for a similar alert in the Workspace `Recommendations` tab. 

    - Escalate the alert to an incident by checking `Select All` and `Include this record` then running the playbook **Escalate**. Please provide all incident details. (An incident is created with the link available in the alert's comment)

    - Incident get correlated with all the **IOCs**, **Alerts**, **Assets**, **Technique**, **Mitigation**, and **Software**.

    - Click on **Quarantine Asset and Raise Ticket** to quarantine assets and raise ticket for assets.

    - You can generate report by using **Generate Incident Summary Report**
    
    - Use the `Setup War Room` button to create a war room. All of the alerts, incidents, affected assets, and IOCs will be in the war room.
    
    - Playbooks in the War Room can be used to take action, such as `Isolate Devices From Network`, `Scan All Assets Involved`, and `Update Firewall Policy`.

4. **OT - Add Sample Asset Change Activity Record**

- Browse to `Simulations` > `OT - Add Sample Asset Change Activity Record` scenario and click **Simulate Scenario**.

    >**NOTE**: Playbook: **Scenario - OT - Asset Change Activity** has variable `dueDays` (*Days required to complete change activity*). You can populate these variables with your preferred values in the *Configuration* step.

- With a given value of due date in `dueDays` two Asset Change Activity entries are made.
    - Add New Cyber Asset - Siemens S7-400-S621
    - Medium Impact Baseline Change - Stratix 5950-RW41

- Assets are linked and can be seen in the Assets & Vulnerabilities tab.

- Once the record has been created, execute the **Add Task From Templates** to assign different tasks to different people. 

- New tasks get created as priority `Medium` once the previous task is completed.

- New task can be added by using **Add New Task** playbook.

- Once all task get completed record get closed.

- To generate the report, execute **Generate Compliance Report** and report get attached to particular record comments.