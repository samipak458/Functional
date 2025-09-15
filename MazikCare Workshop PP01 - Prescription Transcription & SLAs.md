**MazikCare Workshop PP01 - Prescription Transcription &
SLAs-20250212_093422-Meeting Recording**

0:02\
In in a little while.

0:05\
I think we\'re probably probably good to get started.

0:11\
So yeah, let\'s go Cheryl and a couple on to the other call that\'s on
at the moment, the migration.

0:16\
Yeah.

0:16\
So Cheryl\'s running going to set on the the data migration session,
which we\'ve got running in parallel.

0:22\
Alex is over there.

0:23\
Let me just see who\'s in that call.

0:26\
I think that\'s why numbers are down here.

0:28\
Yeah, that\'s so that\'s, that\'s the data migration session.

0:32\
So people like Chris Bateman with data science over there, Gideon, I
think, I think there\'s Jess over in that one as as well.

0:42\
So, yeah, I mean, ideally we\'d all go, we\'ll be able to get to all of
them, but I think we have to split our split our attention slightly.

0:50\
Let\'s make a let\'s make a start.

0:52\
I think Mashoud Anas, Yes.

1:02\
Azula Anas, can you please share your screen and let\'s start.

1:07\
Yeah, give me a minute.

1:16\
So we got up to the point yesterday where we\'ve had a, we\'ve created a
new patient, we\'ve assigned them onto the the right contract.

1:22\
We\'ve done our welcome calls.

1:25\
They\'re they\'re up and ready to go effectively.

1:27\
I mean, that\'s about where we got to in that that flight.

1:32\
Yeah, yesterday\'s session was about phone calls and phone calls
basically are like generated after like the whole prescription has been,
you know, ACD verified and generated.

1:42\
So like technically this is like a process that comes before it, right?

1:46\
And OK, so today\'s session will be around prescription management,
right, where we will be covering part 1-2 and three.

1:58\
There\'s might be some overlap with like tomorrow\'s calls as well, but
I\'ll try to keep it like only focused on the transcription process and
basically what a person must do before the transcription process, right?

2:13\
So OK, our agenda for today is just to like, basically give like a first
we\'ll give a brief overview of the prescription workflow that will be
followed.

2:22\
Like moving forward, we will be showing the prescription form, the
prescription types, we showing patient orders, we\'ll be showing label
generation.

2:32\
Right after that, we will move on to the transcription rules.

2:35\
So I\'d like basically categorise them into like 3 specific areas, which
is like, so for example, transcription rules basically like cheques,
whether certain information is available on the product that you\'ve
selected, whether your prescription follows the contract specification
that you\'ve done, right.

2:53\
And basically it also cheques whether the patient ordered the, you know,
the medication line that you\'ve created, right?

3:00\
It has certain information available.

3:02\
And if you have time left, you\'d probably also go over delivery
generation.

3:07\
OK on right.

3:14\
Yeah.

3:15\
So basically the prescription management workflow that will be followed
in the new system will be like whatever prescriptions you get, they will
be scanned into the system, right?

3:25\
The AI will be read the document right?

3:28\
And when it reads the document, it basically like create some sort of
XML file which it will use to create the specific record right?

3:37\
As in fill in the prescription form with the relevant information and
then create the medication lines of that prescription right after that.

3:46\
Once all of that is done, then the basically a user will have to like,
you know, open the prescription form, just check, recheck the details,
and then select the, you know, verify transcription button.

3:58\
Then after that, the system will generate delivery orders.

4:02\
The user will then have to check like basically the labels and the
quantities, right?

4:08\
And as deliveries are, you know, being sent to the patient, the
prescription will eventually expire and then basically we\'ll start like
the renewal process as part of it.

4:20\
I\'m assuming that\'s clear.

4:21\
So move on, right?

4:24\
So basically like I believe in the Monday session probably would have
gone through some part of like the scanning activity where basically the
scanning activity is the record that\'s created when you scan documents
into the system, right?

4:39\
So we have like the scanning, we basically for each scanning activity,
we have like different batch classes, right?

4:46\
So, so one of them is registration form.

4:49\
One of them is the prescription type where basically only the
prescription is present or we have like say a scanning activity where
only the referral is present, right?

5:00\
And in certain in basically we also have like the ability to create a
batch class for a referral and a prescription right?

5:09\
Where you got both documents and you scan both both of them into the
system.

5:14\
Any questions so far, I will be moving on to the scanning activity
screen.

5:19\
But yeah, just like any question regarding like what I\'ve described so
far, Yeah, I think that as a no, right.

5:33\
So I\'ll just move on to the system now to show like the scanning
activity screens, right?

5:38\
So basically within the scanning activity, right.

5:42\
This is the prescription version, right, Where a person scanned a
prescription document into the system, right?

5:50\
So basically what the what the AI will have to do is like for example,
in the document, right, it would mention for example, what the
hospital\'s name is, what kind of prescription it is, the patient\'s
name, the therapy code and like the diagnosis, right?

6:07\
Based on that, the system would be able to like associate the
prescription to the relevant reference, right?

6:15\
And also get like the name of the referrer so that it can like associate
the right contracts using the therapy code and the healthcare provider
information that\'s given, right?

6:26\
And if for example, the transcript like the system was not able to
create a record, right, it will provide a failure reason in this field.

6:38\
OK, and then what?

6:39\
Basically at that point a user will have to like check for will have to
check the document and then make these associations themselves.

6:47\
And then they will the system.

6:49\
There is a option to like convert a spanning activity into a record
following so far or no, Like I can\'t really see whether anyone that has
their hands free stuff.

7:02\
Yeah, yeah.

7:02\
I think you just need to keep going unless someone stops.

7:06\
So just one very brief question.

7:08\
So if there is a failure and someone has to do it manually, does that go
into some kind of work queue somewhere or something?

7:15\
Yeah.

7:15\
So basically we at this, in this area, we have, you know, views for open
scanning activities.

7:21\
The idea is like as soon as the scanning activity is created into the
system, right, a bad job will pick up all of them, right?

7:27\
And then close the scanning activities, right, And create the specific
record if it\'s still open.

7:33\
That means like, you know, there\'s a failure reason.

7:35\
And like we can like, for example, create a view where say the failure
reason is populated and then the user can pick up that.

7:43\
Yes.

7:44\
Can you expand the drop down for the less views these?

7:49\
Yes, I can.

7:49\
Give me a second.

7:51\
I\'ll also add the failure reason column.

7:54\
OK, yeah.

7:54\
Which specific 1 Mashu?

7:58\
Can you just expand the open scanning activities?

8:01\
Can you change the view?

8:03\
OK, So what?

8:08\
Yeah.

8:08\
So underneath here you would have a system view that would give you all
failed scanning activities through which you can just philtre them down
and and within that view you would have a column that NS has just added
into the given list view.

8:27\
By default, that column would be available and you would be able to find
the errors that occurred against those scanning activities.

8:37\
OK, fine.

8:37\
Yeah.

8:38\
OK.

8:39\
So similar to what you are seeing in here, you\'ll have one more value
of the list view saying that scanning activities failed scanning
activities basically.

8:52\
So we can effectively create 2 flows then.

8:55\
So one would be we could have a team, I\'m just making stuff up.

8:59\
We could have a team that are just looking at the scanned activity
successes and reviewing those.

9:04\
And then maybe a more of a troubleshooting team that we\'d have look at
the failed ones where we know there\'s going to be more problem.

9:13\
Yeah, exactly.

9:14\
Someone just said some clears the exceptions.

9:16\
Yeah, yeah.

9:16\
OK.

9:17\
So sorry if I, I missed the last two days because I was on annual leave.

9:21\
So in terms of has scanning been covered already in terms of how we, you
know, the methods and all that kind of stuff or because I\'ll catch up
from the video, but I, I was just about to ask that actually.

9:33\
So we, we, we this, this demo this morning has sort of started at the
product.

9:38\
Has the product, the prescription has been scanned.

9:41\
What will that actual scanning look like for a user?

9:44\
Because presumably somebody\'s going to sit there with pilot
prescriptions that\'s come in the post that morning.

9:49\
What exact steps do we go through to get to this screen?

9:52\
Because we need, we need to work out whether our current hardware is
going to work to do this activity or not, whether we scan, you know, 100
pieces of paper together and the system sorts it all out, or whether we
have to do it 1 by 1.

10:05\
And what the process is going to be, please.

10:07\
Yeah.

10:12\
Is that a question for us that like, yeah, so So what what does that,
what does that first bit of the process look like?

10:20\
The first screen you showed us, the first screen you showed us here had
a scanned prescription already sitting there and the AI had done it
stuff, which is great.

10:28\
But what how do we get from receiving a piece of paper in the post to
that screen?

10:36\
OK, I believe the session regarding like the whole, you know, AI regard
AI stuff, right?

10:42\
That\'s in week 5 I believe.

10:46\
But that would be AI piece.

10:47\
OK, but what what gets it even into so the AI can look at it?

10:50\
What what\'s the actual scanning process basically like each scanning
record you could each like document you scan is like supposed to like
integrate into our system as like scanning activity records, right?

11:04\
Yeah.

11:04\
And but how?

11:07\
How I guess.

11:08\
I guess the question is, can you be scanning bulk or does it have to be
done individually?

11:15\
You were saying something.

11:16\
Yeah.

11:16\
So the process that we are demonstrating today starts from onwards where
the scanning activity itself has been synced into dynamic 365 or the
magic a system, right.

11:26\
And the, and the process prior to that is, is more of a technical side
of things that where there are some bad jobs written in here, there,
there is ATP folder where the, the PDF files are dumped, right?

11:38\
And through which those are being paid on the, you know, scheduled,
scheduled bad jobs, those files.

11:46\
And then they convert those into this, these scanning activity record
that session.

11:51\
If you are looking for at this point of time, that is for the next week
when we will be discussing the AI side of things.

11:57\
So OK, for, for today onwards, we have the scanning activities and
converted like created in the system.

12:03\
And they will then be just they\'ll be available along with the
prescription record converted for them.

12:09\
That\'s fine.

12:10\
OK, we\'ll park the question for now.

12:11\
We\'ll come back to it next week when you, when you show us that part,
OK?

12:16\
OK.

12:19\
Right.

12:20\
So basically like after like the scanning activity has been added into a
system, that\'s the AI\'s job to like read this, read the specific file
and then like associate the specific patient, the referral, the
provider, et cetera, right?

12:32\
And after that the prescription is created, right?

12:35\
I\'ll move back to the view, OK, right.

12:41\
Within prescription management, right, we have 3, three prescription
types, right?

12:46\
One is the new patient, one is renewal and one is dose change, right?

12:50\
And in the prescription form, right, the, the three mandatory fields are
the patient, the referral and the start date, OK.

12:58\
When you\'re creating a prescription, right?

13:00\
Normally, I guess the scenario would be that, you know, a prescription
is scanned into the system, but there is like the provision to like
manually create a prescription from the referral or episode of care.

13:14\
If like this specific option does need to be locked, for example, then
we can also like, you know, hide the specific button like and basically
if you\'re only expecting prescriptions to be created via the scanned
documents, then this is like a, you know, a option that we can hide for
you guys.

13:33\
OK, so because like the prescription form general tab is very big,
right?

13:40\
Like it has lots of fields.

13:41\
It\'s sort of like summarise what the what processes occur when the
prescription is like in the general tab, right?

13:51\
So basically on the general tab, we have like the delivery visit
calculation, right?

13:55\
Where the formula to calculate the number of deliveries is the duration
in days which is the duration between the end date and the start date,
right?

14:08\
And if for example no end date is given then the user has like the
ability to provide their own duration, OK.

14:15\
And formula is basically duration in days and delivery frequency in
days.

14:20\
So for example, if you have duration of 100 days, right, and your
delivery frequency is four weeks, right, then the formula will calculate
it as 3 deliveries, OK.

14:37\
In the prescription form, we also have like the next projected delivery
date.

14:41\
This is basically a sort of prioritisation mechanism, right?

14:46\
Where, for example, if you have already have a prescription in the
system, right, that had deliveries, right, or had confirmed orders or
something, right?

14:55\
Then basically what the system is able to do is that it uses the
previous prescription, right, to get the delivery date of a specific
order that was associated with your previous prescription, right?

15:08\
And then what it does is it adds the delivery frequency to that, right?

