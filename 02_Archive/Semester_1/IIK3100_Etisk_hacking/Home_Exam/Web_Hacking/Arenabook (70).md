# Flag

> **UiO-Hacking-Arena{Sigurd_is_a_flink_bisk}**

# Prompt

> **Hi, Check out the latest social media platform: [http://sidious.hackingarena.com:803](http://sidious.hackingarena.com:803/) Sandra already tried it. :)**

# Solution

Entering the website, I immediately see that I can search up an user and check out information regarding the person and their username.

Inputting Sandra resulted in the username - "serdodisen" and facts regarding her current living situation, hobbies and her family.

The fact that I have gotten her username, hints me towards an attempt to log onto her account (not really a nice thing to do) by pressing "sign in".

Since I don't have a password, I'll begin with "Forgot password" instead. Entering the username "serdodisen" in the text field, I am further asked to enter the place of birth of her grandmother.

This information can be further researched based on the facts about Sandra an her family. The fact that her whole family being born in Telemark county, tells me that I simply have to brute force every village from Telemark. ([Wikipedia](https://en.wikipedia.org/wiki/List_of_villages_in_Telemark))

I imported the table of villages from Wiki to Excel and adjusted the formatting by removing symbols and unnecessary information. Applied it to the attack payload by "Simple list"

![[Pasted image 20241024135735.png]]

From Kali I used **BurpSuite** to intrude and attack the text field with the list of villages I had collected. The result is the largest length response, village called "Vinjastranda" and password "MyDogNameIsSigurd". After logging in, I'm greeted by the flag "UiO-Hacking-Arena{Sigurd_is_a_flink_bisk}"


# Additional Info

Alternative solution after collecting all villages of Telemark, is to use Hydra to attack the website and page "forgot password"

```
hydra -L Desktop/villages -p '' sidious.hackingarena.com -s 803 http-post-form "/forgot/reminder.php:birthplace=^USER^:incorrect answer"
```

* -L villages.txt: Specifies file of villages
* -p '': Specifies an the empty field for villages
* sidious.hackingarena.com: Target web domain
* -s 803: Web server port (non-standard port)
* http-post-form: Use a POST form module
* "/forgot/reminder.php:birthplace=^USER^": Specify page and form field for birthplace, replacing ^USER^ with the villages.
* :incorrect answer: Message returned by webpage when post fails

Running the command returns the attempt and hopefully a password return if succeeded.

![[Pasted image 20241024141838.png]]

Further steps is as mentioned above, logging in and retrieving the flag.