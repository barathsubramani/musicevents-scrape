## Web Scrape Events – Automated Event Notification System

This project focuses on web scraping upcoming music events using Python, retrieving the event’s Name, Location, and Date, and automatically notifying the user via email when a new event is found.

The process begins with an empty SQLite database, which will serve as the storage for event details. The Python script uses the **requests** library to fetch HTML content from a target events webpage. The **selectorlib** library is then employed to parse and extract relevant event information specifically, the event name, venue, and scheduled date using CSS selectors defined in a configured file.

Once the data is extracted, the script checks the database to determine if the event is already stored. If the event is new (not previously recorded), it is inserted into the database using **sqlite3**. This prevents duplicate entries and ensures the user is only notified about fresh events.

For notification, the project uses Python’s **smtplib** to send an email alert directly to the user’s inbox. This email contains the name, venue, and date of the new upcoming event, ensuring the user stays informed without manually checking websites.

The system can be useful and is user-friendly that the users don't have to visit the websites and check for events, instead they get notified by an email with the event details.