15:12\
So for example, if your last prescription\'s last delivery occurred on
1st Feb, right?

15:18\
And you create a new prescription where the delivery frequency is 28
days, right?

15:24\
So basically what the system will do is it will use that delivery visit
of the last prescription, right?

15:30\
And then add on the delivery frequency as like your next projected
delivery date in the prescription, right?

15:36\
And basically what this allows is that it sort of lets you prioritise
what kind, what prescription you must act on first, OK.

15:45\
How we define a, you know, a valid prescription is basically that the
prescription is, you know, in active state and hasn\'t been expired as a
duplicate, right?

15:55\
And there\'s a flag on that prescription that says act verified is yes
or and the status is expired on hold already, right?

16:05\
In the general tab, we also have like the scanned prescription document.

16:09\
So whatever document was used to create that prescription is visible
from the prescription from general tab, right?

16:15\
We input the purchase order numbers and we are able to like create
activities from the timeline, like go back to the app just to show you
the various fields at the general tab.

16:30\
And second.

16:33\
Yeah, so yeah, this is the general tab form, right?

16:38\
So like I said, it\'s like a very big form.

16:40\
It\'s like has a lot of fields.

16:42\
So like your first field is the regarding the hospital details, right?

16:46\
Where it just adds in the hospital health care provider that you know,
send the prescription, right?

16:52\
This is the, we have like the patient field referral contracts.

16:56\
And here is where we define whether you know it, what kind of
prescription it is, right?

17:02\
If this information is available on the scanned document, then the
system would pick it up from that.

17:06\
Otherwise the user would have to specify it, right?

17:09\
We have the start date and end date, which basically like calculates the
total duration, right?

17:15\
And this is what I meant when I said you could override it as like you
know your duration and you could specify the duration unit.

17:22\
So for example, right now it\'s set as 12 weeks, right?

17:24\
And the total duration is added in as because that\'s basically what we
always use for our calculations, right?

17:31\
In that I will be showing up in the patient order creation for OK.

17:37\
Within the general tab.

17:40\
We also have the flags to specify whether a prescription has been
clinical screen, whether loading dose is required, whether it\'s a
controlled prescription, right?

17:51\
And right now we also, once we get to this stage, basically these, these
specific fields will be relevant.

18:00\
Right now we\'re at the awaiting transcription stage, right where this
information is not yet populated, right?

18:07\
We have the duplicate prescription flag here, right?

18:10\
This is what the system uses to identify, for example, if the previous
prescription was valid.

18:14\
So for example, if I expire a prescription with a reason of duplicate,
right, then basically the system will just flag that prescription with
this field set to yes, right?

18:26\
Prescription required by date is not a factor right?

18:31\
Now these are the scanning details.

18:34\
As you can see, there\'s like no document here.

18:35\
So basically this was just created manually.

18:37\
But for example, if it were created via scanning activity, then you
would see like the scanning activity that record that was create a
scanning activity record that was used to create this prescription
alongside the prescription PDF, right?

18:54\
These this is where you would specify the delivery details such as the
purchase order number, the and confirm the purchase order number.

19:02\
This is the next projected delivery date field I was talking about.

19:05\
So this is like the first prescription in this reference, right?

19:08\
This field is not calculated.

19:09\
However, if there was like more than one prescription, then this field
would have been populated.

19:14\
OK.

19:15\
And this specific area is related to the description amendment that we
might go in the second session if we get to it, right.

19:30\
So I will move back to the presentation.

19:36\
Are we following so far or were there like specific questions on general
if?

19:42\
Yeah, quick, quickly.

19:44\
Yes, if there\'s so you mentioned about if there\'s an active
prescription that\'s not been expired, then it will calculate the start
date of the new prescription, not start date, next projected delivery
date, meaning when you have to send the delivery for this new
prescription.

20:00\
Fine.

20:00\
OK.

20:01\
So if there is no active prescription, it can\'t calculate that at all.

20:06\
No, because like this specific field uses like the previous
prescriptions to figure out what the next delivery date could be, right.

20:13\
So if you have like some logic in mind that you would want to use, so
for example, something like if a start date is populated, then use the
delivery frequency, then that is something we can also do.

20:24\
Yeah.

20:24\
So I, I was thinking perhaps we sent a delivery to this patient, yeah,
last week and it was the last delivery from their previous prescription.

20:34\
So now their previous prescription is expired because it\'s fully
dispensed.

20:39\
And we in that delivery last week, we sent 8 weeks supply and the new
prescription is the same.

20:45\
There\'s no dose change.

20:46\
Then we will send the new, we will send the next predicted delivery.

20:52\
Next predicted delivery will it will be in seven weeks from today yeah,
it would basically use the previous prescription.

20:58\
So what I mean by active prescription, right so yeah within like
dynamics we have like the we have like an activate and deactivate,
right.

21:05\
This is like for your record, status 1 is the prescription status,
right, Which is this field, right.

21:11\
And this is a separate act activate and deactivate button that comes
out-of-the-box, right?

21:17\
So OK, any prescription that you don\'t use or like basically it\'s the
equivalent of like deleting a prescription from, yeah, like a user
standpoint, since we don\'t give like people a delete privileges.

21:28\
Like for example, if you, someone just created a prescription by
mistake, then they would use the deactivate button to like make sure
that it\'s like, you know, completely ignored from any logic.

21:38\
Yeah.

21:38\
OK, so, so we can have a prescription which has expired or been
completely fulfilled, but it\'s still active in terms of triggering a
next projected date from it.

21:48\
Yeah.

21:48\
OK.

21:48\
We understand.

21:49\
Yeah, we understand.

21:50\
We call, we call this void in our current system, deactivate void, we
call it.

21:55\
OK.

21:56\
Does that come with division or like it\'s something you guys did?

21:59\
Yeah, it.

22:01\
Yeah, it it\'s just the way they\'ve built our system.

22:04\
Yeah.

22:04\
Yeah.

22:05\
OK.

22:05\
OK.

22:08\
Right.

22:09\
Any other questions regarding the next projected delivery date or no any
other screen here?

22:14\
Nope.

22:14\
OK.

22:15\
No, thank you.

22:17\
So the next tab is basically the patient details tab, right?

22:22\
Where it\'s.

22:25\
Yeah.

22:25\
So within the patient details tab, it just gives you like a quick view
of the patient and like you can add like the weight, height, et cetera
in this part of the tab, right?

22:35\
The next tab shows the, this is the prescriptions tab.

22:39\
Basically, like this gives you a view of all the prescription that are
associated with your left rib, right.

22:48\
From this, you\'re gonna have like a quick view as to like, you know how
many prescription this patient has been on, right?

22:53\
What kind of prescription type it is and like, for example, what the end
date and start date was of the previous prescriptions, right.

23:00\
If it shows, sorry, it shows the inactive ones as well, or just it
doesn\'t show the inactive ones.

23:05\
It does deactivate status.

23:07\
Yeah.

23:07\
OK.

23:07\
Yeah, if you deactivate, it\'s gone.

23:09\
Like, yeah, like I said, it\'s basically like the equivalent of delete,
but it\'s something you can like, you know, recover.

23:13\
Yeah.

23:14\
Auditable.

23:15\
Yeah.

23:15\
Yeah.

23:15\
OK, fine.

23:15\
Yeah, yeah.

23:17\
So basically this particular columns are configurable.

23:20\
So if like for example, you want more information here, then that is
something we can add, right?

23:26\
The next tab is the delivery orders tab, which basically shows all of
the deliveries that are associated with the specific prescription,
right?

23:36\
It also shows the, yeah, it also shows the scanned document and the work
order like the all the products that are present on this delivery order
in these deliveries.

23:47\
OK.

23:49\
The next tab is the stock check tab, which will become more relevant
when we get to the awaiting ACD stage, right?

23:56\
But I think we partially discussed it in the last session.

24:01\
So basically stock check is like how you, for example, you are
administrating like an AMG Vita product, right, to a patient, right?

24:09\
And you\'ve given like the first delivery and then you basically on the
second delivery, right?

24:13\
You want to record, for example, what the current stock levels are.

24:16\
Obviously, you can also like check what the current stock, like stock
levels are on the 1st delivery.

24:21\
But in a new prescription, you probably won\'t do that because it\'s
new.

24:26\
Yeah.

24:26\
So in this case, basically like you can record, for example, like what
the current patient\'s current stock is.

24:33\
PDF comparison is basically.

24:36\
So for example, if you have two prescriptions, right, then this
basically follows like the same ish logic where you have like a previous
prescription which, you know, follows the criteria I mentioned, where,
you know, it shows the last prescription that you got which was ACT
verified was either expired, ready or on hold, right?

24:54\
And it\'s not inactive, right?

24:57\
And you can like compare it with the current prescription that you\'re
on, on that, sorry.

25:08\
If there\'s a discrepancy, we have a process where we do prescription
querying.

25:13\
What happens there?

25:15\
What what happens there discrepancy meaning like there\'s a difference
between like the two prescriptions in terms of dosage, etcetera.

25:25\
Yes.

25:26\
OK, so I\'ll get to it when we get to like the transcription process.

25:30\
So basically there\'s like specific rules in the system that you know,
like sort of define what you can call like a renewal prescription, what
you can call a new patient prescription and what is what can classify as
a dose change prescription.

25:44\
Right.

25:45\
So I\'ll get to that when we are in the awaiting transcription stage.

25:49\
Yeah.

25:50\
And basically this is the document tab.

25:52\
This is like out-of-the-box feature where first people can attach
documents to specific prescription and then, you know, preview them.

26:00\
OK, I\'ll go back to the form just to show you, right.

26:08\
So yeah, like I said, just specific patient details, last prescriptions,
delivery orders here you can add like specific clinical annotations.

26:17\
I remember in the business process overview you mentioned like you
wanted the ability to for example, write in notes into the prescription
document itself.

26:29\
Yes, that\'s correct.

26:30\
Yes, Yeah.

26:32\
Right now we only like have this feature and we will log that the
document thing as like a separate requirement.

26:41\
Thank you.

26:43\
OK, right now this is a prescription that hasn\'t really gotten to the
delivery stage.

26:47\
So right now there\'s like nothing available.

26:50\
Drop check, same thing.

26:51\
And for PDF comparison, this is basically right.

26:55\
As of right now, there\'s no specific prescription on here, but I can
show the one I showed in my screenshot.

27:00\
Give me a second 331.

27:18\
So within the PDF comparison, we also have like these specific details.

27:22\
So it\'s the prescription details, right?

27:24\
These So what for example, you\'ve selected here prescription, say 329
and this is the current prescription that you\'re on, right?

27:32\
So what the system does, it basically like creates the sort of view,
right, where it shows you what\'s on the what the specific status was in
the prescription that you\'re on in the previous prescription or the
previous prescriptions.

27:45\
Prescription type was what clinical annotations were added in any in the
previous prescription, right?

27:51\
And the prescription status reason, right?

27:54\
And this is the clinical field change portion of it where, for example,
basically within each prescription, right, we add in patient order
lines, which sort of like signify the medication that we\'ve added,
right?

28:08\
So what this does is basically like for example, it shows you what the,
the frequency Rd administration method and total quantities where of
each of the prescription lines that you\'ve added into the prescription,
right?

28:27\
So like you can compare without say moving from screen to screen for
like, you know, it\'s like just like a quick look into what\'s in this
prescription, what, you know, medication was added here and what
medications present here.

28:42\
And this is the documents tab which I was showing earlier.

28:46\
They again, like, like I said, you can like, you know, associate a
specific document.

28:50\
And this is the related tab which shows like, you know, all the entities
that the prescription is related to, right?

29:00\
So right now, I guess like most of this is available here, but like you
can, you know, so hide specific tabs that are present if are needed.

29:10\
So like we can like make it just like the others where we discussed just
having the audit history here.

29:17\
OK.

29:19\
I\'ll just go put the stock check.

29:21\
Is that checking the stock the patient has on hand or checking the stock
that\'s in our warehouse of that product?

29:27\
It\'s meant to check the stock that the patient has on hand, right?

29:31\
So for example, if I\'m like prescribing this specific drug, right?

29:36\
So within each delivery, right, I can ask, for example, what\'s your
current stock of Metformin, right?

29:44\
And this is generated like way down the prescription stage at like the
ACT verification level, which we will go through as we like go through
these specific stages.

