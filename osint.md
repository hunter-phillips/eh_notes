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
