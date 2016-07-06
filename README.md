# Overlay Snap

Snaps are squashfs images, which by definition are read-only. This can make them
difficult to debug, since they cannot be edited. That's where this snap comes
in. Run the following command:

    $ /snap/overlay/current/overlay /snap/<name>/<version>

Now the snap can be edited! This is done via overlayfs, and it's temporary. One
can undo it by rebooting, or by simply unmounting the overlay:

    $ sudo umount /snap/<name>/<version>