29:55\
OK.

29:57\
Any questions about check?

29:58\
Yes, yeah, Yeah.

29:59\
About the stock check.

30:00\
So is this like the history of the stock cheques that have been done?

30:03\
Because that will be done on the telephone call of the patient, right.

30:07\
It\'s not done during the prescription process.

30:09\
Oh, no.

30:10\
So basically, yeah, this is like something that you would do during the
phone call process, right?

30:15\
It just, this is just a view of all the stock check records that it
creates.

30:18\
So like you wouldn\'t, for example.

30:20\
Yeah, OK, yeah, yeah, yeah.

30:21\
So you wouldn\'t, for example, you know, want like to create like a
stock check line the moment you\'re, you know, building the delivery,
right?

30:30\
Like, right.

30:30\
We basically just set it up beforehand so that the only thing the user
needs to do is just like, you know, add in their current stock quantity
and it\'s like specific field.

30:39\
Yeah.

30:40\
Or OK, good.

30:41\
The medication listed.

30:42\
Yeah.

30:42\
So basically it shows stock check line per delivery.

30:45\
So for example, if you have 3 deliveries, it will show 3 stock check
lines.

30:50\
Yeah, yeah, yeah.

30:51\
So is this mandatory as part of the delivery booking process that they
have to do this or?

30:57\
No, it\'s not currently mandatory that they have to complete a stock
check.

31:00\
It\'s just something we give them the provision for.

31:02\
If you want to make it mandatory as part of confirmation or something,
then we can do it.

31:06\
But what did like if it\'s your first prescription, right, this is not
something they would do, right?

31:12\
Like wouldn\'t specifically ask for the stock because they haven\'t
delivered any medications yet.

31:18\
So it\'s not something we can make mandatory.

31:21\
So if there\'s like, well, yeah, I mean, we we can ask.

31:25\
The question is just if, if it\'s the first delivery, then maybe the
current stock level is 0.

31:30\
So, OK.

31:33\
And we do have new patients that hold stock because they\'ve been with a
previous provider or yeah or the pay per hospital they would have to
stop them or something.

31:43\
Yeah.

31:43\
So you would want them to add 0 if it\'s zero like OK, yeah, no, that\'s
fine.

31:49\
We can refit it as part of delivery booking process.

31:51\
That\'s OK.

31:53\
Currently it\'s kind of mainly captured in free type.

31:57\
So if, if here it\'s being captured as structured fields and that\'s
much better.

32:03\
It means that we can use it for reporting and things.

32:05\
So that\'s good.

32:06\
OK.

32:11\
Any other questions regarding this or can we move on to deliveries?

32:15\
Sorry, the mitigation orders creation.

32:18\
I was just going to say on the PDF comparison piece, is that is that
something we have we have today where the system throws up and
automatically spots that something\'s changed between prescriptions?

32:28\
No, no.

32:29\
So that looks quite that looks quite impressive.

32:31\
I would have thought.

32:34\
Yeah, we yes, yeah.

32:37\
I mean, if it\'s yeah, it if it works accurately, then yes, it is.

32:40\
Yeah, yeah.

32:42\
Cool.

32:48\
There\'s no questions.

32:50\
I\'ll just move on to the patient order part of this, right.

32:54\
So within prescription management, right, we, we have the ability to
create like two kinds of prescription lines, right.

33:01\
One is the regular dose, which we basically like say you have like a
very standard frequency that the person is meant to take.

33:10\
So for example, it\'s just, you know, take one MJ Vita 40MG pen every
day for 10 weeks by subcutaneous injection, right?

33:18\
So it\'s the standard frequency.

33:19\
There\'s no chain.

33:20\
They\'re just supposed to do this specific thing for 10 weeks, right?

33:24\
And the second type that we have is loading dose, right, where basically
a prescriber like advises a higher dose at the initial.

33:32\
Right?

33:33\
And then they they sort of like weaned off it to like, you know, follow
like a more normal dose, right?

33:39\
So like I\'ve given like, for example, an example here of like how that
would look.

33:44\
So it\'s just like, you know, say for loading dose, you would sort of
specify, for example, what they\'re meant to do on day one or day 2 or
day three.

33:53\
And like at what point they can like, you know, start taking the more a
more like consistent regimen, right.

34:02\
So within like current your current system, do you have like any other
kind of prescription lines or some other kind of like doses that you
manage?

34:10\
Yeah, So, yeah, well, kind of.

34:20\
So there will be different drugs which are used together, but I think
we\'ve already talked about that in terms of like primary drug and key
drug and all that kind of stuff.

34:35\
And then all the purposes of creating deliveries and prescriptions, we
would enter answer the reason currently in in the same kind of process.

34:49\
So.

34:54\
So I have a question which I think will probably answer the question
that you\'ve asked.

34:59\
So when you\'ve used the term here for the same product, what do you
mean by product?

35:08\
Sorry.

35:10\
Oh, basically, yeah.

35:11\
This means like for example, you\'ve created like say an Amgevita
loading dose type, Yeah, product type, medication order.

35:19\
So you cannot have like for example, that on its own.

35:22\
You will also need to have like a regular dose to mention, for example,
at what point they are meant to take like more consistent schedule.

35:29\
Yeah.

35:30\
So like you see right here where it says day 1-3, day 10 three, day 10,
two and day 30 onwards.

35:35\
Just take one every week or something.

35:37\
Yeah.

35:38\
So this is what I mean by same product.

35:42\
Yeah.

35:43\
So say for example, like it has to be the same VMP.

35:49\
Yeah, yeah, OK.

35:50\
Basically the same product.

35:51\
Yeah, yeah.

35:52\
So this this might be a this could be a problem.

35:56\
So say for example, it\'s easy with this particular drug with Anjuvita
because the loading dose might be two pens or three pens or whatever of
the of the exact same product.

36:08\
But sometimes the loading dose might be a different product pack.

36:14\
So say for example, with another drug, they might give you a special
pack which contains 2 milligramme and three milligramme tablets and then
the continuation dose is five milligramme tablets.

36:26\
So it will be a different product.

36:29\
I think compared to, you know, in the way that you\'ve described it,
technically it\'s a different product.

36:34\
It\'s not the same.

36:35\
It\'s not the same VMP is that almost like a one off, just one off
dispensing of that product and venue following products are actually
it\'s almost like separate dispensing, isn\'t it?

36:48\
Or a separate prescription, although it\'s not the separate person.

36:51\
That\'s what it means.

36:52\
So physically it\'s on.

36:53\
It\'s so physically it\'s written on the same prescription.

36:56\
Yeah, it\'s going to be entered together.

36:57\
But say for example, yeah, you might in the first, like the first
delivery might be different from the 2nd and 3rd and 4th deliveries
because you you have product one and product 2 and then deliveries 2-3
and four only have product 2, for example.

37:12\
Yeah, So it\'s like a single supply, right?

37:15\
Like only on the like in your example, there\'s three milligramme and
five milligrammes.

37:19\
So you get.

37:20\
So for the three milligramme 1, you only send it on the first delivery.

37:24\
And but all others like first, second, third, fourth can have the 5th 5
milligrammes tablets.

37:30\
Yeah, yeah, yeah, OK.

37:31\
Yeah.

37:32\
So I guess yeah, we would like you can like take that out as a
requirement and like give it a like a separate medication type for
example, that just for basically because this like sort of seems to have
different roles in the loading dose and the regular dose.

37:50\
So yeah, like we can take that down.

37:53\
It\'s although, although it although it is a a loading dose of that
drug, it\'s almost not a loading dose of that product, isn\'t it?

37:59\
It\'s almost like a short, yeah, a short course of yeah, it\'s a higher
dose product and then you go into your regular, it\'s creating loading
dose in a different way.

38:08\
Yeah, yeah, yeah, yeah, yeah.

38:13\
It it\'s the same current concept for the loading dose.

38:16\
It was for yeah, for the same product.

38:18\
It\'s just in case if you want to just have in the first initial few
weeks, you want that medication dose to be different comparatively to
the regular.

38:27\
That was the original concept for the current loading dose.

38:30\
But what we are seeing now as a requirement is a different concept that
the the brand or the product itself can be varied at the loading dose.

38:43\
Yeah.

38:43\
So like it\'s the same chemical entity, but it\'s a different VMP.

38:46\
Yeah, right.

38:55\
I think this is one of those ones where it once we can get actually into
the system, it would be good to work that, work that through and then
work out how we we do it.

39:03\
It\'s it\'s obviously doable within that, but it\'s how we make that
happen.

39:09\
Do you have like any other kind of doses like so you mentioned, you
know, different product, but like are, is there anything else that
doesn\'t like fit in within like say the regular dose and loading those
schedules?

39:23\
I don\'t think so, no.

39:25\
OK.

39:26\
I know you mentioned that ancillaries and basically like within Mesacare
you don\'t really add in ancillaries at prescription level right now.

39:34\
You just like add it in when you\'re building the delivery, right.

39:37\
So it\'s something you would need to do is like point of when you\'re
calling the patient, et cetera.

39:42\
Which is which is better?

39:43\
Yeah, that\'s fine.

39:44\
That\'s how we want which, yeah, yes, that\'s how we want to do it.

39:47\
Can I ask a dumb ex community pharmacist question, which is do we not,
do we do things like PRNS where we don\'t know how quickly they\'re used
or we should warfarin where, where patients would set their doses
themselves based on their their their own tests?

40:02\
Do we is, do we have any of those sorts of scenarios here?

40:06\
Similar?

40:07\
Yeah, could be, yeah.

40:10\
I\'m also thinking about growth hormone.

40:13\
Tarik does that.

40:14\
Is that in scope for as a, as a low tech products?

40:17\
Because I\'m thinking with that you\'ve got the product, but then
obviously the dose could be pretty much anything.

40:27\
Yeah, there will be lots of, there will be lots of things like that
daily doses.

40:31\
So where it\'s got regular dose and it\'s defined, can you have several
different defined doses or is it just or, or an open dose essentially
that can be then I suppose it Yeah.

40:47\
OK.

40:47\
So it will come down to how dose units are handled in the system.

40:52\
So yeah, it\'s easy when you have a box and it has five pens then you
will know will be 5 doses if the dose is 1 pen every something but say
for example there will be medicines where it\'s freely administered
where it can it\'s like a multi use, multi dose.

41:10\
So you might have A10 milligramme pen and it will be injects 0.5
milligrammes daily.

41:16\
So then the system would need to calculate 10 / 0.5.

41:21\
That means that there\'s 20 doses in this in this 10 milligramme dose
unit.

41:30\
Yeah, we do have like something for multi dose units are show that show
that to you guys like and how the calculation is handled for it.

41:39\
OK, perfect.

41:40\
Thanks.

41:43\
Right.

41:43\
So this is our regular dose form, right where basically if the
medication type is regular dose, right we have to some specific
mandatory fields.

41:53\
So for example, the product in the regular dose, the product field is
mandatory, the frequency and route is mandatory.

42:00\
And for example, you mentioned like say prescribed dosage, right?

42:05\
Like so for an AMGI metre type drug, which I believe is not multi dose
units, right?

42:11\
There\'s like a single usable pen, right?

42:15\
And in this case, they just add in the prescribed doses like say you
know, if they\'re supposed to take two pens, right?

42:21\
I\'m assume the prescribed dose would be 80, right?

42:24\
Or if it\'s three pens, then it would be 120, right?

42:27\
So what the system does is basically based on your product, right?

42:32\
We have a field called usable volume, which you can see here, right?

42:36\
So for each product, right, it mentions what the usable volume of that
specific drug is, right?

42:41\
So whatever you add in to the prescribed dose, right, that is divided
with the usable volume to give us like the number of units per dose,
which which basically tells you like how many of that specific product
you\'re supposed to take.

42:56\
And in in the case of say, you know, like the the product is not multi
dose, right?

43:05\
This is always done in like the number of units is never a decimal,
right?

43:10\
It\'s always for example, even if for example, you\'ve set up like the
prescribed dose, it\'s like 60, right?

43:17\
It\'s I\'m not sure what happens with MG beta.

43:19\
But like if for example, you did add 60, right, the you number of units
per dose would be set as 2, not as 1.5.

43:28\
OK.

43:28\
Yeah, yeah, it\'s always like basically it always considers like the
prescribed dose to be like a multiple of the usable volume, right.

