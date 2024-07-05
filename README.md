# Provisioning
1. Update package
2. Install tshark and wireshark-common on main box
3. dkpg-reconfigure wireshark-common
4. Create a user `dumpcap-user`, and then add it to sudo group
5. Add vagrant user to wireshark group

# Execution
- dumpcap-user will execute `sudo dumpcap -i eth1`
- vagrant user will execute `tshark -i eth1`'
- host machine can then ping box1 private ip, and vagrant user session will detect the packets.