# H4_FeedMe

## x. Why to use a feed reader (and RSS/Atom)?

A feed reader is a convenient way to follow different sources in one place. A person who systematically reads several different sources has to visit all of them regularly, for example daily, and pick out interesting articles or important announcements. A feed reader solves this problem. It checks the feeds a user is subscribed to and removes the need to visit each site in the browser whenever something new is published. It also lets the user read without being distracted by advertisements or unimportant content. 

From a cyber security point of view, feeds like [Unit 42](https://unit42.paloaltonetworks.com) provide up-to-date information about recently found vulnerabilities, which can be very important for those who need to be informed as soon as possible.

Some feeds publish whole articles, which allows reading offline, during a flight for example.

RSS and Atom don't necessarily require a feed reader. A feed can even be read in the terminal, though it isn't very convenient, since the output is raw XML:

```bash
curl -L https://www.schneier.com/feed/
```

For the terminal, dedicated software such as [Newsboat](https://newsboat.org/) works better.

A feed reader is the software, while RSS and Atom are standardized formats used to publish a feed. News or update feeds from an organization can also be delivered through this channel.

In short, feed readers save time and help you focus on what matters.

## y. Osuuspankkikeskus port scan KKO:2003:36 

This case shows how important it is to understand the possible consequences of actions taken online, whether the intentions behind them are good or bad.

A 17-year-old computer enthusiast attempted to gain access to the network of Osuuspankkikeskus-OPK. He used a specialised program to perform a port scan in order to:

* scan the organisation's network for open proxy servers;
* find a way to connect to the internet through those servers;
* conceal the real origin of his connection.

The attempt did not get through the organisation's firewall, but the case still offers several important lessons:

* An unsuccessful intrusion attempt can still be a crime.
* Harm does not require data to be destroyed. Having to review and strengthen security systems is itself a cost to the organisation.
* Technical expertise can increase responsibility.
* Good intentions, or the lack of a specific target, do not necessarily provide a defence.

The main takeaway of KKO:2003:36 is that attempting to gain unauthorised access to a protected computer system can create both criminal and financial liability, even when the attempt fails and no data is compromised. The court recognised that an attack can generate real costs for an organisation, independently of any data breach.


## a&ndash;e. Reader and feeds
Show that it can read a feed (RSS or Atom). Include a screenshot of this. You can use any feed reader you like, and you can install the feed reader in your host OS if you like.

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

### g. Identify a port scan against Apache

Voluntary bonus, a bit hard: Identify a port scan against Apache on the host being scanned, e.g. in logs. Perform the test against "localhost" address and disconnect the internet while port scanning.

### h. Modify nmap scan
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

* Karvinen, T. 2026. Cyber Security – 2026 late autumn, homework h4. Accessed 16.11.2026. [https://terokarvinen.com/cyber-security/#h4](https://terokarvinen.com/cyber-security/).
* Korkein oikeus. 2003. KKO:2003:36. [Precedent, Supreme Court of Finland]. Accessed 16.11.2026. [https://www.finlex.fi/en/case-law/supreme-court/precedents/2003/36](https://www.finlex.fi/en/case-law/supreme-court/precedents/2003/36).