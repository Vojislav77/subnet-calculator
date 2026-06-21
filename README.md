**Network Admin Toolkit – Subnet Calculator**

A professional, interactive IPv4 subnet calculator built with vanilla JavaScript, HTML, and CSS.

https://screenshot.png


**Live Demo**

[View Live Demo](https://your-username.github.io/network-admin-toolkit)

**Description**

The **Network Admin Toolkit** is a browser-based subnet calculator designed for IT support, help desk, and networking professionals. It provides instant subnet calculations with visual binary breakdowns to help understand how IP addresses are structured.

**Key Features**

- **Subnet Calculator** – Enter any IPv4 address and CIDR prefix (0–32) to calculate: Network Address, Broadcast Address, Subnet Mask, Usable Host Range, Total IPs & Usable Hosts

- **Binary Visualization** – Color-coded binary representation shows network bits (teal) and host bits (gold)

- **Interactive Controls** – Slider and number input for CIDR prefix, plus quick-preset buttons

- **Export to CSV** – Download subnet data for documentation or sharing

- **Copy to Clipboard** – One-click copy for any value

- **Responsive Design** – Works on desktop, tablet, and mobile

- **No Server Required** – Pure frontend; runs entirely in your browser

**How It Works**

- The calculator uses **bitwise operations** (&, |, >>>) to compute subnet details:

- IP address is converted to a 32-bit integer

- Subnet mask is generated from the CIDR prefix using (~0 >>> (32 - prefix))

- **Network Address** = IP & Mask (bitwise AND)

- **Broadcast Address** = Network | (~Mask) (bitwise OR with inverted mask)

- Usable hosts are calculated, with special handling for /31 (RFC 3021) and /32

- The binary visualization highlights network/host bits by checking i >= (32 - prefix) for each bit position.

**Technologies Used**

- **HTML5** – Semantic markup

- **CSS3** – Custom properties, Flexbox, responsive design

- **JavaScript (ES6)** – Bitwise operations, DOM manipulation, CSV generation

- **Font Awesome** – Icons for visual polish

- **No frameworks or libraries** – 100% vanilla code

**Project Structure**

    network-admin-toolkit/
    ├── index.html          # Single-file application (HTML + CSS + JS)
    ├── README.md           # Project documentation
    ├── screenshot.png      # Project screenshot
    └── LICENSE             # MIT License (optional)

**Getting Started**

Prerequisites
    A modern web browser (Chrome, Firefox, Safari, Edge)

Installation

    Clone the repository
    
    git clone https://github.com/your-username/network-admin-toolkit.git
    
    cd network-admin-toolkit

Open the application

Double-click index.html – it will open in your default browser

Or use a local server (e.g., VS Code Live Server) for development

No build tools, no dependencies, no server required.

**Example Usage**
    
| Input | Result |
|-------|-------|
| IP: 192.168.1.100 CIDR: /24 | Network: 192.168.1.0 Broadcast: 192.168.1.255 Usable: 192.168.1.1 – 192.168.1.254 Total IPs: 256 |
| IP: 10.0.0.0 CIDR: /16 | Network: 10.0.0.0 Broadcast: 10.0.255.255 Usable: 10.0.0.1 – 10.0.255.254 Total IPs: 65,536 |
| IP: 192.168.1.100 CIDR: /30 | Network: 192.168.1.100 Broadcast: 192.168.1.103 Usable: 192.168.1.101 – 192.168.1.102 Total IPs: 4 |


**Export to CSV**

Click the **Export CSV** button in the Detailed Values card to download a .csv file containing: Property name, Dotted decimal value, and Binary representation. Perfect for network documentation or sharing with colleagues.

**Future Improvements**

- [] Dark/Light theme toggle
- [] IPV6 support
- [] Visual subnet diagram
- [] Additional export formats (JSON, PDF)
- [] Unit tests for calculation logic

**Contributing**

This is a personal portfolio project, but feedback and suggestions are always welcome! Feel free to open an issue or submit a pull request.

**License**

This project is open source and available under the [MIT License](LICENSE).

⭐ If you found this project useful, please give it a star on GitHub!
