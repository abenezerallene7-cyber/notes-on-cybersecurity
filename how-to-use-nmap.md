# INSTALLATION
  sudo apt update && sudo apt install nmap

#  BASIC PORT SCANNING
 TCP SYN scan (default, root required)
  nmap -sS target
 TCP Connect scan (no root)
  nmap -sT target
 UDP scan
  nmap -sU target
 Top 1000 ports
  nmap --top-ports 1000 target
     
# TARGET SPECIFICATION
 Single host
  nmap 192.168.1.1
 IP range
  nmap 192.168.1.1-254
 CIDR
  nmap 192.168.1.0/24
 File of targets
  nmap -iL targets.txt
 Exclude hosts
  nmap 192.168.1.0/24 --exclude 192.168.1.1
    
 # SERVICE VERSION DETECTION
  nmap -sV target
  nmap -sV --version-intensity 9 target   # Max intensity
    
 # OS FINGERPRINTING
  nmap -O target
  nmap -O --osscan-guess target

 # AGGRESSIVE SCANNING
  nmap -A target  # it shows OS, version, script, traceroute

 # NSE SCRIPT
  Default scripts
   nmap --script=default target
  Vulnerability scripts
   nmap --script=vuln target
  Specific script
   nmap --script http-enum target

# OUTPUT FORMATS
  nmap -oN normal.txt target  
  nmap -oX xml.xml target   
  nmap -oG grepable.txt target 
  nmap -oA allformats target    

# EVASION TECHNIQUE
 Fragment packets
  nmap -f target
 MTU size
  nmap --mtu 24 target
 Decoy
  nmap -D RND:10 target
 Source IP spoof
  nmap -S 192.168.1.100 target
 Idle scan
  nmap -sI zombie_host target
 Timing templates
  nmap -T4 target  # Aggressive
  nmap --scan-delay 1s target
  
