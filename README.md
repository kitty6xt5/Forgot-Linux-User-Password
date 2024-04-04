# Forgot-Linux-User-Password ???
![Screenshot from 2024-04-04 20-16-46](https://github.com/kitty6xt5/Forgot-Linux-User-Password/assets/141032592/8b4cb1e6-889c-4fa2-89a4-754c343f78c3)
## If you forgot your Ubuntu Linux User Password and unable to get in..here is how you can reset your password by following these simple steps..
  
  
 Restart your Computer.
 
 A GNU GRUB menu will appear.

 ![ubuntu](https://github.com/kitty6xt5/Forgot-Linux-User-Password/assets/141032592/54121233-e398-47bb-8b05-279e9b0df440)
 
 Select the Ubuntu option. Do not click Enter.. just select the ubuntu option and press ``e`` on your keyboard to edit the boot parameters..
 
 Then a box will appear.Find the line that start with ``Linux``.
 
 At the end of that line we will find something like this `` ro quiet splash $vt_handoff``.

![rwedit1 1](https://github.com/kitty6xt5/Forgot-Linux-User-Password/assets/141032592/9c60613c-d345-4479-a8da-c13a94c9eedd)
 
 Remove this last line starting from ro and replace it with ``rw init=/bin/bash``.

![rwedit2](https://github.com/kitty6xt5/Forgot-Linux-User-Password/assets/141032592/6c208d91-5529-4c71-925b-b7794ac4e817)
 
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

 
