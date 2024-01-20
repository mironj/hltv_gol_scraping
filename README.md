Scrapning functions that first obtain relevant information needed to create a series of URLs, which then are used to gather historical information on CS teams (from HLTV) and LoL teams (from Games of Legends) - winrate, basic performance information of each player, and their nationality.

This particular code uses Scraping Bee API, which has worked for me. Scraping API is necessary for accessing HLTV, scraping GoL does not require it.

The code works, but is rather inefficient: there are many instances where function just does not include a particular team, due to lack of certain information. This in particular affects the HLTV scraping, where not including a team essentially wastes two uses of the scraping API. 

There also might appear some problems with scraping when certain teams or players have peculiar names, which somehow interfere with Python RegEx. I included all the exceptions I encountered, but it is possible there are more.
