Glossary
========

## Actors
Term | Description | Synonyms
-----|-------------|---------
User | Every person that uses the system is a User.<br>Any user can assign debts (becoming a Credtor) or pay them off (if he's a Debtor).<br>If a user assigned a debt, he can edit the details at any moment. | Person
Event Creator | A user who created an event. He can manage it by editing its details or by setting it as "closed". | Creator
Participant | A user who participates to an event | Event Member, Member
Credtor | A user who assigned a debt (manually or automatically) to another user (a Debtor)
Debtor | A user who received a debt from his Credtor.

## Application Domain
Term | Description | Synonyms
-----|-------------|---------
Active Event | An event that hasn't expired and hasn't been terminated.
Credit | An amount of money lent by a Credtor to a Debtor.
Common Credit/Debt | A situation in which two or more users owe any amount of money to each other.
Debt | An amount of money owed by a Debtor to a Credtor. A Debt can be *Single* or *Derivate*. A debt can be payed in multiple rates by its Debtor.
Derivate Debt | A debt that has been automatically created as a result of the termination of an Event. It is like a Single Debt, however it indicates as one of the reasons for its creation the Event.
Event | An event is a convenient way to create multiple shared Debts (represented by *Transactions*) in a timespan (if specified) between different Users. An event is created by the Event Creator and any amount of users can join it (by being invited to it or by receiving a link).<br>The Creator can specify an Expiration Date after which the Event has Expired and no more Transactions can be added. The expiration date can be postponed to allow new Transactions.
Event Update | When a Transaction is added, a person joins an Event, an event expires or is terminated an Event Update is sent to all members.
Event Wizard | A step-by-step wizard that assists the Event creator while creating a new Event.
Excluded User | A user that has been specified not to owe anything in a Transaction. He will be ignored during the event's post-termination calculations.
Expiration Date | A date specified for an Event after which the Event expires. It can be postponed, even after the event expires, but before it has been Terminated.
Expired Event | An event whose Expiration Date has passed. It cannot receive new Transactions, except if its Expiration Date is postponed. | Closed Event
Payment Rate | A Debt can be payed off in multiple rates. | Rate
Recalculation Group | A group of users with Common Credits/Debts. Its main purpose is to allow to recalculate their debts and credits to minimize the number of money exchanges needed.
Single Debt | A single debt is a one-time debt created specifically by a Credtor for a Debtor. It isn't linked to an Event, unlike a Derivate Debt.
Terminated Event | An event that has been closed or has expired and whose owner decided to close permanently. After the termination, the single User's debts are calculated.
Transaction | A single Credt/Debt created by a User towards the other participants. It contains some details (amount, time of payment, description). Some participants can be excluded from it.