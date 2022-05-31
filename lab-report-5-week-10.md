# Lab Report 5

To find the different results, I used `vimdiff` to see the differences between my output and the provided implementation.

![image](lab-report-5-week-10-ss/image1.png)

The highlighted portions are where the two implementations differed. Mine is on the left and the provided is on the right.

---

## Test File 1

[file 472](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/472.md)

My Output:
![image](lab-report-5-week-10-ss/image5.png)

Provided Output:
![image](lab-report-5-week-10-ss/image6.png)


Expected Output:

`/url`


The provided implementation produces the correct output. 
![image](lab-report-5-week-10-ss/image7.png)

The bug is from when I modified the code to ignore images. I set it so that if the index of `openBracket` is greater than 0, then there would be the possibility for an `!` to exist, invalidating the link. However, I never added an alternative option for when `openBracket` is at the first index followed by a valid link that should be added to `toReturn`, which is what is producing the bug in this case. 

---

## Test File 2

[file 516](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/516.md)


My Output:
![image](lab-report-5-week-10-ss/image2.png)


Provided Output:
![image](lab-report-5-week-10-ss/image3.png)


Expected Output:

`[]`


My implementation produces the correct output. The bug in the provided implementation is that it does not check whether or not there is an `!` before the brackets, which indicate that the following link is for an image, and should be ignored. 

![image](lab-report-5-week-10-ss/image4.png)

Before the index of `nextOpenBracket` is set, it should check for an `!` at the index before the `[`.

---

![image](https://media.discordapp.net/attachments/635292391330283529/955245931773689876/FB_IMG_1647811021092.jpg)