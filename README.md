# Packet Tracer Semester Project

# Developed By
- Rimsha Arif
- Arose Niazi
- Aeman Fatima
- Maryam Inam

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
        rou rip
			net 156.16.0.0
            ex
```

