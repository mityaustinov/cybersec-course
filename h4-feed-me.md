# H4_FeedMe

## x. Why to use a feed reader (and RSS/Atom)?

A feed reader is a convenient way to follow different sources in one place. A person who systematically reads several different sources has to visit all of them regularly, for example daily, and pick out interesting articles or important announcements. A feed reader solves this problem. It checks the feeds a user is subscribed to and removes the need to visit each site in the browser whenever something new is published. It also lets the user read without being distracted by advertisements or unimportant content. In comparison to social media user can decide what can be there in their feed and not algorithms. 

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

I have previously, as a [voluntary task](h2-scene#feed-reader) already installed [NetNewsWire](https://netnewswire.com/) RSS reader and subscribed to several feeds.

<img src="assets/images/netnewswire2.png" alt="NetNewsWire interface" width="800" />

*Figure 1. NetNewsWire interface with list of subscriptions and opened article.*

* [Krebs on Security](https://krebsonsecurity.com/feed/) (Fig. 1)
* [Schneier on Security](https://www.schneier.com/feed/) (Fig. 1)
* I'm also subscribed for several other feeds:
	* [DarknetDiaries](https://podcast.darknetdiaries.com/) I follow the podcast already for six years now, but it is more convenient to learn about a new episode this way than check, for example in Spotify. I searched for "darknet diaries RSS feed".
	* [Unit 42](https://unit42.paloaltonetworks.com/feed/) Recent updates on cyber security threats. I simply added `/feed` to the address I knew. 
	* [NextJS Release Notes](https://github.com/vercel/next.js/releases.atom) and [React Release Notes](https://github.com/react/react/releases.atom) These are important, because I work a lot with ReactJS and NextJS and sometimes it is important to learn quickly, that a new version has been released. GitHub provides such feeds for public repositories.
 
As I mentioned before, I started using feed reader a while ago. I noticed that my daily "tech news" routine became much more efficient. I simply watch through the feed and as before decide what to read more thoroughly, but now it takes less time. However, there are downsides. Sometimes it can be too much information even to quickly scroll through. Not every source that I typically follow provides RSS/Atom feed. Some entries are very brief about the content or have no summary at all and I need to check the site if that article is something that I really need to read. Nevertheless, the reader gives a very nice experience, because I'm less distracted.


## f. Port scan



## Voluntary bonuses

### g. Identify a port scan against Apache



### h. Modify nmap scan




## References

* Karvinen, T. 2026. Cyber Security – 2026 late autumn, homework h4. Accessed 16.11.2026. [https://terokarvinen.com/cyber-security/#h4](https://terokarvinen.com/cyber-security/).
* Korkein oikeus. 2003. KKO:2003:36. [Precedent, Supreme Court of Finland]. Accessed 16.11.2026. [https://www.finlex.fi/en/case-law/supreme-court/precedents/2003/36](https://www.finlex.fi/en/case-law/supreme-court/precedents/2003/36).