# Ssleepy

We got a pcap file that shows some data transferred through FTP protocol.
Looking at the FTP-Data packets, we can see a zip file being transferred.

![screenshot 345](https://user-images.githubusercontent.com/42334661/44036357-39d95f02-9f2f-11e8-8331-f7e9d053ae4d.png)

Export the bytes as .zip file. The zip contains .pem file(a key). Looking at the task name again, it is actually about ssl traffic.
So, we need to decrypt the SSL traffic using the private key obtained from the zip file.

Edit->Preferences->Choose SSL from the protocols tab
In here, select the private key, client IP, port in RSA key lists.

