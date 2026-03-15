# All in One 
## How the Internet Works
- Every device needs an IP Address.
    - IPv4
    - IPv6 : Created because we ran out of IPv4 addresses.
      
IP Addresses are hard to remember since they are a string of numbers and letters. People use domain names instead.

## DNS Domain Name System
- AWS uses <i>Route53</i>. It converts domain names into IP addresses that computers understand.

When using the internet, such as loading a website or sending an email; everything starts with packets.

## Packets
- Data does NOT move as one big chunks, it gets broken down into small pieces called packets.
- Each packet carries the actual data, and information like:
  - Destination IP: Where it's going
  - Source IP: Where it came from

This is all handled by TCP/IP.
  - TCP: Breaks down data and make sure it <b>arrives</b> correctly.
  - IP: Makes sure the data gets to the right <b>destination</b>.

IP makes sure that it gets there while TCP makes sure that it gets there <b>complete<b>.

## AWS Networking
