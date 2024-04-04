# Forgot-Linux-User-Password ???
## If you forgot your Ubuntu Linux User Password and unable to get in..here is how you can reset your password by following these simple steps..
  
  
 Restart your Computer.
 
 A GNU GRUB menu will appear.
 
 Select the Ubuntu option. Do not click Enter.. just select the ubuntu option and press ``e`` on your keyboard to edit the boot parameters..
 
 Then a box will appear.Find the line that start with ``Linux``.
 
 At the end of that line we will find something like this `` ro quiet splash $vt_handoff``.
 
 Remove this last line starting from ro and replace it with ``rw init=/bin/bash``.
 
 After writing this command press `ctrl+x` or `f10` to boot with the modified parameters.

 This will boot you into a root shell prompt without requiring a password.

 If you want to see the partition type  ``mount | grep -w /``

 Now you can reset the password for any user account using the `passwd` command..

 ``passwd kitty``

 Replace `kitty` with the actual username for which you want to reset the password of your ubuntu user.

 After resetting the password, remount the filesystem as read-write..

 ``mount -o remount,rw /``

 Type `` sync `` to flush any pending write to disk..

 we will reboot our system..

 ``reboot -f ``

 you should now be able to log in with the new password for the specified user account. :)

 
