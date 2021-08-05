### Mad Maxie – Windows GUI/Manager Advance dual plotter for madMax - Chia, Flax, Goji, Seno, Spare Coin.

Latest- https://github.com/JustMeROMs/MadMaxie_GUI/releases/tag/113

Discord Channel : https://discord.gg/2BH4mvBN

![MaxMaxie v1 1 2a](https://user-images.githubusercontent.com/83911433/126649188-4aff40ea-cd6d-46e5-9d6a-6fb34d57e1b5.JPG)


![113](https://user-images.githubusercontent.com/83911433/127073120-8500772c-aca4-4cee-988f-384109b83966.JPG)


[![stable](http://badges.github.io/stability-badges/dist/stable.svg)](http://github.com/badges/stability-badges)


:rocket: Mad Maxie is a Windows Forms application oriented to provide a more usable friendly user interface for the madMax chia plotter. With advance features. like ram disk and more. Run job on each SSD/ram disk, no need for running program in multiple instance anymore

**Features**

**Multiple final destinations.**

You can add multiple final destinations, Mad Maxie will alternate the final destination for each plotting process using both plot windows.
•	Multiple pools and combined solo and pool plotting
Mad Maxie, you can dual plot, 
1.	Dual plot solo or same pool (NFT)
2.	Solo, and pool plot each one (different address or same)
3.	Plot to two different pools.

Extra improvements/features and user path selections
There are some tweaks and hacks to improve stability and performance of the plotter process, have added user path to select where madMax Stotiks exe file is located, 

1.	Delay timer for second plot to stagger if needed for plot 2

2.	Save 2 profiles per plot, so when switching no need to remember setting can just recall when changing pools etc



**Tools Menu there is Chia, Flax, Goji, Seno Spar**e, 

1.	plot checker
2.	start/stop farmer
3.	start/stop harvester
4.	Show Keys
5.	Show NFT keys
6.	Show Version
7.	Many more
Chia Faucet also in the tools menu and now CMD Window

**What do abbreviations mean**

1.	PCA = Pool Contract Address (for mining on pools)
2.	PK = Pool keys (for solo mining)
3.	FK = Farmer keys

### **Usage:**
  chia_plot [OPTION...]

  -n, --count arg      Number of plots to create (default = 1, -1 = infinite)
  -r, --threads arg    Number of threads (default = 4)
  -u, --buckets arg    Number of buckets (default = 256)
  -v, --buckets3 arg   Number of buckets for phase 3+4 (default = buckets)
  -t, --tmpdir arg     Temporary directory, needs ~220 GiB (default = $PWD)
  -2, --tmpdir2 arg    Temporary directory 2, needs ~110 GiB [RAM] (default = <tmpdir>)
  -d, --finaldir arg   Final directory (default = <tmpdir>)
  -w, --waitforcopy    Wait for copy to start next plot
  -p, --poolkey arg    Pool Public Key (48 bytes)
  -c, --contract arg   Pool Contract Address (62 chars)
  -f, --farmerkey arg  Farmer Public Key (48 bytes)
  -G, --tmptoggle      Alternate tmpdir/tmpdir2 (default = false)
  -h, --help           Print help
  -K, --rmulti2        Thread multiplier for P2 (default = 1)

**Ram Disk Features Added** :rocket:

You will need, 128GB Ram installed to allocate 119GB ram for ram disk, ram disk can only be used for temp 2 directory, this will save your SSD’s or NVMe’s from greater wear and also speed up your plot times you must install the ram disk exe file that come with the zip file as Mad Maxie calls for it in the background.



**Future Development**

1.	A Linux version maybe
2.	Added Advance features
3.	Many more goodies coming next release

**Change log:**

**25/06/2021 - V1.0.0 Initial release**
• Initial release

**12/07/2021 - v1.1.1 - Added Features**
• Added Dual plots for multiply pools or combine solo and pool
• Added second Plot delay timer
• Added chia, flax, Goji, Seno Plot checker, show keys, start/stop farmer, start/stop harvester
• Added save profiles so you don't have to retype all the time when changing pools or address and settings
• Added stability and code improvements and plot processing
• Fixed folder options
• Changed theme

**22/07/2021 - v1.1.2 - Added Features**
• Added Spare Coin
• Added CMD Window Tab
• Added CPU & Ram Usage Indicators
• Added Temp 1, Temp 2, Final Directory HDD Space Available
• Added Chia Faucet

**27/07/2021 - v1.1.3 - Added Features**
• Added ram disk feature
• Added hover over textbox hints
• Added -K argument for Phase 2 default is 1
• All files included in zip to make it function as per intended including -K

**On a dual Xeon® E5-2680v2@2.80GHz R720 with 256GB RAM and a 4x500GB Samsung Evo 870 SATA SSD RAID0, using a 119GB RamDisk for <tmpdir2>: 28 minutes per plot**

<details>

**<summary>**Click to expand! to see plot log times**</summary>**

> Final Directory: N:\Farmer12TB_9\
Number of Plots: 40
Crafting plot 1 out of 40
Process ID: 116541
Number of Threads: 38
Number of Buckets P1:    2^9 (512)
Number of Buckets P3+P4: 2^9 (512)
Pool Puzzle Hash:  4c0bd498427be0dcbb61c658c9d963c531297235a76893129d7a18c5b95ef12a
Farmer Public Key: 96d57cb8c0e7b8959bebe021ac5dadd7411B11386f3ae32aa3e5348cf5db8fe74296720347c3bda6382ec0b849aea675
Working Directory:   E:\plot1\
Working Directory 2: Z:\ramdisk\
Plot Name: plot-k32-2021-07-26-21-39-3c2ac68f3fda6bb88c0221199ab5f12291a0124876156e1db14ef2c18fc4950c
[P1] Table 1 took 11.7434 sec
[P1] Table 2 took 112.794 sec, found 4294954540 matches
[P1] Table 3 took 130.572 sec, found 4294905655 matches
[P1] Table 4 took 145.428 sec, found 4294906312 matches
[P1] Table 5 took 143.449 sec, found 4294809946 matches
[P1] Table 6 took 142.851 sec, found 4294678821 matches
[P1] Table 7 took 113.286 sec, found 4294407883 matches
Phase 1 took 800.159 sec
[P2] max_table_size = 4294967296
[P2] Table 7 scan took 7.51377 sec
[P2] Table 7 rewrite took 41.7697 sec, dropped 0 entries (0 %)
[P2] Table 6 scan took 27.4067 sec
[P2] Table 6 rewrite took 39.5276 sec, dropped 581291667 entries (13.5352 %)
[P2] Table 5 scan took 24.1976 sec
[P2] Table 5 rewrite took 36.9839 sec, dropped 761993098 entries (17.7422 %)
[P2] Table 4 scan took 23.643 sec
[P2] Table 4 rewrite took 36.9741 sec, dropped 828898709 entries (19.2996 %)
[P2] Table 3 scan took 22.905 sec
[P2] Table 3 rewrite took 35.9288 sec, dropped 855093619 entries (19.9095 %)
[P2] Table 2 scan took 23.0391 sec
[P2] Table 2 rewrite took 33.2392 sec, dropped 865597352 entries (20.1538 %)
Phase 2 took 383.231 sec
Wrote plot header with 252 bytes
[P3-1] Table 2 took 33.8893 sec, wrote 3429357188 right entries
[P3-2] Table 2 took 33.8603 sec, wrote 3429357188 left entries, 3429357188 final
[P3-1] Table 3 took 43.9242 sec, wrote 3439812036 right entries
[P3-2] Table 3 took 34.9996 sec, wrote 3439812036 left entries, 3439812036 final
[P3-1] Table 4 took 44.3806 sec, wrote 3466007603 right entries
[P3-2] Table 4 took 34.2283 sec, wrote 3466007603 left entries, 3466007603 final
[P3-1] Table 5 took 44.8432 sec, wrote 3532816848 right entries
[P3-2] Table 5 took 33.4012 sec, wrote 3532816848 left entries, 3532816848 final
[P3-1] Table 6 took 47.9729 sec, wrote 3713387154 right entries
[P3-2] Table 6 took 36.3375 sec, wrote 3713387154 left entries, 3713387154 final
[P3-1] Table 7 took 42.7023 sec, wrote 4294407883 right entries
[P3-2] Table 7 took 42.6982 sec, wrote 4294407883 left entries, 4294407883 final
Phase 3 took 479.976 sec, wrote 21875788712 entries to final plot
[P4] Starting to write C1 and C3 tables
[P4] Finished writing C1 and C3 tables
[P4] Writing C2 table
[P4] Finished writing C2 table
Phase 4 took 67.1524 sec, final plot size is 108827497155 bytes
Total plot creation time was 1730.63 sec (28.8438 min)

</details>

-----------------


**Big Thank you to the following:**

madMAx43v3r - https://github.com/madMAx43v3r
  
stotiks - https://github.com/stotiks/chia-plotter/releases
  
Flax Devs - https://flaxnetwork.org/
  
Goji Devs – https://getgoji.net/
  
Seno Devs - https://seno.uno/

  
Bozniack, flux103, Big T, Travola, Gutspiller And most important Mad Maxie our Cavoodle Puppy 😊

**By JustMe ROMs -  https://github.com/JustMeROMs/MadMaxie_GUI**

### Your donation will help and allow me build newer versions:

XCH: xch12zn2c05g5m0fr5r6ytyn0v3q5qfu80wyapgvzrhkm5g79fdrxtzsgus777

XFX: xfx1aq4edjr2fx3l65uennly5m72c62gavmvyj7r5cfq6wmf022y0zwqhd8hvg
  
BTC: 1E4Rwk4Afw49Vfi15Ee8iY8Z21Yw8cjFtq
  
ETH: 0x0f90dc50b87934cc4ddf1259aa7168aa4b4a37a6
