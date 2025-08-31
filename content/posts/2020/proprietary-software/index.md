+++
title = "Proprietary Software"
date = "2020-05-16"
updated = "2025-08-31"

[taxonomies]
tags=["Open Source"]

[extra]
repo_view = true
comment = true
read_time = true
+++
![Richard Stallman would be disapointed in me...](https://sjc1.vultrobjects.com/apaxq-blog/2020/proprietary-software/disgusting.jpg)

*This was originally posted on my [old blog](https://github.com/apaxq/oldblog). You can find the original source code [here](https://github.com/apaxq/oldblog/blob/master/content/blog/proprietary-software/index.md).*

In general, I tend to favor free and open source software over proprietary software. However, there are a few instances when I do run proprietary software on my personal machines. The following is a list of proprietary software on my personal machines.

This list should not be viewed as a list of software I support, but rather a list of software that I use that is proprietary and am looking for open source alternatives. Also note that this list does not include software I use at Work since I am required to use proprietary software as part of my job duties. Also, I am not listing video games since that’s an entirely different ecosystem (also this list would get way too long).

If anyone has any better open source recommendations for the software below, please let me know (REDACTED AT REDACTED DOT net).

# Nvidia Drivers

Nvidia drivers provide hardware acceleration for users with Nvidia Cards (such as myself). The reason I still use the proprietary drivers is that they provide better graphical and video encoding/decoding performance compared to nouveau (the open source alternative).

The downside of the proprietary drivers is that it bakes itself into the kernel. You must recompile the kernel with every driver update. Also, configuring video settings requires using `nvidia-settings` (which is also proprietary).

I do not see Nvidia open-sourcing their drivers since they most likely contain proprietary information regarding how it's line of graphic cards work (which may be beneficial to competition). Nvidia drivers may also contain proprietary data from game studios to improve the performance of video games on their cards (hints why some games have Nvidia listed as the preferred graphics card to run their game).

Nvidia drivers may also contain data for proprietary video interfaces (i.e. HDMI) that cannot be open-sourced. Finally, and probably the most likely case, Nvidia drivers may have lots of spaghetti code that they don't want the public to see.

With all that said, I hope the nouveau project continues to get better so that we no longer have to put up with Nvidia’s antics.

# MakeMKV

MakeMKV allows you to rip UHD/Blu-ray/DVD disk files into mkv files. As far as I am aware, makeMKV is the only application that allows you to rip encrypted Blu-ray videos and put them in MKV container files for """free""". I say """free""" since makeMKV is technically shareware, and you’ll need a license key to use the software.

However, makeMKV is free during the """BETA""", once the so-called BETA is over, you will need to buy a license in order to continue using it. The beta key only last for a month, so you will need to reactivate every month (which is annoying). This software has been in beta since 2008. I am not expecting it to exit beta anytime soon, but when it does, I'll be shit out of luck.

I have had people recommend HandBreak to me in the past. I have two issues with HandBreak. First, Handbreak is an encoding software, which means when you rip a disk, you are not getting an exact copy of the mpeg stream from the disk, you are getting an encoded stream of that stream. makeMKV on the other hand, simply decrypts the mpeg file, and puts it into an mkv file. Second, as far as I am aware, Handbreak does not support ripping encrypted Blu-rays currently. It can rip encrypted DVDs (using libdvdcss).

I do not see Mike (the guy who makes makeMKV) open-sourcing this code anytime soon for a few reasons. For one, MakeMKV may be taking advantage of an exploit in Blu-ray software. If this code gets released, the Blu-ray association may simply patch the bug, and prevent ripping of Blu-ray’s after that point. Also, makeMKV is shareware, and Mike fully intends to take the software out of BETA eventually.

My hope is that someone in the open source community figures out how to bypass the DRM in Blu-ray’s so that I can start manually stripping the mpeg file using ffmpeg.

# Ripcorde

Ripcord is a lightweight desktop chat client for group-centric services like Slack and Discord built upon the Qt toolkit. I mostly use it for connecting to Discord on machines that do not have PulseAudio installed (since the official client only supports PulseAudio).

One of the nice things about it is that more lightweight and uses less ram compared to the official Discord client. Also, as far as I am aware, this is the only third-party Discord client that supports voice calls. You can also view deleted posts and have separate windows for voice chat.

There are a few issues with Ripcord. For one, support for push to talk is kind of broken (this may just be an issue on my machine, but I have not been able to get the application to notice my keypresses when I’m trying to turn on my mic. Also, [no video support coming anytime soon](https://dev.cancel.fm/tktview?name=a60cedc90a) in keeping with the minimalistic approach (not a huge issue, though would be nice to have a pipe feature to view someone’s stream with mpv).

But the biggest issue with Ripcord is that it is considered a third-party client. Discord (the service) has been very hostile towards both developers and users of third-party clients, even going as far as banning users who use third-party clients. I personally have not been banned from Discord yet for using third-party clients. But if I do, mark my words, that will be the last time I ever use Discord.

I do not see Ripcord being open-sourced any time soon. [The author has no intentions on doing so currently](https://dev.cancel.fm/tktview?name=71f8ccfa7b). My hope is that someone will write a third-party client that also supports voice as well soon.

# Exact Audio Copy

Exact Audio Copy is an application that rips audio from CDs with a focus on accuracy. When you rip a CD, if it finds an error, it will attempt to fix that error before proceeding to the next part. If there are any errors that cannot be corrected, it will tell you on which time position the (possible) error occurred. This is useful for reading CDs that have been scratched or damaged. It is free for non-commercial purposes.

Only big issue is that it only works in Windows (though I have been told it works fine in WINE). As for why it is not open sourced is beyond me. My hope is that someone writes a CD ripper that also focuses and accuracy as well.

*Again, if anyone has any good recommendations, please reach out to me (REDACTED AT REDACTED DOT net)*