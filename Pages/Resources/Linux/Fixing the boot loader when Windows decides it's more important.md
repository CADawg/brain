---
dg-publish: true
---
Today I booted into windows for the first time in months in order to use some disk cloning software, however, in the process Windows decided not to play nice with my Arch Linux boot loader and somehow made it stop appearing as an option in my bios.

I know how to fix it once I am inside Arch Linux so the main issue I faced was with getting back into Arch Linux. I tried many guides in order to boot from it from an old GRUB command line I had laying about from my other system (the GRUB GUI had it listed but it just froze).

After a while, I came across [rEFInd](https://www.rodsbooks.com/refind/), a boot loader which shows all the available EFI boot loaders, I put this on my [Ventoy](https://www.ventoy.net/en/index.html) USB (a USB that lets you boot from a selection of different ISO files that you place on it). I could see my Arch Linux GRUB EFI was still there and so I gave this a go. It showed my Arch Linux GRUB boot loader as the second option and upon hitting it I was glad to be taken to the login screen of my Arch Install.

I then reinstalled GRUB as mentioned in section 1.1 of the [GRUB Arch Wiki Page](https://wiki.archlinux.org/title/GRUB) and order was restored to the universe once again. I'd strongly recommend both these tools as it saved me a lot of hassle and meant I actually needed to know no commands, although this likely won't always work.