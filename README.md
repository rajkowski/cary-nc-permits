# Cary-Permits
Scrapes Cary Permit Data

Based on the PHP project Cary-Permits, without it this project would not be possible. At first changes were made to the PHP version, but then ultimately lessons were learned and a Java version was created. This has been forked and released in the spirit of providing additional data.

A Java version was created to address a few issues:

- The PHP version lacked the Parcel Id and Structure Description fields
- The Java version uses OpenCSV for well-formed CSV output
- A resume feature was added so that the script can be re-run to append new data
- Note though that previously scraped data is not updated, so you may have to blow out old data periodically.

To do: An additional URL is sometimes present with extra data, like mechanical, electrical contractor, etc.

Requires Java 7.

$ sh scrapeCaryPermits.bsh [year(>=1993)|now] <offset:0> <limit:99999>

- Specify 'now' to use today's date
- Data will be appended to data/cary_[year]_permits.csv
- Offset 0 will include a header row with column names
- This script will resume automatically when a file exists

