# VanBitCrakcen GUI

![image](https://github.com/Mizogg/VanBitCracken-GUI/assets/88630056/166b14cf-c83a-473c-a586-60b7827c0c83)

## GET it HERE https://mizogg.co.uk/vanbitcrakcen/

# VanBitCrakcenS
VanBitCracken Spread

This is the VanBitCracken Spread Version. The Spread means that this specific version is geared towards covering ranges, not doing any random mode.  The random mode will come later.

This is a fork of Jean Luc Pons Vanity Search program and Telariust's Vanity Search Bitcrack program.  

You can use the flags/options that the program known as "Bitcrack" uses, except the -b -t -p options.  This program uses the grid size options that JLPs version used in version 15.  If you want to adjust grid size, use the -g option.  Since this is based off of version 15, the y grid size is hard coded so all you can adjust is the x grid size.

Example: -gpu -g 512 -gpuId 0 .

The other bonus feature of this program versus Bitcrack is it supports multiple GPUs.

The other difference from Bitcrack is this program will search for partial/strings of addresses and does not need a full address and can search for wildcards.

I will update this more in-depth later.

Other flags include:

-t for CPU threads (not optimized for CPU use, that was not the intent/focus)

-gpu for gpu use
-gpuId 0 (if more than one gpu use -gpuId 0,1,2,3,4  etc.)

-g to adjust x grid size; -g 256

--keyspace to enter your start and end range; example 80000:FFFFF

--continue to save work/progress; --continue continue.txt

-o for output/results file; -o outputfile.txt (if you do not add -o option, keys found will print on screen and to a text file named "KeysFound.txt")

-i for input file of addresses/strings; -i inputfile.txt

-r for rekey; -r 100000
the -r is important because in this spread version, it really tells the program how often to save your continue file in MKey/s. Based on your gpu and its MKey/s, you need to adjust the -r.  If your gpu's speed is 100 MKey/s and you want to save your continue file every minute, then you would calculate 60 (seconds) multiplied by 100 = 6000; so you would want to input -r 6000. If you do not input a -r it will go to the default of 10000 and depending on your card you could be saving every 5 to seconds (not recommended.)
You can also enter a single address/string at the end of your command line/batch file; comannd line ....... 19Hed12

Basic command line/batch file:
VanBitCrackenS1 -t 0 -gpu -gpuId 0 -r 150000 --keyspace 8000:FFFF -o output.txt -i input.txt (or just add address/string instead of input file)
pause

More to follow...



# VanBitCrackenRandom
VanBitCracken Random
Here is VBCRandom in action.
Batch file settings:
```
VBCRandom -t 0 -gpu -gpuId 0 -topr 8000000000000000 -subr 48 -r 480 --keyspace 8000000000000000:FFFFFFFFFFFFFFFF -o randomtest.txt 16jY7q
```

Results:
```
Started Sat Aug 28 12:32:28 2021
Start Range  :  8000000000000000
End   Range  :  FFFFFFFFFFFFFFFF
Searching For:  16jY7q
Compression  :  Compressed
CPU threads  :  0
GPU          :  GPU #0 NVIDIA GeForce GTX 1060 6GB (10x128 cores) Grid(80x512)

Random Key   :  800007AC8B3D5525
Random Key   :  8000201C33F5235B
Random Key   :  8000E2F090E63C7D
 [00:00:04 Run Time ] [Speed 82.524 MK/s] [Total Keys: 335,544,320] [# Rekeys: 0] [Found: 2]
Random Key   :  8000208FB1B474F6
Random Key   :  8000B9FC61E9ABA1
Random Key   :  8000F0310FBE3DD2
 [00:00:08 Run Time ] [Speed 82.563 MK/s] [Total Keys: 671,088,640] [# Rekeys: 1] [Found: 4]
Random Key   :  80004698D58E9E8F
Random Key   :  800089612D96CDA0
Random Key   :  8000C2190CD91261
 [00:00:15 Run Time ] [Speed 81.609 MK/s] [Total Keys: 1,258,291,200] [# Rekeys: 2] [Found: 6]
Random Key   :  800043E67DBAB51D
Random Key   :  800098B29829B7A7
Random Key   :  800045B53E8E1753
 [00:00:20 Run Time ] [Speed 79.286 MK/s] [Total Keys: 1,593,835,520] [# Rekeys: 2] [Found: 6]
 ```

Key results:
```
Pub Addr: 16jY7qzxujzi1K7GaEc17ZFokFymagY3jG
Priv (WIF): p2pkh:KwDiBf89QgGbjEhKnhXJuH7LrciVrZi3qYvLz94bU7Lw952JxZUX
Priv (HEX): 0x000000000000000000000000000000000000000000000000800015BE8DF950C5

Pub Addr: 16jY7qdry8xB4v6JeMH2R3ViVTSTzDGv2B
Priv (WIF): p2pkh:KwDiBf89QgGbjEhKnhXJuH7LrciVrZi3qYvLzUZ1qwKHqCmVgPRj
Priv (HEX): 0x000000000000000000000000000000000000000000000000800064574E06912E

Pub Addr: 16jY7qwSUyCss5jZYDjgJofLe7KgKxiCQo
Priv (WIF): p2pkh:KwDiBf89QgGbjEhKnhXJuH7LrciVrZi3qYvLzGCmCHBUm9fupLgz
Priv (HEX): 0x0000000000000000000000000000000000000000000000008000328A78D70051

Pub Addr: 16jY7q7x9EjwysPAYtappeDX6Lqtm32ekf
Priv (WIF): p2pkh:KwDiBf89QgGbjEhKnhXJuH7LrciVrZi3qYvLzCiYnMdjWKzRsXUn
Priv (HEX): 0x0000000000000000000000000000000000000000000000008000247B3183BFDC

Pub Addr: 16jY7qTWTgUzCEEH7E9UFxVKALnvCcykwV
Priv (WIF): p2pkh:KwDiBf89QgGbjEhKnhXJuH7LrciVrZi3qYvLziDMQ1SzkL55t52w
Priv (HEX): 0x00000000000000000000000000000000000000000000000080009B6E64AE0CAD

Pub Addr: 16jY7qwSwoyaH2NT2dKsY15h11Gma5bccb
Priv (WIF): p2pkh:KwDiBf89QgGbjEhKnhXJuH7LrciVrZi3qYvLzSjUdaY9XWkAo8pE
Priv (HEX): 0x00000000000000000000000000000000000000000000000080005D00CB38A1B5

Pub Addr: 16jY7qCNptT19yStBa3tgVFy2k7CvhLi8t
Priv (WIF): p2pkh:KwDiBf89QgGbjEhKnhXJuH7LrciVrZi3qYvM13ZD8mLPHJMsj9c6
Priv (HEX): 0x0000000000000000000000000000000000000000000000008000E96EBB6FFC70

Pub Addr: 16jY7q3WZumGZ4gbrDTSte9JTbhEniZpqP
Priv (WIF): p2pkh:KwDiBf89QgGbjEhKnhXJuH7LrciVrZi3qYvLzLQVfZGJ81tzYnbi
Priv (HEX): 0x0000000000000000000000000000000000000000000000008000437CBF9A4063

Pub Addr: 16jY7qSaxGdCNribBnf6oxcpaw7aBUA6nN
Priv (WIF): p2pkh:KwDiBf89QgGbjEhKnhXJuH7LrciVrZi3qYvLzMkoUUXmUpiqDSm1
Priv (HEX): 0x000000000000000000000000000000000000000000000000800048EE90360155

Pub Addr: 16jY7qSV4qyaXJNmwWCu2t4DRWHuTnQuwz
Priv (WIF): p2pkh:KwDiBf89QgGbjEhKnhXJuH7LrciVrZi3qYvLz9toCoHuQiZuBD2p
Priv (HEX): 0x000000000000000000000000000000000000000000000000800019188671357A

Pub Addr: 16jY7qJ3MdatyubzBQ4e67n5D2iJRqFrDY
Priv (WIF): p2pkh:KwDiBf89QgGbjEhKnhXJuH7LrciVrZi3qYvLzZLFmMZj3v26fWhh
Priv (HEX): 0x0000000000000000000000000000000000000000000000008000779DFF73D53B
```

See how every new random key is within the same 48 bit range? Now you could change the -topr to whatever toprange and the -subr to whatever subrange. If in the example above you wanted to search every possible range in the toprange of 8000000000000000, you would use -topr 8000000000000000 and -subr 60.

Make sense?

use the -b for compressed and uncompressed.
