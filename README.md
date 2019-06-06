# CoCoDragon-CC2-32K-EPROM-CARTRIDGE-2012-V1RA
CC2-32K-EPROM-CARTRIDGE-2012-Version-1-Revision-A-07.02.2012 is a 32K EPROM Cartridge for the Tandy Radio Shack TRS-80 Color Computer 1, 2, 3 and Dragon Data Dragon computers. Notes: The CoCo 1, 2 and Dragon can only access the first 16K. The CoCo 3 can access the entire 32K, minus the 0xFFnn I/O and Vector page. Many other similar (but much improved) cartridges are forthcoming. There are much better designs in my possession and I intend to post them all, in no particular order.

There is an OSHPark Page Here: https://oshpark.com/shared_projects/z65Q8QQk

 PLEASE NOTE: THIS VERSION HAS NOT YET BEEN TESTED. 

Please note: This is derived from an original design by "Little" John Eric and/or his father "Big" John Robert (J.R.) by "Uncle" Robert Allen. It should be thoroughly scrutinized and verified prior to actual use of any kind. DISCLAIMER: The following article is provided for informational purposes only. Any attempt to modify your computer without the proper skills to do so may void your computer. Any attempt to modify your computer without unplugging it first may void you. This Information is provided "as-is" with no guarantee of fitness for any purpose, either explicit or implied. We disclaim any and all responsibility for losses incurred through the use of this information. By using this information, you are deemed to have accepted these conditions of use, and you agree NOT to sue us. CLARIFICATION: The above disclaimer states as plainly as possible that if you decide to make use of any of the information contained within this document that you do so at your own risk. Designing hardware for the CoCo (ColorComputer) and other vintage hardware is a hobby of ours and is not motivated by any desire of profits. As this is a not for profit venture, obviously we can't afford not to disclaim the use of this information.

