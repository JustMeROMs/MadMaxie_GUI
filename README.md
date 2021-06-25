# MadMaxie_GUI v1.0.0


$$\      $$\                 $$\       $$\      $$\                     $$\                  $$$$$$\            $$\       $$$$$$$\                  
$$$\    $$$ |                $$ |      $$$\    $$$ |                    \__|                $$  __$$\           \__|      $$  __$$\                 
$$$$\  $$$$ | $$$$$$\   $$$$$$$ |      $$$$\  $$$$ | $$$$$$\  $$\   $$\ $$\  $$$$$$\        $$ /  \__|$$\   $$\ $$\       $$ |  $$ |$$\   $$\       
$$\$$\$$ $$ | \____$$\ $$  __$$ |      $$\$$\$$ $$ | \____$$\ \$$\ $$  |$$ |$$  __$$\       $$ |$$$$\ $$ |  $$ |$$ |      $$$$$$$\ |$$ |  $$ |      
$$ \$$$  $$ | $$$$$$$ |$$ /  $$ |      $$ \$$$  $$ | $$$$$$$ | \$$$$  / $$ |$$$$$$$$ |      $$ |\_$$ |$$ |  $$ |$$ |      $$  __$$\ $$ |  $$ |      
$$ |\$  /$$ |$$  __$$ |$$ |  $$ |      $$ |\$  /$$ |$$  __$$ | $$  $$<  $$ |$$   ____|      $$ |  $$ |$$ |  $$ |$$ |      $$ |  $$ |$$ |  $$ |      
$$ | \_/ $$ |\$$$$$$$ |\$$$$$$$ |      $$ | \_/ $$ |\$$$$$$$ |$$  /\$$\ $$ |\$$$$$$$\       \$$$$$$  |\$$$$$$  |$$ |      $$$$$$$  |\$$$$$$$ |      
\__|     \__| \_______| \_______|      \__|     \__| \_______|\__/  \__|\__| \_______|       \______/  \______/ \__|      \_______/  \____$$ |      
                                                                                                                                    $$\   $$ |      
                                                                                                                                    \$$$$$$  |      
                                                                                                                                     \______/       
   $$$$$\ $$\   $$\  $$$$$$\ $$$$$$$$\ $$\      $$\ $$$$$$$$\       $$$$$$$\   $$$$$$\  $$\      $$\  $$$$$$\                                       
   \__$$ |$$ |  $$ |$$  __$$\\__$$  __|$$$\    $$$ |$$  _____|      $$  __$$\ $$  __$$\ $$$\    $$$ |$$  __$$\                                      
      $$ |$$ |  $$ |$$ /  \__|  $$ |   $$$$\  $$$$ |$$ |            $$ |  $$ |$$ /  $$ |$$$$\  $$$$ |$$ /  \__|                                     
      $$ |$$ |  $$ |\$$$$$$\    $$ |   $$\$$\$$ $$ |$$$$$\          $$$$$$$  |$$ |  $$ |$$\$$\$$ $$ |\$$$$$$\                                       
$$\   $$ |$$ |  $$ | \____$$\   $$ |   $$ \$$$  $$ |$$  __|         $$  __$$< $$ |  $$ |$$ \$$$  $$ | \____$$\                                      
$$ |  $$ |$$ |  $$ |$$\   $$ |  $$ |   $$ |\$  /$$ |$$ |            $$ |  $$ |$$ |  $$ |$$ |\$  /$$ |$$\   $$ |                                     
\$$$$$$  |\$$$$$$  |\$$$$$$  |  $$ |   $$ | \_/ $$ |$$$$$$$$\       $$ |  $$ | $$$$$$  |$$ | \_/ $$ |\$$$$$$  |                                     
 \______/  \______/  \______/   \__|   \__|     \__|\________|      \__|  \__| \______/ \__|     \__| \______/                                      
                                                                                                                                                    
                                                                                                                                                    
  

Designed on v0.0.6

  
chia-plotter (pipelined multi-threaded)

This is a new implementation of a chia plotter which is designed as a processing pipeline, similar to how GPUs work, only the "cores" are normal software CPU threads.

As a result this plotter is able to fully max out any storage device's bandwidth, simply by increasing the number of "cores", ie. threads.

Usage
Join the Discord for support: https://discord.gg/YJ4GSMMY


What I have done is take the briliant work from https://github.com/madMAx43v3r/chia-plotter#chia-plotter-pipelined-multi-threaded
and from https://github.com/stotiks/chia-plotter/releases/ and created a front end windows gui, this is the 1st release, and there is more features to be released
in the next version comming real soon. This Gui will also work with Flax and Chia.


For <poolkey> and <farmerkey> see output of `chia keys show`.
<tmpdir> needs about 220 GiB space, it will handle about 25% of all writes. (Examples: './', '/mnt/tmp/')
<tmpdir2> needs about 110 GiB space and ideally is a RAM drive, it will handle about 75% of all writes.
Combined (tmpdir + tmpdir2) peak disk usage is less than 256 GiB.
In case of <count> != 1, you may press Ctrl-C for graceful termination after current plot is finished or double Ctrl-c to terminate immediatelly\

Usage:
  chia_plot [OPTION...]

  -n, --count arg      Number of plots to create (default = 1, -1 = infinite)
  -r, --threads arg    Number of threads (default = 4)
  -u, --buckets arg    Number of buckets (default = 256)
  -v, --buckets3 arg   Number of buckets for phase 3+4 (default = buckets)
  -t, --tmpdir arg     Temporary directory, needs ~220 GiB (default = $PWD)
  -2, --tmpdir2 arg    Temporary directory 2, needs ~110 GiB [RAM] (default = <tmpdir>)
  -d, --finaldir arg   Final directory (default = <tmpdir>)
  -p, --poolkey arg    Pool Public Key (48 bytes)
  -f, --farmerkey arg  Farmer Public Key (48 bytes)
  -G, --tmptoggle      Alternate tmpdir/tmpdir2 (default = false)
      --hwinfo         Print information regarding underlying hardware
      --help           Print help
	  
Make sure to crank up <threads> if you have plenty of cores, the default is 4. Depending on the phase more threads will be launched, the setting is just a multiplier.

RAM usage depends on <threads> and <buckets>. With the new default of 256 buckets it's about 0.5 GB per thread at most.

-G option will alternate the temp dirs used while plotting to give each one, tmpdir and tmpdir2, equal usage. The first plot creation will use tmpdir and tmpdir2 as expected. 
The next run, if -n equals 2 or more, will swap the order to tmpdir2 and tmpdir. 
The next run swaps again to tmpdir and tmpdir2. This will occur until the number of plots created is reached or until stopped.


Youtube CHannel : https://www.youtube.com/channel/UC8u6GqwR7oP9FHtVhS0iFRw


Change log: 

25/06/2021 - V1.0.0 Intial release

- may contain some bugs
- screen shot - https://prnt.sc/166jngx


TBA - v1.0.1 - Added Features 

- Coming soon



Your donation will help me build new versions:

XCH: xch12zn2c05g5m0fr5r6ytyn0v3q5qfu80wyapgvzrhkm5g79fdrxtzsgus777
XFX: xfx1aq4edjr2fx3l65uennly5m72c62gavmvyj7r5cfq6wmf022y0zwqhd8hvg
BTC: 1E4Rwk4Afw49Vfi15Ee8iY8Z21Yw8cjFtq
ETH: 0x0f90dc50b87934cc4ddf1259aa7168aa4b4a37a6
