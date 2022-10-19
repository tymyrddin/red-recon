# Advanced searching

Search engines crawl the world wide web day and night to index new web pages and files. Sometimes this can lead to 
indexing confidential information:

* Documents for internal company use
* Confidential spreadsheets with usernames, email addresses, and even passwords
* Files containing usernames
* Sensitive directories
* Service version number (some of which might be vulnerable and unpatched)
* Error messages

Popular search modifiers that work with many popular search engines.

| Symbol / Syntax 	             | Function                                          |
|:------------------------------|:--------------------------------------------------|
| "search phrase" 	             | Find results with exact search phrase             |
| OSINT filetype:pdf            | Find files of type PDF related to a certain term  |
| salary site:blog.target.com 	 | Limit search results to a specific site           |
| pentest -site:target.com      | Exclude a specific site from results              |
| walkthrough intitle:TryHackMe | Find pages with a specific term in the page title |
| challenge inurl:tryhackme     | Find pages with a specific term in the page URL   |

Note: In addition to `pdf`, other interesting filetypes are: `doc`, `docx`, `ppt`, `pptx`, `xls` and `xlsx`.

Public Google Drive documents:

    site:docs.google.com "Target Name"

Documents on `documentcloud.org`:

    site:documentcloud.org "Target Name"

Documents uploaded to Scribd:

    site:scribd.com "targetname.tld"

Public PowerPoint presentations:

    intext:"Target Name" filetype:pptx

Public PDF documents:

    intext:"Target Name" filetype:pdf

`.docx` documents on GP's website:

    intext:"Target Name" filetype:docx

Google observes copyright infringement laws and moderates its search output, so also try other search engines.

## Resources

* [Google Advanced Search](https://www.google.com/advanced_search) 
* [Google Refine Web Searches](https://support.google.com/websearch/answer/2466433) 
* [DuckDuckGo Search Syntax](https://help.duckduckgo.com/duckduckgo-help-pages/results/syntax/) 
* [Bing Advanced Search Options](https://help.bing.microsoft.com/apex/index/18/en-US/10002)
* [YaCy](https://yacy.net/download_installation/) will allow you to set up your own collections. You can wipe your index when done.
