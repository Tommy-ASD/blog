# Documenting My New Network Setup

## Background
A few weeks ago, I noticed an unknown device on my network and coincidentally observed 200 Mbps of bandwidth being used. My ISP-provided router has limited monitoring and configuration options, so I couldn’t immediately determine what was happening. After some investigation with the people I live with, I discovered that the high bandwidth usage was due to my mom downloading Outer Wilds on her laptop. While this resolved the immediate issue, it highlighted my lack of control over my network. I couldn’t identify who was connected, what traffic was being sent to my servers, or when new devices joined the network. The presence of unencrypted SMB traffic further fueled my concerns about potential bad actors accessing sensitive data.

This experience motivated me to find a better networking solution. I stumbled upon a great deal on a UniFi Security Gateway (USG) and a UniFi Cloud Key for only $20 on the Norwegian used market. I decided to purchase them and migrate to a more robust UniFi network.

## Transitioning from ISP Router/AP to My Own Setup
Like most ISP-provided routers, mine served multiple functions: local network routing, WiFi access point, switching, and internet connection. To replace it, I needed to allocate these roles to other components.

### The Switch
To start, I retrieved an old network switch from my electronics crate. I disconnected all LAN cables from my ISP router and connected them to the switch. I then connected the switch back to the ISP router. This setup maintained the network’s functionality while preparing for the new UniFi components.

### The USG
The UniFi Security Gateway became the heart of the new network, handling routing and gateway tasks. Since it has only one WAN and one LAN port, I routed all LAN cables through the switch. I then connected the WAN and LAN ports of the ISP router to the USG, enabling it to act as the primary router.

### The Access Point
I found a Google WiFi node in the same crate as the switch. I connected this to the switch and completed the basic setup using the Google Home app. This node became the new wireless access point for the network.

## Completed UniFi Setup
With these changes, I can now monitor and manage the network using the UniFi Cloud Key. This setup allows me to:
- Identify connected devices.
- Monitor bandwidth usage per device.
- Implement MAC address whitelisting/blacklisting.
- Quarantine specific devices.
- Experiment with VLANs (though I’m still learning how to use them).

## Next Steps
This is a very minimal UniFi network, consisting only of the USG and Cloud Key. While this provides a significant improvement over the ISP-provided router, there are limitations. I plan to:
1. Expand the network with UniFi switches and possibly a UniFi U6+ for more comprehensive management.
2. Learn more about VLANs and implement them to segment the network.
3. Explore advanced monitoring and configuration options through the UniFi system.

## Conclusion
Switching to a UniFi network has given me much more control over my home network and improved my confidence in its security and management. While I’m just starting with the UniFi ecosystem, the potential for future expansion and learning is exciting.


I gave GPT the blog post and asked for steps forward and it spit this out??? I am so confused rn