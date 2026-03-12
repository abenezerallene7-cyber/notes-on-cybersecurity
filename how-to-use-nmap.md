# INSTALLATION
  sudo apt update && sudo apt install nmap

#  BASIC PORT SCANNING
  nmap -sS target # TCP SYN scan (default, root required)
  nmap -sT target # TCP Connect scan (no root)
  nmap -sU target # UDP scan
  nmap --top-ports 1000 target  # Top 1000 ports
     
# TARGET SPECIFICATION
 
  nmap 192.168.1.1 # Single host
  nmap 192.168.1.1-254  # IP range
  nmap 192.168.1.0/24  # CIDR
  nmap -iL targets.txt  #File of targets
  nmap 192.168.1.0/24 --exclude 192.168.1.1  #Exclude hosts
    
 # SERVICE VERSION DETECTION
  nmap -sV target # Service version detection
  nmap -sV --version-intensity 9 target   # Max intensity
    
 # OS FINGERPRINTING
  nmap -O target # OS fingerprinting
  nmap -O --osscan-guess target  # OS fingerprinting with guess


 # AGGRESSIVE SCANNING
  nmap -A target  # it shows OS, version, script, traceroute

 # NSE SCRIPT
   nmap --script=default target  # Default scripts
   nmap --script=vuln target  # Vulnerability scripts
   nmap --script http-enum target # Specific script

 # OUTPUT FORMATS
   nmap -oN normal.txt 192.168.1.1     # Human-readable output
   nmap -oX xml.xml 192.168.1.1        # XML output
   nmap -oG grepable.txt 192.168.1.1   # Grepable output
   nmap -oA allformats 192.168.1.1     # All output formats
  