43:36\
So it\'s never like a fraction if it\'s going to be like if the, you
know, calculation of prescribed dose divided by usable volume comes out
as .5, it will round that up to one.

43:47\
If it\'s 1.1, it will round it up to two.

43:50\
OK, well, will there be some kind of error message or warning or
something to say it\'s, it\'s not possible to give that dose or it\'s
not possible to like set it up as a decimal node?

44:01\
We don\'t have that.

44:02\
We just like automatically set it up as a two or three or four when they
add in the prescribed dose.

44:07\
But yeah, yeah, or for example, then error messages.

44:09\
And that\'s something we can do.

44:11\
Yeah, \'cause I guess you know, if someone, if in this example somebody
who wrote 60 or 90 or something like that, then we would want the system
to say that\'s that\'s not possible because.

44:22\
Oh, so you\'re saying like the prescribed dose should always be a
multiple.

44:26\
That\'s the error message.

44:27\
OK, It it, Yeah, exactly.

44:28\
In this example where it\'s OK, single use device that\'s your usable
volume is.

44:36\
Yeah.

44:37\
In that example that you\'ve given where it has to be a multiple
prescribed dose must be a multiple of usable volume.

44:45\
Then if user enters something which is not a multiple of usable volume,
then error should be you can only the the prescribed dose must be a
multiple of the usable volume.

44:58\
Yeah, OK.

44:59\
We\'ll take that down as a requirement, right.

45:03\
So basically we have the frequency and route where frequency is
basically where you mention like how many times per day they\'re
supposed to take it.

45:10\
So it\'s like you have like this is a configurable field, meaning that
you, I\'ll show you, you know how it works in the, when I\'m like
demoing the screens.

45:20\
But for example, in frequency, right, you can set up multiple kinds of
frequencies every week, twice per day, thrice per day, et cetera.

45:27\
And all of that like basically effects what the eventual total quantity
calculation would be, right?

45:34\
And we have the route will basically mentions, you know, how they\'re
supposed to take the drug.

45:38\
We have a maximum supply quantity, which is like a sort of like a
restriction, right, on how much a person can you know.

45:50\
So yeah, which is basically a cap on the total quantity for.

45:54\
So for example, right?

45:55\
Like right now you can see this is set up as 16, right?

45:58\
The the system calculated like the dosage as 16, right?

46:03\
But the maximum supply quantity that you have like maybe mentioned on
the prescription is 10, right?

46:08\
So what the user can do is, for example, they can add in 10 here, right?

46:12\
When they, you know, change the maximum supply quantity to 10, it will
update the total quantity as well to the value that you\'ve added in.

46:20\
But if for example, you added in say maximum supply quantity at 30,
right, then basically what the system, the system does not like change
the total quantity, right?

46:35\
OK.

46:36\
We also have like the concept of maximum supply per order, right?

46:40\
Where basically in a like for a medication you can specify that like in
a single delivery visit you, you\'re only supposed to give like 10
deliveries or specific medication or five, et cetera.

46:53\
And the system like stops you from delivering more than the quantity
we\'ve specified here for this specific product.

47:02\
So if I\'m like building a delivery, right, and I\'m updating my and my
maximum supply order for this Amgvita product is 5, right?

47:10\
When I\'m building the delivery and trying to like, you know, deliver 6
medications in one delivery, right, the system will stop me.

47:16\
OK.

47:18\
And you set, you set that up on the product level.

47:21\
You set that up and the patient order level.

47:23\
So basically because like with each prescription, right, you probably
get like a different maximum supply as to how much you\'re supposed to
give to the specific patient.

47:31\
So we\'ve done this at patient order level that you cannot prescribe
like more than sorry, you cannot like deliver more than this quantity of
medication for this prescription.

47:41\
That\'s your maximum supply quantity and maximum supply per orders.

47:44\
You cannot like, you know, deliver more than this, this quantity of
medication in a specific delivery in OK, we have the outer distribute
quantity, which basically like it\'s give me a SEC.

48:05\
Yeah.

48:05\
So outer, the way outer distribute works is basically, for example, in
this case you have the total quantity set as 16, right?

48:14\
And your number of deliveries is 4, right?

48:17\
So what the system does is basically like it if this flag is set to yes,
what it does is it divides the total quantity with the number of
deliveries.

48:26\
And when the delivery orders are created, each of the delivery for
example is just will deliver 4 quantities, right?

48:33\
Because it basically like divides the total quantity between your number
of work deliveries.

48:41\
Now, for example, if it\'s not like completely divisible, right, your
total quantity is 18, then whatever the remainder is, right?

48:48\
So like in the case of like say 18 / 4, your remainder is 2, right?

48:52\
So your first delivery will deliver the six doses, the six quantity,
right?

48:58\
And the rest will deliver 4.

49:04\
Does that make sense or?

49:06\
Yeah.

49:07\
So that the spares always go on the 1st delivery?

49:09\
Yeah, Yes, the spares will always go on the 1st delivery.

49:12\
OK.

49:14\
You mentioned about finding frequency.

49:17\
Yes.

49:18\
And we can, we can set those up ourselves, ourselves.

49:22\
Yeah, you can like create order setups for example, for one week, two
week, three-week, twice a day, twice a day, etc.

49:28\
That\'s something you can create.

49:30\
And so then there needs to be some kind of fraction or something
attached to each one.

49:34\
Yeah, I\'ll be showing that.

49:37\
Exactly.

49:37\
I\'ll be showing that.

49:38\
And I\'m.

49:39\
Yeah, like, yeah, fine.

49:40\
OK, it\'s cool.

49:42\
OK.

49:43\
This is basically like a sort of a recap of what I\'ve just said.

49:47\
But like, right now for a regular dose, the mandatory fields are product
frequency and route, right?

49:53\
Product selection, right.

49:54\
So for example, what products are shown in the specific?

49:59\
The product field right is based on these specific criteria.

50:04\
So it will only show products that are on active contract lines, right?

50:10\
The primary field on that contract line must be set to yes, right?

50:13\
The product must be active and a medication product right?

50:17\
The product must not be in the restricted VMP grid, right?

50:21\
And product is in the allowable alternative script.

50:25\
So during the referral process, you may have gone over some parts of
restricted VMP, but I will be showing that right now actually so that I
can like show you these multiple criterias, right?

50:37\
And in this field, we also have like the ability to like, you know, sort
of disregard the above criteria.

50:44\
If, for example, a user sets the allowable products on patient order
field to know where it in that case, it just shows products that meet
these three criteria, right?

50:54\
And as part of the, I believe during the contract calls, right when we
were discussing like how the contract lines must interact with like
product selection.

51:04\
So we will be adding like we will need to basically add in two more
criteria, for example, that the contract line must, you know, the start
date must not be greater than today\'s date or you know, lesser than and
the end date must not be lesser than pay\'s date, right?

51:20\
So it\'ll basically like the idea is it will only show product
selections from valid contract lines.

51:25\
OK, I\'ll go back to the screen.

51:27\
So I can like show you all the things I mentioned, like just with
regards to product selection, OK, right.

51:52\
Yeah.

51:53\
So this is the field I was talking about, show allowable products,
right?

51:57\
When it\'s yes or no, it basically like, you know, changes what kind of
products are available.

52:02\
If it\'s set to yes, right?

52:03\
Then in this case, basically what it would do is so it goes to the
contract lines, right?

52:10\
Where?

52:12\
Well, just for like moving through schemes a lot, but like I can\'t
really show it without it, OK?

52:18\
Right.

52:18\
So basically if in your contract, right, you have like specific sets of
contract lines, OK, We went through this briefly over during the
contract decision, but this is like where it becomes more relevant,
right?

52:32\
Like what kind of products you can select, OK?

52:35\
So for example, right now what the products you can select are basically
those that are in an active contract line.

52:41\
So this is active, right?

52:43\
It\'s the same thing we mentioned in the previously regarding like void
and what is a void in your system and like what is, you know, active and
deactivating.

52:55\
So basically deactivation is like the equivalent of delete, deleting
something, right?

53:02\
So within the contract line, basically if a product exists on the
contract line and the primary field is set to yes, right and.

53:18\
Sorry.

53:26\
Yeah.

53:27\
So basically what the allowable products would show is like stuff
that\'s on your contract line products where it is active, right and
where the type is set to medication, OK.

53:39\
And also at the level right, we have like a sorry.

53:54\
OK.

53:59\
Like I have all my screens, OK.

54:04\
So within the referral, we also have like this restricted VMP is great,
right?

54:07\
Where you can sort of mention what kind of products, right?

54:11\
Should not be shown on this, this product look up, right?

54:15\
And whatever products you add in here will not be visible in this
specific look up, right?

54:20\
And for each say restricted VMP that you add in, right, you can specify
what the allowable alternatives are, right?

54:29\
So, so right now, for example, I\'m adding Cosentyx, right?

54:33\
So I can mention here in this specific area, right?

54:37\
What kind of products can be used as an alternative, right?

54:41\
And basically this selection is driven by the VMP, right?

54:44\
And so for example, this product look up will show stuff that\'s in the
contract line, right, where this specific field is set to.

54:51\
Yes, right.

54:53\
The product is active in a medication, right?

54:57\
It\'s not a restricted VMP and is present in this allowable alternative
script.

55:03\
Does that make sense or?

55:05\
Yeah.

55:06\
So yeah, I had to move through so many screens, but yeah, like it\'s
sort of like divided between like lots of subprocesses when you jump
between a lot of screens.

55:17\
But I think the logic is fairly sound that it needs to.

55:21\
Yeah, it needs to essentially it needs to be an allowed product, isn\'t
it?

55:24\
Yeah, essentially it needs to be an allowed product.

55:27\
And how it defines an allowed product is that it\'s not a restricted
VMP, it\'s present on the contract line.

55:32\
And the product is a medication type and it will go to the primary one
first, right?

55:37\
Yeah, yeah, yeah.

55:39\
So it will go to the primary one first.

55:40\
If that\'s not available, it then goes.

55:42\
If that\'s not active, it will then go to the alternative.

55:46\
Yeah, not completely.

55:48\
Basically it shows like all of the products that meet like specific
criteria that I\'ve mentioned here, right?

55:54\
So if you have like multiple products that are set up as primary, none
of them are restricted and all of them are medications, right, Then all
of them would show up in this specific look up.

56:03\
OK, but, but actually the the logic then is driving what you can see in
that product line that you\'re on now.

56:09\
So actually a user doesn\'t need to worry about checking all of those
screens.

56:13\
They just need to do the look up and see what\'s available to them.

56:17\
Yeah, I had to mention all of that as like a prerequisite.

56:19\
Oh yeah.

56:20\
Like we have like specific areas that mention like what you can and
cannot select.

56:24\
And yeah, that\'s, yeah, basically those were the screens I was going
through.

56:27\
Yeah.

56:28\
OK.

56:29\
Yeah.

56:29\
So as what we\'ve in terms of what we\'ve got.

56:31\
So just quick question, so certain drugs are contracted to certain
hospitals when we set this up, would it be an individual kind of trust
level that the the drug will be a primary for?

56:43\
Does that make sense?

56:45\
So for example, for a specific therapy and preferred combination, right,
that\'s like basically what drive like the therapy the preferred
combination is.

56:56\
Yeah, yeah, that\'s what like drives your product selection, right?

56:59\
So if it\'s Angie Vita and your preferred is like, I don\'t know,
Vale\'s Hospital, right, then you can like set up, for example, for this
combination, what is a primary product and what kind of products you
can, you know, select in the prescription.

57:14\
Yeah, that makes sense.

57:15\
Cheers.

57:16\
Yeah.

57:16\
So for a different hospital and therapy combination, you can specify a
different list of products with a different list of primary products if
that\'s required.

57:27\
OK.

57:30\
So yeah, that is the product selection part of it.

57:34\
And like this is the frequency part.

57:36\
So basically right now we have like lots of like frequency set up.

57:40\
So when a user is selecting them, they basically have like as many
options as they set up.

57:46\
So currently we\'ve set up like lots of them, right?

57:49\
So we have like AST, but twice a day, every 11 days, 12 days, 13 days,
et cetera, right?

57:54\
And if I go into the frequency screen, right, this is where you know
that decimal value is added to like help with the calculation, right?

58:03\
So for every 10 days, for example, right, the frequency per day is .1,
right?

