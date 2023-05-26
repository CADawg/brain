---
dg-publish: true
---
Today I booted into windows for the first time in months in order to use some disk cloning software, however, in the process Windows decided not to play nice with my Arch Linux boot loader and somehow made it stop appearing as an option in my bios.

I know how to fix it once I am inside Arch Linux so the main issue I faced was with getting back into Arch Linux. I tried many guides in order to boot from it from an old GRUB command line I had laying about from my other system (the GRUB GUI had it listed but it just froze).

After a while, I came across [rEFInd](https://www.rodsbooks.com/refind/), a boot loader which shows all the available EFI bootloaders. I could see my Arch Linux GRUB EFI was still there and so I gave this a go. It showed my Ar