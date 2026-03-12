# File & Directory Navigation
    ls -la                          # List files with details
    ls -lh                          # Human-readable sizes
    cd /tmp                         # Change to /tmp
    cd ~                            # Home directory
    pwd                             # Print working directory
    mkdir hackdir                   # Create directory
    rm -rf /tmp/*                   # Force delete (dangerous!)
    cp file1 file2                  # Copy file
    mv old new                      # Move/rename
    find / -name "*ssh*" 2>/dev/null  # Find files
    locate ssh                      # Locate files (mlocate)
    du -sh *                        # Disk usage
    cat file.txt                    # View file
    less file.txt                   # Paginated view
    tail -f /var/log/auth.log       # Live log tail

# User & Privilege Enumeration
    whoami                          # Current user
    id                              # User/group IDs
    sudo -l                         # Sudo permissions
    groups                          # User groups
    w                               # Who is logged in
    last                            # Last logins
    lastlog                         # Last logins detailed
    cat /etc/passwd                 # User list
    cat /etc/shadow                 # Password hashes (root)
    getent passwd                   # Users (NSS)
    getent group                    # Groups
    passwd -S                       # Password status
    chage -l user                   # Password aging

# System Information
    uname -a                        # Kernel/OS info
    hostnamectl                     # System info
    cat /etc/os-release             # Distro info
    dmidecode | grep -i bios        # BIOS info
    lscpu                           # CPU details
    free -h                         # Memory usage
    df -h                           # Disk usage
    uptime                          # System uptime
    dmesg | tail                    # Kernel messages
    lsmod                           # Loaded modules
    cat /proc/version               # Kernel version
    cat /proc/cpuinfo               # CPU info

# Network Enumeration
    ifconfig || ip a                # Interfaces
    ip route                        # Routes
    netstat -tuln                   # Listening TCP/UDP
    ss -tuln                        # Modern netstat
    lsof -i                         # Open ports by process
    arp -a                          # ARP table
    route -n                        # Routing table
    ping -c 4 8.8.
