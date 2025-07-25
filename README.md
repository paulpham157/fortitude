# fortitude
If you're looking for some fortunes with attitude to fortify your ```fortune``` installation, then it's fortunate that you've stumbled on this repo!

![fortune | cowsay | lolcat](https://github.com/theodric/misfortune/raw/master/misfortune.png)

_[You may also be interested in FOTD](https://github.com/theodric/fotd), a tool that allows an MOTD file to produce an endless stream of random fortunes!_

* 9front/theo: from the 9front project, quotes from OpenBSD founder Theo de Raadt
* 9front/troll: from the 9front project, fortunes designed to provoke and annoy
* PCoK: back in the 90s/00s there was a collaborative writing/trolling site called "Pete's Compendium of Knowledge." These quotes are from there.
* alexjones: the lucid and cogent pontifications of the world's premiere policy wonk
* awobmolg: the complete text of the poetry book "All Watched Over By Machines of Loving Grace" by Richard Brautigan. Given his proximity to the early days of computing, and the free license under which he published his work ("Permission is granted to reprint any of these poems in magazines, books and newspapers if they are given away free.") it seems only appropriate to include them in my repository of fortune files.
* bash.org: ~20,000 bash.org qdb entries converted into fortunes
* billcooper: mostly quotes from ur-conspiracist William Cooper's book "Behold A Pale Horse"
* bobross: the contents of http://www.bobrossquotes.com/quotes.shtml in fortune form
* boris: Boris Johnson's hilarious witticisms
* jennyholzer: a collection of quotes from [notable quotable neo-conceptualist artist Jenny Holzer](https://en.wikipedia.org/wiki/Jenny_Holzer), of large scrolling LED sign installation fame. These quips were found in various places around the Internet, and are presented here for your confusion. If you've been through Amsterdam Schiphol airport in the last 22 years, you probably saw at least [one of her pieces](https://www.youtube.com/watch?v=6IGEoVJG39Y) there.
* minilinux: 'Zippy' Fortunes scraped from 1993's Slackware release distributed in 1995 as "MiniLinux" which could be installed and launched from within MS-DOS.
* off: these are the 'offensive' fortunes that are slowly being yoinked from distributions due to the off-the-rails level of political correctness and its associated iconoclasm currently prevailing in the Open Source world as well as our broader culture. The specific files provided here were extracted from openSUSE Tumbleweed in late November, 2024.
* princephilip: quips from the last man in Britain who wouldn't be arrested for racism
* poli: genius-level political insight
* randomquotes: if this directory exists, then it contains random quotes that I like. If not, then I haven't gotten around to creating it yet.
* zizek: sniffing and pontificating from radical Hegelian Marxist philosopher Slavoj Žižek
* cowfart.cow: a farting cow for you to use with 'cowthink' (part of the 'cowsay' package on most distributions)

Also of note in this repo is ```fortunefilecreator.sh```.
In case you couldn't guess, it creates fortune files. It's nothing special, or particularly good, but it does the job. I'm sure you can do it better: please do; I stop caring once it works. 

You feed it a text file with fortunes separated by empty lines containing linefeeds (just LF, not CRLF-- we're on UNIX, eh buddy?) and it spits out the %-delimited fortune file and runs strfile to create the requisite .dat.

Your input text file needs to look like this:

```
Alienation produces eccentrics or revolutionary.

Savor kindness because cruelty is always possible later.

In a dream you saw a way to survive and you were full of joy.
```

Running ```fortunefilecreator.sh``` with no arguments will also tell you what you need to know.

```
Takes a text file with blocks of text separated by whole blank lines and turns it into a %-delimited fortune file and a corresponding dat file.

Usage: ./fortunefilecreator.sh inputfile outputfile

Example:
 ./fortunefilecreator.sh brc.txt bobross
Output: bobross bobross.dat
Usage: fortune /path/to/bobross
```

You'll probably want to install ```fortune``` so that you have ```strfile``` installed, because you'll need it to create the dat file. Also because none of this is of much use to you without ```fortune``` installed to, you know, display the fortunes.
If you're on OSX, I recommend my fork of johnpneumann's now-archived Fortune-OSX port https://github.com/theodric/Fortune-OSX

Additionally, you'll need GNU ```sed```, and not that BSD shit that OS X ships with. Linux users will be fine; for Macs, ```brew install gnu-sed --with-default-names``` will sort you out. BSD people are on their own, but you're probably used to that by now.
Incidentally, I recommend checking the output file after you run the script just to confirm that everything is sane, i.e. no missing % (there needs to be one under each fortune) and no blank lines with a % under them (because that will result in a blank fortune). You can clean this up in a text editor, then run e.g. ```strfile bobross bobross.dat``` to regenerate the dat file.

# Thanks
Thanks to bradthemad for [his page](http://bradthemad.org/tech/notes/fortune_makefile.php) showing me what needed to be done.

Thanks to johnpneumann for [Fortune-OSX](https://github.com/johnpneumann/Fortune-OSX).

______________________________________________________________________________________

