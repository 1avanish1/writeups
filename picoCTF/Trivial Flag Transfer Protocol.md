# Trivial Flag Transfer Protocol
 
```
GSGCQBRFAGRAPELCGBHEGENSSVPFBJRZHFGQVFTHVFRBHESYNTGENAFSRE.SVTHERBHGNJNLGBUVQRGURSYNTNAQVJVYYPURPXONPXSBEGURCYNA
```
seeing the packet transfer i found this interesting string of characters,i used the tftp filter on all transfers
this was the 2nd one that popped up under data packet.
applying an rot 13 and adding spaces:
```
TFTP DOESNT ENCRYPT OUR TRAFFIC SO WE MUST DISGUISE OUR FLAG TRANSFER. FIGURE OUT A WAY TO HIDE THE FLAG AND I WILL CHECK BACK FOR THE PLAN
```
after this i checked extract objects under tftp:
under the .deb file,i kept digging and found a file called steghide,
setganography is used for hiding data in images.
Steghide is a program that helps us with this.
i used it,along with the passphrase DUEDILIGENCE,which
was cleverly given,to get:

picoCTF{h1dd3n_1n_pLa1n_51GHT_18375919}

