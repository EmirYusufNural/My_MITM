# My_MITM
#Legal warning!! I will not accept responsibility for illegal uses.
#ARP Poisoning Tool
This is a Python script that performs ARP poisoning attacks on a local network. It takes the target IP and the gateway IP as user inputs and sends spoofed ARP packets to both devices, making them believe that they are communicating with each other through the attacker’s machine. This allows the attacker to intercept and modify the traffic between them.

Requirements
To run this script, you need to have Python 3 installed on your system. You also need to install the scapy library using pip:

pip install scapy

You also need to enable IP forwarding on your system to forward the packets between the target and the gateway. On Linux, you can do this by typing:

echo 1 > /proc/sys/net/ipv4/ip_forward

Usage
To run the script, open a terminal and navigate to the folder where you saved the file. Then type:

python arp_poisoning.py -t target_ip -g gateway_ip

You will need to replace target_ip and gateway_ip with the actual IP addresses of the devices you want to attack. For example:

python arp_poisoning.py -t 192.168.1.10 -g 192.168.1.1

The script will then start sending spoofed ARP packets to both devices every 3 seconds and display the number of packets sent on the screen. For example:

Sending packets 20

To stop the script, press Ctrl+C. The script will then send reset ARP packets to both devices to restore their original ARP tables.

Improvements
There are some possible ways to improve this script, such as:

Adding error handling for invalid IP addresses or network issues
Adding a feature to sniff and analyze the intercepted traffic using scapy or other libraries
Adding a feature to modify or inject packets into the traffic using scapy or other libraries
Adding a feature to perform ARP poisoning on multiple targets or the whole network
Adding a feature to perform ARP poisoning in stealth mode by sending gratuitous ARP packets instead of replies
