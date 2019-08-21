# University of New Brunswick's CTF 2019 Writeup

## Background Information
This is my first Capture The Flag (CTF) competition that I’ve ever participated in. I joined the Cyber Security Club at my school where our club highly encouraged members to give these competitions a shot to test our current knowledge of web applications. I had taken a bunch of networking courses in my previous semester so I thought I would give it shot and really apply what I learn to this competition. 
The club gets together on a weekly basis to test out new web application tools off the Kali Linux distribution, so I had pretty good working knowledge of when to use these tools at the right time. 

##  My attempt at only three of the challenges:  
I attempted was the  *Exploit The Code* as my first challenge. I took a look at the PHP script and immediately turned to Google to understand the whole idea of what’s being passed down to the flag variable. From my research online; the string called ` flag_is_here` is what’s being decoded as stated in the script, and where the initial value for the string is its Unicode equivalent. For example; if I put in: `kevin’s%25first%25challenge` into the url bar would be decoded as `kevin’s_first_challenge`. From there I saw that if I attempted to write my string in unicode, it would trigger the IF statement and reveal the flag. I put in: `<name of host address>/php?flag=flag%5Fis%5Fhere` but didn’t reveal the flag. I tried everything from checking the syntax to seeing if I called the php script correctly by its name and URL formatting. I probably would have put a period to call the script instead of a slash to call the script. I unfortunately didn’t get the flag for this challenge. 
  
I moved onto the second challenge which was the *SQL Injection challenge*. At first, I tried to provoke a error by adding in single quotations to reveal what kind of SQL error was generated and attack it that way. That didn’t work so I used **OWASP ZAP Proxy** to do an initial scan to see if an injection was possible. After pasting the URL from ZAP Proxy into the URL bar, I fail to bypass the login screen and wasn’t able to retrieve the flag. 

I moved onto the third and final  challenge called *Find the Password* where you need to crack the password to reveal the flag. I tried to brute force into the page in Kali Liunx by seeing if I can retrieve a GET request that has the PHP cookie embedded in it. I also tried simple password guesses like test123, password and many other easy to guess passwords. I didn’t obtain the flag but had a close feeling that the flag itself was revealed on the screen as:  `flag{ (Find)[thePassword] }`. 


In the future, I would prefer to work with a group where we all share our knowledge and experience of doing these challenges with one another so that I may have a better result for my next CTF endeavor!

Thanks for taking the time to read my writeup! :)






