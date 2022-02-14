# S71200_TCP/IP Communication
PLC S71200 time counter with TCP/IP communication TIA14 between PLC and 1 computer

## PLC S7 1200 CPU 1215C
#### TIA Potal 14 => If you have a TIA Portal 15/15.1/16 you can update for your version

In this software its possible send 2 bytes and receive 8 bytes in ASCII

### To config

#### STEP 1

In device configuration/General/PROFINET Interface [X1]/Ethernet address you can
can config the PLC IP Address

![image](https://user-images.githubusercontent.com/55773189/153865593-5ad67f97-5407-4222-9910-826cc9b320db.png)


### STEP 2

In Program block/TCP_COMMS[FB1]/Configuration/Connection parameter config the second machine IP

![image](https://user-images.githubusercontent.com/55773189/153865859-112fe07b-c096-4be6-8b89-facd274556aa.png)

### STEP 3

If you change the bytes quantity to send and/or receive alter the DATA[DB6] Array size

![image](https://user-images.githubusercontent.com/55773189/153867516-8c83cab3-131f-4099-8a55-6ce0b4b42d06.png)

##### STEP 4

Compile -> Hardware(compile all)
Compile -> Software (Software All)
Download to device Hardware configuration
Download to device Software(all)

### Step 5

Use Hercules SETUP utility by HW-group.com to test communication

![image](https://user-images.githubusercontent.com/55773189/153869262-3c540805-9e67-4238-9724-354d9a7c9fee.png)

### Step 6

When DATA.Receive[0]->%DB6.DBB0 = 1 counter enable <br />
When DATA.Receive[0]->%DB6.DBB0 = 0 counter disable <br />
When DATA.Receive[0]->%DB6.DBB0 = R reset counter <br />

InverterAssy = 0 Counter is start <br />
InverterAssy = 1 Counter stop <br />

![image](https://user-images.githubusercontent.com/55773189/153869668-05a035ee-c89d-4ca8-9bdf-747733c6571d.png)

### TIP => Always you change some IP configuration, make a Download "Hardware configuration" and "Software configuration"

## ENJOY!!
