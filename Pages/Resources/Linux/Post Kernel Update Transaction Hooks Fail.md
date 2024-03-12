---
dg-publish: true
---

In Manjaro, if transaction hooks fail and you have to cancel the update process, run
`sudo mkinitcpio -P` to rerun all the post transaction hooks for a kernel update.