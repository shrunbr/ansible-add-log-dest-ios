# ansible-add-log-dest-ios
Add a logging destination to any number of Cisco IOS devices using Ansible

**Prerequisites**

 - Ansible 2.7+
 - Cisco IOS Devices
 - Privilege Level 15 access on your IOS devices

**File Customization**

You will need to customize the update_dest.yml and inventory files to use this playbook.

 - YML File
	- Enter your logging destination IP where it says "LOGGING_DEST" under "add new logging destination"
	- Enter your logging servers open port where it says "DEST_PORT" under "add new logging destination"
	- Set which hosts to target in the inventory file under "Add Logging Destination" at the top
- inventory
	- You will need to add your device hostnames or IPs under the respective category; routers or switches.

**Running the playbook**

When running the playbook you'll get asked to provide device login credentials. These need to match across all devices you're going to hit otherwise you will receive failures. We are assuming with this that you are using RADIUS/TACACS+ authentication giving yourself privilege level 15 access.

**Additional Information**

You'll find at the bottom of the playbook commented out lines. I was using these in an attempt to log before and after configs but after testing never had a need for them at that time. I kept them there but commented out, they should work as expected.