58:08\
If it\'s twice a day, then the frequency per day would be two.

58:10\
If it\'s eleven, then you would just add in like 2, like 4 decimal
points what the actual frequency per day would be.

58:20\
Does that make sense?

58:27\
Yeah.

58:29\
OK.

58:30\
Would we need to do an exercise to match that to codes or frequencies
that we have today or are they similar in?

58:37\
Yes, you should be basically like checking what\'s present in your
current system and then setting them up as frequencies here.

58:44\
So they\'re they\'re not currently in, they\'re not currently in
structured fields in our current system.

58:49\
OK.

58:50\
So yeah, you will have some difficulty with that.

58:55\
We will probably have to make an assessment to to set the initial ones
up.

59:01\
So is it is, is that I\'m thinking how to phrase the question.

59:10\
So when we set up a frequency, is that product specific, contract
specific or global throughout the system?

59:19\
Global throughout the system at the moment.

59:21\
All right, cool.

59:22\
Thank you.

59:24\
Yeah.

59:24\
So we also have the root field, right, which basically mentions how
you\'re supposed to take this drug.

59:29\
So this is also like something you can set up to have as many as you
currently use, right.

59:35\
I\'ll just show the advanced lookup because like there\'s we basically
like set up a whole list of them.

59:40\
So yeah, like, for example, you can like create like your specific codes
and then mention like in the description, like what kind of code it is,
right?

59:49\
Yeah.

59:50\
Does does it need to come up from the the product master?

59:54\
Yeah, we do have like in the product master, we do have like this
information available like how you\'re supposed to take it.

1:00:01\
Give me a second.

1:00:02\
Where was that field?

1:00:07\
Yeah, yeah.

1:00:08\
Route of administration.

1:00:09\
Sorry.

1:00:09\
Yeah.

1:00:12\
So you can like fairly probably thought it\'s quite an exception, isn\'t
it that we\'re not following the standard route of administration for
most of these products?

1:00:20\
We haven\'t really set up any for like the products that we have since
this is like a test environment.

1:00:24\
But like if you set up something to have a product to have like a
specific route, then yeah, it will just default that.

1:00:33\
And if it\'s present on your scan document, then it would also like show
that as well.

1:00:39\
Yeah, it doesn\'t come from the DM and D by by product now.

1:00:47\
It can be thought I would have thought it wouldn\'t it the assault.

1:00:50\
Yes, yeah, it can be OK.

1:00:53\
The only problem with that, Pete, is where unlicensed use or say for
example, injections given by nebulization that that would be the
probably the main exception to the but I think it\'s probably it\'s an
exception scenario rather than wanting to fill this in for every yeah,
yeah, correct.

1:01:14\
That forming we do yeah, yeah.

1:01:17\
Can you repeat that?

1:01:17\
What did you mean by exception?

1:01:18\
What\'s the exception?

1:01:20\
So, so usually we would want it to present only the options which are
set up for that.

1:01:28\
So for example, for yeah, from the DM and D for the for the specific
product.

1:01:32\
Like we wouldn\'t want someone to be able to choose anything.

1:01:37\
It should be product specific, the options.

1:01:40\
But there will be cases where we have prescriptions for unlicensed use.

1:01:44\
So say for example it\'s a injectable product and so the options would
be Ivy from from the product database, but the actual prescription may
be for inhaled.

1:01:59\
So they will use the injection by inhalation.

1:02:04\
So, so like for a single product you can have multiple routes, but like
in the prescription itself, it would just be like 1 route, right?

1:02:10\
Like like you wouldn\'t say have say I don\'t know one Amgevita that
says, you know, route subject subcutaneous injection and the other
Amgevita product that like sorry for the same product you would have
like 2 methods of two routes.

1:02:24\
Basically it it maybe sometimes they will write on the prescription I
intramuscular or subcutaneous.

1:02:31\
Yeah, it\'s possible for some products or something can be, Yeah, Yeah.

1:02:37\
OK.

1:02:38\
So for a single medication line, you would have a scenario where
there\'s like 2 routes.

1:02:45\
It\'s an OR scenario.

1:02:46\
OK, it\'s possible.

1:02:47\
Yeah, yeah.

1:02:54\
But like the frequency etcetera doesn\'t really change, right?

1:02:56\
It\'s just the route.

1:02:57\
Like you\'re still supposed to take it every day, but you can have it
via this or this specific route there.

1:03:08\
There will be some scenarios where it\'s where it\'s where the duration
is chosen by the patient.

1:03:15\
You know it\'s possible.

1:03:22\
And also, that\'s never off licence situation as well, isn\'t it?

1:03:25\
Yeah.

1:03:25\
So say, say for example, with paracetamol, you can take every four to
six hours.

1:03:29\
That would be an example.

1:03:30\
So the patient can take it, you know, every four hours or every six
hours.

1:03:34\
You know, sometimes it\'s different, sometimes it\'s the same.

1:03:40\
OK.

1:03:42\
No, my question was like more along the lines of like whether or not we
would like need to create like two different patient orders for this.

1:03:48\
If like if it\'s the same, for example, you know, it says, you know,
take this tablet once per day by this route or this route then, right.

1:03:56\
You would like, we could just, you know, create like a single prescript
patient order and like let you know people use like one of two routes.

1:04:05\
Yeah.

1:04:05\
I, I think for the, for the purpose of this, I think yes, I think yes,
that\'s, that\'s, that would be fine.

1:04:09\
Yeah.

1:04:11\
OK.

1:04:16\
Yeah.

1:04:16\
So this is the total quantity which is calculated via like specific way
US formula that I\'ll show in the next slide.

1:04:26\
This is the outer distribute quantity where user can like save.

1:04:31\
So for example, if they set this to no, right, then every delivery will
be created with like quantity set to 0 and the user has to manually like
add that in.

1:04:43\
So instead of like, say dividing 16 and like sorry, yeah, dividing say
16 between 4 deliveries by, you know, just adding in four to each,
right?

1:04:55\
When you set this to no, you can basically like specify that, you know,
the first one should go to the first one should be 6, the other one
should be 3 two it\'s or 321.

1:05:05\
And then and the last one, you can like specify like how much like
basically you can manually enter like within each delivery what you
need.

1:05:16\
If you set this field to no, right, the default option would be just be
that it\'s set to 0 and a person has to like make the judgement when
they\'re calling or contacting the patient.

1:05:26\
OK, this is the mandatory instructions field, right?

1:05:30\
Basically, this is a field that is copied over from the product, right?

1:05:33\
So within the product, we also have like a mandatory information, right?

1:05:38\
Whatever value is added here is also then copied onto the specific field
when like, sorry, this field when a person selects a specific product,
right?

1:05:51\
Auditing.

1:05:52\
I think we said that would be the DM and D warnings, didn\'t we?

1:05:54\
If there was mandatory warning, yeah, yeah.

1:05:55\
DNF warnings, yes, some of work order quantities and supply, et cetera.

1:06:02\
They become more relevant after like the work order creation phase.

1:06:06\
But basically what happens is like to give a brief overview when you
like set up or when you set a prescription to ready, as in like the
final stage, right?

1:06:15\
What this does is basically whatever it calculates, like all of the
product quantities that have you have like added into each delivery,
sums that up and adds that value here, right, We have the supply
quantity, delivered quantity, remaining quantity and undispensed
quantity.

1:06:33\
So supply quantity is basically just something we use as a reference to
like figure out how many deliveries do we need to make against a
specific patient order, right before we set the order status to
delivered, right?

1:06:47\
But delivered quantity updates basically as like each order gets
delivered the quantity on that delivery, right?

1:06:53\
It\'s updated here.

1:06:54\
So for example, you have two work orders, right?

1:06:57\
And they both have this product, right?

1:07:00\
The first delivery delivered a quantity of eight, right?

1:07:03\
Then this system will basically like update the delivered quantity to 8,
right?

1:07:08\
Then the second delivery, like whatever quantities on the second
delivery would just be added on to it, right?

1:07:14\
And for example, if your delivered quantity is greater than or greater
than or equal to the supply quantity, then the the patient order is
marked as expired, right?

1:07:27\
And remaining quantity is basically like the difference between the
delivered quantity and the total quantity.

1:07:33\
So whatever, yeah.

1:07:37\
So your total quantity is just minus from the delivered quantity and
it\'s just added into the remaining quantity, right?

1:07:43\
Right.

1:07:45\
Any questions regarding this or I can move on to total quantity
calculation in more detail.

1:08:02\
If there\'s no question, then I\'ll ask one of my own.

1:08:04\
Basically, like, for example, do you need like for example,
restrictions?

1:08:10\
Do you know stop like oversupply?

1:08:12\
So for example, you\'ve set up like say a total quantity of 16, right?

1:08:17\
And you don\'t want a user to, you know, set it like deliver 18
quantities like it should flag for errors or, you know, give
notifications, for example, if you\'re delivering more than what you\'ve
set out here in your total quantity.

1:08:34\
Yeah, we, we can\'t send more than the total quantity here.

1:08:37\
So you would need like notifications, for example, and restrictions when
they\'re updating like quantities on a work order.

1:08:46\
Yeah.

1:08:46\
So how how would how would that be possible?

1:08:49\
How would So like I said, right, we have the sum of work order quantity.

1:08:53\
So like basically what we consider like a prescription to be, you know,
ready.

1:08:58\
Actually, I\'ll just open the prescription.

1:09:00\
So like there\'s a proper deference point.

1:09:04\
Yeah.

1:09:04\
So basically, when a prescription is considered ready for delivery, when
we\'ve set the prescription status to ready, meaning it\'s like past all
of these BPF stages, right?

1:09:14\
So they have completed transcription, they\'ve completed validation and
the person has like set the ACD check, right?

1:09:21\
So basically what the system does afterwards is that for each delivery
that you have like say you had like 3 deliveries, the quantity of this
specific product on that delivery, right?

1:09:34\
So like you have in all three deliveries and the sum of quantity you are
delivering is 15, right.

1:09:41\
So since the moment where the prescription was set to ready, the
quantity you\'ve set up is 15, then we use like that sum as our that sum
as our restriction, right.

1:09:55\
So for example, if a person is updating quantities after a prescription
has been set to ready and it\'s becoming greater than 15, like the sum
of all the quantities, right, then we can flag for a flag a user for
errors.

1:10:08\
Yeah, OK.

1:10:09\
You know, like they cannot, you know, over prescribe, right?

1:10:12\
They they\'d be amending it in here or they\'d be amending it in
Business Central.

1:10:19\
So part of the quantity that\'s being updated is done within our system
before a delivery would be confirmed.

1:10:26\
Yeah, right.

1:10:26\
So yeah, when you have deliveries here, right?

1:10:30\
Yeah, basically you would have like the quantities that you can update
from say 4 to like the for example, in, in the initial you\'re
delivering 4 quantities, right?

1:10:41\
Then you can update that to 567, right.

1:10:44\
But if it\'s going above the sum of work order quantities that you\'ve
set up, right, then the system is lacked forever errors in this system,
not in the centre, right, fine.

1:10:53\
So in our current system, once this once the prescription has passed
through validation and verification, then the quantities are locked.

1:11:04\
And if you try and change a quantity for a future delivery, then the
system will force you to remove that quantity from another delivery so
you can redistribute the quantity.

1:11:15\
So say, for example, you\'ve got 444, you can make it 2244 or you can
make it 264, or you could make it, you know, 4, 8 and 0.

1:11:30\
But you can\'t just, you know, add, you can\'t make it like 644 because
you\'ve added the, you know, you\'ve increased the total amount.

1:11:37\
So that\'s the kind of thing that we would want.

1:11:40\
So we don\'t want it to allow someone to edit the quantity and then
increase it above what\'s been validated and verified.

1:11:50\
Yeah.

1:11:51\
OK.

1:11:53\
Basically, for example, if they do need to like, you know, update the
quantities like for any reason, the basically the step they would have
to follow is they would have to amend the prescription, bring it back to
draught and then they would be able to like change this prescribed dose,
et cetera, to like calculate a new sum of our order quantities.

1:12:09\
Yeah, fine.

1:12:10\
And and you can do that if you sent a delivery or only if nothing has
been delivered, you can amend at any point in the prescription.

1:12:19\
Fine.

1:12:19\
OK, Expiry, fine.

