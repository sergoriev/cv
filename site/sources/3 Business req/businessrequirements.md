# Business Requirements Document
# "Russian Post Service Modification"
Version 1.0
02/13/2019
___

## Version and approvals

| Version | Date | Revised by | Reason for change |
| ------- | ---- | ---------- | ----------------- |
| 1.0     | 12\03\2019 | -| -|

## Project Details

| Project Name | "Russian Post service modification" |
| -----------  |  --------------------------------- |
|Project type| New Initiative|
|Project start date|02/10/2018|
|Project end date|05/10/2018|
|Project Sponsor|Federal state unitary enterprise "Russian Post"|
|Primary driver|Deputy CEO Emelchenkov Sergey |
|Secondary driver|-|
|Version |1.0|
|Project manager|John Doe|

## Overview

### Document resources 
[2016 AR](https://fc.russianpost.ru/Download/AboutRussianPost/russianpost_ann_report2016.pdf "2016AR")
[2017 AR](https://fc.russianpost.ru/Download/AboutRussianPost/russianpost_ann_report2017.pdf "2017AR")
[Order of the Government of Russia of June 28, 2002 No. 885-p](http://portal.ncnd.mts.by/nf/?time_stamp=1554050418738)
[Russian Post official website](https://www.pochta.ru)
[Changes from 20.05.2005 in the Charter of FSUE “Russian Post”](https://fc.russianpost.ru/Download/AboutRussianPost/charter/02_20_05_2005.pdf)


### Definitions

- **Post** (Russian Post, RP) -- Client company
- **CAO** – Complex Action for Optimization (automation)
- **Client** – client(-s), who use RP services
- **CSI** – Customer Satisfaction Index

### Project overview and background
FSUE Russian Post – Russian state post operator with the largest subsidiary network (41 901 post offices) and 351 753 employees.In 2015, Russian Post entered the list of strategic enterprises of Russia. Unfortunately CSI as well as the company's image constantly declines. Also, clients believe that processes on post offices are outdated, and there is a need for some changes.

The main goal of this project is to increase the company reputation by implementing the following:
- Use high-tech devices to reduce the burden on employees;
- Reduce queues in post offices;
- Make visiting post offices a matter of not more than 5 minutes.

It will be possible with various CAO, such as:
1. E-queue with an (paid) opportunity to book certain time slots for getting/sending parcels.
2. Parcel delivery with **QR**-codes, pre-generated in PR application, through special vending machines.
3. Use notifications via SMS, different messengers (_Viber_, _Telegram_, etc.) instead of paper-notifications.
4. Live-stream of queue load in certain post offices.
5. Install feedback terminals.

### Project stakeholders

| # | Stakeholders |
| ---- | ---- |
| 1 | Deputy CEO Emelchenkov Sergey |
| 2 | John Doe |
| 3 | Jane Doe |

## Key assumptions and constraints

### Assumptions

1. After implementing SMS and messenger notifications there will be no need in paper notices.
2. Paid e-queue and ranking parcels with QR codes will significantly decrease operation time, increase CSI and NPS and will generate additional revenue to company.

### Constraints

1. Customers may have difficulty in using the vending machine for the first time.
2. Some part of RP's client can be dissatisfied with new notifications system.


## Use cases

This section containt Use cases of improvment RP system.

### Use Case - 003 
#### This use case describes the way user (post's client) will fill form for sending parcel in certain date. 

|Actors|User|
|---|---|
|Pre-conditions|User authorized in russian post system.|
|Post-conditions|Visit application registered.|
|Normal course|1. User fills all necessary fields (name, address, etc.). 2. User chooses post office, time and date of visiting. 3. User confirms correctness of entered data. 4.System requires to choose payment method 5. User pays for registering 6. System notifies that user's application registered.|
|Alternative course|1. User fills all necessary fields (name, address, etc.) 2. User chooses post office, time and date of visiting 3.System notifies that choosed time and date are unavailable 4. System returns to p.2 condition|
|Exceptions|-|
|Includes|-|
|Priority|High|
|Frequency of Use|Medium|
|Business Rules|-|
|Special requirements|User needs to have their own account on RP system.|
|Assumptions|-|
|Notes and Issues|-|



### Use Case - 011
#### This use case describes the way user (post's client) will act in PR system to get parcel, which less than X,Y (where X - size (weight) of parcel, Y - value in money equivalent). 

|Actors|User|
|---|---|
|Preconditions|1. User authorized in russian post system. 2. Parcel should be arrived in post office.|
|Postconditions|Parcel loaded in vending machine. |
|Normal course|1.User chooses option "Take parcel" in post office 2.System, according to User's profile, suggests take parcel in their post office (linked to his addres). 3.User accepts suggested post office. 4. System offers to choose available parcels 5.User chooses payment method. 6. User confirms payment. 7.Operator of selected post office gets request for loading vending machnine with User's parcel. 8.User receives QR code via RP system.|
|Exceptions|-|
|Includes|-|
|Priority|High|
|Frequency of Use|Medium|
|Business Rules|-|
|Special requirements|User need to have their own account on RP system. User need paying card be linked to his account.|
|Assumptions|-|
|Notes and Issues|-|

### Use Case - 013
#### This use case describes the way user (post's client) will act in PR system to get parcel, which more than X,Y (where X - size (weight) of parcel, Y - value in money equivalent). 

|Actors|User|
|---|---|
|Preconditions|1. User authorized in russian post system. 2. Parcel should be arrived in post office.|
|Postconditions|Parcel sent to checkout window.|
|Normal course|1.User choose option "Take parcel" in post office. 2.System, according to User's profile, suggests take parcel in their post office (linked to their addres). 3.User accepts suggested post office. 4. System offers to choose available parcels 5.User choose payment method 6. User confirms payment. 7.Operator of selected post office gets request for transfering User's parcel to checkout window 8.User receives QR code via RP system.|
|Alternative course||
|Exceptions|-|
|Includes|-|
|Priority|High|
|Frequency of Use|Low|
|Business Rules|-|
|Special requirements|Look [UC-011](#uc-011)|
|Assumptions|-|
|Notes and Issues|-|

### Use Case - 023
#### This use case describes the way admin (post office manager) will look through client's requests on post office visit.

|Actors|SuperUser|
|---|---|
|Preconditions|SuperUser authorized in russian post system with admin access level.|
|Postconditions|System allows admin to look through visit requests.|
|Normal course|1. Admin chooses option "confirmed visits". 2.Admin chooses option "confirmed to send" or "parcels, available to get". 3. System allows to choose days needed to be checked. 4. Admin chooses needed dates. 5. System shows all visit requests for chosed period, sorted by request date (descending).|
|Exceptions|-|
|Includes|-|
|Priority|Medium|
|Frequency of Use|Low|
|Business Rules|BR1|
|Special requirements|Access to this feature only possible with admin access level.|
|Assumptions|-|
|Notes and Issues|-|

# Use case diagram

# Business requirements
The following sections document the various business requirements of this project. The requirements in this document are prioritized as follows:

|Value|Rating|Description|
|-----|------|----|
|1|Critical|This requirement is critical to the success of the project. The project will not be possible without this requirement.|
|2|High|This requirement is high priority, but the project can be implemented at a bare minimum without this requirement.|
|3|Medium|This requirement is somewhat important, as it provides some value but the project can proceed without it.|
|4|Low|This is a low priority requirement, or a “nice to have” feature, if time and cost allow it.|
|5|Future|This requirement is out of scope for this project, and has been included here for a possible future release.|

## General/Base
|REQ#|Priority|Description|Rationale|Use case #|
|---|-|-|-|-|
|BReq1|2|Only stuff with admin access level can apply changes in client's requests.|-|UC-011, UC-012|
|BReq2|3|Client should have an opportunity to look though all his confirmed and finished requests for all time.|-|-|

## Security
|REQ#|Priority|Description|Rationale|Use case #|
|---|-|-|-|-|
|SReq1|1|After QR code has been scaned, it should be removed from database.|-|-|
|SReq2|3|Employees passwords should change at least 1 time in a month.|-|-|
|SReq3|2|After operator received vending machine load request, he need to confirm this in a system.|-|-|

## Usability
|REQ#|Priority|Description|Rationale|Use case #|
|---|-|-|-|-|
|UReq1|2|4 of 5 novice user should perform "Get parcel" feature less than 4 minutes.|-|UC-011,UC-012|
|UReq2|4|Client need to have convinient access to "Live translation of neccessary post office" feature from any device.|-|-|


# Appendixes
## Appendix A - "As Is" - "To Be" Diagrams
<as is diagram>
"As is" description:
1. Client receives post notification.
2. As usual, client takes queue ticket in post office via queue terminal (still not in every office).
3. Operator looks for parcel in database.
4. Operator searches for the parcel in post office. 
4.1 Client checks parcel content (optional).
5. Client signs post notification.
6. Operator gives parcel to client.

Current state of issues:
- It is not very practical to use paper notification - they could be lost, damaged. This procces also includes the fact that postmen need to bring this notification to a client, and human factor issues;
- If post notification isn't acquired, parcel can stay in office for a long period of time (relevant for goods from internet shops);
- Uneven workload of the department during the month, which complicates the assessment of the time that can be spent in the queue at the office;
- As usual client don't have opportunity to leave any feedback fast and easy, if they were dissatisfied with operator's service.

<to be diagram>
"To be" state description:
1. Client receives post notification via SMS or a messenger.
2. Client authorizes in RP's app.
3. Client chooses payment method and pays to take parcel in needed time.
    3.1 If parcel less than X,Y (X - size of parcel, Y - value in money amount), operator sends parcel in vending machine .
    3.2 If parcel more than X,Y operator takes it to checkout window.
    3.3 RP's system generates special QR code linked to client's parcel.
4. Client receives this special QR code.
5. In post office client scanning QR code:
    5.1 At checkout window, if parcel more than X,Y, and takes it.
    5.2 In a vending machine, if parcel less than X,Y and takes it.
6. (optional) Client leaves feedback via feedback terminal.

"To be" state pros:
- Client receives notification just in time when parcel came to post office.
- Client still has an option to take his parcel in old way (wait in a queue), but new option can generate extra revenue.
- So, there is no need to wait in a queue anymore, if client wants to take his parcel at a certain time.
- Client can also leave feedback via feedback terminal, which gives Post offices managers extra information of employees work.


## Appendix B - Data Flow
dataflow d











