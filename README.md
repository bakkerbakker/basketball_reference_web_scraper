# Basketball Reference Web Scraper
[Basketball Reference](http://www.basketball-reference.com) is a great site (especially for a basketball stats nut like me), and hopefully they don't get too pissed off at me for creating this.

Basically, I created this repository as a utility for another project where I'm trying to estimate an NBA player's productivity as it relates to daily fantasy sports.  For that project, I need box score and scheduling information, which is provided by this utility. Here's the [PyPi package](https://pypi.python.org/pypi/basketball_reference_web_scraper/1.7).

## Installing via pip
I wrote this library as an exercise for creating my first PyPi package.  Hopefully this means that if you'd like to use this library, you can by simply downloading the package via [pip](https://pypi.python.org/pypi/pip) like so:

`pip install basketball_reference_web_scraper`

## Getting Box Scores
There are two methods that return box scores for a given date:

### Methods located in `web_scrapers.py`
* `return_box_scores_for_date(date)`
  * Returns a list of Box Score objects
* `return_json_encoded_box_scores_for_date(date)`
  * Returns a JSON object representation of a list of Box Score objects

## Getting Season Schedule Information
There are also two methods that return scheduling information for a given season start year (note that the NBA season generally spans two calendar years):

### Methods located in `web_scrapers.py`
* `return_schedule(season_start_year)`
  * Returns a Schedule object
* `return_json_encoded_schedule(season_start_year)`
  * Returns a JSON representation of a Schedule object

### Methods located in `web_scrapers.py`
* `return_player_season_statistics(season_start_year)`
  * Returns a list of Player Season Statistic objects
* `return_json_encoded_player_season_statistics(season_start_year)`
  *  Returns a JSON object representation of a list of all player season statistic totals for the given season

## Writing to CSV
I also created utility methods that write box score and season data to csv. They are located in `csv_writers.py`.