1:12:21\
So if we\'ve delivered say one delivery or four and there\'s two
deliveries or 4 left, then we can go back and amend it and as long as it
goes through verification and yeah, validation again, fine, OK, great.

1:12:33\
Thank you.

1:12:33\
Yeah, because the system basically like you know stores the delivered
quantity already.

1:12:37\
So do you like even then you\'re not like at risk of oversupply?

1:12:40\
So because basically this orders, the patient order would just expire
when, you know, you\'ve sort of match the quantity that you were meant
to supply in the sum of work order product quantities.

1:12:52\
So like for example, if you if it was originally 15 and you\'ve
delivered 7, right, and you update this to 21 after amending, right, you
can still only deliver like 14 more before this like prescription.

1:13:04\
Sorry, this patient order would expire.

1:13:06\
Yeah.

1:13:06\
And OK would probably expire the prescription with it.

1:13:09\
Perfect.

1:13:10\
Yeah, if it\'s the OK.

1:13:16\
I assume this is all understood, so I\'ll just move on.

1:13:19\
So right now what we have like for regular doses is total quantity
calculation.

1:13:25\
We have some specific prerequisites, right?

1:13:28\
So basically the patient order, sorry, the product on your patient order
must have a usable volume, right?

1:13:35\
Your patient order must have a prescribed dose, meaning like there
should be something to identify, like how much the person is supposed to
take must have a frequency, right?

1:13:45\
It must have a unit per dose, right?

1:13:48\
And basically this is calculated like based on whether or not it\'s a
multi dose or not.

1:13:53\
So if it\'s multi dose, right, that means that this specific product,
right?

1:13:59\
If the unit per dose can be done in fractions, right?

1:14:02\
So in decimals, I mean, right.

1:14:04\
So the formula for this is basically 11 divided by the round down value
of the usable volume and prescribed dose, right?

1:14:15\
So for example, your usable volume is 50, right?

1:14:20\
And your prescribed dose is 130, right?

1:14:22\
So basically, yeah, yeah.

1:14:28\
So yeah, if your usable volume is 50 and your prescribed dose is 130,
right, then the system basically like divides 50 by 1:30.

1:14:35\
It rounds it down to like, say, the second decimal point.

1:14:38\
So if it\'s like 1.38666, it will just set it to 1.38, right.

1:14:43\
And then basically it would just, you know, like .138 rather anyway,
yeah.

1:14:52\
So basically whatever value comes out of rounding down the specific
calculation would be set up as your unit per dose.

1:14:58\
OK.

1:14:59\
And if the, if it\'s set to multi dose equals no, then basically like
your unit per dose can always be like a result that\'s like a multiple
of your prescribed dose, which we just discussed, right?

1:15:14\
The next prerequisite is basically having like a pack size value on your
product.

1:15:18\
So you\'re supposed to, for example, mention like whether you know this
is like A10 tablet, like say it\'s something like Panadol, right?

1:15:26\
Which is like has 10 tablets in one pack, right?

1:15:29\
So you would like say mention on your product product master that this
specific product is like A10 size product, which I\'ll show when I show
you like the product form again, right?

1:15:42\
So basically right now for total quantity calculation, we have like 2
two calculation methods, right?

1:15:50\
1 is where the, you know, the contract lines allows you to split the
pack, right?

1:15:56\
So for example, you have a scenario with Panadol again, right?

1:15:59\
Where you have like, say 10 tablets, right?

1:16:03\
But patient only needs 6, right?

1:16:05\
So in this case, like basically you\'re allowed to like split the pack
and only give like 66 tablets to a specific patient, right?

1:16:14\
Or your contract line can have like, say the split pack set to no split
right?

1:16:19\
And you\'re basically only allowed to sell the parent all is like that
10 pack, right?

1:16:25\
And basically after that, we have like the specific logic that like
accounts for both of these scenarios.

1:16:32\
OK, So I\'ll just go back to the screen so I can like show you what I\'m
talking about.

1:16:37\
Like again, I\'ll probably be moving through a thumbscreen.

1:16:40\
So yeah, give me a second.

1:16:42\
OK.

1:16:43\
So, so I think it\'s, I think it\'s what we would want.

1:16:46\
Yeah, yeah.

1:16:49\
OK.

1:16:49\
So within the product itself, right, we have like this specific pack
size value, which I mentioned, right?

1:16:54\
This would probably be 60 because like it has 60 in one pack.

1:16:58\
But yeah, and basically at this point, you can mention whether it\'s
like a multidose unit or not, right?

1:17:05\
This is something that\'s done within the product master, OK.

1:17:08\
And at the contract line level, you can mention whether like say you\'re
allowed to split it or not split it, right?

1:17:16\
And over here in this specific field basically mentions whether you can
round up or round down.

1:17:22\
OK.

1:17:24\
So I\'ll just go through what like each of these things mean, right?

1:17:29\
So right now I\'ll go back to my slide, right?

1:17:33\
So basically if you\'re calculating like the total quantity, right for a
product where contract line has allowed split, right.

1:17:40\
So what it does is basically it takes the unit per dose from your
patient order, your frequency, the fraction that we mentioned here in
our frequency record.

1:17:52\
So like for example, it\'s .1 and your duration which comes from the
prescription, right?

1:17:58\
So in this case it\'s, I guess 7, right?

1:18:00\
So basically what the system will do is that it will use this specific
field, the decimal that\'s mentioned in the frequency, and then multiply
it by their total duration to give you the total quantity, OK, right.

1:18:14\
And for example, if the contract has not allowed split, right?

1:18:19\
So what basically happens is it does do the initial calculation that we
mentioned earlier, right?

1:18:26\
But the system keeps adding one to it until it becomes like a multiple
of the pack size value, right?

1:18:34\
So basically, for example, if your total quantity for unit per doors
frequency and total duration came up to 8, right?

1:18:41\
This would be this would be rounded up to 10.

1:18:44\
Or in the case where like say the pack size is 10 tablets, right?

1:18:49\
And sorry last, yeah, yeah.

1:18:54\
So in the case where like the pack size is 10 tablets, so it is rounded
up to 10.

1:18:58\
And then that is your that would be your total quantity, right?

1:19:01\
So, and if for example, the roundup is set to down, right, meaning you
know your in this example for where we calculated the total quantity and
it came up to sorry, 11, right.

1:19:17\
So the system will basically like subtract 1 until it becomes like a
multiple of your pack size value, sorry in 11, sorry.

1:19:37\
Yeah.

1:19:37\
Does that make sense or and does that meet requirements in terms of like
what you can do with regards to split packs and multidose units?

1:19:47\
Yeah, I think it makes sense.

1:19:48\
Yeah.

1:19:48\
Thank you.

1:19:57\
Sorry.

1:20:00\
So this was basically how we calculate total quantities for regular
doses, right?

1:20:05\
And the next step is basically like the slide where I mentioned, like
what you can do with regards to maximum supply, so.

1:20:12\
It is like some that I\'ve already mentioned, but yeah, the brief
highlight like if your maximum quantity that you\'ve added is less than
your total quantity, the system will basically update the total quantity
to the maximum and what maximum supply per order is meant to do and how
auto distribution works.

1:20:29\
OK.

1:20:30\
Let\'s move through this slide.

1:20:34\
And this is our loading dose form, right?

1:20:37\
As you can see, it\'s like a bit more, it\'s a bit smaller with regards
to like the regular dose.

1:20:43\
So we don\'t have like a concept of a maximum supply here or a maximum
supply per order, right?

1:20:49\
We have the same product field which follows the same lookup rules,
right?

1:20:54\
And how, And it basically also has like the root mentioned in the
loading dose and like what their total quantities are.

1:21:05\
Most of this is like, you know, follow some of the same logic, it\'s
just that how the total quantity is calculated is a bit different.

1:21:13\
OK, so within the loading dose form, we have like the concept of
medication doses, right?

1:21:18\
Where basically this is how we sort of mention right, what the loading
dose schedule is, right?

1:21:26\
So for example, if I\'m creating like a yeah, so if I\'m creating a
loading dose for Amjvita, right, I\'m supposed to mention like what the
schedule of that loading dose is.

1:21:39\
And the way I do it is via the medication dose form, right?

1:21:42\
So against each loading dose, I would mention, for example, what the
dosage is, right?

1:21:48\
What week it\'s prescribed for, right?

1:21:51\
And whether or not it\'s like the final loading dose, OK.

1:21:55\
So basically what this means is that you mentioned, for example, using
the medication dose form.

1:22:02\
You mentioned, for example, what they\'re meant to do on day one, day 2,
day three, day 4.

1:22:07\
You can get to that level of granularity.

1:22:09\
Or you can mention what they\'re supposed to do on week one, Week 2, day
15, day 16, et cetera, right?

1:22:16\
And within each medication dose form, you can mention whether it\'s like
the last, yeah, whether it\'s like the last loading dose schedule, last
regimen of the loading dose via the final loading dose feed, right.

1:22:32\
And you can mention, for example, at what point they are supposed to
start taking like the regular doses.

1:22:40\
So this is like the configuration that we have at medication dose level.

1:22:47\
So do you see here, do you see anything here that might be missing or
no?

1:22:55\
I think it\'s OK.

1:22:56\
So I mean apologies if I missed it because someone came and disturbed
me.

1:23:01\
What is there?

1:23:04\
Is there the ability to specify several different loading doses?

1:23:11\
So say, for example, with this drug, it could be 80 milligramme week
zero, 80 milligramme at week 1 and then 40 milligramme every other week.

1:23:22\
So how, how would we construct that?

1:23:24\
There is a, there is the ability to add like 2 initial separate,
separate doses.

1:23:31\
And then so in the case of like 80 milligrammes, you would just tell
them to take two pens, right?

1:23:36\
Or is what do you say like take the 80 milligramme product?

1:23:39\
Yeah, yeah, 2, two pens, Yep, Yep, 2 pens, yeah.

1:23:41\
So basically, yeah, you can mention for example, week 1, take 2 using
the number of unit per dose field, right.

1:23:49\
Take two of the MJ Vita on week one, right.

1:23:52\
And then you can create a medic, another medication dose form that\'s
associated with the loading dose.

1:23:57\
I\'ll show the screens in a minute to show you like how it\'s done, but
basically like I think I haven\'t.

1:24:04\
Yes, yeah.

1:24:05\
So for each medication dose you can mention, yeah, you can like
associate it with your loading dose.

1:24:09\
Yes, exactly.

1:24:10\
Fine, OK.

1:24:11\
Yeah.

1:24:12\
And yeah, in that other example, so say for example, we wanted to give
them the 80 milligramme pen for the loading doses and then 40
milligramme for the future, like the regular dose then we can do that as
well or not if it\'s an 80 milligramme pen and the wait, your loading
dose has the 80 milligramme pen and your regular dose has the 41, right.

1:24:37\
Correct.

1:24:37\
Yeah, Yeah, Yeah, not exactly.

1:24:41\
No, you have like basically right now it\'s done at product level.

1:24:43\
So you yeah, have to be the same product.

1:24:46\
OK.

1:24:46\
So it\'s like the the scenario we talked about earlier on the three
milligramme and five milligramme and all this stuff.

1:24:51\
Yeah, yes, OK, fine.

1:24:53\
So like you would have to use like the first order supply sort of
scenario for that like fine.

1:24:58\
Yeah, Yep.

1:24:58\
Got it.

1:24:59\
Thanks.

1:25:01\
OK.

1:25:04\
So basically like this is the screen I was mentioning, right?

1:25:07\
So you can like this is your loading dose, right?

1:25:09\
And you can mention for example, how many medication doses there are,
right?

1:25:13\
And basically how it calculates like the total quantity for a loading
dose is like for each record you have say you had like 3 medication
doses and all of them had two, right?

1:25:23\
The system sums up that value and just adds it to the total quantity,
right?

1:25:29\
And basically for loading dose, what we do is like all of the quantity
of the loading dose is sent in the first delivery, right?

1:25:35\
Where we basically have a formula to determine what quantity we\'re
supposed to send via the first delivery order, right?

1:25:43\
So it\'s basically what like, yeah, yeah.

1:25:57\
So basically in the previous screen I mentioned like the maintenance
start date, right, which this is what we basically used to like figure
out like ratio of like at what point, right?

1:26:13\
What ratio of the delivery frequency is like meant to be covered by the
loading dose, right?

