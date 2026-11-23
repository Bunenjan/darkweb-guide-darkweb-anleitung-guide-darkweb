# Advanced Security, OpSec and Practical Tips

[← Back to overview](../../README.md)

Tor Browser protects your connection. Real anonymity, however, depends mostly on your behaviour. Here you will find typical beginner mistakes, important features like Tor bridges, and how Tor Browser compares to specialised operating systems.

## 1. Avoid typical OpSec traps

- **Do not change the window size:** Tor Browser deliberately starts with a standardised window size. Websites can recognise your device from its window or screen size (*browser fingerprinting*). Tor Browser protects against this with **letterboxing**: it adds grey margins and so hides your real window size. Still, the default size is the safest. So do not maximise the window and do not browse in full screen.
- **No VPN in addition to Tor:** The Tor Project generally advises against it, unless you are an advanced user who knows exactly how to configure both correctly. A VPN provider knows your real IP address and usually your payment details, so you only shift your trust to a company. If you want to hide that you use Tor, use **Tor bridges** (section 3).
- **Watch out for metadata in files:** Photos often contain EXIF data such as camera model or GPS coordinates; documents often contain author and editing time. The safest option is not to share your own files. Otherwise, remove the metadata first, for example with the *MAT2* program.
- **Do not carry over habits:** Never use the same username, password pattern or profile picture in Tor Browser as on the normal internet (clearnet).

## 2. Tor Browser, Tails or Whonix?

| Solution | How it works | When it makes sense |
| --- | --- | --- |
| **Tor Browser** | A normal app on Windows, macOS, Linux or Android. | For private browsing and research. It can leave traces on the main system, and malware on the device also endangers the browser. |
| **Tails** | A separate operating system that starts from a USB stick and forgets everything when shut down (*amnesic*). | If your computer is not fully trustworthy or no traces may remain on the hard drive. |
| **Whonix** | Two virtual machines (Gateway and Workstation) that force all network traffic through Tor. | For advanced users who want maximum protection against IP leaks caused by malware or software bugs. |

## 3. Get around blocks with Tor bridges

Some internet providers, public Wi-Fi networks (e.g. in hotels, schools or trains) or countries block connections to the Tor network. **Bridges** help here: Tor entry servers whose addresses are not public.

1. Open **Settings** in Tor Browser and choose **Connection** on the left.
2. Scroll to the **Bridges** section.
3. Click **Select a Built-In Bridge** and choose a type:
    - **obfs4:** disguises Tor traffic as a random data stream.
    - **Snowflake:** routes your connection through proxies run by volunteers. Good for strict blocks.
4. Confirm with **OK**. The setting is saved as soon as you close the tab.

On the very first start, you can also use **Configure Connection** in the start window.

## 4. Recognise real sites

There are no certificate authorities on the dark web like on the normal web. Scam sites copy well-known services with slightly changed .onion addresses.

- **Official sources only:** Never take .onion addresses from social media, forums or unmoderated wikis. Always go through the provider's normal website, e.g. via the ".onion available" button, or use the [Real-World Onion Sites](https://github.com/alecmuffett/real-world-onion-sites) list.
- **PGP signatures:** Some providers also publish their .onion address or important messages with a **PGP signature** (*Pretty Good Privacy*). With programs like *GnuPG* or *Kleopatra*, you can check whether a message really comes from the real operator. This is a topic for advanced users.

## 5. DuckDuckGo in Tor Browser

DuckDuckGo is the **default search engine** in Tor Browser. By default, however, it is the normal website, not the .onion version. Use the **"Onionize"** option on DuckDuckGo to switch to the .onion version.

## 6. Mini glossary

- **Clearnet:** The normal, public internet, reachable with standard browsers and search engines.
- **Deep web:** All parts of the internet that search engines do not index, e.g. online banking, email inboxes or company intranets. The deep web is **not** the same as the dark web.
- **Dark web / darknet:** A small part of the internet that can only be reached with special software such as Tor or I2P.
- **Onion routing:** Data is encrypted several times and routed through several random servers. For normal websites there are three (*guard*, *middle*, *exit*). For .onion sites the connection never leaves the Tor network, so there is no exit server.
- **Letterboxing:** Grey margins in Tor Browser that hide your real window size from websites.
- **Bridge:** A Tor entry server whose address is not public. Helps when Tor is blocked.
- **v3 onion address:** The current standard. 56 characters long, ends in `.onion`. The old, short v2 addresses no longer work.

## Sources

- [Tor Support: Protection against browser fingerprinting](https://support.torproject.org/anti-fingerprinting/)
- [Tor Support: Letterboxing](https://support.torproject.org/glossary/letterboxing)
- [Tor Support: Using Tor Browser with a VPN](https://support.torproject.org/faq/faq-5/)
- [Tor Support: What to do if Tor is blocked](https://support.torproject.org/tor-browser/circumvention/unblocking-tor/)
- [Tor Browser Manual: Bridges](https://tb-manual.torproject.org/bridges)
- [Tor Support: DuckDuckGo as default search engine](https://support.torproject.org/tbb/tbb-24/)
- [Tails](https://tails.net) · [Whonix](https://www.whonix.org)
