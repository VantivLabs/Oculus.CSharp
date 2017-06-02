# Oculus.CSharp

# Overview

This repository provides information about the Oculus Rift specifically for those that are going to accept the Vantiv API challenge at Money20/20.  There will be some interesting challenges, but we believe there is no reward without challenge.  This repository will jumpstart your development.


The first ten teams that are interested in accepting this specific hardware challenge will receive the Oculus Rift DK2 kit: https://www.oculus.com/en-us/dk2/.  The Oculus Rift has prerequisites that you need to be aware of, but we believe that participating in this challenge has a huge upside.  There is a statistic that about 170,000 Oculus Rift dev kits have been sold as of June 2015 (http://www.roadtovr.com/oculus-reveals-175000-rift-development-kits-sold/).  That number obviously does not include other VR manufacturers, but you can bet that if you accept this challenge you will become a VR leader.  It really is a great time to be a geek!

You will hear two different stories about this device.  One is from a complete newbie (Dan) and one is from a total pro (Paul).  Dan has not touched a video game in about 15 years after being addicted to the original Halo.  Paul on the other hand, is still going strong in the world of gaming after many years (check him out here:  http://www.vantivintegratedpayments.com/blogpost/friday-geekout-gaming-industry/).  Dan's work computer is about five or six years old and has one small 25" monitor.  Paul's computer is the latest and greatest with 500 27" monitors and one giant 50" monitor attached.

Working with the Oculus Rift was an eye opening experience.  Hopefully the following story will provide answers to some of the issues you will face with this challenge.  They are easy to overcome, but not necessarily easy to solve on the day of the hackathon.  So beware....if you want to accept this challenge you will likely need to start now and also be prepared to ship some equipment in advance.

# Unboxing the Rift DK2

Here's the initial packaging and contents after opening:

![Oculus.CSharp](https://github.com/vantivlabs/Oculus.CSharp/blob/master/images/oculusinabox.JPG)

The simple box within a box:

![Oculus.CSharp](https://github.com/vantivlabs/Oculus.CSharp/blob/master/images/dk2boxsimple.JPG)

Let's see what's inside...looks interesting and fairly simple…

![Oculus.CSharp](https://github.com/vantivlabs/Oculus.CSharp/blob/master/images/initialboxopening.JPG)

Unpacking the box...not quite as simple as originally expected;

![Oculus.CSharp](https://github.com/vantivlabs/Oculus.CSharp/blob/master/images/unpackingthebox.JPG)

Lots of cables!

![Oculus.CSharp](https://github.com/vantivlabs/Oculus.CSharp/blob/master/images/lotsofcables.JPG)

# Prereqs

If you want to be a true hacker there are likely many different setups/configs, but with the limited amount of time you will have during the hackathon our guess is that you will want to hit the ground running.

Here's a link to the Oculus site that lists the requirements:  https://support.oculus.com/hc/en-us/articles/201955653-Minimum-requirements-for-the-Oculus-Rift-Development-Kit-2.

What we found is that a GeForce GTX 970, a 500 watt power supply, i5 processor, 8GB RAM, and Windows 10 allowed for an easy setup.  Feel free to hunt around for other setups that might work--we realize it will be difficult to get this type of system to the hackathon, but it is a known quantity.

We plan to bring at least one system with us that we can provide demos on but you will not be able to use this system for your personal use during the hackathon.

It would be a beautiful thing if the Oculus Rift worked on laptops, and indeed the Oculus site says it is possible:  https://support.oculus.com/hc/en-us/articles/203002766-Can-my-Oculus-Rift-Development-Kit-2-run-on-a-laptop-, but it might be a challenge and we want you setup and hacking quickly--not trying to troubleshoot setup issues all day (unless that is your interest).


# Setup

Now that we're through with the prereqs let’s discuss the setup process.  This is where we get into the tale of two hackers.

## Dan

My story is going to be a little more in-depth than Paul's. I never knew what kind of power supply I had in my computer and did not even really understand what a power supply did other than turn on when I pushed the button. It turns out that my trusty computer which I have developed on for five years only has a 250 watt power supply and no extra slots for a graphics card.  Who knew?  After trying to come up with a plan to spend the absolute minimum dollars on this process, I decided to bite the bullet and buy a new computer.  There are not many places to purchase a computer where I live, and I needed one quickly so Best Buy won.  The computer even came with an NVIDIA GT 720 which, as you already read, was enough to meet the prereqs, and a 250 watt power supply.  Oddly enough no one at Best Buy was able to tell me what power supply was in the computer before purchasing, but they did say, "sure, it will be easy to install the GTX 970 and a different power supply."  Famous last words.  Coincidentally, I had just looked up the GT 720 and it said it needs a 300 watt power supply. Those of you that are more technically inclined please chime in on what that might mean.  It makes no difference because I went big and purchased the GTX 970 and an 850 watt power supply (thinking at some point in the future, quite stupidly, that I might want two graphics cards to do some GPU cryptocurrency mining for fun.  Do not question my math skills as I was convinced that 500 + 500 was around 850).

After filling the back of an SUV with computer equipment I made it home and started unboxing.  The computer setup was fairly easy, then I upgraded to Windows 10, plugged in all of the Oculus Rift cables, setup the positional tracker, and crossed my fingers.  It didn't work at all. I kept seeing an error that I do not recall at this point but eventually discovered that I needed the latest NVIDIA drivers for Windows 10. I downloaded those and magically, everything started. I clicked on the demo scene button and right away I was addicted.  I will not ruin it for everyone by describing the experience but I was certainly impressed.  And I was only using the GT 720!

Here's the GT 720 after removing it.  I thought it looked pretty cool until I compared to the GTX 970.

![Oculus.CSharp](https://github.com/vantivlabs/Oculus.CSharp/blob/master/images/oldcard.JPG)

Next up was installing the GTX 970.  I was in complete shock when I opened the box.  This graphics card is huge and I went  down a minor rabbit hole while trying to decipher exactly what a graphics card means.  CUDA cores, texture units, memory, etc.  Fascinating...it's like I was in a whole new world.  This graphics card was almost double the length of the 720 and that presented some challenges on how to stuff it into the case.  It's so long that while it's in the case it's impossible to open the onboard memory slots.  Not a huge deal, but it was another issue that I would run into later.

![Oculus.CSharp](https://github.com/vantivlabs/Oculus.CSharp/blob/master/images/oldvsnew.JPG)

Finally with the card in place, it was time to install the new power supply.  The new power supply was a little longer than the pre-installed power supply which caused some issues, and I had to reroute cables to make things fit.  After removing almost everything from the case (even the new graphics card) I managed to install the power supply and attach all the power cables....except for one.  I'm not sure what it is called, but the cabling from the new power supply had an "8 pin connector" and the motherboard expected a 4 pin connector.  I was almost ready to give up but after some googling I found it is possible to "break" the 8 pin connector to create two 4 pin connectors.  I'm a little embarrassed to admit I had no clue about the power connector thingy but by now you get it...I am hardware challenged...but I did it!

![Oculus.CSharp](https://github.com/vantivlabs/Oculus.CSharp/blob/master/images/finallycomplete.JPG)

And now for the final test...it actually worked!  Everything powered up as expected and the GTX 970 glowed a most magnificent green!

![Oculus.CSharp](https://github.com/vantivlabs/Oculus.CSharp/blob/master/images/powerworks.JPG)

I plugged everything in again, watched some additional demos, and now I'm a VR addict with a cool new computer I "built" myself.  I know I didn't actually bake the silicon in the chips, but I did feel fairly good about myself.


## Paul

Unboxing the Oculus Rift was a dream come true for me. I found out I was dreaming about the wrong things though. Apparently when they say to get the latest video drivers, they mean the drivers from this morning. I had the latest video driver for my shiny new EVGA GTX 970, which is the recommended video card. After I hooked up everything, I downloaded the Oculus runtime .7 beta and ran the configuration app. It told me that there was no HMD connected. The Oculus was connected and it had a light on, so I wasn’t sure what to do; there were no bangs in device manager . I put on the Oculus headset and saw a little bit of my desktop, but it was upside down. I ran the demo scene, and using keyboard combinations I got it moved over to the 1920x1080 monitor the Oculus had become. The scene was upside down for some reason. I made the monitor landscape and then the text was backwards, so I flipped the monitor. Now I could see the scene, but it was like I had strapped a 55 inch monitor to my head: wherever I looked the scene moved with me. I would rather have just looked at the scene on my actual 55 inch monitor.  

I decided to do major surgery to see what was wrong.  I looked at the motion tracking camera I had set on my monitor. No lights were on. I saw that the light flashed if I unplugged then plugged in the camera. The configuration app said it was detected. Then I realized the camera had a lens cap and it was still on—lol! I removed the cap but it still didn’t work right. 

I went back to the software and ran an older Oculus runtime, .6, and found it did not work at all in Windows 10. So I reinstalled .7, and as a hail mary, since I was working on motion tracking and not video, I upgraded to some beta video drivers I saw on reddit . I rebooted and it was as if someone had inserted the magic pill into the Oculus! The “no HMD found” error had gone away and it said the Oculus was ready to go.  

I put on the headset and loaded the test scene. You really have to see it yourself to understand how 3D it really is. When I put on the headset, the 55 inch monitor strapped to my head locked in place and I could move my head within the scene. It is truly amazing—the head tracking makes the experience come alive! I am very impressed with how far they have come with virtual reality. You have to give this thing a try and watch some 3D video—you will not be disappointed.



# Writing Code

I realize this repo is named CSharp...so where's the code?  It turns out that I named the repo before I knew what I was doing.  Instead of writing code I decided to try out Unreal Engine 4 which, so far, does not require much coding to create a very simple 3d world.  If you do not already know Unreal Engine 4, Unity 5, and Cryengine all support VR development for the Oculus Rift, but I only tried Unreal Engine 4 as it seemed more people thought it was better.  But if I ever do manage to write some c# code you will find it here!


This is where the "hardware" challenge gets interesting.  In theory developing a VR app with one of these engines is exactly like developing any other app and then you simply attach a VR device.  That's cool because now you, as a hackathon participant, can develop a software-only solution, demo the app with the Window'd version, and then for the people that want to really get immersed, you can provide an actual VR viewing if/when you have time.  This is likely the best option for a hackathon, but as always we do not want to put any limits on your hackathon experience.  If you want to bring hardware that satisfies the prereqs, and include the actual Oculus Rift in your two minute demo, we cannot wait to meet you and will do everything we can to make you successful!

# Good Things to Know

* We cannot stress enough the importance of the prerequisites.  We would hate for your hackathon pleasure to be killed by setup issues.  On the other hand if you plan accordingly this could be the coolest thing you do all year.

* If you are going to accept this challenge, have a plan in place before you arrive.  Do you plan on actually attaching the Oculus Rift and using it?  Or do you plan on having a VR themed product without needing to demo the actual gear?  Or do you plan on building something in Unreal Engine or Unity and using that as your product?  All are very acceptable but each has different pros/cons.

* If you accept this challenge and want to actually use the Oculus Rift for your demo, you need to plan ahead even more.  A two minute demo does not give you much time for setup and no one is going to be able to see the VR other than the person wearing the headset.  We can think of some very creative ways to still demo so do not let this deter you, but we do want to call it out.

* If you prefer a different VR device and want to bring it you are more than welcome to.

# Vantiv Challenge

There are many commerce-related use cases for VR, but the one we are going to highlight occurred to us during a brainstorming session with the team from the Vantiv Entertainment division (https://www.vantiventertainment.com/).  The concept of peer to peer betting was discussed in the context of a VR game.  Let's say Paul challenged me to a game of VR 3D Donkey Kong and we each provided five dollars to our betting pool for the "game".  We then wagered with that $5 for certain aspects of the game:  highest points, first person to clear the first screen, furthest in levels, most barrels jumped, etc.  The game itself would need to provide an API that we could connect to obtain the outcome statistics, and we would also need an application to facilitate the transfer of funds.

One way to integrate this solution to the Vantiv platform would be to use our ACH API.  This API is "hidden" inside of our Soap and REST API as a transaction type.  We would collect bank account information during participant signup, allow participants to transfer money to a house account, and then the house account would distribute funds back to the players based on the API game statistics and in-game betting, and take a certain percentage for profit.

The legality of the above approach idea needs to be validated, but the cool thing about Vantiv is we have the best team in the business (Vantiv Entertainment) to help us run the compliance gauntlet of the gaming industry.  But for now, at the hackathon, we can dream to our heart's content.  If the magical day arrives when you want to turn your masterpiece into an actual product, we will introduce you to the Vantiv Entertainment team who are always more than happy to assist.

Pretty sweet eh?

# Useful Links

* Oculus -- https://www.oculus.com/en-us/
* Unreal Engine 4 -- https://www.unrealengine.com/what-is-unreal-engine-4
* Unity 5 -- http://unity3d.com/5

# Other cool things

* Virtual Desktop -- https://share.oculus.com/app/virtual-desktop -- after installing this and watching a few youtube 360 degree videos we are convinced this is one of the best demos out there.
* The Chair -- https://share.oculus.com/app/sightline-the-chair -- we liked this one for demo purposes as well

# Legal Stuff

[Privacy Policy, Copyright Notices, and Terms of Use](https://vantiv.com/privacy-policy)

Oculus Rift, Oculus Rift DK2, and GEFORCE GTX, NVIDIA, Unity 5, Unreal Engine 4, and Corsair CX850M are registered or unregistered marks belonging to their respective owners who are unaffiliated with and do not endorse or sponsor Vantiv, and Vantiv likewise does not endorse or sponsor Oculus Rift, Oculus Rift DK2, and GEFORCE GTX, NVIDIA, Unity 5, Unreal Engine 4, and Corsair CX850M.
