# Firewall evasion

Fragment packets:

    # nmap -f <IP>

Specify a specific MTU:

    # nmap --mtu [MTU] <IP>

Use a decoy:

    # nmap -D RND:[number] <IP>

Idle zombie scan:

    # nmap -sI [zombie] <IP>

Manually specify a source port:

    # nmap --source-port [port] <IP>

Append random data:

    # nmap --data-length [size] <IP>

Randomize target scan order:

    # nmap --randomize-hosts <IP>

Spoof MAC address:

    # nmap --spoof-mac [MAC|0|vendor] <IP>

Send bad checksums:

    # nmap --badsum <IP>