1:26:19\
And what part is meant to be covered by the regular dose?

1:26:23\
So we have like say the maintenance start date and delivery frequency,
we calculate them in days to figure out like that ratio.

1:26:30\
So for example, your delivery frequency is 4 weeks, which is 28 days and
your maintenance starts from the third week, right?

1:26:38\
So basically what this means is from the patient\'s like four week
regimen, right?

1:26:43\
Three weeks of it is meant to be covered by the loading, by the loading
dose, right?

1:26:48\
And what we do with that ratio is we multiply it with the quantity of
the regular, like the quantity division of the regular dose, right?

1:26:56\
So quantity division is like what we I described earlier.

1:27:00\
Well, you know how the system like determines how like the, the total
quantity is meant to be delivered across like say delivery.

1:27:10\
So if it\'s like 12/12/12 is your total quantity and you have 3
deliveries, then basically your quantity per delivery is like 4, right?

1:27:20\
So this is the calculation that\'s used here.

1:27:21\
It means like out of the four quantity, it only needs to like only one
week of it would be covered by the regular dose.

1:27:30\
So we only need to send like 1 quantity from the regular dose, right?

1:27:33\
And the rest will be covered by the loading dose quantity.

1:27:41\
Does that make sense?

1:27:44\
Yeah, I think so, Yeah.

1:27:46\
OK.

1:27:47\
So is this any different from how you would like, you know, categorise
loading doses now, like how they all like make?

1:27:54\
Yeah, I, I think we, we just, we just make all of these calculations
manually right now.

1:27:58\
But yeah, it\'s, it\'s the same, it\'s the same logic, I think so, yeah.

1:28:02\
It basically like it\'s just trying to figure out the ratio of the
delivery frequency, the regimen the patient is meant to follow that will
be covered by the loading dose and whatever\'s left will be covered by
the regular dose.

1:28:13\
Yeah.

1:28:13\
Yeah, exactly.

1:28:14\
Yeah.

1:28:17\
So within this we also have like say label generation, right, where a
patient where for example, if a actually let me just show you the
screens first.

1:28:31\
Yeah.

1:28:34\
So I\'ll go to the loading doors which I have.

1:29:13\
Yeah.

1:29:14\
So this is the loading dose form with the medication dose tab here where
again like like I said, you can like for example, just create multiple
loading doses against the delivery for.

1:29:28\
So basically how we manage like say the label generation at like loading
dose level is so for each loading dose line that you add into the
prescription, right, they are added in as specific lines in this text
that you see here, right?

1:29:45\
So for example, you mentioned like say week 1 take two doses, Week 2
take 3 doses, et cetera, right?

1:29:51\
So that is basically like you know, mentioned at the loading dose level,
right, for the labels that we generate.

1:30:01\
So like this week one would just be like the first loading dose slide,
right?

1:30:07\
And then Week 2 and onwards mentions the at what point like the
maintenance dose is starting right.

1:30:19\
And for a regular regular like loading dose line, the, the format that
we use is basically like say it mentions the number of unit per dose,
the strength of your product, right, the form and you know what like
frequency it must be taken in, right?

1:30:38\
So like I showed you in my first screen, right?

1:30:40\
Like how the, yeah, sorry, I showed in my like first screen how like the
system mentions regular dose where it\'s just like a standard regimen.

1:30:53\
So for example, if you have an AMG Vita 40MG, right, and you\'re
prescribing 2 doses, right?

1:31:00\
So what it does is it basically like calculates it as set take 2 pins of
40MG AMG Vita product and basically like what the frequency is and how
they\'re supposed to take it, right?

1:31:23\
So that\'s like basically how you would show the label generation.

1:31:30\
I also have like another example of like a more for loading doses.

1:31:35\
How like what a more like an example basically which has more like
medication doses.

1:31:44\
So it\'s like day one, day 10, day 18, day 30 and onwards, like what
they\'re meant to do.

1:31:48\
So this is the part that is taken directly from like the regular dose
line SO1MG50 pen to be administered by subcutaneous injection, your
frequency and like as directed by your prescriber.

1:31:59\
And the warning label that you\'re seeing here that just comes from the
mandatory instructions.

1:32:04\
Perfect.

1:32:04\
Yeah.

1:32:05\
And can we make some manual, if there\'s some manual instructions to
add, So say for example with the if we did the the scenario where we
have a different item in the first delivery, we have the 160 milligramme
pens.

1:32:28\
Then when we have the regular dose, maybe we want to add to the end of
the instructions to be taken only after 160 milligramme pens have been
finished or something.

1:32:40\
We can add that manual text at the end as well.

1:32:44\
We have like the ability to like say add in like the off label
prescription.

1:32:49\
So for example, like what?

1:32:50\
The format that you see here, right?

1:32:52\
Like sorry.

1:32:55\
So basically by default we get like this format that I mentioned here,
right?

1:32:59\
Yeah.

1:32:59\
And it calculates the specific values and if you set like say off label
prescription to yes, you can like add on to stuff that\'s generated here
and it just shows up in the label.

1:33:09\
OK, fine.

1:33:09\
Yeah.

1:33:11\
OK.

1:33:13\
Any question?

1:33:14\
So, so off label prescription means you we can amend the label.

1:33:18\
It\'s not necessarily the same as unlicensed prescription.

1:33:21\
Yeah, to off label to mean that.

1:33:23\
Yeah.

1:33:25\
Yeah.

1:33:26\
OK.

1:33:28\
Any questions so far or we can move on Like is all of this like clear or
like how our total quantities are meant to be calculated, how we manage
like the prescriptions and what kind of medication types we have?

1:33:42\
Yeah, Yeah, I think so.

1:33:43\
Yeah.

1:33:45\
So we\'ve OK.

1:33:47\
So like the only like say missing part is like the where you have like a
separate medication for your first where that\'s only sent at the first
delivery, but yeah, first delivery specific.

1:33:59\
Yeah, OK.

1:34:01\
Right.

1:34:02\
So this is the transcription stage of our of our prescription, right.

1:34:09\
So when a prescription is initially created in the system, right, we
have what do you call them?

1:34:16\
Yeah.

1:34:16\
So when a prescription is initially created in the system, our business
process flow is like at awaiting transcription stage, right.

1:34:23\
And our prescription status is set to draught, right?

1:34:26\
And when a user selects the verify transcription button, the system like
cheques multiple criteria and then moves it on to the next stage towards
like delivery creation and the transcription stage.

1:34:38\
OK, so transcription rules are basically like divided into like say four
categories where each area cheques like a specific thing.

1:34:50\
So there\'s contract driven, there\'s product driven and there\'s
patient order driven, right, and prescription tribe driven, right.

1:34:57\
So basically what that means is for example, at the contract level,
right, we discussed like the ability to handle like contract Slas,
right?

1:35:05\
Where I think the example we gave in the contract call was the making
like say pharmacy screening mandatory, right and adding like a patient
height and weight mandatory, right.

1:35:20\
So basically at for the contract driven rules would just be like those
specific Slas that it cheques, right.

1:35:28\
We also have like product driven.

1:35:30\
So basically these would just be this would check like for each product
that you\'ve added into the prescription, right?

1:35:38\
Whether it like meets the specific criteria that we\'ve outlined, right,
that the product record must have these specific fields populated,
right?

1:35:46\
There\'s patient order driven, right?

1:35:49\
So these are like rules that we expect to be followed when a person is
creating like specific medication types.

1:35:56\
And then there\'s the prescription type driven where we have like rules,
for example, for each like prescription type, right?

1:36:05\
So if for example, the prescription, sorry, the system like notes that,
you know, you failed the specific roles in the contract driven part in
the product driven part in the prescription type driven part, right?

1:36:19\
Then it basically generates like queries that it basically generates
like a single query which has like all of the errors mentioned.

1:36:26\
OK.

1:36:27\
So I\'ll move on to the contract driven side.

1:36:32\
So basically at contract level, you can mention like like I said, you
can mention whether height and weight is mandatory, right?

1:36:39\
You can mention whether pharmacist screening is required, right?

1:36:42\
And basically the system would check whether the project present on your
prescription is from an active contract line.

1:36:50\
I know that we\'re supposed to like add in more rules from like the
contract meetings regarding like how the start date and end date is
structured, right?

1:36:58\
And the basically the system cheques whether at least one product on the
prescription is mentioned like is a primary product, right.

1:37:10\
So are there any rules that you feel here are missing or something
that\'s like driven by say a therapy and referral combination?

1:37:25\
No, I think this is OK.

1:37:28\
OK, So like OK, right.

1:37:31\
So the next part is the transcription rules that are product driven,
right?

1:37:35\
Basically in this point it mentions like whether the product has like
specific fields populated, right?

1:37:43\
And whether the product like exists in the allowable alternative is
great of the left.

1:37:49\
Like even if for example, like say it was, you know, like the product
was available in the allowable alternatives like, and one day, right?

1:37:57\
And the person basically created the patient order then, right?

1:38:01\
And the next day it wasn\'t available.

1:38:03\
And when the user tries to like, say, transcribe the prescription, the
system is flagged for an error, right?

1:38:10\
So this is like the parts that I\'ve, you know, categorised as product
ribbon.

1:38:18\
Is there anything like that you feel would be like, you know, any other
information at product level that you think should always be available
that we need to check our transcription level?

1:38:29\
So if I open like say the product form, right, are there like specific
things at the product level that you feel we should check right, when
we\'re just transcribing the prescription that you know that it\'s
active, it\'s like the VMP ID is available or this strength field is
available form etcetera?

1:38:58\
Or like mandatory instructions is available because there will be some
drugs which don\'t have mandatory instructions.

1:39:06\
So no, it\'s fine.

1:39:08\
I think it\'s fine.

1:39:09\
Like so these cover like all of the rules you would expect to check at
product side, right?

1:39:17\
Yeah, yeah, Yeah.

1:39:18\
OK.

1:39:21\
Right.

1:39:21\
Our next step is the patient order driven thing.

1:39:25\
So the patient order driven transcription rules.

1:39:27\
So basically what it cheques is that a total quantity is present on each
of your patient orders, right.

1:39:34\
Every patient order line must have the root present.

1:39:37\
Every patient order line must have a unit per dose, right.

1:39:41\
Each medication dose associated with your loading dose must have a
prescribed unit.

1:39:45\
So for example, right, we saw the maintenance, the loading dose
medication forms, right, where if a person, for example, did not specify
when there\'s in the medication form, it said that like, you know, for
that they haven\'t added the prescribed unit as in like what day
they\'re supposed to take it.

1:40:04\
The system flags it as an error, right?

1:40:07\
And the last rule that it cheques is basically at if a loading dose is
present right, then the user must specify using the medication dose form
what is the last loading dose.

1:40:23\
So like if for example, it does not mention like when the user sorry,
when the patient is going to stop, like, you know, taking that loading
dose and like from what time they\'re supposed to take the regular
doses, right, it will flag for an error.

1:40:54\
Is that fine or like do you see any other rules that you would need?

1:40:59\
I think this is OK, Yes, OK.

1:41:02\
So our last transcription rule is basically like patient prescription
driven, right?

1:41:08\
This is again something where they\'ll have to like move through screens
a bit.

1:41:11\
So basically in our system, right, what we\'d have is like the specific
yeah, prescription types, right?

1:41:20\
So you see the newer dose change etcetera, OK, new patient renewal
dosage.

1:41:26\
So for example, if you\'re specifying that a prescription is a renewal
prescription, right, And you try to select the verify transcription
button, right, What the system does is it cheques whether there\'s like
a previous prescription available on this referral.

1:41:40\
So in this case it would check it against prescription 329, right?

1:41:45\
And basically what it does is it compares the medication and what like
can be called medication instructions from prescription, from this
prescription, the one you specified as a renewal and the old
prescription which would be like specified as anything, right?

1:42:00\
So for example, in my previous prescription, I transcribed actually
I\'ll open the previous prescription for clear, OK, right.

1:42:14\
So in this prescription, in my renewal prescription, I transcribed a
metamorphin product, right, where I specified that the number of units
is 1.

1:42:21\
The route it\'s meant to take is inhalation the frequencies every 10
days.

1:42:26\
This is the prescribed dose, right?

1:42:28\
And yeah, these are like our main fields that we consider like As for
medication instructions, right?

