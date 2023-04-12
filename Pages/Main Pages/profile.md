# Profile Page

The aim of ours when creating a profile page to give opportunity to both event managers and ordinary users. Event managers should have been able to create events, mint tickets and sell them starting from their profile pages. Also, they should have been able to see their created events. On the other hand, ordinary users should have been able to see their own tickets.
Also, all users should be able to login into application.

To reach our aims, we have created the profile page with 3 different states:
- Logged out state
- Logged in state
- Settings

## Logged Out State
The aim of logged out state to give opportunity to end user to login with Metamask.
Logged out state has pretty simple structure. It just has a button to login to app. To see how login works, see [Workflows](/Workflows/introduction.md).

The logged out state can be seen below:
<br/> <br/>
<img src="https://raw.githubusercontent.com/sadigulbey/tickript.github.io/main/static/pages/profile_logged_out.png" style="height:500px;"></img>

## Logged In State
There are more than one reason why we created logged in state. First, users should be able to reach their profile settings. Secondly, event owners should be able to create new events. Thirdly, ordinary users should be able to see their tickets (because of hiearchy, also event owners).

In the picture below, we see that there is button which redirects the end user to settings state.
Here, a little difference comes: even though there is my events section, an ordinary user cannot see it. One should be event owner to see the part of My Events.
<br/> <br/>
<img src="https://raw.githubusercontent.com/sadigulbey/tickript.github.io/main/static/pages/profile_logged_in.png" style="height:500px;"></img>

In the picture below, one can see that there is Attending section. Attending section is visible to users who own any ticket. Please note that if you are event owner and listed new tickets, the tickets will not be here.
The attending section has two parts: tickets that is not outdated (event's start date is not passed), and outdated tickets.
<br/> <br/>
<img src="https://raw.githubusercontent.com/sadigulbey/tickript.github.io/main/static/pages/profile_logged_in_attending.png" style="height:500px;"></img>

# Settings State
Settings state should be able to provide changing the username and changing the profile picture. When one is an event owner, profile picture and username makes sense since others see who is organizing the event. However, for an ordinary user these are not important.

In the picture below, we see a clickable picture and text box with which an user can change its name:
<br/> <br/>
<img src="https://raw.githubusercontent.com/sadigulbey/tickript.github.io/main/static/pages/profile_settings_state.png" style="height:500px;"></img>






