# Ssleepy

We got a pcap file that shows some data transferred through FTP protocol.
Looking at the FTP-Data packets, we can see a zip file being transferred.

![screenshot 345](https://user-images.githubusercontent.com/42334661/44036357-39d95f02-9f2f-11e8-8331-f7e9d053ae4d.png)

Export the bytes as .zip file. The zip contains .pem file(a key). 
Looking at the task name again, it is actually about ssl traffic.
So, we need to decrypt the SSL traffic using the private key obtained from the zip file.

Go to Edit --> Preferences --> Choose SSL in the protocols tab.

In here, select the private key, client IP, port in **"RSA key lists"**.


![screenshot 347](https://user-images.githubusercontent.com/42334661/44036999-df98f618-9f30-11e8-862a-1bd756683338.png)

After applying the key, we can see the decrypted traffic.


![screenshot 344](https://user-images.githubusercontent.com/42334661/44037261-89180986-9f31-11e8-8b51-70ad2856841c.png)

We can see the GET request of Flag.jpg. Following the **SSL Stream**, gives us the JPEG file.

![screenshot 348](https://user-images.githubusercontent.com/42334661/44037615-61bab5ea-9f32-11e8-9cce-bff9b93975fb.png)

Editing the top few lines of the jpeg in HexEditor gives the flag.
Flag : **tjctf{WIRESHARK_OR_SHARKWIRE?}**

![shark](https://user-images.githubusercontent.com/42334661/44037755-c26ec7be-9f32-11e8-852d-fa0015ace0f0.png)

### Flag can be seen before extracting the .jpg file

Following the SSL Stream of the GET /index.html, shows the flag in the title of the webpage.
It is shown as Sharkwire_or_Wireshark?(the two strings are in different positons though:P)


