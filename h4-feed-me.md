# H4_FeedMe

## x. Why to use a feed reader (and RSS/Atom)?

Couldn't you just browse to each website? (This task does not require tests with a computer. Find suitable sources yourself if needed.).

## y. Osuuspankkikeskus port scan KKO:2003:36 

Supreme court of Finland, case Osuuspankkikeskus port scan KKO:2003:36. Have a brief look, summarize the key thing in a couple of bullets or sentences. It's in Finnish, but Firefox has offline machine translation from Finnish to English. (This task does not require tests with a computer. This task does not require thorough legal analysis of the case.)

## a. Install a feed reader
Show that it can read a feed (RSS or Atom). Include a screenshot of this. You can use any feed reader you like, and you can install the feed reader in your host OS if you like.

## b&ndash;e. Feeds
b)Add the feed for Krebs. https://krebsonsecurity.com/feed/
c) Add a feed for Schneier on Security. Find the blog, and locate the feed.
d) Find and add two more security related feeds. Explain how you found them, and why you chose them.
e) Follow security feeds for a while. What did you learn? What are the benefits and downsides of following feeds with a reader, compared to some other methods of following cyber security scene?


## f. Port scan

How can criminals know what services your employer has? Disconnect your computer from the internet while doing the test (after you have installed the required software). Do the test inside your virtual machine.
Install nmap port scanner
Disconnect from the internet. Show that 'ping 8.8.8.8' stops working when internet is disconnected.
Port scan your own computer. Use "localhost" as the address.
Install a daemon
Port scan again
Analyze and explain the results
Do not scan random computers.

## Voluntary bonuses
###g. Identify a port scan against Apache

Voluntary bonus, a bit hard: Identify a port scan against Apache on the host being scanned, e.g. in logs. Perform the test against "localhost" address and disconnect the internet while port scanning.

## Modify nmap scan
Voluntary bonus, a bit hard: Modify nmap scan so that it cannot be detected by the method you found above.


Tips:
Port scan (notes from memory)
sudo apt-get update; sudo apt-get -y install nmap
ping 1.1.1.1 # quit with Ctrl-C
sudo nmap -A -v localhost
sudo apt-get install apache2; sudo systemctl start apache2;
Do not scan computers you don't own. Disconnect computer from the internet while port scanning.

Feed readers
Thunderbird is the easiest choice
Brief is a Firefox extension, maybe it's also available for Chromium.
Newsboat 'nb' is a fast and versatile tool with proper APIs. It has some learning curve, it's Linux only and uses TUI (text user interface).
There are many other feed readers, too.
Thunderbird. Easy to install, simple graphical user interface, established project. But it's an email app first, feed reader third.
Install: Linux 'sudo apt-get update; sudo apt-get -y install thunderbird'. Windows and Mac: download installer. They even have an Android version.

Add Feed Account
Click Alt to show menu bars.
File: New: Feed Account.
Add a Feed (RSS/Atom for specific website)
"Blogs & News Feeds" is shown on Folder pane "All Folders" on the left.
Right click "Blogs & News Feeds" for context menu: Subscribe... (Same as "Manage feed subscriptions")
Feed URL: https://terokarvinen.com/index.xml
Click "Add" on the left. Only click blue "Close" after you have clicked "Add" on the left.
"Tero Karvinen..." feed appears on folder pane "All Folders", inside "Blogs & News Feeds". You can see latest articles from the website.
River of News
"River of news" means a single view that shows posts from all your subscriptions, latest first. It's quite an obvious feature of a feed reader, but in Thunderbird you have to set it up yourself.
Right click "Blogs & News Feeds" for context menu: Search Messages...
"Age in Days" "is less than" "30"
Save search as folder (button)
Name: "month". Create.
Close the search modal.
"month" appears in folder pane "All Folders", in "Blogs & News Feeds". You can see latest posts from all of the feedds you follow. It's even more interesting if you follow more than one feed.
Finding feeds
Website often has a button for RSS feed
Search the page for text: "RSS", "Atom", "Feed", "Subscribe"
Check for RSS icon, a dot with two concentric arcs
Try common URLs, like /feed/ - https://example.com/feed/
Use an addon to detect feeds, like RSSPreview
View HTML source code, search for "rss", "atom", "xml", "alternate"

## References

* Heinonen, J. n.d.: [How to Install Linux to Virtualbox?](https://github.com/johannaheinonen/johanna-test-repo/blob/main/module_1.md) GitHub repository johanna-test-repo.
* Karvinen, T. 2020: [Command Line Basics Revisited](https://terokarvinen.com/2020/command-line-basics-revisited/).
* Karvinen, T. 2022: [Cracking Passwords with Hashcat](https://terokarvinen.com/2022/cracking-passwords-with-hashcat/).
* Karvinen, T. 2026. Cyber Security – 2026 late autumn, homework h3 Cyber lab. [https://terokarvinen.com/cyber-security/#h3-cyber-lab](https://terokarvinen.com/cyber-security/#h3-cyber-lab).