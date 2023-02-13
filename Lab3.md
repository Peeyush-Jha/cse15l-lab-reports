# LAB REPORT 3
## Reseraching Commands
I have chosen `grep` command for this lab report. Therefore, in the following report I will give 4 interesting command-line options to use `grep`. I will be writing the commands inside the `/written_2` directory. This means `/Users/Documents/GitHub/docsearch/written_2` will be my present working directory.
   
**1) `-m [num]` option -**
Suppose we want to search for a limited occurence of the string, how should we go about it? If we just use `grep` then we will get all the occurences of the string in the spcified file. To solve this issue, we can use `-m` option.  

* Example 1 - 

```
grep -m 3 "Paris" travel_guides/berlitz1/HistoryFrance.txt
```

Output of Example 1 -

```
converting to Christianity ten years later. With Paris as his capital,
plundering Paris in 845. In addition, Saracens invaded the Provençal
churches, the soaring Gothic cathedrals of Chartres, Paris
```
Here, since we specified `-m 3`, we got only 3 occurences of "Paris" in the file.
* Example 2 -
```
grep -m 2 "Cairo" travel_guides/berlitz1/WhereToEgypt.txt
```

Output of Example 2 -

```
Cairo and the Pyramids
century, Cairo — Al-Qahira or “the City of Victory” —  became one of
```

Here, since we specified `-m 2`, we got only 2 occurences of "Cairo" in the file.

So we can say that `grep -m [num]` is used to read the file until "num" matches of the specified string are found and print out those "num" lines. 

I found this option by using the command `man grep` on terminal.

**2) `-i` option -**
If I write `grep "gReeCe" travel_guides/berlitz2/Athens-Intro.txt` I will get no output despite the fact that the file contains the string "Greece" in it. This is because `grep` is case-sensitive so "gReeCe" and "Greece" are treated differenty. To combat this issue, we use `-i` option.

* Example 1 -
```
grep -i "gReeCe" travel_guides/berlitz2/Athens-Intro.txt
```

Output of Example 1 -

```
However, the city of Athens is more than a sum of these ancient parts. 
Though it disappeared from the record books following the decline of the Roman Empire in the fifth century — 
its lineage and magnificent monuments unappreciated — 
it has risen like a phoenix from the ashes since 1834, the year that it became capital of the modern country of Greece. 
```
* Example 2-

```
grep -i "wILLiam saYLe" travel_guides/berlitz2/Bahamas-History.txt
```

Output of Example 2 - 

```
In 1648 a group of English Puritans from Bermuda, led by William Sayle, sailed to Bahamian waters 
and established the first permanent European settlement on the island they named Eleutheria (now Eleuthera)
after the Greek word for freedom.
```

We are getting the above outputs due to the fact that `grep -i` treats uppercase and lowercases similarly. This option should be used when you want your grep search to be case-insensitive

I found this option with the help of this [webpage](https://en.wikibooks.org/wiki/Grep)

**3) `-o` option -**
In order to print just the specified part of the line instead of the whole line we can use `-o` option. This definition will become clear after going through the below examples.

* Example 1 -
 
```
grep -o "Indus river" travel_guides/berlitz1/*.txt
```

Output of Example 1 -

```
travel_guides/berlitz1/HistoryIndia.txt:Indus river
travel_guides/berlitz1/HistoryIndia.txt:Indus river
```
This output tells us that `HistoryIndia.txt` file has the string "Indus river" mentioned twice in the text.

* Example 2 -

```
grep -o "Bond Stores" non-fiction/OUP/*/*.txt
```
Output of Example 2 -

```
non-fiction/OUP/Abernathy/ch1.txt:Bond Stores
non-fiction/OUP/Abernathy/ch1.txt:Bond Stores
non-fiction/OUP/Abernathy/ch1.txt:Bond Stores
non-fiction/OUP/Abernathy/ch1.txt:Bond Stores
non-fiction/OUP/Abernathy/ch1.txt:Bond Stores
non-fiction/OUP/Abernathy/ch1.txt:Bond Stores
non-fiction/OUP/Abernathy/ch2.txt:Bond Stores
```
This output is showing us all the occurences of "Bond Stores" in the file `non-fiction/OUP/*/*.txt`. In other words, "Bond Stores" appear 7 times inside the `non-fiction/OUP` directory

Hence `grep -o` prints only the matching part of the lines and could be useful if we don't want the whole line, but just want the specified string occurences.  

I found this option by using the command `man grep` on terminal.

**4) `-n` option -**
In order to find the line number in the text at which the string occurs, we can use `-n` option 

* Example 1 -
 
```
grep -n "Hollywood" travel_guides/berlitz1/HistoryLasVegas.txt
```

Output of Example 1 -

```
169:        Hollywood flair and the new Vegas flash. But the Mafia bosses who
179:        busily selling Las Vegas as a glamorous Hollywood in the desert. From
189:        Hollywood stars came as well, simply because Las Vegas was the place to
```
This output tells us that the string "Hollywood" has been used in the file `travel_guides/berlitz1/HistoryLasVegas.txt` exactly 3 times at lines 169, 179 and 189.

* Example 2 -

```
grep -n "Buddha" travel_guides/berlitz1/IntroIndia.txt
```

Output of Example 2 -

```
266:        Buddha’s own life explains his teachings, but the truth is
284:        truly Enlightened — Buddha as he is called today. He preached his new
286:        to spread his word. Buddha himself converted ruthless bandits and whole
291:        desire, Buddha had advocated the Middle Way of the Eightfold Path:
295:        This original doctrine, without any sense of Buddha’s
311:        b.c. in Bihar and, like Buddha, was the son of a chief. He, too,
```
This output tells us that the string "Buddha" has been used in the file `travel_guides/berlitz1/IntroIndia.txt` exactly 6 times at lines 266, 284, 286, 291, 295 and 311.

Hence `grep -n` prints the lines along with the numbers of those lines in the file which contain the specified string.

I found this option by using the command `man grep` on terminal.

---

That was it for Lab Report 3. Thanks a lot for reading this page !!!