1:42:35\
So what it does it it goes to the like the last valid prescription,
right and cheques whether the products match, whether the number of
units match right, whether the route matches, and whether the frequency
matches right.

1:42:50\
If all of these details match, only then can you transcribe this
specific prescription as a renewal, right?

1:43:00\
So basically just goes through the last valid prescription and cheques,
for example, how many prescription lines there are, what kind, what the
dosage instructions were in these prescriptions, right?

1:43:09\
And whether they match from new prescription to old prescription.

1:43:16\
Is that something you do today?

1:43:19\
And like, does it like cover a specific requirement that you have?

1:43:22\
Don\'t you do it in the system?

1:43:27\
No.

1:43:29\
Do we store it, store it in the system as structured data?

1:43:34\
No.

1:43:36\
Do we do it as part of the process?

1:43:39\
Yes.

1:43:40\
It\'s part of the business process because it will determine how the
person will use the prescription and calculate the delivery required by
date and all this kind of stuff.

1:43:53\
So say for example, if prescription is a renewal, then delivery required
by date will follow on from the previous prescription.

1:44:00\
If prescription is not a renewal, IE it\'s a dose change, then delivery,
prescription, delivery required by date will be ASAP.

1:44:09\
Oh, so like this is where like the next projected delivery date can like
come into play where if it\'s a dose change you would want like what
would the what formula would we use?

1:44:17\
Like start date plus delivery frequency or what if it\'s a dose change,
what should we do?

1:44:22\
It it it\'s like it\'s like ring the patient straight away and tell them
we have a new prescription and it\'s a dose change.

1:44:28\
And when would you like us to make delivery, Mrs.

1:44:31\
Smith?

1:44:31\
Yeah.

1:44:33\
OK.

1:44:34\
So basically we just use like the start date of the prescription as our
projected delivery date for a dose change.

1:44:39\
Yeah, Yeah, Yeah, exactly.

1:44:42\
Yeah, OK.

1:44:44\
And for those changes, we basically like also have the same
transcription rules where for example, if you are prescribing a dose
change, the system does check for example if you know like the doses
match or not, right?

1:44:56\
The same criteria that we saw here, right?

1:44:58\
It cheques it against the last valid prescription, whether the product
is the same, the dose is the same and whether the prescribed dose is the
same, right.

1:45:07\
And based on that, it\'s like provides like a specific query.

1:45:13\
OK, fine.

1:45:14\
Yeah, yeah, for the those changes as well.

1:45:16\
So a bit bit of a left field question.

1:45:19\
If we we\'ve, we do add it on and there\'s an existing prescription,
could there be a pop up to to have an indicator that we need to cancel
the future deliveries and to you know, call the page in ASAP of of the
current prescription.

1:45:32\
If you have transcribed a dose change successfully, that\'s when you
want like a notification.

1:45:37\
I think it\'d be good to have the notification.

1:45:39\
I don\'t know tariff what you think?

1:45:41\
Yeah.

1:45:41\
So if if there is an active prescription with future deliveries already
in the system and we receive a new prescription for a dose change, then
we must expire the old prescription and then the new one.

1:45:57\
The next projected delivery date is ASAP.

1:46:00\
Yeah.

1:46:02\
OK.

1:46:04\
So that\'s dose change and renewal.

1:46:07\
And for basically our like we also have like a validation for new
patient, right, where basically a prescription you can transcribe a
prescription as new patient if it\'s the only prescription on your, you
know, on your reference, right.

1:46:21\
Or for example, if the start date between these two prescriptions right
is more than like 180 days and that\'s like a configurable field more
than 180 days.

1:46:31\
OK.

1:46:32\
So yeah, if if more than if more than six months, then patient\'s
treated as new patient.

1:46:38\
Yeah, basically your prescription type is set to new patient.

1:46:40\
Yes.

1:46:41\
And it yeah.

1:46:43\
But say for example, like this week the patient, you know, last week the
patient was on Amjavita and then the hospital said expire this one,
close it, we\'re gonna change the drug.

1:46:54\
And then next week we receive a new registration and prescription for a
different contract.

1:47:02\
Patients switching to like etanercept or whatever, Yeah, then then
they\'re treated as new patient for the new one.

1:47:11\
Yeah, new.

1:47:12\
Yeah, because it\'s a new referral, right?

1:47:14\
Like when you get like a new contract, Yeah, we consider in our system
it would be considered new referral.

1:47:19\
And since that prescription is like the newest prescription on that
referral or the only prescription, sorry in that reference, right, then
it basically like would consider it a new, like it would allow you to
transcribe it as a new patient prescription.

1:47:33\
Yeah, OK, fine.

1:47:35\
Yeah, new referral, new patient.

1:47:37\
Yeah, OK.

1:47:37\
And but they would keep the same patient record.

1:47:39\
All of the history would be yeah, yeah, it would just like all of your
reference for example, put are always like within like a patient
context, right.

1:47:48\
So it basically like whatever you have like a master patient record,
right.

1:47:53\
And within sorry.

1:48:02\
So in in that scenario, would we get a separate message from the
prescriber to say cease the previous medication?

1:48:09\
So if you just got a new referral for a new product, that wouldn\'t
necessarily trigger you to switch off the old product.

1:48:17\
Sometimes yes, sometimes no.

1:48:19\
It depends.

1:48:22\
That could be a fun one then.

1:48:23\
So you\'ve got a Yeah, Yeah, it depends.

1:48:27\
Yeah.

1:48:27\
So like I said, the process should be yeah, The process should be that
they inform us and then separately they send the new referral.

1:48:35\
But sometimes it doesn\'t work out that way.

1:48:37\
Yeah.

1:48:37\
So your in your specific scenario, what what happened is I guess like
since they were on a previous some other contract beforehand, right And
they switch over to a new contract, right?

1:48:46\
And they mentioned that, you know, the previous one is invalid.

1:48:49\
You can just like finish this referral and then just create a new
referral and start over with that one.

1:48:53\
But like this, I guess the the point is someone\'s got to make it a a
judgement.

1:48:57\
There is, is this a treatment switching or is it almost, almost like a
coincidence that this patient is also starting up another another
treatment?

1:49:08\
Do both both of them want to run in parallel or do we need to stop one
of them?

1:49:12\
Yeah, yeah, that\'s a yeah, that\'s a business process.

1:49:14\
That\'s a business process in in this specific case, right?

1:49:17\
Like the you would like get a new registration form also, right.

1:49:21\
Like if it\'s you\'re switching a referral if in in both cases, yeah,
yeah, in both cases.

1:49:27\
So it might be the patient is starting because we have some patients
which are dual therapy, right?

1:49:33\
They have one high tech therapy and they have one low tech therapy
because they might have arthritis, but also they need to have TPN or
something.

1:49:44\
So there will be patients which can have two active therapies contracts,
but then equally there will be somewhere the contracts are exclusive,
they can\'t be combined.

1:50:00\
So you would only have one contract probably for a like arthritis drug
or something.

1:50:11\
So they would only, you know, they couldn\'t have both Androvita and
also Cosentyx together like the, the combination is not compatible.

1:50:21\
But that, that, that\'s, that would be for our business process to to
decide.

1:50:28\
We I don\'t think we would expect the system to know which therapies or
which contracts are compatible with each other, right?

1:50:40\
So from the transcription rules point of view, that\'s basically it.

1:50:45\
So the last thing you\'ve just like I mentioned is like the prescription
type portion, right?

1:50:49\
At which point, for example, when you have like completed, like once all
the rules have been like, you know, cleared, you can set up the, you can
select the verify transcription button, right?

1:51:00\
And it basically will move to the next stage and switch this to receive.

1:51:05\
So from, I guess from a prescription types point of view, like our
basically like what I\'ve mentioned, does match with what you would do
in your business process, right?

1:51:16\
Where renewal has like specific criteria to be transcribed as a renewal,
meaning it should match with the previous prescription if it\'s
available.

1:51:23\
And for dose change it shouldn\'t match like the medication lines.

1:51:27\
And for new patient you can have it if for example there\'s more than
180 days between the previous prescription and new one or if it\'s the
only prescription on the reference.

1:51:37\
OK.

1:51:38\
The, the only thing about the 180 days, it\'s 180 days measured from the
expiry of the previous prescription or from the start date of the
previous prescription start date, because we will have some
prescriptions which are valid for like one year, 2 years.

1:51:53\
So those ones will be more than 180 days.

1:51:59\
Can that like differ based on therapy code or yes, is it like a system
wide thing?

1:52:04\
OK, so that means like for now.

1:52:05\
Yeah, sorry for, for for two, for two years is contracts for specific,
but for like a between six months or 12 months, it will be global.

1:52:17\
It\'s across the the service and you mentioned like we should choose the
end date instead of the start date.

1:52:24\
Yeah.

1:52:24\
So the way that we would usually do it is if the patient has been, you
know, if it\'s been more than, I think it might maybe six months.

1:52:33\
I, I\'m not 100% certain if it\'s more than a defined period of time
since the expiry of the last prescription, then we would want to treat
it as a new patient.

1:52:43\
I, I feel like it\'s 12 months rather than six months, but I could be
wrong.

1:52:48\
I think it\'s so right now, right now, basically this is like a
configurable value.

1:52:53\
So you can set it up as one year, 2 year, three-year, etcetera, right?

1:52:56\
And you can also like right now.

1:52:59\
So it\'s at system wide level.

1:53:01\
If, if you\'re saying that it can change based on therapy, then this is
something like we would need to bring back to like a contract so that
you can manage it as like therapy referral combinations.

1:53:12\
I, I think for the purposes of this, then we can use it for global, we
can use it across the system rather than saying that it\'s specific to
therapy.

1:53:21\
Yeah.

1:53:22\
In your prescription, do you always get an end date or is do you only
get like a duration?

1:53:28\
Because like right now end date is not a mandatory field.

1:53:31\
And if we are saying that, you know, we have to base it based on the end
date, right, then that is like, you know, I guess that is a field that
we would need to make mandatory.

1:53:41\
There are, there are, there are some hospitals and some services, some
contracts where they will provide an end date and expiry date on the
prescription.

1:53:53\
There is one hospital in particular which always does it.

1:53:57\
But no, it\'s not, it\'s not, it\'s not common.

1:54:01\
It will be the majority.

1:54:03\
The prescription will just specify a duration.

1:54:06\
So it will say deliver every four weeks for six months or 12 months or
whatever.

1:54:12\
But then there will be some which is supplied every 12 weeks until the
12th of January 2026, for example, like an expiry date.

1:54:28\
I guess like in that case we put as an end date.

1:54:32\
Can we like, for example, take it as the day this prescription was set
to expire if it\'s not already available, like if we want to?

1:54:40\
Because if we\'re using like an end date as our criteria to figure out,
right?

1:54:44\
Like what\'s the, you know, at what point do we like, start our count
right?

1:54:49\
So yeah, for example, the moment like a prescription is set to expired
in this field is like, you know, not filled in, right?

1:54:55\
Do we just take the time stamp of that to like help us with the logic?

1:55:00\
Expiry date?

1:55:00\
Yeah.

1:55:01\
Well, the date, the date when the prescription changed to expired.

1:55:04\
Yeah.

1:55:04\
Mm Hmm.

1:55:05\
Yes, yes, yeah.

1:55:08\
Mm hmm.

1:55:10\
OK.

1:55:10\
So I\'ll take that down as a requirement.

1:55:11\
Also, I think we\'re done with like the time frame on the session.

1:55:17\
If there\'s any questions, we can pick them up in the session that\'s in
1 1/2 hours.

1:55:24\
Yeah, cool.

1:55:25\
That\'s, that\'s fine.

1:55:26\
That\'s that felt really good actually.

1:55:28\
It felt like there\'s a lot of things which are going to be better than
we\'ve got today.

1:55:31\
And it didn\'t sound like there\'s very much in there that isn\'t isn\'t
covered in that that area.

1:55:36\
So yeah, I\'m good.

1:55:41\
Right.

1:55:41\
We will catch up then at 1:00 when we\'re covering pharmacist
validation.

1:55:45\
Yeah.

1:55:47\
Yep.

1:55:48\
See you later.

1:55:48\
Thank you.

1:55:49\
Yeah, sure.

1:55:49\
A little bit.

1:55:50\
Thank you.

1:55:50\
Bye.

1:55:51\
Cheers.

1:55:51\
Thank you everyone.