<p align="center"><b><center>
A Project By <a href="http://www.TheLittleEngineers.org/">
The Little Engineers</a>.</b>
<br>Copyright &copy;2019, by:<br>
Robert "The R.A.T." Allen Turner<br>
<a href="http://www.TheLittleEngineers.org/">http://www.TheLittleEngineers.org/</a><br>
<a href="mailto:TheLittleEngineers@outlook.com">TheLittleEngineers@outlook.com</a><br>
<a href="mailto:OurLittleEngineers@gMail.com">OurLittleEngineers@gMail.com</a><br>
</center></p>
<p align="justify">
<big>This first paragraph relates to our KiCAD and E.A.G.L.E. CAD Libraries:</big><br>
You may use the components contained in this library in your own projects, however, please 
take note that we CANNOT guarantee the accuracy of these components (nor any part of this 
library). We make NO guarantees that the components, footprints or schematic symbols in this 
library are flawless, and we make no promises of fitness for production, prototyping or any 
other purpose. These libraries are provided for informational purposes only, and are used at 
your own discretion. By downloading these libraries, you agree that we cannot be held 
responsible for faulty PCBs. You should always check the footprints with a 1:1 printout. 
Neither Robert Allen Turner, <a href="http://www.TheLittleEngineers.org/">The Little 
Engineers</a>, <a href="http://www.TheLittleEngineers.org/">TheLittleEngineers.org,</a> 
<a href="http://www.GIMEchip.com/">GIMEchip.com</a>, nor anyone affiliated with same shall 
be held responsible for any outcome resulting from the usage of these files. Should any 
errors be found, please contact us at one of the above email addresses and we will attempt to 
repair them. Unless otherwise noted, content of this library is licensed under a 
<a href="https://creativecommons.org/licenses/by-sa/4.0/">Creative Commons 
Attribution-ShareAlike 4.0 International</a> 
<a href=" https://creativecommons.org/licenses/by-sa/4.0/legalcode">(CC BY-SA 4.0)</a> 
License on 04 Junel 2019 in memory of my Father, Robert Embry Turner, 1945-2019 - I LOVE YOU 
DAD! Rest In Peace.<br><br><big>The remainder of this documents serves as a general 
<i>Introduction</i> to Robert "The R.A.T." Allen Turner, Zombie Software Systems, Binary 
Systems, <a href="http://www.GIMEchip.com/">GIMEchip.com</a> and 
<a href="http://www.TheLittleEngineers.org/">The Little Engineers</a> (
<a href="http://www.TheLittleEngineers.org/">http://www.TheLittleEngineers.org/</a>). Please 
note that the <a href="http://www.GIMEchip.com/">GIMEchip.com</a> 
domain was acquired by Robert "The R.A.T." Allen Turner on December 25, 2018 from the prior 
owners, which happen to be his brother (J.R. a.k.a. John Robert a.k.a. "Big John") and nephew 
(J.E. a.k.a. John Eric a.k.a. "Little John"). As such, "The R.A.T." is unable to answer any 
inquiries regarding any products or services of <a href="http://www.GIMEchip.com/">
GIMEchip.com</a> prior to that date. "The R.A.T." also acquired the rights to all products 
previously produced by <a href="http://www.GIMEchip.com/">GIMEchip.com</a> and its previous 
owners. Those products will all be released as open source, under a 
<a href="https://creativecommons.org/licenses/by-sa/4.0/">Creative Commons 
Attribution-ShareAlike 4.0 International</a> 
<a href=" https://creativecommons.org/licenses/by-sa/4.0/legalcode">(CC BY-SA 4.0)</a> 
License, as time and resources permit.<hr><b>Introducing "The R.A.T.": </b>I have started 
writing this introduction numerous times only to get sidetracked and derailed. Hopefully, I 
will be able to  properly introduce myself this time. I will start at the beginning of my 
computer usage. This would be March 30, 1982. My fourteenth birthday. My parents presented 
me with a <b>Timex Sinclair 1000 (TS1000)</b> computer, after much begging and pleading. The 
<b>TS1000</b> is a <b>ZX81</b> with a few differences: 2K of RAM, an [ENTER] key instead of 
[NEW LINE] or [N/L] and Timex branding. I had wanted a computer for so long, and <b>Sir Clive 
Sinclair</b> succeeded in making it affordable. Timex made it even more affordable as the 
<b>TS1000</b> was placed on sale for $59.99 at the local "Big B" drug store, at the time, a 
division of Brunos Corporation (Food World, Food Fair, Consumer Warehouse, etcetera). I was 
ectstatic - I finally had a computer, limited as it was, I still learned a great deal from 
that machine and it led to the creation of <b>Zombie Software Systems</b>, my first computer 
venture. When Timex announced the <b>Timex Sinclair 2068 (TS2068)</b> after cancelling the 
<b>TS2000</b> (a <b>48K Spectrum</b> clone), I knew that I wanted it to be my next computer 
and my parents agreed to buy it for me for Christmas of 1983. Then, it happened: I walked 
into the local franchised Radio Shack store, operated at the time by Cisco Auto Parts, and 
there, on display right next to the entrance, was the newly introduced <b>Color Computer 2 
with 16K and Extended Color BASIC</b>. It took mere moments for me to fall in love with that 
machine and I asked my parents for the <b>Color Computer 2</b> instead of the <b>TS2068</b>. 
They placed it on lay-a-way as Christmas approached. It was eventually paid off and sat under 
the Christmas tree until Christmas Evening of 1983. They allowed me to open it on Christmas 
Evening and I was up all night working through the programs in the manuals. It was wonderful. 
This led to the creation of <b>Binary Systems</b>, my second computer venture. Eventually, I 
came across an advertisement in Radio-Electronics from a company by the name of Unicorn 
Electronics. They had a set of 4164 Dynamic RAM chips with a 150nS access time for, I think 
$9.95. The chips were used but tested. I ordered them, along with a bag of keyboard switches 
(intended to be used for buildinmg a better keyboard for my <b>TS1000</b>). When they arrived, 
I opened the case of my <b>Color Computer 2</b>, installed the 64K chips, soldered in the W1 
jumper and voila - I had a <b>64K ECB Color Computer 2</b>. Although other systems of the 
time had better graphics and sound, the <b>Color Computer</b> line of systems by Radio Shack, 
a division of Tandy Corporation, would become (and remain) my favorite computers of all time. 
In fact, I still use them to this very day, having kept one <b>Color Computer 3 (CoCo 3)</b> 
when I passed my vintage computing collection to my brother, J.R. (John Robert) who then passed 
it on to his son, "Little John" (John Eric), but I will get to that after a brief reminiscence 
of <b>ZSS</b> and <b>BS</b>, as follows:<br><b><center>ZSS or Zombie Software Systems:</center>
<br>Zombie Software Systems</b> was formed on my fourteenth birthday, 30 March 1982, as a sole 
proprietorship supporting the Timex and Sinclair computer systems. Supported systems initially 
included:<ul>
<li>Sinclair ZX80</li>
<li>Sinclair ZX81</li>
<li>Timex Sinclair 1000</li></ul>
Support was eventually added for:<ul>
<li>Timex Sinclair 1500</li>
<li>The PC-8300 "Your Computer"</li>
<li>Sinclair Spectrum (All Versions)</li>
<li>Timex Sinclair 2068</li>
<li>Sinclair QL</li></ul>
By 1991, and in conjunction with Binary Systems, support had been added for machines from Mattel, 
Atari, Tomy, Texas Instruments, Tandy Radio Shack, Commodore and many others.<br><br><b><center>
BS or Binary Systems:</center><br>Binary Systems</b> was formed on 23 December 1983, as a sole 
proprietorship supporting the Tandy Radio Shack computer systems. Supported systems initially 
included:<ul>
<li>TRS-80 Color Computer (CoCo 1)</li>
<li>Tandy Data Products TDP-100</li>
<li>TRS-80 Color Computer 2 (CoCo 2)</li>
<li>Dragon Data Dragon 32</li>
<li>Tano Dragon 64</li>
<li>TRS-80 Model I</li></ul>
Support was eventually added for:<ul>
<li>TRS-80 Model III</li>
<li>TRS-80 Model IV</li>
<li>TRS-80 Model 4/4P</li>
<li>Tandy Color Computer 3</li></ul>
By 1991, and in conjunction with Zombie Software Systems, support had been added for machines from 
Mattel, Atari, Tomy, Texas Instruments, Sinclair, Commodore, Amstrad, Kaypro and many others. The 
operation of <b>Zombie Software Systems</b> and <b>Binary Systems</b> was a <b>labor of love</b> 
more than anything else, as it never made a profit, but it was fun and remains among the best 
memories of my youth and early adulthood and I am thankful that the stroke (see below) did not take 
these memories from me.<hr>I continued to support these vintage machines until 2007 when I suffered 
a stroke. At that point, I passed operations on to my son, John (he and his cousin share both the 
same name and same date of birth through a very odd coincidence). My son eventually made a mess of 
things and finally moved on to other hobbies. A side effect of the stroke was that I lost all 
interest in computers and electronics, vintage and otherwise. It was thus that I presented my entire 
collection of vintage computers and electronics to my brother J.R. (John Robert or "Big John"). He 
took the opportunity to bond with his son, J.E. (John Eric or "Little John"). "Little John" was 
facing a number of health issues, but he jumped in with both feet, teaching himself all about the 
<b>Color Computer</b> and other systems. He began to develop a plethora of hardware projects for the 
<b>Color Computer</b> and other vintage systems. The earliest of his design were rubbish due to his 
lack of skill, but he appears to have learned rather quickly, producing some amazing designs. I have 
taken it upon myself to "redo" his earliest works, hopefully producing manufacturable products from 
them. The first of his designs to receive the "redesign" treatment from me is the "FlexiMIDI" and 
"FlexiROM" projects. Those two designs were excellent in concept, but rubbish in practice due to his 
lack of circuit design skills at the time that he developed them. They are certainly worth the time 
and effort to redesign. He would eventually become disillusioned and abandon the hobby altogether. 
This was, in no small part, due to hackers repeatedly taking down his website: 
<a href="http://www.GIMEchip.com/">GIMEchip.com</a>. They (the unknown hackers) eventually compromised 
his eBay and PayPal accounts, rendering them completely useless. That was the straw that broke the 
camels back, so to speak. He ("Little John") gave up and moved to Tennessee. He left everything with 
his father, my brother, and asked that his father release all of his works as open source. J.R. made 
several valiant efforts to honor that request, but never fully succeeded in releasing all of the works 
of "Little John". Fast Forward almost a decade...<br><hr>
<b>The Beginning of a Family Tragedy:</b><br>November of 2018, my father fell ill and was hospitalized. 
As Christmas approached, he remained in the hospital. Many family members visited and it came to pass 
that I reconnected with J.R. and "Little John". They asked me if I would like to have my old vintage 
computing collection back. At first, I was hesitant and uninterested. As my fathers condition worsened, 
I began to remember how hard my father worked to buy me those first computers. Tons of memories, good 
and bad, began to flood my mind. I decided to accept their offer. In addition to the hardware and 
software, they presented me with the <a href="http://www.GIMEchip.com/">GIMEchip.com</a> domain name. 
This became my Christmas present from my brother and his son. "Little John" asked that I finish what 
his father started: <i>the release of all of "Little John's" work as open source</i>. I reluctantly 
agreed, though I was unsure if I could ever manage the time and effort to do so. I honestly was not 
prepared to take on such a monumental task. Then, <b>tragedy</b> struck.<br><br>On the day of 
January 4, 2019, my father died as I held his hand in that hospital room. His death had quite a profound 
effect on me. I almost lost my job while trying to come to terms with never being able to speak to my father 
again. I eventually began to recover, to an extent, but I began to think of everything and everyone that I 
had lost over the years. For one thing, my own son, also named John Eric Turner, and I are estranged. We 
"speak" online, but I have not seen him in a very long time. He was unable to be at the hospital and did 
not get to say goodbye to my father before he died. As mentioned, my son and his cousin are both named 
John Eric Turner, and there is a story behind it, however, for the moment, suffice it to say that they 
both were named In Memory of Jon-Erik Hexum, who died on the set of "Cover Up" on Friday, October 12, 
1984. As my mind wandered, I thought of my mother in law, Sarah Ann Channell, who passed away on 
January 12, 2003 and my father in law, Frank Leon Channell, who passed away on August 23, 2003. Even 
though I was divorced from their daughter, they were still family and their deaths were very painful to 
me and my son. Indeed, their deaths affected my son in such a way that he never fully recovered and that 
is partially what eventually led to our falling out in 2007 or 2008 and the resulting estrangement. I am 
sure that my addled state after that stroke also played a hand in the troubles between my son 
and I because I became very difficult to be around. Thinking about Sarah and Frank caused me to really 
begin missing my son and, even more, my father. I then thought about my best friend from high school, 
David Ray Poe, who died on May 20, 2013. Eight days prior to his death, he had sent me an email that I 
did not see until after he died. That email was a single sentence: "Did you die?". You can perhaps imagine 
the effect that reading the message had on me. In reality, he would often send a message like that when he 
had not heard from me in a while. Another close friend from high school, Steve Allen cox, died on September 
6, 2016. As all of the thoughts of everything and everyone that I had lost flooded my mind, I began to 
spiral and was in peril of losing myself. I needed a distraction, something to keep my mind occupied and 
perhaps aid in my coming to terms with the death of my father. I found that distraction in the form of that 
vintage computing collection and the projects that "Little John" had created. It is for that reason alone 
that you are now reading this and seeing those products, which I have decided to release under a 
<a href="https://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 
International</a> <a href=" https://creativecommons.org/licenses/by-sa/4.0/legalcode">(CC BY-SA 4.0)</a> 
License. What this means is that you, or anyone else for that matter, can use the products in almost any 
way that you may desire, even commercially. I am doing all of this to honor the memory of my father, Robert 
Embry Turner, and everyone else that I have lost. I truly hope that these products provide much enjoyment 
to all who discover them. I should point out that I have absolutely no desire to revive the 
<a href="http://www.GIMEchip.com/">GIMEchip.com</a> website, primarily because I do not have all of the 
files necessary to recreate <a href="http://www.GIMEchip.com/">GIMEchip.com</a>. It is very likely that I 
will stumble across some or all of the <a href="http://www.GIMEchip.com/">GIMEchip.com</a> website files as 
I begin to inventory everything that was included with my 2018 Christmas gift from "Big and Little John". I 
also <b>DO NOT</b> wish to invoke the ire of those hackers who targeted my nephew and destroyed his website, 
eBay and PayPal accounts. I will very likely, however, forward the <a href="http://www.GIMEchip.com/">
GIMEchip.com</a> domain to a page on my <a href="http://www.TheLittleEngineers.org/">
http://www.TheLittleEngineers.org/</a> <a href="https://www.facebook.com/OurLittleEngineers/">website</a> 
or perhaps I will forward it to the <a href="https://github.com/TheLittleEngineers?tab=repositories">GitHub
</a> page - I am currently undecided.<br><br>So, there you have it - most of what I wanted to say about how I 
came to posses all of the works of my nephew and his father, as well as their domain name, 
<a href="http://www.GIMEchip.com/">GIMEchip.com</a>. In addition to releasing all of their products under a 
<a href="https://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 
International</a> <a href=" https://creativecommons.org/licenses/by-sa/4.0/legalcode">(CC BY-SA 4.0)</a> 
License, I will also be releasing all of the <b>Zombie Software Systems</b> and <b>Binary Systems</b> 
products under <a href="https://creativecommons.org/licenses/by-sa/4.0/">identical</a> 
<a href=" https://creativecommons.org/licenses/by-sa/4.0/legalcode">licensing</a> 
<a href="https://creativecommons.org/licenses/by-sa/4.0/">terms</a>. As I said, I am primarily doing all of 
this to keep my mind occupied. I miss my Father more than any words, written or spoken, could possibly 
express and I keep breaking down, crying like an infant. Focusing on these projects has helped more than I 
could ever have imagined possible. <i>Rest In Peace</i> <b>DAD</b>, I Love and Miss You. I wanted to do 
something to honor my father and to keep his memory alive. Thus, in honor of my Father, Robert Embry Turner 
and all of the others that I have lost, I will be releasing hundreds of products developed by myself and/or 
my son, my nephew "Little John" and/or his father, Zombie Software Systems and Binary Systems under an open 
source license, specifically the <a href="https://creativecommons.org/licenses/by-sa/4.0/">Creative Commons 
Attribution-ShareAlike 4.0 International</a> 
<a href=" https://creativecommons.org/licenses/by-sa/4.0/legalcode">(CC BY-SA 4.0)</a> License. I have 
absolutely <b>no intention</b> of charging any fees whatsoever in regards to the use of these products. 
Anyone who so desires may manufacture and sell any of these products, though they must state specifically 
that they will be providing any and all support as may be required. However, If you would care to support my 
work, donations are happily accepted, whether they be in the form of funds, vintage computing equipment, 
tools, components, etcetera. I am always in need of such items. I specifically need PAL versions of the TRS80 
Color Computer series (1,2 and 3) as well as NTSC/PAL Dragon D32, D64, D200, etcetera for developmental 
purposes. Monetary donations help to support the hosting needs of 
<a href="http://www.TheLittleEngineers.org/">http://www.TheLittleEngineers.org/</a> as well as the 
development and manufacture of the prototype Printed Circuit Boards.<br><br>Perhaps the easiest and most 
beneficial method of supporting <a href="http://www.TheLittleEngineers.org">The Little Engineers</a> 
(monetarily) would be by becoming a 
<a href="https://www.patreon.com/rss/TheLittleEngineers?auth=Lf2lxAb1hC7CqtfFqcd47ysxUUx_8AvY">Patron</a> on 
<a href="https://www.patreon.com/rss/TheLittleEngineers?auth=Lf2lxAb1hC7CqtfFqcd47ysxUUx_8AvY">Patreon</a>: 
<a href="https://www.patreon.com/rss/TheLittleEngineers?auth=Lf2lxAb1hC7CqtfFqcd47ysxUUx_8AvY">
https://www.patreon.com/rss/TheLittleEngineers?auth=Lf2lxAb1hC7CqtfFqcd47ysxUUx_8AvY</a> The following are 
among the benefits offered to 
<a href="https://www.patreon.com/rss/TheLittleEngineers?auth=Lf2lxAb1hC7CqtfFqcd47ysxUUx_8AvY">Patrons</a>.
<a href="https://www.patreon.com/rss/TheLittleEngineers?auth=Lf2lxAb1hC7CqtfFqcd47ysxUUx_8AvY">Patrons</a> will 
receive several exclusive benefits, such as:<br><ul>
<li>FREE copies of ANY of our detailed Theory of Operation and Assembly 
<a href="https://www.amazon.com/Robert-Allen-Turner/e/B07K5L5HW9">e-books</a> relating to our projects.</li> 
<li>Random giveaways of bare Printed Circuit Boards (PCB's) developed by 
<a href="http://www.TheLittleEngineers.org">The Little Engineers</a>.</li>
<li>Random giveaways of Kits developed by 
<a href="http://www.TheLittleEngineers.org">The Little Engineers</a>.</li>
<li>Random giveaways of assembled projects developed by 
<a href="http://www.TheLittleEngineers.org">The Little Engineers</a>.</li>
<li>The opportunity to purchase various bare Printed Circuit Boards (PCB's) developed by 
<a href="http://www.TheLittleEngineers.org">The Little Engineers</a> at discounts of up to 50% off.</li>
<li>The opportunity to purchase various Kits developed by 
<a href="http://www.TheLittleEngineers.org">The Little Engineers</a> at discounts of up to 50% off.</li>
<li>The opportunity to purchase various assembled projects developed by 
<a href="http://www.TheLittleEngineers.org">The Little Engineers</a> at discounts of up to 50% off.</li>
</ul>A plethora of other benefits will be added exclusively for 
<a href="https://www.patreon.com/rss/TheLittleEngineers?auth=Lf2lxAb1hC7CqtfFqcd47ysxUUx_8AvY">Patrons</a> as 
time and resources allow. Remember, however, that NO donations are required to access the 
<a href="https://github.com/TheLittleEngineers/">project</a> 
<a href="https://github.com/TheLittleEngineers?tab=repositories">repositories</a> which are available to all 
for FREE. Another method of making monetary donations is the use of the 
<a href="https://www.facebook.com/OurLittleEngineers/">FaceBook</a> 
<a href="https://www.facebook.com/TheLittleEngineers.org">Messenger</a> 
<a href="https://www.facebook.com/groups/985537051651794/">Payment</a> 
<a href="https://www.facebook.com/OurLittleEngineers/">App</a>. 
<a href="http://www.TheLittleEngineers.org">The Little Engineers</a> may be found on 
<a href="https://www.facebook.com/OurLittleEngineers/">FaceBook</a> at the following urls:<br>
<a href="https://www.facebook.com/profile.php?id=100036295840711">
https://www.facebook.com/profile.php?id=100036295840711</a><br>
<a href="https://www.facebook.com/TheLittleEngineers.org">https://www.facebook.com/TheLittleEngineers.org</a>
<br><a href="https://www.facebook.com/OurLittleEngineers/">https://www.facebook.com/OurLittleEngineers/</a>
<br><a href="https://www.facebook.com/groups/985537051651794/">
https://www.facebook.com/groups/985537051651794/</a><br>
We will also be publishing detailed Theory of Operation and assembly manuals for all of our open source 
products in e-book and paperback formats. Purchases of these e-books and/or paperbacks helps to 
support <a href="http://www.TheLittleEngineers.org">The Little Engineers</a> and our continued developmental 
efforts. Donations may also be made in almost any variety of digital currency, including, but not limited to, 
the following:<br><ul>
<li>BitCoin (BTC): 18C75HESRUSQX7TUZycEiRUBG6wVpqANVv</li>
<li>Ethereum (ETH) or any Ethereum based tokens: 0x1374528109EDd54ecC2db6F4Ec29a2f520463499</li>
<li>BitCoin Cash (BCH): qpu25q42e9zpqc7mx5r0l3yvftw7ezp37v7899c4x6</li>
<li>BitCoin Gold (BTG): GRaxchWNUQGcnHaZa3e1guS5HmCakRFpZ3</li>
<li>BitCoin SV (BSV): qr7nkqqu83z0k8mx92s76kku48ulnr5jcup06aj4wy</li>
<li>LiteCoin (LTC): LdqZaNopx5xVbBZJcQqRRzX9rJhWstgKwp</li>
<li>Ethereum Classic (ETC) including any ETC Tokens: 0xd9518F33E822eea56FBE8aA0bcEffFbbfa2456C7</li>
<li>Stellar Lumens (XLM): GAXIJLUY7NSDAN22TSSYZKIWSBVM5OS5KVTY7MGR6I7PXFTS7U3JK3YV</li>
<li>Ripple (XRP): r3dMH6J596vV1LqSMB62ewuuWtsuhdWaoL</li></ul>
Should you wish to use digital currency, I highly recommend checking out this referral link: 
<a href="https://www.coinbase.com/join/5a42ff8478e76b05ef28e185">Digital Currency.</a> Signing up from 
that link also helps <a href="http://www.TheLittleEngineers.org">The Little Engineers</a> in the long run. 
If you would like to make a donation by some other means, feel free to contact me by 
<a href="mailto:TheLittleEngineers@outlook.com">e-mail</a> or 
<a href="https://www.facebook.com/profile.php?id=100036295840711">FaceBook</a> 
<a href="https://www.facebook.com/OurLittleEngineers/">Messenger</a>. Please note, however, that donations 
are completely optional, but they do help to further product development. All products developed by 
<a href="http://www.TheLittleEngineers.org">The Little Engineers</a> are completely free to use under the 
terms of the <a href="https://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 
4.0 International</a> <a href=" https://creativecommons.org/licenses/by-sa/4.0/legalcode">(CC BY-SA 4.0)</a> 
License, even for commercial purposes.
<hr> 
Please consider subscribing to our <a href="https://www.youtube.com/channel/UCgAwso8p5hkLFN9AdN6oxQg">
YouTube</a> Channel: <a href="https://www.youtube.com/channel/UCgAwso8p5hkLFN9AdN6oxQg">
https://www.youtube.com/channel/UCgAwso8p5hkLFN9AdN6oxQg</a><br>
Please follow us on <a href="https://twitter.com/TLEngineers">Twitter</a>: 
<a href="https://twitter.com/TLEngineers">https://twitter.com/TLEngineers</a><br>
Please check us out on <a href="https://www.twitch.tv/thelittleengineers">Twitch</a>: 
<a href="https://www.twitch.tv/thelittleengineers">https://www.twitch.tv/thelittleengineers</a>
<br>
Please consider following us on <a href="https://www.instagram.com/thelittleengineers_org/">
Instagram</a>: <a href="https://www.instagram.com/thelittleengineers_org/">
https://www.instagram.com/thelittleengineers_org/</a><br>
Please follow us on <a href="https://github.com/TheLittleEngineers">GitHub</a> in order to access all 
of our projects.<br><br>
Thank You for your time. I hope that you enjoy using these products as much as I enjoyed developing them 
(or debugging them in the case of the designs produced by my nephew and his father). - 
<i>Robert "The R.A.T." Allen Turner</i>
<hr><a href="http://www.TheLittleEngineers.org">The Little Engineers</a> is a project started in 
2011 by Robert Allen Turner to benefit Foster Children and their families, foster and biological. Follow 
our <a href="http://www.TheLittleEngineers.org">blog</a> if you would like additional information 
regarding this wonderful project.
</p>
