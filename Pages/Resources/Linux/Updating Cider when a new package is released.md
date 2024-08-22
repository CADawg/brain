---
dg-publish: true
---

Since Cider performs it's own internal updates, the file state is not always what pacman expects. Thus, you need to run the following command (where Cider-git-arch-x64.pacman) is the name of the .tar.gz or .pacman archive. Overwrite just allows it to overwrite the files in inconsistent state.

`sudo pacman -U ./Cider-git-arch-x64.pacman --overwrite \*`