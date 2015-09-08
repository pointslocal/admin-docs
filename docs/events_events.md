# Managing Events

# The Events List
## User Queue
The User Queue - represented by one of the three primary buttons at the top of the events list page - represents user-submitted events.  Depending on your setup, this can serve as a reference for events that are set to go live on submission or require being set to "published" to be available on your site.

## Your Queue
Your Queue - also one of the primary buttons on the events list - represents a working collection of events that can be utilized for print export, batch operations, compiling an editorial package or simply workflow clarity.

## Batch Operations
![Managing Multiple Images](img/events_events_multi.png)
In the events list, by selecting any number of events with the corresponding checkbox, a dropdown menu of batch operations will slide open.  These represent the most common actions for

### Queue
By selecting Queue, you'll add the selected events to your working group of events.

### Set Publish Status
Set Print Published, Set Web Published and Set Web & Print Published allow quick access to setting multiple publication statuses.  This can also be done individually by clicking the globe icon (for web) or the A icon (for print).

### Merge
Merging an event means taking the maximum amount of information from two or more events and combining it into a single instance.  This is most commonly used when duplicate events are submitted.  Pointslocal will attempt to prevent duplication on imports but allows users to submit duplicates if they choose to ignore the "your event may already be in our system" message.  This is a destructive operation, which means that some information will be lost in most cases.  For example, if both events have a URL but the URL is not the same, the merge process will take the first event submitted's value, destroying the second (and successive) event's value.

### Connect
Connect is utilized when an event is a recursion of an existing event - this allows the metadata for both to be shared.  It also allows the event to show in "more dates" on the event details page.  Like Merge, Connect is destructive - by connecting an instance to an existing event, the meta data around the event will yield to the existing event's meta data.