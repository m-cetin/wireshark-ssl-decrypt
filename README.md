# Guide to Decrypting SSL Traffic in Wireshark

Decrypting SSL traffic is an essential skill for security professionals and developers. Here, we'll walk you through how to decrypt SSL traffic in Wireshark using an environment variable SSLKEYLOGFILE. This method allows you to view encrypted traffic in plaintext. 

## Step 1: Install Wireshark

Make sure you have Wireshark installed on your computer. You can download and install Wireshark from the official website.

## Step 2: Create SSLKEYLOGFILE

Open Command Prompt (CMD) as an administrator. Use the following command to create an environment variable SSLKEYLOGFILE:

```
setx SSLKEYLOGFILE "C:\path\to\keylog.log"
```

Replace "C:\path\to\keylog.log" with the desired location for your keylog file. This file will store SSL keys for decryption.

## Step 3: Start Wireshark
Launch Wireshark. Go to "Edit" > "Preferences" and look for "Protocols" > "TLS". Specify the path to your SSLKEYLOGFILE you defined in step 2.

## Step 4: Record Traffic
Begin recording SSL traffic in Wireshark as you normally would.

## Step 5: Decrypt SSL Traffic
Wireshark will now decrypt SSL traffic and display the plaintext.

## Tips
Alternative Browsers: If you encounter issues with Chrome and traffic isn't captured correctly, consider using a different browser like Firefox. Sometimes, Chrome prematurely closes the TLS session, making decryption challenging.
