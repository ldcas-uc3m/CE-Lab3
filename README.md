# Lab 3: Traffic Analysis
By Luis Daniel Casais Mezquida  
Cybersecurity Engineering 22/23  
Bachelor's Degree in Computer Science and Engineering, grp. 89  
Universidad Carlos III de Madrid

## Project statement
The goal of this lab is to learn to identify network behaviors in a trace using a network traffic analysis tool. To do the lab, you will need a machine with a root account that you control and the [Wireshark](https://www.wireshark.org/) tool installed.

1. Packet trace [`a.pcap`](data/a.pcap)
    1. What is the most prevalent application protocol in the trace?
    2. What are the IP addresses and ports of the client and the server?
    3. Which server (type and version) is running?
    4. Write a filter to display the first TCP packet sent in each flow in the trace.
    5. Looking at the whole trace, what is the client trying to achieve?
2. Packet trace [`b.pcapng`](b.pcapng)
    1. How many TCP and UDP conversations are contained in the trace, and how many hosts are involved?
    2. Looking at the whole trace, what is the host `192.168.5.51` doing?
    3. Enumerate all different techniques that `192.168.5.51` is using.
    4. Which ports are open at `192.168.5.20`?
3. Packet trace [`c.pcap.ng`](c.pcapng)
    1. Write a filter to display all HTTP conversations in the packet trace.
    2. What is the server and the user agent?
    3. Get all the passwords (in plaintext) of the HTTP Authorization headers contained in the trace.


## Installation and execution

First install Wireshark, through your preferred package manager.  
For example, APT:
```bash
sudo apt install wireshark
```

In order to open each file (found in [`data/`](data/)), use:
```bash
wireshark data/<file>
```
E.g.:
```bash
wireshark data/a.pcap
```

You can find the results of the analysis in the report ([`report/parts/1-main.tex`](report/parts/1-main.tex)).  
You can compile the report (make sure `texlive` is installed) with:
```bash
pdflatex report/report.tex
```

## Useful links
- [Wireshark display filters](https://wiki.wireshark.org/DisplayFilters)
- [Wireshark capture filters](https://wiki.wireshark.org/CaptureFilters)
- [Wireshark filter man page](https://www.wireshark.org/docs/man-pages/wireshark-filter.html)

