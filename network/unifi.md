# A couple weeks ago, I noticed an unknown device on my network, and coincidentally 200Mbps of bandwidth being used
## Now, I currently use my ISP provided router, which has relatively limited monitoring systems and configuration options
I was very curious (and kind of a bit scared?) as to what this unknown device could be. My mind immediately went to someone having connected to my WiFi and was torrenting with it, which could get me in trouble with my ISP.

My router does have a management interface where I can monitor at currently and previously connected devices. Features are limited to which router port they're connected to (if wired), WiFi they're connected to (if wireless), device uptime, device name, MAC address and IP address. I can also assign devices static IPs and custon aliases from this interface.

I went through every connected device and figured out which was which with the people I live with. We found out the device using a lot of bandwidth was my mom's laptop; she was downloading Outer Wilds on her laptop.

But this experience stuck with me; I do not have very good control over my network. I don't know who's connected, I don't know who's talking to my servers and I don't know when new devices connect. There's also a lot of unencrypted SMB traffic on my network, and any bad actors connected could potentially see what files are being transferred.

My mind has been marinating in these fears for the past few weeks, and I've been trying to find a good (budget) networking solution. When browsing Norwegian used markets, I found a listing for both a UniFi Security Gateway (USG) and a UniFi Cloud Key for only $20, and I bought it without a second thought.
The USG is essentially just the gateway for a UniFi network; It has one WAN port and one LAN port. The LAN port is intended to be connected to a switch or similar.

Now, I have this USG and Cloud Key, and I need to migrate from my ISP-provided network to my new UniFi network, preferably with as little downtime as possible. Ideally, I would get a couple UniFi switches and maybe a UniFi U6+ for the network to be complete, but I'd like to see how I like the basic network management before I go all in. 

## Changing from ISP-provided router/AP to my own setup
Like most ISP-provided routers, the one provided to us has several jobs; routing on the local network, WiFi access point, switching, and of course connecting to the internet. If I am to replace this, I need to find new components to take over all these jobs.

#### The Switch
First things first, I dug up an old network switch from my old electronics crate. I disconnected all LAN cables from my ISP router and connected them all to my switch. Afterwards, I connected my switch to my ISP router, and the setup remained virtually the same; only noticable difference is that I only use one WAN port and one LAN port for my router.

#### The USG
The UniFi Security Gateway acts as the router and gateway for any UniFi network. As previously stated, it only has one WAN and one LAN port, which is why I moved all cables from my router to my switch. Now, all I need to do is plug the WAN and LAN cables from my ISP router to my USG

#### The AP
In the same stash I dug up the switch from, I found a Google WiFi node. After simply plugging this into the switch and doing some basic setup in the Google Home app, I have a new AP for my network.

### UniFi setup completed
After these steps, I can stop using my ISP router for monitoring my network, and I can more easily see who's connected to my network and who's using how much bandwidth. I can also add MAC whitelist/blacklist if I want to, and quarantine certain devices. VLANs are also possible now, but as I've never used them before, I am slightly intimidated by them.

## Next steps
This is a very *very* minimal UniFi network. I *only* have the USG and Cloud Key, which severely limits my monitoring and configuration options.