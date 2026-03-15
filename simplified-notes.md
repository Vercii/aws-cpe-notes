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

IP makes sure that it gets there while TCP makes sure that it gets there <b>complete</b>.

## AWS Networking
AWS has public and private spaces. Creating a network in AWS (aka VPC), things are divided into subnets.

You can configure these subnets to determine what can to talk to what, and what can access the internet.
- Web Server need to accept traffic from users on the internet, thus they go to the PUBLIC subnet. Users can access your website, but you also need to have extra security.
    - Public subnets have a connection to the internet through <i>Internet Gateway</i>.
- Databases should not be exposed, making PRIVATE subnets the perfect fit for them.
    - Private subnets have NO direct path to the internet. In case of updates, these subnets can be accessed through a <i>Nat Gateway</i>.
 
In order to control traffic within networks, AWS offers two tools: <b>Security Groups</b>, and <b>Network ACLs</b>.

## Security Groups
Controls traffic for individual resources, like EC2 servers.
When setting up, you need to SPECIFY EXACTLY what kind of traffic can reach that server. <br><br><b>Typical</b> configurations are:
- Web Server
  - HTTP traffic on port 80 so people can access website.
  - HTTPS on port 443 for secure connections.
  - SSH on port 22 to manage the server.
 
You may change this as you like and/or to suit what is needed for your own web server.

## Network ACLs
- Controls traffic for ENTIRE sections of your network (subnets).

Together they help build multiple layers of security.

## Example Scenario
1. Someone types the web address.
   - Route 53 converts the domain name into an IP address that computers can understand.
   - AWS S3 stores static content like images, JS and CSS files.
   - CloudFront keeps copies of your content in data centers around the world.
   - ELB distributes all incoming traffic across multiple servers.
     - <b> This is crucial because if one server gets overloaded, ELB can send the traffic to other healthy servers. </b>
     - Auto Scaling ELB can create new servers automatically when you need more capacity, and remove them when you don't. <br><br>
     
To sum it up:
- AWs S3 handles file storage. 
- CloudFront delivers content quickly. 
- AWS VPC provides network isolation.
- ELB distributes traffic.
