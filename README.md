# MailExtractor
To extract mails from a website.

It is a C# library.This library gives you a hand about finding and listing e-mails in a website. It just gives the addresses at a single webpage. However, you can modify it to get mail addresses from multi-links.

How It Works

It works very simply. It gets the source code of a website as html, find matches (e-mails) via RegEx, then put it in a "MatchCollection". Then, for every "Match" in "MatchCollection", it adds the "Match" to mail's body. Then send it to the address that you want.

How To Use

It's very simple to use.First you should create a "MailInfos" object. Then fill its properties by hand or from a form. Finally,you should invoke the "execute" function, in "func" class. To invoke it, you should give it a "MailInfos" object and a website.

Example

A website : "https://eksisozluk.com/ilginc-e-mail-adresleri--1434320"

An example mail (Splitted by ", "(includes space)): Bodyyemin@walla.com, yemin@walla.com, yemin@walla.com, sevmisim_vermiyorlaryourname@example.com, adimgobekadimsoyadim@tirtmail.com, lmaz@gmail.com, neytavuk_hayvanmi@xxx.com, g_sivrisinek@falancamail.com, pilavustu@xxx.com, ateshlipilich@xxx.com, pirzola@kasapnuri.com.tr,
