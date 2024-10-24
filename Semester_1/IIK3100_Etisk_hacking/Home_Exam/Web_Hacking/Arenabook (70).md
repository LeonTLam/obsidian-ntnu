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

