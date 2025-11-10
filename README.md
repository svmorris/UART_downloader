# UART_downloader
This script downloads files from a UART connection. It can even download entire disks or partitions.


# Small warning

This is just a script that worked for my need. It might work for other applications and it might not.

All configurations have to be made inside the c file, but I've left some comments so you know what to change.



# Prerequesites

1. GCC

2. UART shell

This script works by running dd on the target device. Make sure you have a shell where dd is accessible. The script probably works if you replace dd with cat in some cases.


# Additional notes

Sometimes your shell might not support piping binary data to sdtout. If this is the case, add some sort of encoding to the data. On the router I ran this on, I could add  `| openssl base64` to the end of the command to get encoded data. This should work for other encodings depending on what you have available.
