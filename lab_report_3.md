# CSE 15L Lab Report 3: Researching Commands
The text processing commands, such as `less`, `find`, and `grep`, aim to manipulate and analyze text files. These commands can preview text contents, search for specific files/directories, sort out specific patterns or strings of text, and perform many other complex operations.

In this lab report, we will focus on the functionality and various command-line options of the `grep` command.

## Functionality of the `grep` command
The `grep` command is a powerful tool for searching for patterns in text files. It search a file or files for the given string and print matching lines. Its format is `grep <string> <file name>`.

In the next four section, we will go through four interesting `grep` options with their specific functionality. There would be 2 examples using each option. Note that all examples are operations on files and directories from ./technical from the repository [docsearch](https://github.com/ucsd-cse15l-s23/docsearch).

## Command-line option: `-i`
The command-line option `-i` ignores case distinctions between upper and lower cases in both the pattern and the input files.

**Example 1:**
```
grep -i "flight" technical/911report/*.txt
```
By running this command, we get output displaying every line that contains "flight" regardless of case sensitivity from all txt files in directory `technical/911report/`. The below codeblock shows a portion excerpted from the actual output:
```
...
technical/911report/chapter-9.txt:     the 17 minutes from the crash of the hijacked American Airlines Flight 11 into
technical/911report/chapter-9.txt:     the 56 minutes from the crash of the hijacked United Airlines Flight 175 into
technical/911report/chapter-9.txt:     At 8:46:40, the hijacked American Airlines Flight 11 flew into the upper portion of
technical/911report/chapter-9.txt:     At 9:03:11, the hijacked United Airlines Flight 175 hit 2 WTC (the South Tower) from
technical/911report/chapter-9.txt:     and handrails were a significant help. Several flights down, however, the evacuee
technical/911report/chapter-9.txt:     Some officers positioned themselves at the top of a flight of stairs by 5WTC that led
technical/911report/chapter-9.txt:     At 9:37, the west wall of the Pentagon was hit by hijacked American Airlines Flight
technical/911report/chapter-9.txt:     of a very few civilians could have caused a dangerous and panicked mob flight. But
hongweicong@Wendys-MacBook-Air docsearch % grep 
```

**Example 2:**
```
grep -i "CIRCADIAN" technical/biomed/*.txt
```
By running this command, we get output displaying every line that contains "circadian" regardless of case sensitivity from all txt files in directory `technical/biomed/`. The below codeblock shows a portion excerpted from the actual output:
```
...
technical/biomed/1472-6793-1-6.txt:     less active phases of the mouse circadian cycle. Future
technical/biomed/1472-6874-2-13.txt:     control for circadian rhythm in hormone levels. Serum and
technical/biomed/cc1498.txt:     not affect the circadian adrenocortical patterns and the
technical/biomed/gb-2001-2-3-research0008.txt:     drive circadian rhythms in locomoter activity [ 16, 17].
technical/biomed/gb-2001-3-1-research0001.txt:     functional, they seem to be for the control of circadian
technical/biomed/gb-2001-3-1-research0001.txt:     signals [ 31, 36, 51]. ABA, auxin, light and circadian
technical/biomed/gb-2002-3-9-research0045.txt:     difference. During a more complete study of the circadian
technical/biomed/gb-2002-3-9-research0045.txt:     expression with a circadian rhythm [ 41]. From the data
```

The `grep -i` command is useful when you want to perform a case-insensitive search using the grep tool. By using the `-i` option, grep will neglect the case sensitivity of the search pattern, allowing you to match text regardless of whether it is in uppercase or lowercase.

## Command-line option: `-v`
The command-line option `-v` inverts the sense of the search, which means it shows only the lines that do not match the given pattern.

**Example 1:**
```
grep -v "the" technical/911report/chapter-1.txt
```
By running this command, we get output displaying every line that does not contain "the" from the file `technical/911report/chapter-1.txt`. The below codeblock shows a portion excerpted from the actual output:
```
"WE HAVE SOME PLANES"
INSIDE THE FOUR FLIGHTS
    Boston: American 11 and United 175. Atta and Omari boarded a 6:00 A.M. flight from Portland to Boston's Logan International Airport.
    Between 6:45 and 7:40, Atta and Omari, along with Satam al Suqami, Wail al Shehri, and Waleed al Shehri, checked in and boarded American Airlines Flight 11, bound for Los Angeles. The flight was scheduled to depart at 7:45.
    Their flight was scheduled to depart at 8:00.
    The 19 men were aboard four transcontinental flights.
...
```

**Example 2:**
```
grep -v "a" technical/911report/chapter-1.txt
```
By running this command, we get output displaying every line that does not contain "a" from the file `technical/911report/chapter-1.txt`. The below codeblock shows a portion excerpted from the actual output:
```
"WE HAVE SOME PLANES"
INSIDE THE FOUR FLIGHTS
IMPROVISING A HOMELAND DEFENSE
United Airlines Flight 175
    Center: Do you know who he is?
    FAA: Yes.
...
```

The `grep -v` command is useful when you want to find the non-matching pattern in grep. The `-v` option allows you to exclude lines that match a specific pattern. The pattern is case sensitive for the `-v` option.

## Command-line option: `-c`
The command-line option `-c` counts the number of matching lines.

**Example 1:**
```
grep -c "human" technical/biomed/*.txt
```
By running this command, we get output displaying a count of lines containing "human" for each txt file under the directory `technical/biomed`. The below codeblock shows a portion excerpted from the actual output:
```
...
technical/biomed/rr171.txt:10
technical/biomed/rr172.txt:10
technical/biomed/rr191.txt:19
technical/biomed/rr196.txt:15
technical/biomed/rr37.txt:0
technical/biomed/rr73.txt:1
technical/biomed/rr74.txt:0
```

**Example 2:**
```
grep -c "U.S." technical/911report/*.txt
```
By running this command, we get output displaying a count of lines containing "U.S." for each txt file under the directory `technical/biomed`. The below codeblock shows a portion excerpted from the actual output:
```
...
technical/911report/chapter-2.txt:32
technical/911report/chapter-3.txt:110
technical/911report/chapter-5.txt:48
technical/911report/chapter-6.txt:71
technical/911report/chapter-7.txt:22
technical/911report/chapter-8.txt:37
technical/911report/chapter-9.txt:2
technical/911report/preface.txt:0
```

The `grep -c` command is useful when you want to count the number of lines that match a specific pattern using the grep tool. The `-c` option allows you to obtain a count of occurrences without displaying the actual matching lines. The pattern is case sensitive for the `-c` option.

## Command-line option: `-w`
The command-line option `-w` matches only whole words, which means it treats the given pattern as a whole word and searches for lines that contain the exact given word.

**Example 1:**
```
grep -w "flight" technical/911report/*.txt
```
By running this command, we get output displaying every line that contains the whole word "flight" from all txt files in directory `technical/911report/`. The below codeblock shows a portion excerpted from the actual output:
```
...
technical/911report/chapter-8.txt:     goals." He also believed Moussaoui's plan was related to his flight training.
technical/911report/chapter-8.txt:     Paris regarding "subjects involved in suspicious 747 flight training" that described
technical/911report/chapter-8.txt:     was not unusual for Middle Easterners to attend flight training schools in the
technical/911report/chapter-8.txt:     interested to learn the doors do not open in flight, and wanted to fly a simulated
technical/911report/chapter-8.txt:     flight from London to New York. He was told that the FBI had arrested Moussaoui
technical/911report/chapter-9.txt:     Some officers positioned themselves at the top of a flight of stairs by 5WTC that led
technical/911report/chapter-9.txt:     of a very few civilians could have caused a dangerous and panicked mob flight. But
```

**Example 2:**
```
grep -w "Circadian" technical/biomed/*.txt
```
By running this command, we get output displaying every line that contains the whole word "Circadian" from all txt files in directory `technical/biomed/`. The below codeblock shows the actual output:
```
technical/biomed/1471-213X-1-9.txt:     Circadian rhythms, synchronized to external
technical/biomed/1471-213X-1-9.txt:     Rhythms of mNocmRNA Abundance are Circadian in
technical/biomed/1471-2202-3-20.txt:     Circadian gene expression in the brain of cry1,2
technical/biomed/1471-2202-3-5.txt:     Circadian clocks located within metazoan brains have
technical/biomed/1471-244X-3-5.txt:     level of light exposure. Circadian rhythms in postpartum
```

The `grep -w` command is useful when you want to perform a whole-word search using the grep tool. The `-w` option allows you to match only those lines that contain the specified pattern as a whole word, rather than partial matches within words. The pattern is case sensitive for the `-w` option.

## Sources
To complete this lab report, I consulted the following websites for `grep` command-line options:
- [Wikibooks: Grep](https://en.wikibooks.org/wiki/Grep)
- [GeeksforGeeks: grep command in Unix/Linux](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
