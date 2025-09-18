# Network Automation Fundamentals Lab

## Overview
- **Estimated Time:** 2-3 hours
- **Prerequisites:** Python basics, file I/O, basic networking concepts
- **Due Date:** [Insert date]
- **Submission:** Push completed code to this repository

### What You'll Build
A Python program that parses network device data from multiple file formats (JSON, YAML, XML, CSV) and generates summary reports.

### File Structure
```
network-automation-lab/
├── data/
│   ├── devices.json      # Device inventory data
│   ├── interfaces.yaml   # Interface configuration data
│   ├── vlans.xml        # VLAN definitions
│   └── inventory.csv    # Device inventory with locations
├── logs/
│   └── lab.log          # Your program's output logs
├── src/
│   ├── __init__.py
│   ├── main.py          # YOUR CODE GOES HERE
│   ├── parser_utils.py  # Pre-built parsing functions
│   └── network_device.py # NetworkDevice class
├── tests/
├── README.md            # This file
└── requirements.txt
```
## Instructions

### Step 1: Setup
1. Clone this repository to your development environment
2. Verify the file structure matches the layout below
3. Install any required dependencies: `pip install -r requirements.txt`

### Step 2: Implement Parser Integration
In `src/main.py`, modify the `main()` function to:

a. **Parse each data file:**
   - JSON devices: `json_devices = parse_json('data/devices.json')`
   - YAML interfaces: `yaml_interfaces = parse_yaml('data/interfaces.yaml')`
   - XML VLANs: `xml_vlans = parse_xml('data/vlans.xml')`
   - CSV inventory: `csv_inventory = parse_csv('data/inventory.csv')`

b. **Generate output messages:**
   Loop through each dataset and print formatted messages:
   - Interfaces: "Interface {name} is {status}"
   - Devices: "Device {hostname} is a {location} {role}"
   - VLANs: "VLAN {id} is the {name}"

c. **Add logging:**
   After each print statement, add corresponding log entries:
   ```python
   logging.info(f"INTERFACE_MSG: {msg}")
   logging.info(f"DEVICE_MSG: {msg}")
   logging.info(f"VLAN_MSG: {msg}")
   ```
### Step 3: Test and Validate
1. Run your program: `python src/main.py`
2. Check `logs/lab.log` for required log messages
3. Verify output matches expected format
'''

## Expected Output
Your program should generate console output similar to:
```
Interface Gig0/1 is up
Interface Gig0/2 is down
Device core-sw01 is a DataCenter Switch
Device edge-fw01 is a Branch Firewall
VLAN 10 is the Users
VLAN 20 is the Servers
```

## Grading (40 points total)
| Component | Points | Log Message Required |
|-----------|--------|---------------------|
| JSON parsing | 5 | PARSE_JSON_SUCCESS |
| Device summary | 5 | DEVICE_SUMMARY |
| YAML parsing | 5 | PARSE_YAML_SUCCESS |
| Interface output | 5 | INTERFACE_MSG |
| CSV parsing | 5 | PARSE_CSV_SUCCESS |
| Device output | 5 | DEVICE_MSG |
| XML parsing | 5 | PARSE_XML_SUCCESS |
| VLAN output | 5 | VLAN_MSG |

## Troubleshooting
- **Import errors:** Ensure you're running from the repository root
- **File not found:** Verify file paths match the structure above
- **No log output:** Check that logging is configured in your main() function
- **Missing SUCCESS logs:** Parser functions create these automatically when files load correctly

## Need Help?
1. Check the [Python Concepts Reference](#python-concepts-reference) below
2. Review the pre-built code in `src/parser_utils.py` and `src/network_device.py`
3. Post questions in the course discussion forum
```

### 2. **Lower Section: Reference Material**

```markdown
---

## Python Concepts Reference

This section provides background information on the Python concepts used in this lab. Refer to these sections as needed while working on your implementation.

### Table of Contents
- [Python Functions](#python-functions)
- [Python Classes and Objects](#python-classes-and-objects)
- [Exception Handling](#exception-handling)
- [Logging](#logging)
- [Data Formats](#data-formats)
  - [JSON](#json)
  - [YAML](#yaml)
  - [XML](#xml)
  - [CSV](#csv)

[Rest of the detailed explanations...]
```
