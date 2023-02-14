# Open-Source Intelligence (OSINT)
## Passive OSINT: Google Hacking
This can be used to filter Google searches for specific types of information.
* https://www.exploit-db.com/google-hacking-database
* https://dorksearch.com/
* https://www.shodan.io/
  * Search Engine for the Internet of Everything
* https://abhijithb200.github.io/investigator/
  * Creates queries
* https://dorks.faisalahmed.me/
  * Creates queries

These are example queries:
* `filetype:[ext] [website]` | finds all documents on a website with a certain extension
  * `filetype:pdf apnews.com
* `filetype:[ext] site:[ending] inurl:[word]` | find all documents ending with `ext` and only urls with `word` in them and an ending of `ending`
  * `filetype:pdf site:gov inurl:contact`
  * `filetype:xls inurl:email.xls`
* `intitle:"[phrase]"` | search for webpages with a certain phrase in the title
  * `intitle:"site administration: please log in"`
  * `intitle:"curriculum vitae" filetype:docx`
  * `intitle: "index of /" inurl:(cv | resume)`

# theHarvester
* [This](https://github.com/laramies/theHarvester) is the link for the Github.
* It is used to gather OSINT on a company or domain.

## Commands
* `theHarvester -d [domain] -l [limit] -b [source]` | domain to harvest from, the number of search results, and the search engine
  * `theHarvester -d example.com -l 50 -b all` | return 50 results for example.com from all the search engines
* `theHarvester -d [domain] -l [limit] -b [source] -f [filename]` | save the results to XML and JSON files
  * `theHarvester -d example.com -l 50 -b all -f test` | saves the results in test.json and test.xml

# holehe
* [This](https://github.com/megadose/holehe) is the link for the Github.
* Holehe checks if an email is attached to an account on sites like Twitter, Instagram, Imgur and more than 120 others.

## Installation
* `git clone https://github.com/megadose/holehe`
* `cd holehe`
* `sudo python3 setup.py install`

## Commands
* `holehe [email]` | returns results on whether or not the email is registered with a site
  * `[+] Email used`| green
  * `[-] Email not used` | purple
  * `[x] Rate limit` | red
 * 
