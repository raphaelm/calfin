calfin
======

*calfin* is the proposal of an accounting system for personal use which is entirely based on a calendar.

Design goals
------------
* It's not about professional bookkeeping, sloppy use is allowed
* The protocol is defined independently from the software to allow various implementations
* It can manage multiple accounts (like bank account, credit card and cash)
* The system only knows about accounts and transactions. Every transaction is connected to a point in time and thus can be stored as a calendar event
* Good support of recurring events
* The protocol is an extension to the popular iCalendar format. This comes with various benefits
  * We get a mature definition and implementation of recurring events
  * We get a ready synchronization protocol, CalDAV, which is based on WebDav
  * We get third-party libraries for the two things mentioned above, which saves us huge complexity


Open Questions
--------------
* How to store finance-specific data
  * JSON formatted in the description of calendar events, which would be more compatible with existing sync servers
  * In custom ``X-CALFIN-`` prefixed fields of the iCalendar events, which would be a more tidy

