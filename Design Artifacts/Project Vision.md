Introduction
============

The project aims to provide a service to allow people to manage and keep track of debts and credits with other persons.

There are two types of roles:
 - **User**: every person that uses the system is a user.  
 Anybody can assign a debt to a person. This is a *single debt*, meaning that a single transaction for a good has occurred (e.g. a beer, some money lent).   
 The transaction cost for a good can be split evenly among many persons.

 - **Event Creator** (also called a **creator**): a user who created an *event*. Multiple people can join or be added to an event, which usually has an expiration date.  
 Anybody who joined an event can add any number of transactions. The cost of the transaction will be split evenly among all the users, unless some members of the event are explicitly excluded from it.

The system can show the debts one person has against another (with any eventual detail that has been added) and it is possible to mark them as paid off.

Since the interaction between the user and the system could take some time in particular circumstances, it is important that the system is able to keep track of the progression of interactions.

Single Debts
============

A person can assign a debt to one or more persons.  
While doing so, it is possible to add details like:
 - Reason for the debt
 - When the debt has been created (if it existed before the moment it is being added to the system)
 - What currency has been used (**since the bot will not convert between different currencies**)

A user can cancel the debt if he created it, or he can pay it off if he is a debtor. The debt cannot be edited after it has been created.

A debtor can pay off a debt in multiple rates, or all at once.  
Every time something happens about a debt/credit, both the creditor and the debtor are notified.

Events
======
An event can be created by a user, who becomes the *event creator*.  
The Creator can add members to his events at any time, or he can share it to allow anyone to join.

The creator can add a title and a description to specify what the event is for.
The currency must also be indicated (Euro, USD, GBP...)

An event wizard should assist the creator step-by-step while creating the event.

Any member can add a transaction to the event while it is active. It represents a credit directed to the other members.\
*Example:*

    David buys a gift. By doing so, he lent some money to the other event members.
    He wants to divide its cost among all, so he adds a transaction to the event. 
    
    Then, Alex buys some crackers to use as a surprise for the party.
    He wants to divide the cost among all participants the same way, so he creates another transaction.

The transaction can have some members excluded from it.  
After its creation it cannot be edited, however it can be deleted, both by the participant and by the event creator.

At any moment, it is possible to add or edit the expiration date. When the specified date passes, it isn't possible to add new transactions to the event.  
It is allowed to postpone the expiration date to allow new transactions.

Alternatively, the creator can manually close the event. This action has the same effect of passing the expiration date. Again, the event can be re-opened.

When the event has been closed, it can be terminated by the event creator.  
When he chooses to do so, the system automatically calculates the final amount of money that every member of the event owes to every other member.

An event that has been terminated cannot be re-enabled.

When any update happens in the event, the system should notice every member.

If a user is misbehaving, he can be kicked out of the event. He will not be able to join again through links and must be manually invited by the event creator.

Paying off debts
================

A debt can be marked as paid by both the debtor and the creditor.  
In any case, the action must be confirmed by the other part to ensure that it wasn't marked as paid by error or maliciously.

To help remember the debts and credits, the system periodically sends notifications about them.

A creditor can query the system to receive a summary of all the debts that a person owes to him, and vice versa.

If a debt is paid in several separate times, each time is listed with the specific amount.

It is possible to create a *recalculation group* to recalculate debts and credits between people who have debts/credits in common, to reduce the number of exchanges of money needed.