### Phase 1 - Summary Report

### 1: Tasks Done
- Introduction to Network Security Monitoring
- Setting Up the Environment
- Packet Capture with Wireshark


### 2: Challenges
- I had issues seting up localized network permissble to my VMs where each VM can talk to the other on same network. This was due to lack of knowledge on how to set it up. I had to do my research on how to setup VMs on same network where i got a website where i can select prepared Vulnerable VMs - https://www.vulnhub.com. I also leveraged on Youtube videos (https://www.youtube.com/watch?v=Gcw2MX44REI) to understand some setup especially around DHCP configuration of th VirtualBox.
- While trying to monitor packets, I was not sure what network was being monitored. I had to drill down to understand which network is being used and why. It led me to do more research on different network configurations. I came to uderstand the different usecases for netwrok adapters:
1. NAT: Provides internet access to the VM via the host's network. here, the VM can communicate with external networks but cannot directly see traffic originating from the host (e.g., macOS browser traffic). Packets from the host machine (in my case my physical PC) will not be captured in this setup.

2. Internal Network: Allows communication between multiple VMs on the same internal network. The internal network is isolated from the host's network. Thus, traffic from the host machine (in my case my physical PC) will not be visible here as well.

3. Bridged Adapter: Connects the VM directly to the same network as the host (e.g., your Wi-Fi network). The VM acts as if it is another device on the same physical network as the host. So, the VM (in this case, my kali machine) can capture traffic originating from the host machine (in my case my physical PC) (e.g., browser traffic) if the traffic passes through the shared network.

### 3: Improvements