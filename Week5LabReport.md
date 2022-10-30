# **Week 5 Lab Report - grep command and options**

In this project we will use the command ``` grep [options] pattern [files] ```, where option is our special command line option to make grep function differently. 
---

## -n : Display the matched lines and their line numbers.
- full command: ``` grep -n pattern [files] ```

**Command in action**
``` 
grep -n "chapter" technical/*/*.txt > matchedlines.txt
vim matchedLines.txt

technical/911report/chapter-1.txt:560:    Others in the agency were aware of it, as we explained earlier in this chapter.
technical/911report/chapter-10.txt:162:                chapter 3). Ashcroft told us he was determined to take every conceivable action,
technical/911report/chapter-10.txt:420:                Iraqi intelligence officer (discussed in chapter 7) and a Polish report that
technical/911report/chapter-11.txt:226:                (reprinted in chapter 4), brought the focus back to more traditional hostage taking;
technical/911report/chapter-11.txt:299:                the main focus (war in Korea), and as too unrealistic. As we pointed out in chapter
```
**what it’s doing and why it’s useful.**
- The -n prints the line number of the desired result, the path to that file, and the line its self.
- This is useful because normal grep just prints out file path. For example, what happens when you want to go to that line in the text document but it is 10,000+ lines long? With this you can search for the exact line number and change it if needed. In addition it gives you incite on how that word was used.

```
grep -n "month" technical/*/*.txt > matchedlines.txt
vim matchedLines.txt

technical/911report/chapter-10.txt:566:                    secured-after arduous effort-by the end of that month.
technical/911report/chapter-10.txt:588:            Within about two months of the start of combat operations, several hundred CIA
technical/911report/chapter-11.txt:70:            As best we can determine, neither in 2000 nor in the first eight months of 2001 did
technical/911report/chapter-11.txt:165:                months before 9/11:"It would be a mistake to redefine counterterrorism as a task of
technical/911report/chapter-11.txt:192:                network was a nuisance that killed a score of Americans every 18-24 months. If that
technical/911report/chapter-11.txt:437:                been required, extending over months and perhaps years, with associated costs and
technical/911report/chapter-12.txt:504:                disbelief and denial. In the following months, as the truth became clear, some
```
**what it’s doing and why it’s useful.**

- Here is another example of how to see if the word "month" was in any of the txt files. It gave us the path location and line location with a short description of what was said.

```
grep -n "day" technical/*/*.txt > matchedlines.txt
vim matchedLines.txt

technical/911report/chapter-1.txt:6:    Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied themselves for work. Some made their way to the Twin Towers, the signature structures of the World Trade Center complex in New York City. Others went to Arlington, Virginia, to the Pentagon. Across the Potomac River, the United States Congress was back in session. At the other end of Pennsylvania Avenue, people began to line up for a White House tour. In Sarasota, Florida, President George W. Bush went for an early morning run.
```
**what it’s doing and why it’s useful.**

- Lastly, here is another example of how we can see if a word like "day" was used in any of these documents. This gives us the path of the file as well as the line number and short description.

---

## -i : Ignores, case for matching
- full command: ``` grep -i pattern [files] ```

**Command in action**

```
grep -i "Chapter" technical/*/*.txt > matchedlines.txt
vim matchedLines.txt

technical/911report/chapter-1.txt:    At the same time or shortly thereafter, Atta-the only terrorist on board trained to fly a jet-would have moved to the cockpit from his business-class seat, possibly accompanied by Omari. As this was happening, passenger Daniel Lewin, who was seated in the row just behind Atta and Omari, was stabbed by one of the hijackers-probably Satam al Suqami, who was seated directly behind Lewin. Lewin had served four years as an officer in the Israeli military. He may have made an attempt to stop the hijackers in front of him, not realizing that another was sitting behind him.
technical/911report/chapter-1.txt:    No one at the FAA or the airlines that day had ever dealt with multiple hijackings. Such a plot had not been carried out anywhere in the world 
```

**what it’s doing and why it’s useful.**
- This ignores the capitalization of our search. Furthermore, this is useful when we want both lowercase and upper case results combined or if we don't know if that word is capitalized or not. For example, if I didn't use the -i option matchedlines.txt would be a blank document because non of the chapters are capitalized.

```
grep -i "Chapter" technical/*/*.txt > matchedlines.txt
vim matchedLines.txt
~                                                                                    
~                                                                                    
~                                                                                    
~                                                                                    
~                                                                                    
~                                                                                    
~                                                                                    
~                                                                                    
~                                                                                    
~                                                                                    
~                                                                                    
"matchedLines.txt" 8L, 1006B

```
**what it’s doing and why it’s useful.**
- This example was given to show why -i is important because without it we can lose results we wanted. As shown above we got a blank document because non of the C's in chapter were capitalized in the txt files.

```
grep -i "Chapter" technical/*/*.txt > matchedlines.txt
vim matchedLines.txt

technical/911report/chapter-10.txt:                    secured-after arduous effort-by the end of that month.
technical/911report/chapter-10.txt:            Within about two months of the start of combat operations, several hundred CIA
```
**what it’s doing and why it’s useful.**
- Same thing with Month if there was no -i then the document would have been blank. This is due to the fact that non of the files had Month with a capital M.
---


## -c : This prints only a count of the lines that match a pattern
- full command: ``` grep -c pattern [files] ```

**Command in action**

```
grep -c "chapter" technical/*/*.txt > matchedLines.txt
vim matchedLines.txt


technical/911report/chapter-1.txt:1
technical/911report/chapter-10.txt:2
technical/911report/chapter-11.txt:6
technical/911report/chapter-12.txt:5
technical/911report/chapter-13.1.txt:10
technical/911report/chapter-13.2.txt:0
technical/911report/chapter-13.3.txt:1
technical/911report/chapter-13.4.txt:8
technical/911report/chapter-13.5.txt:13
technical/911report/chapter-2.txt:2
technical/911report/chapter-3.txt:6
technical/911report/chapter-5.txt:4
technical/911report/chapter-6.txt:8
technical/911report/chapter-7.txt:4
```
**what it’s doing and why it’s useful.**
- This command option prints out the file path along with the number of occurrences of the desired search. This could be useful for maybe a professor teaching teaching an english class wanted to know the most overly used word in students essays so they could teach substitutes for that word. 

```
grep -c "Weeks" technical/*/*.txt > matchedLines.txt
vim matchedLines.txt

technical/911report/chapter-1.txt:0
technical/911report/chapter-10.txt:0
technical/911report/chapter-11.txt:0
technical/911report/chapter-12.txt:0
technical/911report/chapter-13.1.txt:0
technical/911report/chapter-13.2.txt:0
technical/911report/chapter-13.3.txt:0
technical/911report/chapter-13.4.txt:0
```
- This also could be useful for CSE30 TA's to make sure no illegal methods were used in any projects from the C library to make the project easier. Additionally, for me it could be useful for seeing the number of times I have used a particular identifier in my code.


```
grep -c "Weeks" technical/*/*.txt > matchedLines.txt
vim matchedLines.txt

technical/911report/chapter-13.5.txt:30
technical/911report/chapter-2.txt:0
technical/911report/chapter-3.txt:0
technical/911report/chapter-5.txt:0
technical/911report/chapter-6.txt:0
technical/911report/chapter-7.txt:0
technical/911report/chapter-8.txt:0
technical/911report/chapter-9.txt:40

```

- With large data sets, it could also be useful for seeing the number of occurrences of a particular search example. For example, maybe you want to know the number of blue cars pulled over.  