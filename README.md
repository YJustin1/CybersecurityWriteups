# Backdoor
### Category: Forensics / Networking
### Difficulty: Easy
### @YJustin1

You notice that the only item provided to you is a network capture. Opening the pcap with Wireshark (or similar) reveals a large amount of seemingly ordinary network traffic. However, by parsing through the network traffic by type reveals HTTP packets, indicating that someone was communicating with a website of some sort. Analyzing the GET packets reveals a URL. Opening the website directs you to a login page.

Your first instinct is to return to the PCAP in search of credentials. While you fortunately find the POST packet to the login form, you unfortunately notice that the credentials are corrupted/encrypted and not in plaintext. HOwever, you notice that one of the form members is an item titled "set_has_logged_in". 

Subsequently, you return to the login in page. Working with develop tools, you noticed that there is a cookie with the "set_has_logged_in" parameter. You modify the value to true and refresh the page.

Now able to access the website, you are granted access to an informational panel. There, you are given your flag: utflag{one_does_not_simply_log_in}
