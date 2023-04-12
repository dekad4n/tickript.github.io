# Event Page
Event page is an input-specific page. Therefore, it needs to be accessed through several ways:
- With horizontal event card
- With vertical event card

These event cards can be found in Home, Profile or in search section. 

Event page is fed from event modal. To see what event modal looks like, see [Event Modal](/Models/event.md).

Events are created with event creation process. Therefore, the event page is formed from actually event owner's inputs.

Event page has three forms: an ordinary user's view, checker's view, event owner's view. Ownership is automatically detected via states of mobile application, therefore the two forms are located in the same page.

An ordinary event page starts with picture of the event and title of it. They are located in the beginning of the page. The owner, the date and the description of the event follows the first part. These are all constant parts that does not change if an user is ordinary or event owner.

Then, there is a table in which minted tickets (available but not on sale), listed tickets (on sale), sold tickets (tickets that are listed once, and not on sale right now), on sale (tickets someone is selling after listed once). This part is not constant since event owner will see + button if they did not mint any tickets yet. One can see the difference between event owner's view and an ordinary user's view at the end of the page.

Then, the page has Your Ticket status section. This part shows tickets you own or you are selling. Via refreshing it, one can see newly bought tickets. If one has a ticket, the right arrow button appers. This button redirects user to [My Tickets](/Pages/Subpages/mytickets.md) page.

After that, we have the name of tickets and description of it. The important part here is price of tickets (or sold out part) here. Also, one can buy or view auctions through this section.

An event owner will see floating actions button on the right bottom section. The action button with people redirect you to [Add Event Checker Page](/Pages/Subpages/addeventchecker.md). 

The checker will see the floating button with qr code will redirect you to [Scan Page](/Pages/Subpages/scanpage.md) instead of add event checker page.

Ordinary user view:
<br><br/>
<img src="https://raw.githubusercontent.com/sadigulbey/tickript.github.io/main/static/pages/ord_event_page_p1.png" style="height:500px;"></img>
<img src="https://raw.githubusercontent.com/sadigulbey/tickript.github.io/main/static/pages/ord_event_page_p2.png" style="height:500px;"></img>
<br/><br/>

Event owner view:
<img src="https://raw.githubusercontent.com/sadigulbey/tickript.github.io/main/static/pages/ev_ow_event_page_p1.png" style="height:500px;"></img>
<img src="https://raw.githubusercontent.com/sadigulbey/tickript.github.io/main/static/pages/ev_ow_event_page_p2.png" style="height:500px;"></img>





