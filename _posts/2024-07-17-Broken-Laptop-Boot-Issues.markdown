---
layout: post
title:  "Correcting BIOS boot sequence and reformat PC"
date:   2024-07-16 21:00:00 +0200
categories: Technical Issues
---

I found an old laptop and when booting up it opened up GNU GRUB v2.02.

I couldn't access the BIOS.

I listed the available partitions and saw there was one that had a FAT filesystem.

I set the root to that partition and set boot sequence to the microsoft loader.

{% highlight bash %}
	set root=(hd1,gpt1)
	chainloader /EFI/Microsoft/Boot/bootmgfw.efi
	boot
{% endhighlight %}

Once I got Windows operational I used the OS to access the BIOS

1. Open Windows Settings:

Click on the Start menu (Windows icon) or press Win + I on your keyboard to open Settings.

2. Navigate to Recovery Options:

In the Settings window, click on "System" (the first icon in the sidebar).

3. Access Advanced Startup:

Scroll down and click on "Recovery & advanced startup" under the "Advanced startup" section.

4. Restart Now:

Under the "Advanced startup" section, click on "Restart now." This will restart your computer into the advanced startup options.

5. Choose UEFI Firmware Settings:

After restarting, you'll see a blue screen with options. Click on "Troubleshoot."

6. Access UEFI Firmware Settings:

Next, click on "Advanced options."
Click on "UEFI Firmware Settings" and then click "Restart" to access your UEFI/BIOS settings.

From here I was able to select the Microsoft bootloader as the default.