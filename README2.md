# Network Automation Fundamentals Lab

## Quick Start
- **Estimated Time:** 2-3 hours
- **Prerequisites:** Python basics, file I/O, basic networking concepts
- **Due Date:** [Insert date]
- **Submission:** Push completed code to this repository

## What You'll Build
A Python program that parses network device data from multiple file formats (JSON, YAML, XML, CSV) and generates summary reports.

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
