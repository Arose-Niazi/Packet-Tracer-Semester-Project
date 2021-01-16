# Packet Tracer Semester Project

# Developed By
- Rimsha Arif
- Arose Niazi
- Aeman Fatima
- Maryam Inam

# Important!
- Due to Spanning Tree Protocol, this project requires at between 5 minutes to 1 hour to start working perfectly. The DHCP takes a lot of time to get applied to all the devices. 
- Know Problem, Wireless devices connect to other AP's in different locations. Reason for this is that we need to maintain the structure in physical aspect of packet tracer which we don't care at the moment as it's not required. The project had very little weightage in our semester. 

## Commands Applied on Router
```
en
	conf t
		in fa 0/0
			ip ad 156.16.0.1 255.255.252.0
			no sh
		ex
			ip dhcp pool FA18-BSE-010-1	
			net 156.16.0.0 255.255.252.0
			de 156.16.0.1
			dns 156.16.3.253
        	ex
		in fa 1/0
			ip ad 156.16.4.1 255.255.252.0
			no sh
		ex
			ip dhcp pool FA18-BSE-010-2	
			net 156.16.4.0 255.255.252.0
			de 156.16.4.1
			dns 156.16.3.253
        	ex

		in fa 6/0
			ip ad 156.16.8.1 255.255.252.0
			no sh
		ex
			ip dhcp pool FA18-BSE-010-3	
			net 156.16.8.0 255.255.252.0
			de 156.16.8.1
			dns 156.16.3.253
        	ex
		in fa 7/0
			ip ad 156.16.12.1 255.255.252.0
			no sh
		ex
			ip dhcp pool FA18-BSE-010-4	
			net 156.16.12.0 255.255.252.0
			de 156.16.12.1
			dns 156.16.3.253
        	ex
		in fa 8/0
			ip ad 156.16.16.1 255.255.252.0
			no sh
		ex
			ip dhcp pool FA18-BSE-010-5	
			net 156.16.16.0 255.255.252.0
			de 156.16.16.1
			dns 156.16.3.253
        	ex
		ip dhcp excluded-address 156.16.0.1 156.16.0.10
		ip dhcp excluded-address 156.16.4.1 156.16.4.10
		ip dhcp excluded-address 156.16.8.1 156.16.8.10
		ip dhcp excluded-address 156.16.12.1 156.16.12.10
		ip dhcp excluded-address 156.16.16.1 156.16.16.10
```

## Main switch connections with Ports

### Main Switch
- C Block FA 0/1 -> FA 0/2
- H Block FA 0/1 -> FA 0/3
- Data Center FA 0/1 -> FA 0/4
- D Block FA 0/1 -> FA 0/5
- Main Server -> FA 0/6

### Main Switch 2
- B Block FA 0/2 -> FA 0/1
- Common Room Port 0 ->  FA 0/2
- Masjid Port 0 -> FA 0/3
- Girls Hostel Port 0 -> 2 FA 0/4

### Main Switch 3
- Architecture FA 0/1 -> FA 0/1
- IRCBM FA 0/1 -> FA 0/2
- Phd Block FA 0/1 -> FA 0/3
- N Block FA 0/1 -> FA 0/4

### Main Switch 4
- SSC FA 0/1 -> FA 0/1
- Cafe FA 0/1 -> FA 0/2
- O Block Port 0 -> FA 0/3
- GYM Port 0 -> FA 0/4

### Main Switch 5
- Chemical FA 0/1 -> FA 0/1
- Pharmacy FA 0/1 -> FA 0/2
- Library FA 0/1 -> FA 0/3
- K Block FA 0/1 -> FA 0/4
- A Block FA 0/1 -> FA 0/6

## Subnetting FLSM IP [156.16.0.0]
### Main Switch IP's
- Network: `156.16.0.0`
- Broadcast: `156.16.3.255`
- Range: `156.16.0.1` to `156.16.3.254`
- Subnet Mask: `255.255.252.0`

### Main Switch 2 IP's
- Network: `156.16.4.0`
- Broadcast: `156.16.7.255`
- Range: `156.16.4.1` to `156.16.7.254`
- Subnet Mask: `255.255.252.0`

### Main Switch 3 IP's
- Network: `156.16.16.0`
- Broadcast: `156.16.19.255`
- Range: `156.16.16.1` to `156.16.19.254`
- Subnet Mask: `255.255.252.0`

### Main Switch 4 IP's
- Network: `156.16.12.0`
- Broadcast: `156.16.15.255`
- Range: `156.16.12.1` to `156.16.15.254`
- Subnet Mask: `255.255.252.0`

### Main Switch 5 IP's
- Network: `156.16.8.0`
- Broadcast: `156.16.11.255`
- Range: `156.16.8.1` to `156.16.11.254`
- Subnet Mask: `255.255.252.0`

## WIFI Settings (Access Points)
- SSID: Edurem 
- Password: `12345678`

## Connection Explained
Router (Server Room C Block)
- Main Switches (Server Room C Block)
    - Department Switches
        - Floor Switches (Multi Floor Structure)
            - Access Points
                - Laptops / Mobiles
            - Lab Switches
                - Lab PC's
            - Class PC's
    - Department Switch (Single Floor Structure)
        - Access Points
            - Laptops / Mobiles
        - Lab Switches
            - Lab PC's
        - Class PC's

    - Access Points  (Just wireless netowrk)
        - Laptops / Mobiles

# Images
![Main Structure](https://github.com/Arose-Niazi/Packet-Tracer-Semester-Project/blob/main/Main.png?raw=true)
![Server Room](https://github.com/Arose-Niazi/Packet-Tracer-Semester-Project/blob/main/Server%20Room.png?raw=true)
![Department](https://github.com/Arose-Niazi/Packet-Tracer-Semester-Project/blob/main/C%20Block.png?raw=true)
![Floor](https://github.com/Arose-Niazi/Packet-Tracer-Semester-Project/blob/main/Floor.png?raw=true)
![Lab](https://github.com/Arose-Niazi/Packet-Tracer-Semester-Project/blob/main/Lab.png?raw=true)