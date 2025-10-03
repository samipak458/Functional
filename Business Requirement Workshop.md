# Alberta Health - Business Requirement Workshop -2 Meeting Transcript

## Meeting Information
- **Date:** August 7, 2025  
- **Time:** 4:27 PM
- **Duration:** 1h 28m 30s
- **Transcription started by:** Amirah Mahomed

## Transcript

0:07\
Ultimately, like the the.
This is kind of like the constant like the program of care stuff, so we
can ignore this stuff because that theoretically would all be entered
right digitally.
Clinical information.
Right history investigations.
Describe any relevant information so these all align up. We can have BC
clinical information continued. No problem. You know, summary of
physical exam findings. I think this actually aligns relatively well
with kind of the structure that we're looking at.
Right.
Eight, are there any factors? Yes. No tick box outcome measures. In an
ideal world, again, the outcome measures are aligned with the program,
right? And if the?
Client or the claimant basically fills out like the neck disability or
the aswestry or whatever. The score is automatically calculated and
entered into the report, right?

1:19\
They submitted multiple then wouldn't just pick the most recent.

1:20\
We can.
It picks the one, yes, theoretically in the like the follow up
assessments and stuff, it should show like the table type of thing but
but as an example it would just you know like we have it. I'm gonna
show you the the the view that we have.

1:29\
I.

1:43\
Potentially just pulling the table over time, but you know they've set
these PDFs up to be relatively simple and not totally valuable, but I
think there's things that we can do there way better. So now that I'm
looking at this.
You know, and you kind of look at kind of the way that it's structured
and stuff.
You know, I think.
There's parts of it that are in a table. There's parts of it that are
not in a table, whether or not we just keep everything in a table and
have those types of questions underneath these different sections, I
think that could be doable.
It says there is 11 to your door, no friends and PP expressions stop
online and get $15.00 in TC personal go down.

2:31\
Yes, I I think we have something ready and we can potentially invest our
efforts to fine tune it and look at it as desired.

2:40\
Yeah.
Yeah, I think I think that's the way to go, guys. I think that's the
way to go. Now that I'm looking at kind of like the functionality and
stuff that we have 'cause, we have the diagnosis stuff. You know, we
can enter in that they, you know have concussion, it's already there.

2:52\
Yeah.
None.

2:58\
You know, all these things are searchable, you know, lower.
They have lower back, no.
Right.
So low back, I guess we have so, so all that stuff is kind of in there
as an example or we can kind of you know we can kind of do those types
of things.
None.
You know, cute.
Their primary, you know, provisional, whatever. Like like, you know,
like all of this stuff, I think is actually pretty good, right?
ICD codes plan of care assessment care plan. This is the one that we
would have to add in kind of some additional questions, but I think
that's fine.
What are your thoughts, Amira?
I think we can get by with. This is a pretty good demo.

4:01\
Yeah, I think that makes the most sense. Yeah. And ultimately, they're
still in their own decision making process for some of these things too,
right? And so I don't think they are going to be looking for something
in particular. I think they just want to see that that functionality.

4:10\
Yeah.

4:17\
Is there and not to say that we're overwhelming them, but I think
we're showing them we have this already. So I think this works well.
And then they've also seen parts of this already too, you know. And so
there's going to be looking for some sense of familiarity. And if we go
do a complete 180 on this and be like, wait, what the heck did you just
show us last time?

4:29\
Yeah.
Yeah.

4:37\
So I think keeping this as the core and then obviously tailoring it to
the Alberta context, I think will work well for them.

4:45\
Yeah. And I think if it's, if I think if it's staged properly, where
we basically have multiple follow-ups. You know as an example like their
initial assessment and everything. Then I think I think it can look good
like I think it can work pretty well.

4:57\
Agreed.
Yeah, agreed. Agreed.

5:00\
'Cause this is your appointment appointment type. You need kind of the
assessment diagnosis. I think that I think we can make that work guys.

5:10\
Yes, other than that in the bigger picture, how we can proceed? First, I
think I said unless we need all the users to reach in Dev OPS right,
then we can decide how we are implementing it. Start putting efforts
around it so we can come with the overall project plan, right. And I
think too quickly.
We push, proceed with that with the deployments my recommend like I as I
discussed in the last meeting, there was step that deploy the latest
builds. What I would recommend what we have either for CRN on we can
just create a replica environment and and deploy stuff what we have and
on top of the do or customizations that will be the.

5:49\
Yeah.

5:50\
Cookies jump start way and this, but I will not recommend deploying
latest magic here or the big because to make it comfortable it's a
separate effort that I don't recommend at this. At this point for the
demo, but we can definitely do that later on.

5:55\
And.

6:07\
Yeah, I know. I I'm in. I'm in full agreement with that now, but I
think that you know, while it's nice, like I said, the only reason to
do that would be if you said, hey, you know this, we have this new like
provider registration function that works perfect and everybody loves it
and it you know it achieves like a big part of your you know what you
need to showcase.
And I'd say maybe it's worth it, but if you don't, then guess what,
you know, you know it's it's probably not worth it at this point in
time until, you know contract is awarded or until there's an agreement
that, yeah, we have an early start letter or something like that, right.

6:38\
Right.
Right.

6:42\
So I I I would agree. I think we're better off spending the time
configuring what we currently have, you know aligned with the care first
model in the best possible way to showcase it than trying to.
You know, kind of get up, you know, kind of, you know, redo a bunch of
the technical stuff behind the scenes. You know, I I don't think that
that's going to be in our best interest to, you know, to try to do all
that.

7:12\
And and I have some detail level technicals. Can I do this in this call
like if we are going for that route for example we discuss we'll be
using the same tenant right? But the Azure subscription will be new that
we have to request, right?

7:27\
Correct.

7:28\
OK, to now to initiate that process customer I I can request positive,
but I think the way currently it works like the access is controlled by
you or or your IT team, right that that who have the access also how we
can initiate that conversation who I need to.

7:43\
Yeah.
It's with garish and myself, you know, we'll we can create a a DevOps
item and stuff as well. What we need to though know is we need to
understand from Kevin and we could flag this for for the meeting
tomorrow, I guess Amira. But but we do need to know.

7:49\
Keep in loop for that.

8:10\
We've done two things with inquisitive in our different environment. So
we've done them where we have it set up and Arthur Health has full
access and control and visualization of of the subscription. As far as
costs and everything else. And then there's a second model where
basically.
It's set up under inquisitive and then inquisitive. Basically bills us
for it, right? But we don't have all the line of sight to everything
that ideally I want, right? So like our own instance is set up where
Arthur has control over.
Everything I I see, everything we can do everything and we give you guys
access to it. The other the other one like RAC. As an example, I I I
can't see everything I have to request from inquisitive if I want to
see certain you know certain numbers and then inquisitive invoices US
every month.
You know, for the cost of the Azure environment and stuff like that,
right?

9:10\
Right.

9:12\
But there has been some communication that if we want to set this up, we
want it to have some some subscription ID or something so that you know,
Arthur, inquisitive basically can get.
You know, get recognition for it, assuming that it does go to be a full
like implementation in in Alberta, you know because it'll be you know
quite a decent amount of Azure consumption resources.
So there's supposed to be like some ID that you enter in when you
create a subscription, but nobody knows how to do it and nobody knows
where it exists or exactly what it is. But that's theoretically what
you know was supposed to happen. Like I can create a new subscription in
two seconds. I just. I don't know if it.

10:12\
Yeah, I think it.

10:13\
Example like we have our own subscription rack subscription Arthur Care
subscription, the Arthur Care and the RAC subscription. Theoretically
you guys created inquisitive, created those the own subscription I
created. I have full access to this and can see everything the RAC and
Arthur Care you guys Bill us under.

10:14\
Yeah.
Play trailer of the song.

10:33\
Different billing statements basically every month, right?
So my preference is to create a care first subscription, basically that
we have access to, but I don't know if that's, you know if that you
know that if that meets the specific needs or not, right?

10:54\
Yeah, I think we can initiate an e-mail conversation with Kevin and I
think it will do best if we can discuss it within a call. I think it
will be great.

11:02\
OK.
OK.

11:06\
Yeah, we can find that this afternoon. Christian, we have this to your
code meeting. So I put down a note for us to raise that with Kevin and
then we can take that there as a maybe book a secondary call.

11:15\
Yeah.
Yeah, like I said, I can create a new subscription in two seconds and
it's not, you know.
It's it's not, it's not an issue, right? Like it's a it's a ad. And
then give people, you know, give people access, right? That's that's
basically all that it is. Right. So I'm happy to happy to do that. But
but at the same time.
My understanding is the way that these subscriptions are set up.
Inquisitive and and Arthur, don't get any anything through Microsoft
Canada for any consumption through these for some reason, right?

11:58\
Right. I I think yeah, that that's one point. Second point is related
to the creation of a new database environment or we can leverage any
existing environment that we have that we need to consider I guess in
the storage part as well that how we can manage storage because.

12:15\
Yeah.

12:16\
Because Mukaram told me that currently on the tenant we are running low
on the space for logs and the file storage. So if we need a new
environment, we need to acquire storage or we can consider if any
environment we can repurpose.
Or I know there are some environment that were planned to be
decommunitioned as they were not in use. Maybe we can take your approval
to delete those environments to so that to free up space.
Or we can just repurpose any existing environment.

12:54\
Yeah, I don't think that we should repurpose an existing environment. I
think ultimately it's, you know, there was one Roxy production that we
were trying to deprecate.
I think all the other ones mukram have been removed.

13:15\
Yes, yes, we have done all.

13:15\
Yes, mukaram, can you please confirm? I think you are maintaining some
documentation for that, right?

13:16\
Aside.

13:21\
Yes, yes, we have done all the all lack environments.

13:30\
Yeah, I think the only one that's still kicking around is Roxy
production that we haven't fully taken offline yet.
All the other ones I believe are are used or in use. There is the CI
hub, one that.
I don't know if we need to leave it or not.
I don't know how much space that one's taking up.
Do we know how much space the CI Hub one is taking out muckram?

14:05\
K I'm.

14:14\
No, I don't have the access for CI hub environment. I am not able to
see guest base consuming by CIA.

14:15\
Ah.
OK, I'm akaran. Do you have any suggestion in mind that can any in my
environment that's used by us can be Reaper for that we are not using.

14:37\
Yeah. Currently, as you know, Christian in Owen, we are using only UAT
environment like there is one more environment that is certain
environment.
The purpose of it, you know, was to verify any items by accuser team.
Right now we are verifying all the items in the same environment on U8.
So sit.
I think we can use.
For this purpose or.
The ACN environment, yeah.

15:16\
Yeah, but I don't. I don't really want to use a new environment
because I think that the goal is to set up a new environment, basically
new new subscription, new Azure resources like so that basically
everything that we were going to use or do like.
You know, is kind of underneath that new, that new structure, right? So
the only thing that like I said, if if something isn't being used, like
if rack sit is not being used, then theoretically this should be
removed. You know what I mean like.

15:35\
Yeah.
Yeah.

15:53\
If it's not being used.

15:54\
Rexec Rexec is being in used oven tech is not in use.

15:58\
OK.
We don't have an own sit. You're talking about QA.

16:06\
Yeah, it's owing QA, correct? Yeah.

16:08\
Yeah. So like to me then, if it's not being used, then theoretically it
should just be removed. You know what I mean? Like, we should just clean
it up.
Ultimately.

16:19\
Yeah, right now this environment is not consuming too much space.
You know, I agree with you. We need to go with the new environment for
this purpose, for demo and the one more thing I would like to highlight
here after creating new environment for demo.
For care 1st we will be using restoring over in UAT environment.

16:54\
Own you at environment.

17:00\
That can be the base for the new environment, right?

17:01\
Yeah.

17:03\
Yeah, as a benchmark.

17:03\
Yeah, I mean right, I mean that's that's on top of the Arthur care
base. Then though, too, right or.

17:13\
Yeah.

17:16\
Because obviously like the own you at stuff doesn't have.
Some of the connections I guess for provider portal or stuff like that,
but I guess those are on the Azure resource side of things anyways. But
yeah, yes, I think I think.

17:30\
Mm-hmm.

17:33\
Setting up the O&U is then fine. It's going to have to be though in a
unmanaged version because are we going to? We're essentially going to
be making updates to it and doing everything kind of within it, right?

17:45\
Yes.
Yeah, right.

17:50\
Right. Like we're not going to have a separate like I don't at this
stage, I don't believe like we should just have the one environment and
basically just make all the updates and stuff everything within it.
And then we get contract or whatever else. Then we'll set up the, you
know, data this, that the other right, yeah.

18:05\
Yes, exactly.
Yes, because you know Kesha it, it will be better if you have like
separate dev environment separate demo because there were two
independent environments like on dev environments we keep on on on, on
adding new stuff, compiling and and the desk can be adding.
Some random test data that doesn't look meaningful, so it's best to
have a separate demo environment, but we can definitely configure it
that way later on, not for the initial demo.

18:38\
Yeah.
I mean, the biggest thing we need to do is we need to deprecate this
bloody thing. Roxy production. We need to kind of just get all the
records out and create the database for it and get we need to get rid of
all these files.
Back them up and get rid of it. Same thing with all the logs for Roxy,
right? So.

19:06\
Yes, last time I I connected with Ellie, Ellie was saying like he will
connect with you. I don't know if he connected or not then.

19:07\
That's what we kind of need to do.
Yeah.
We just need a plan to get like 'cause we we, you know, obviously like
Microsoft when it deletes it, it deletes it. There's no way to like
create a backup of it. Like ideally I wanna create a backup of it and
just store it in a storage, you know Azure storage.
And and leave it and if we ever need to restore it, then restore it. But
Microsoft's smart enough to not allow anybody to do that because they
want you to basically pay more money to keep it around, right?

19:45\
Yes. Yeah, right. Yes.

19:47\
Yeah.

19:51\
So then Muckamir was saying the only way to do that is to basically
export this using XRM toolkit or whatever into different entities and
everything else, and then you know with the files the same thing
there's a file.

19:59\
Yes.

20:07\
Haven't we already moved all of these things to that CNP like as part
of the data migration actor?

20:14\
Yes.
So in theory it can be it could could theoretically be deleted.
Everything exists in theory, but everybody still is kind of, you know,
worried about fully deleting it.

20:29\
None.

20:30\
Because, you know, we need the storage for the new environment. So if we
are not taking the decision to delete anything and we are not getting a
storage means we have to go with the route of acquiring new storage.

20:41\
Yeah.
Yeah. No, I understand. I I can't remember. What? What is our capacity?
What is our capacity right now? We're just down on logs. I mean, we
have lots of database and we have like lots of files.
Right. Like you can see like our database is like 314. So we have plenty
there. We have plenty files. It's really just the log storage, right.

21:14\
Hmm.

21:34\
Each time it says because you have other you know.
You have other you don't need to worry about this but but I agree I
don't, you know.
Like, here's like an example like the guy I don't, I don't. I have no
idea why our log usage is so high for owned CIMP, but it's it's like
crazy high.

22:07\
Yeah. The on TNT production is taking too much faith for long.

22:07\
But.

22:14\
Even I say if we cannot decide within this call, we can just notice an
action item because it's a prereq before we create another new
environment and for the.

22:25\
You have. You have enough. You have enough. You have enough space to
create a new environment.

22:31\
Yes, we had. The only issue is with the logs that you've seen, there's
an overage of 13 GB.

22:35\
Yeah, but we're not turning. We're not turning logs. We're not
turning logs on for for the new environments anyways, right for right
now.

22:42\
Hmm.

22:44\
Alright.

22:45\
Right. Like we don't need the logs for the, you know, for the demo for
right now, right. So I don't think that it's, I don't think it's a
rate limiting but.

22:50\
Hmm.

22:55\
At least it looks to me like we have enough. We have enough capacity,
right? Like we have 20% we have capacity available here. We have
capacity available for files, right?

23:04\
Mm-hmm.

23:07\
I agree that we're over on the logs, but I can look into that, but I
don't. I don't think that it's. I don't think that it's a a limit,
right?
And I don't know what these capacity extensions are, Greg, Tennessee.
25% capacity for 45 days. Cool.
I guess I can enable this regardless, I don't know what it does but.
Alright, as I can look into that.
None.
I think we're fine to proceed. We just need to, you know, like I said,
get the tenant set up, get the subscription set up. You know, you guys
can go ahead once that's set up, you have access through through the
acquisitive partnership side of things to to go ahead and.

23:58\
Right.

24:12\
And do that.
And then I think as we move forward, we'll end up, you know,
deprecating RAC.
CE, which frees up a a crap ton of space, right? So.
Aye.

24:32\
Yeah, I think from my side, these are the only two infrastructure
related points like we discussed for Azure, setting a meeting with Kevin
and then from a storage point, I think we have considered that things
are in good shape, right. And apart from that.

24:38\
OK.

24:50\
Can can you further discuss like Anas, do you have any question
regarding the requirement that we discussed in the first session like
our goal is that every every requirement should be in dev OPS so that we
can, you know, esteem do do some estimation against that and.
Come up with it with a high level project plan like by when we can we do
implementing which requirement so it will be great like if you can have
all the requirements within the DevOps.

25:22\
Trying to, I mean I guess that transitions us into the next one.

25:22\
I am like writing down some of the requirements that we yeah, on my end.
I'm also like adding in like the requirements that we were discussing
on want to say Monday wait. Yeah, Monday. So yeah, I am like adding them
in. I don't really have any questions as of yet like.

25:27\
Go ahead and ask. Go ahead and ask.

25:30\
Yeah.

25:41\
I'm going through them. I might have them, so I will probably just tag
you in the relevant user story and ask questions there.

25:51\
OK, So what? So let's just go through that.
So this is the DevOps. I think everybody's confirmed that they have
access to it.

25:58\
Yeah, right now I'm basically adding features against sorry user
stories against that feature solution gap like gap analysis, yeah.

26:02\
Yeah.
Yeah. So what I did, what I did and ask, OK, is I, I've, I've just
slightly restructured it so that I put, I put these used to be features,
right. So the the the previous project plan.

26:13\
Hmm.
Mm-hmm.
Mm-hmm.

26:26\
Kind of had, like, those five kind of features. What I did is I turned
those into epics instead.

26:30\
Yeah.
OK, OK.

26:34\
Right. So I turn those into epics because I think that makes more sense.
And then basically I put these kind of features in place. Basic is what
I've started doing right and there'll be some features that are for
now and there'll be some features that are for future. We don't need
to worry about like we're not.

26:39\
Mm-hmm.
OK.
Mm-hmm.
Yeah.

26:54\
Going to worry about Guidewire API integration right now, right? Like as
an example right? But carepath portal caroling portal? You know,
they'll be ones that kind of go under that. So I was going to take the
previous epics that that like as an example epic one.

26:54\
Got it.
Yeah, yeah, yeah.
Mm-hmm.
No, yeah, that's fine. I think I.

27:10\
I had. I had put these ones kind of underneath there. I was going to
move these ones kind of to the proper new feature as an example. So
I'll and then if you move yours to kind of whatever or create a new
feature like if you think that it belongs under a feature, put it as a
new feature.

27:20\
I'll move mine. Then too, yeah.
No, no, it's. I think the ones that you've mentioned are what I was
actually going to create myself. But yeah, like basically core app
portal provider and portal patient. That's correct. Yeah. I think that
works.

27:38\
Yeah.
So so I put these kind of in place and I think that, you know, we've
kind of used them. I put one up here for branding. I was.

27:47\
Mm-hmm.

27:48\
Considering calling these features that are more for demo like you know
demo, but instead you know I think it's. I think we're fine to
actually just use like a demo tag and are we fine.

27:55\
Mm-hmm.
Yeah. Demo tag, yeah.

28:05\
Amira just just using like the word demo. Or should we, like do
something else like.

28:10\
Yeah, I think demo's sufficient. I think demo's sufficient and then
the ones that are for production we can do a production tag and then if
something is both demo and production related, we can have both of those
tags present knowing that some do.

28:13\
Yeah.
Yeah.

28:27\
Spill over into both sides of the process.

28:30\
So then demo from that perspective, we can then create a query for kind
of all the demo items and line everything up for the demo items.

28:41\
Yep, OK.

28:46\
So so I think our goal should be to have, like most of this stuff in
place by like essentially end of end of week tomorrow, right? Like as
far as like the tasks and like I think we probably need to if we're
going to hit our timelines, right.

28:56\
Hmm.
Yeah.

29:02\
And.
And then literally.
You know, we're going to, we're going to need to set the timelines
for, you know, for when the environment and stuff is going to be ready.
Right.

29:27\
There is one part of the provider portal that I had a question on. Would
like the providers be like editing the patient information or like
creating like readiness records, sort of what they didn't own or would
like it just be related to like treatment like services appointments and
recommendation basically and this.
Charge.

29:48\
Yeah. So they're so sorry. What was that? Were they gonna? What was the
first part?

29:51\
Play song.
Right now, would they like, would the providers right? Would they mostly
be focusing on like say the like treatment side of things like creating
recommendations, the services like adding diagnosis or discharge et
cetera? Or would they also be like editing in the patient information
like would they be like contacting to the patient to like, say edit like
their mobile?
Number stuff like, stuff like that, basically.

30:16\
No, theoretically they shouldn't. That should all be done at the
insurer level.
Yeah. So they won't be editing any of that patient information.

30:22\
Would they be using the assessment readiness assessment readiness? Would
that be used or OK?

30:30\
At this point in time, No, no.

30:31\
OK, then yeah, OK.

30:33\
I don't need to worry about that. Basically the providers need to be
able to select A select a template completed assessment or upload,
upload a structured assessment and then you know make recommendations,
select a diagnosis, make recommendations.

30:48\
Mm-hmm. Mm-hmm.

30:49\
For, for, for treatment and then you know once something is complete,
you know like once a report is complete or an assessment is complete, it
gets submitted for for billing.

31:03\
Do they have the concept of like blocks or follow-ups or would they just
be like raising a separate recommendation from within like their current
appointment?

31:07\
Yes.
Yes.
So I think the way that we're gonna we're gonna need to structure it.

31:12\
OK.

31:18\
Is.
Still a little bit in flight, but the way the wsib structures their
program of care is single site versus multi site.

31:29\
Hmm.

31:36\
And then there's an initial assessment report. The assessment report
gets paid at a certain fee. Then there is a block of treatment for six
weeks.

31:41\
Mm-hmm.

31:52\
At 4 weeks, there is a midterm report that midterm report determines
whether there is continuation and another block of treatment or the
claimant has basically improved enough that they'll be discharged at
the end of the first block of treatment.

31:57\
Hmm.
Yeah.
Yeah. OK.

32:12\
Right. And then if they do the second block of treatment, then there is
a final discharge report at the end.

32:21\
OK.

32:25\
And then in theory, they could. There could be a supplementary report as
well. So there's essentially and I can share all these files, there's
essentially 4 different, four different reports.

32:26\
Right. So we need to bring in that.
Mm-hmm.

32:41\
Within the context this is I'm talking to wsab because this is kind of
like the way that we're going to have to structure it. So there's the
initial assessment.

32:48\
Uh-huh.

32:52\
Right. So there's the initial assessment for the MSK program of care.
This could be MTBI as well or there's different programs of care,
right? So this is for the MSK one, which will be the bulk of them, but
this is the initial assessment report, OK.

33:10\
Hmm.

33:11\
Then.
There is a midpoint report.
OK, so midpoint report.
And it kind of goes through same questions. So we'll need to kind of
set up these questions and stuff in there and then there is the final
report.
And there's basically like number of sessions provided in block two
number of sessions right? So this one here.
Number of Sessions provided in block one right you know so so that's
kind of what they're.

34:02\
Hmm.

34:07\
So this is this, this report, the midterm report is completed at the end
of block one. You know how many sessions did they do as part of that? In
essence, that whole thing should be paid as a single fee, right?
On our end, we would ideally like them to be able to select the the
number of treatments right? It's like boom, boom, boom, boom, boom.
There's this many treatments, obviously, in. In own it's it's much
more complicated, right? It's like, you know, you got like record
service da da da da da and status and each of them is.

34:23\
Yeah.
Yeah, like.
Mm-hmm.
Uh-huh.

34:41\
Kind of separate, you know, here I think it's a little bit more more
simple. That being said, I think we need to be able to highlight that
they, you know underneath this block there was 8 treatments and here
were the treatment dates as an example, right.

34:58\
Mm-hmm.
OK.

35:10\
You know, so that's that's kind of the way that it's said, but then
there is one other report that I think they ask at times supplementary
report.
So I guess complete a program of care supplementary. So there's a
supplementary block that I think that they can authorize. I I don't
know the specifics on this when they're able to do that.

35:32\
In terms of like getting a recommendation, it follows like the same
processes in own right, like for functional treatments you get you
basically like ask for approval for the whole block but for neurology
and psychology you asked it for session.

35:45\
For the second block, for the second block, first Block auto approve,
second block requires approval for this for this yeah.

35:48\
OK.
Got it.
Got it. Yeah.

35:58\
None.
But the same fields as basically are here. You know for the most part.

36:04\
Mm-hmm.

36:08\
And then there are.
You know, then the question is, well, how do we structure the programs
of care? I think we go ahead and we do MSK, which is fine.
I did some.
Work, potentially looking at what?
What the predicted care pathways might be, Amira, based off of Peter
Cote's prior work.
Based off of his 2015 publication, he kind of structured things into
specific injury types. You know, these are kind of like the seven that
he basically had in various different ways. Obviously like, you know,
MSK kind of lines up with lower upper.

36:51\
Yeah.

36:57\
Right. And some level this will lower back as an example, whether
there's going to be separate ones or you, you know, kind of one MSK
single multiple I think would remain to be seen.

37:07\
Mm-hmm.

37:13\
MTBI concussion, you know, obviously we kind of know that there were a
couple in there that he had like TMD, right temple, mandibular
disorders, I guess is quite frequently headaches.

37:14\
Yeah.
Sure.

37:29\
You know? And then neck pain. So these are kind of actually like were
separated in his prior work whether they would be you know combined into
something but I think.

37:37\
Mm-hmm.
Yeah, I think that it makes sense. I ultimately, I think from the way
that folks have described Dr. Koteast, I don't think he's going to be
changing the content dramatically, but then also the segmentation I
think is easy for people to understand like particularly the government
and the folks from we're helping.

37:53\
Yeah.

38:00\
Bring them out. Like anything more, detailed or granular might overwhelm
them. So I think this is reasonable and it's rooted in what he's done.

38:10\
So I think we'll end up configuring things to kind of be like this, you
know, and still aligned with the concept of initial assessment, one
block six weeks midterm report, second block, six weeks final report,
right.
So that would be the structure and ***.

38:36\
Yep.

38:53\
Then kind of on our end, we'll kind of create some PDFs where we change
out wsib for care 1st and kind of potentially show both ways whereby you
know if the provider fills this out, you know great.
You know, and it can be, you know, uploaded. They do it digitally.
Great. You know, here's here's what happens if they do it digitally,
right?
And I think the current provider portal actually blends itself nicely to
do that.
Does that answer that question as far as the workflow and ask that
you're?

39:39\
Yeah.

39:41\
That help. OK.
None.
On the provider registration side of things, OK, like theoretically
there's a a component where the the providers need to register. Amir,
do you think that based off of our discussion that we need to kind of?
Take that into account as far as the demonstration.

40:06\
Are you thinking of like demoing how a provider might sign up to be like
in APPN or be a part of that process?

40:13\
Well to yeah. To sign like to sign up, basically to provide care within
care first, yeah.

40:16\
Yeah.
I don't think it's necessarily a priority because I think from my
understanding, there are some insurers who might already have their own
list that then are populated into the system. And then there's also
some of the work with.
Care connect that already exists, I think in Alberta's.
Operator health, with their epic system. So I don't think it's
necessarily a priority given that multiple interests have their own
process.

40:54\
I I think that we're going to have to do something like I I think
because the reason the reason why I'm saying that.

40:57\
I agree.

40:59\
I don't think we can like work the. Yeah, but.

41:04\
I'm just gonna say the reason why I'm saying that is because during
our meeting with EY, right, Paul, that was like one of his very first
questions to me when I did the demo like one of his very first questions
was like how do you like, you know, how do you handle like the provider
registration?

41:10\
Mm-hmm.
Yeah.

41:24\
You know and and on our end, you know, like I said, well, there's a
registration form and they go in and they have the ability to add an
organizational level a lot add, you know, add new, you know, add, you
know, new new users basically below them.

41:25\
Yeah.
Yeah.

41:41\
If they're part of a, you know preferred provider network that needs
to, you know, get authorized by the by the insurance company, stuff like
that, you know, this is what wsib has. They have kind of like these two
options. If you're going to submit your invoices through Telus health
or if you're going to upload and submit claim related documents.

41:53\
Mm-hmm.

41:59\
So I mean on our end it's one and the same. You know whether you're
submitting claim related documents, right, I think you know I think.

42:02\
Mm-hmm.
Yeah.

42:11\
Should matter, right?

42:14\
Well, I guess it's a question.

42:15\
I'm gonna try this.

42:18\
I'm pretty sure you can get pretty far in this process. I've created
multiple wsib accounts, but I think I guess I agree with. I agree with
that and having the provider has their system be created.
But I guess a question that I have is do we think that there's a world
that insurers have their own list or roster in their PPN, and they would
provide, like, let's say, an excel sheet or whatever data file and then
that would trigger to the provider?
Like almost like we have the verification process for the claimant or
the worker. Would that could be would there be something similar to the
provider on that end like I'm seeing two paths like the provider self
signs up and then the insurer auto loads or loads in their their list.

42:59\
We.
Yeah, I I I potentially agree. I I don't exactly know what you know,
Alberta Health is going to settle on.

43:19\
Mm-hmm.

43:21\
I think it'll more likely be, you know, providers go ahead and
register, you know, and then the insurers can, you know, say, well,
these these providers are underneath this, you know, preferred provider
network at our higher level, right.
So they can see them as preferred provider network, but I don't think
that the providers themselves will be registered underneath the insurer.
The the providers will be registered as their own as their own
independent entity.

43:38\
Hmm.
I see what you mean. Yeah, entity.

43:52\
Is is what I think they will be.

43:56\
Yeah, I know that's a great point because a provider could be in
multiple and multiple insurers lists.

44:04\
Right.

44:08\
So to that end, then yes, I think we shouldn't show the provider
registration process.

44:33\
Well already logged in with this e-mail address. I didn't know I had to
log in. All right, well, let's go cancel anyway. So there's an
account.
Oh, I already did this OK.
This is just basically to submit the stuff under.
So then if I go to Telus.
Oh, this is this one.
Where's my Telus provider portal login?
That's always reassuring. That's not secure. There you go.
I think I have a log in here, yeah.
Oh.

45:50\
I'm making you really jump through all the hoops today.

45:59\
You guys can see my password now.

46:02\
Yeah.
We'll start submitting claims on your behalf and then change the the
billing address to to ours.

46:13\
So this is, you know, like this is this is basically what Telus has in
place and this is what they enable and this is this is what other this
is what other organizations basically use in Ontario instead of own,
right.
New wsib form, so this is like if there's a form 826 or Faf or bill.
Umm.
So here is different locations.
Physician WCB location theoretically. So this is what you do. So you
enter in like a claim number or you basically search by last name you
know patient date of birth, whatever and.

46:44\
Oh.

46:59\
Right.
I don't even know what these are.
I guess these are people that are referred under me or referred. I
don't even know what they are. I've never actually been in here.
Oh yeah. OK.
So submit payment. So basically you have to enter a claim number, date
of birth, hit search and it gives you just a place to basically upload
it.
So this is what I was saying. Like everybody's used to like basically
entering in a claim number to kind of find their person. I think we have
to kind of determine how we're setting that up within the system. I was
trying to see if there's actually.
Oh, here it is. Profile.
No, I didn't want that.
It's really quite an awful.
Portal that isn't overly intuitive.
I was trying to find my organization settings but I don't seem to have
them in here.
Oh, here it is.

48:27\
This is just where you like submit the reports, right?

48:30\
Yeah.

48:31\
Like so far.

48:39\
So here's the referral for SRS and whatever, I don't have the access
right now, but this this part right here. This is where they the the
people that are doing like not within own that are doing it within.
Like outside of own, this is where they submit all their bills manually
and stuff, so they have to log in, enter in a claim number, pull up the
person, load the report, all that stuff, all the stuff that we do kind
of within Karen Nexus. They do all manually.

49:13\
None.

49:17\
I was. I was trying to find my.
Basically, you can put organizations and stuff underneath here.
Oh, here it is. This is. This is what I was trying to find. So.
You can set up different work locate like locations and user access and
stuff like that. You know that's kind of ultimately the question like
how are we going to on board people, do we do we, you know, do it in a
way that they complete a form.
You know on, you know on the provider portal, I believe we had something
set up within the external provider portal.
To do like a registration for the providers.
And muckram if we can, if we can kind of find the the external provider
portal and see if we can get that working just so we can take a look, I
think that'd be really helpful.

50:21\
Yeah, yeah, Christian. So I just checked the link that I have, but that
is not working. I need to check the correct link for an ACN that we were
using for a standard provider portal. I think the same.

50:33\
Yeah.
Yeah. So.

50:36\
Message here appears on your side.

50:41\
Yeah, this one or sorry the.

50:47\
OK so.
The link I am kind to access is care loop author care.com.

50:57\
Yeah, that's what I had. And then this is the one that I had it. This
is what I actually had. The power pages, power apps, portal like linked
to and I couldn't couldn't find it either so.

50:58\
Yeah.
Yeah.

51:12\
I'm just gonna go in.

51:16\
Yeah, I need to check this one.

51:28\
Any other questions that anybody has?

51:35\
So Christian, I have a question. So in care, first we will be using both
patient portal, external provider portal and internal provider portal.

51:50\
What was the last one?

51:53\
Internal provider and external provider Portal that is based on power
pages right now.

51:57\
Yeah. I I I don't know about the external provider portal. The question
is whether or not the external provider portal can be reused or
repurposed, right? I think that's kind of what we what we need to need
to determine.

52:07\
Yeah.
OK.

52:12\
Here's here's what's going on with.
Here's why this isn't working mukram.
To show my screen again.
Looks like the portal has multiple website bindings.
I don't know exactly what that means, but that's.
That's what it's doing. So for some reason the there's multiple
website bindings it looks like.

52:40\
OK.
OK.
Let let me check this.
I will update you and Christian on this one. I need to check this one,
yeah.

52:53\
OK. Yeah.
I know at one point time we're going to change this care loop to care,
connect, you know, so it's going to be care, care, care,
connect.arthurcare.com. But that's not this custom URL isn't set up
yet, but but we can leave it at care loop for now and then we can we can
talk about what we do later down the road.

53:04\
Yeah, yeah, yeah.

53:19\
OK.

53:21\
OK.

53:23\
One question regarding the registration part like that would be like a
provider, a single provider like I need me someone else like it would be
one person like registering under their name. Not like for an
organization. Or would it be something else?

53:38\
I think ultimately it's going to be it's going to have to be a
organization that can then essentially register individual.
Locations and users under a location.
That's what I think. Ultimately, it's going to need to be right. So
you would have as an example, you would have life mark as the
organization. You would then have life Mark having the ability to create
all life Mark locations.

54:00\
Mm-hmm.
Mm-hmm.

54:12\
And then all providers basically underneath life mark.

54:21\
So like basically then any user they visit, like any person they
mentioned within their location, they would be like able to access it
via like what the e-mail that the organization used or like give them
their own.
Uh, give them their own registration, basically, like each user they've
like added under like a live park location.

54:40\
Each.
Each user has their own login, yes. Yeah, theoretically there could be a
manager at each location that then has access only to that location. You
know, I don't think that we need to get into that in the demo that,
that, that kind of stuff, we're not going to get into.

54:47\
OK. OK. OK.
Mm-hmm.
Yeah.
Mm-hmm.

55:03\
Umm.

55:04\
So if we are showing something in a demo, it would be like me as a life
mark user like basically filling out a form and then that like creates a
record in MDA and like someone said like looks at like whatever they've
added in thinks it's OK approves it and like.

55:19\
Yeah.

55:19\
Like, let's say the organizations like it's more features available in
the border, like they're able to see more of it, like how like I guess
registration works normally. OK, that is something we need to show for
the demo. Then like that specific like.

55:25\
Yeah.

55:35\
Workflow that organization goes in, they fill in the registration form,
it creates a record in MBA. This is approved or rejected or and if it's
approved it like shows like more of the app to that user to that
organization user.

55:41\
Yeah.
Yeah, one one of the things that I was wondering right, like in the in
like in the ideal scenario, right? I would ideally like to use like
external tenants, right? So entra I entra external ID.

55:58\
Hmm.
Mm-hmm.

56:07\
Tenants, right, so you would have one for the patient portal like for
the patients, right, consumers and you would have one for the providers
and they would have different flows through that. So I think we should
be looking at how do we leverage or utilize.

56:14\
Mm-hmm.
Mm-hmm.

56:26\
You know Microsoft enter external portals in order to do that.

56:32\
Mm-hmm.

56:33\
Because you have your ability to have your your process sign up process
and workflows and stuff within there and you can cater like the look to
it. Have you guys ever used any of any of those?

56:39\
Mm-hmm.

56:48\
None.
You know, like the Microsoft entry Depot portals.

56:58\
I haven't, but I wouldn't.
I'm sick.

57:10\
Because there's a lot of, there's a lot of good functionality in there
that I think you just because that's that's the way that ideally
we're going to want to do it, right? Like not everybody's going to
live in the tenant like we currently do. They basically need to live in
a separate a separate tenant.

57:19\
Hmm.

57:29\
But the next an external tenant like the next like, that's the way
Microsoft has set it up now.

57:39\
Yeah, Christian, so.

57:39\
Right. Umm mukaram, how do we register patients like I think it uses
something similar or.

57:46\
Yeah, inpatient portal.

57:46\
Patients, patients, you do correct. Patients you currently do that,
yeah.

57:51\
Yeah. In patient portal, we are using Azure ADB 2C.

57:52\
Oh.

57:57\
Yeah, but, but it's now not B to C or Azure B to C they've changed it
to now be called like external ID, right? So like B to C is now dead and
they've kind of like transitioned it into.

57:57\
Close, yeah.
Yes, yes, correct.

58:07\
Yeah.

58:12\
And they now have, like, you know, Microsoft external entry, external
ID. And so that's what I think we should be looking at implementing and
and setting up for both the, the, the, the, the.
Provider for for the the claimant portal and for the provider portal.

58:35\
Would it like a insurance insurer like individually? Look at like anyone
that's registering or no. Like sort of approve it?

58:35\
Question.

58:36\
Is.

58:40\
Yeah.

58:45\
Or they would be doing it from the then.

58:46\
None.
No, they'll be like some the government regulator would be in reviewing
it and approving it.

58:53\
Oh.
OK, OK.

58:55\
Christian, like what I can explain is there what I'm aware of. If
they're, if you're discussing the same to log in into into the portals
previously used to use Azure ADB to C for authenticating the the users.

59:10\
Yeah.

59:12\
The issue with data, for example Azure A to ADB to C tenant is deployed
currently if you deploy it or Azure that resides within the USA right it
it it is not deployed. For example in Canada.
That that can have some issues, potential issues, right and.

59:32\
But their new one isn't their new external ID stuff. Yeah, does have a
proper tendency.

59:36\
Yes. Yeah.
Not not right now, but not not at the moment that we have already tried
because it it's all also just like a your BADB to see it's currently
deployed in USA, but there's something that we can get clear from
Microsoft. It's in their road map that in in.

59:40\
I'm pretty sure. Oh no.

59:58\
Coming in near future, it is expected to be residing in Canada, but we
have we are not at this point clear by by which date it will be fully
deployed within the Canon Canon region. However, this is the thing for
future Microsoft is recommending Microsoft will be keep supporting Azure
ADB.
To see for the existing clients or for the years, but they are not
recommending new implementations with Azure ADB to C intra ID is the way
forward that Microsoft is recommending.

1:00:27\
Correct.
Yeah.
So I would I would. I would say that we set up this instance for the
patient portal and the provider portal with, with and tried the external
ID.

1:00:42\
Yes, that I'm saying because you know the the portal that that we are
are developing right now within mazi care care coordination, V6 VVR
actually in in the analysis phase, we are implementing infra ID as as of
now for the new product what we are doing.

1:00:57\
OK, OK.
Because like there's user flows like that we can do to kind of do
self-service sign up and sign insurance and stuff and everything else.
And I think that, you know, you can have them, we can have them go
through that process and then you know, anyways, I think that that's
what we should kind of.
Look to implement kind of within the you know with how it's kind of set
up and structured.

1:01:19\
Yeah.

1:01:26\
Yeah.

1:01:37\
Yeah. And I think we can keep continuing with the existing registration
process without your ACP 2C for demo at least.

1:01:48\
But you're going to have to create a new one anyways.
Right. Like you're gonna have to create a new external tenant anyways.
Like you're not gonna use the current tenant.
Right. You're not going to use the current own patient tenant or any of
the current to say you got to create a new one anyway. So because
you're creating a new one, I don't think there's really any changes
on the connection side of things, right, so.

1:02:05\
Yeah. Yeah, we.

1:02:06\
Yeah, thing it there.
No, there there, there are. There are changes like like we are actually
converting we are we are our dev team used to work. How are your A do
BTC work now we are actually in that phase there are changes in the
flows.
How password is reset and how we are maintaining the session so
development wise it it is involving changes at at least that that the
dev team right now is looking into in in building the latest product on
top of our pages.

1:02:44\
Right.
But we'll need to do. We'll need to do something that that comes
across crosswell, right, so.

1:02:53\
Right. I think that we can definitely implement this is the way forward
for the the actual work like but Christian for for the demo I think are
we discussing this in from the demos perspective or what's required for
the demo?

1:03:12\
Yeah, I mean, I guess it's, I mean the regular way that the the
patient, the the way the patient stuff works currently I think is fine,
right 'cause the patient is registered at the provider level, fine. It
doesn't matter to me. You can go ahead and use the way that it's
structured and set up if that's using B to C.

1:03:23\
Right.

1:03:31\
That's fine. I think ultimately we need to figure out how we're gonna
implement a provider registration and that's where I wanna see what we
did for the external provider portal. Cuz I do believe the external
provider Portal had a registration function within it.
And and I I I think that actually I do believe that that was through
Azure B to C as well because I I I see I see an external provider
portal.

1:03:50\
Yes.
Yes.

1:04:04\
Tenant B to C tenant on our tenant, right, so.

1:04:11\
Mukaram you're aware about that, right?

1:04:11\
Time.

1:04:13\
Yes, yes, yes, question, you are correct.

1:04:14\
Yeah.

1:04:20\
So I so that's what I see. 'cause I see this here. I can show you.
So I can see this external provider portal tenant.

1:04:39\
Give me.

1:04:41\
So I'm pretty positive that that.
That's for the for that extra provider portal.

1:04:44\
Yes.

1:04:48\
Yes.

1:04:56\
So we'll follow up on that mukram and then we can make final decisions
on what we're going to do on the provider side as we enter in the the,
the, the feature, sorry, the user stories and tasks.

1:05:09\
Right. OK.

1:05:09\
All right. Yeah, I will update you question.

1:05:13\
Now, just as we finished, so who's gonna? Who's gonna actually enter
all this stuff in?
I mean, I'll help a little bit and do some you know.
But ultimately, like, who's gonna who's gonna take full?
There's quite a bit to enter in. I mean, obviously I can, you know, do
some of the stuff and Mira will help do some of the stuff and ask, I
know that you're already putting some of it in.

1:05:39\
Yeah.

1:05:40\
But basically like I can put in user stories, but then somebody
ultimately needs to put in kind of the tasks kind of underneath that,
right?

1:05:52\
Yes.

1:05:53\
In like development and software.

1:05:56\
Yeah, either development or like like as an example like I can put in a
user story for, you know, for the branding and like you know, we need to
change like instances where it says, you know patient to claimant. But
then like it's like OK like.

1:06:05\
Mm-hmm.

1:06:11\
No.

1:06:14\
You kind of have to go through and identify like where it says patient
all over the place. Like, where does it say like where actually did that
exist and where does it need to be changed, right?

1:06:15\
Yeah.

1:06:30\
I can take a look at that.
I mean, I am like going to basically like an easy user story add in like
a proper description of everything that needs to be done. So you can
assign certain user stories to me. If you think they need more updates
and I can add them in.

1:06:47\
OK.
OK.
OK, so we can do that.

1:06:57\
Perfect.
So just as a recap, to make sure I've captured the discussion primarily
for today and ask, you'll help drive forward in putting those
descriptions for the tasks based off of the user stories that Christian
and I will be populating in there today.
When it comes to, I think the portal discussion, particularly the
provider portal, I think the decision is to leverage what we already
have existing, but update the UI to be relevant for Alberta and then
we'll retain the chart style and the core content.
Once again, just update it for the Alberta context. We have two flags
for environment, one around setup and then one around storage. So today
in our steer Co conversation, we'll bring this up to raise with Kevin
and we'll book a follow up conversation I believe will be Kevin Nazim,
Christian and myself.
To make sure which makes the most sense around the authorship, I think
we're around the storage. We have the conversation around which tenant
makes the most sense, and so there seems to be enough space in the
Arthur tenant, partially because we're not turning on logs for now. So
that should be fine to set up there.
And then I think for the Arthur Cara Loop bindings portion, I think
mukhram you mentioned that you will go in and review that and get us an
update on what's going on there. So those are the the key items that
came from follow-up actions that we need to do from today. Was there
anything that was missed?

1:08:37\
Yes, correct.

1:08:37\
OK.
Great.
One of the other action items that was I think discussed was the plan to
action the tickets that are being inserted. So obviously the user
storing tasks are being populated and I think our goal should be get
this done by the end of this week. In terms of timelines to execute on
each of the subsequent tasks.
How would the group like to go about that process in terms of how long
you think it'll take you to action those tasks and who will be doing
what?
Would it help if you book a session or does a group prefer to do self
assigning independently and we review what is the preference for the
collective?

1:09:20\
Yeah, I believe once we have all the user stories entered, I think the
best that we can internally do our part and and by adding all the detail
labeled requirements, we can set up the effort along with who's doing
what and and then we can together review in a joint call.

1:09:34\
Mm-hmm.
OK.

1:09:39\
To see what the plan looks like.

1:09:43\
That sounds great. We have our next day left on Wednesday. Next week. Do
you think that would be reasonable to have all of that completed by
Wednesday so we could use that session to review the tasks, allocations
and efforts?

1:10:00\
Yeah, I I think we we should connect it whatever we have and let's have
a call on Wednesday.

1:10:04\
Yeah.

1:10:07\
OK, OK. So we'll aim for Wednesday to have that all organized so we can
start executing on the tasks perfect. So I'll send a recap summary of
what I just re edited with the group those timings and who's assigned
to what. And then we'll have our session next week on Wednesday. But if
the group needs to meet.
Before then, we can set up time either with the whole group or with the
subsets that need to be part of those conversations.
I said how are you?

1:10:37\
Good. I know I'm joining late, so I'm just sinking in.

1:10:40\
All good. You got the nice recap at the end.

1:10:43\
Yeah, I, but I get the recap, which is the good news. Oh, good for me,
but I think Ani Nazim and Amira, we kind of need to work back from the
September 8th.
Date so Wednesday is viable only if it match with the with the September
8th date and and if it needs to be Monday because otherwise we're not
gonna meet September 8th date. We kind of need to be.

1:10:58\
Agreed.

1:11:13\
Kind of. You know, aligning some of those directions in that way, right.
I think, Christian, you asked earlier who, who owns the user story and
everything, right. The intent is Ani, Nazem and Anas.

1:11:13\
Mm-hmm.

1:11:28\
To make sure that we take everything, whatever we can out from Christian
brain, put it into those DevOps. While Christian Review approved,
agreed. Yes, that's pretty much what it is, but we kind of now taking
the ownership or the driving seat a little bit more.
To make sure that you know means if we're going in the wrong direction,
Christian will tell us we're going and we all know he will. But I want.
I want us to kind of get into the whole driving seat, right. So there
when I think about driving seat, there are three areas that we need to
get ourselves very aligned with.
I think high level business process based on Nazim, you know the details
you have shared earlier. I feel like we kind of have an understanding of
what the high level business process is.
The client portal or provider Portal was the big challenge that we we
don't want to reproduce it, right, but it seemed like that we're in
agreement that let's just minimally adjust in a way that we can pass
through the September 8th date.

1:12:29\
Yes.

1:12:29\
Without making a major change, I'm good with that. So so it seemed like
we got that label. Now we really need to own the generation of user
stories based on the recordings that we have and everything we get, you
know, heavily used GPT.
Instead of manually creating everything, get it you know I mean it's
offline, reviewed with Christian, you know, whenever he has his pajama
time, he can review, provide the feedback, but have a final solution
statement. Ani, you know what I mean? This is what the final world will
look like. Start establishing that.

1:12:47\
Hmm.

1:13:04\
Your our own view and have Christian validate for US versus Christian
create the view for us. You're getting my point.
I I have a feeling that, you know, it's many times, but Christian says
what we understand are not exactly the same thing. You know the the
prior iterations kind of give us some of that experience and I want to
make sure that we kind of take over on the reverse side now and have it
validated by Christian.

1:13:32\
Understood. Yeah.

1:13:35\
Right. So based on both of those days conversation, the user stories
that you're working on and you feel like that you have the good grasp
of where things needs to go.

1:13:45\
I'm getting there. Yeah, I think so.

1:13:45\
Yeah.

1:13:48\
OK, very good, Amit. There was another thing that you mentioned
somewhere. Oh, you know this old upgrade upgrade to new version of music
and on is the most complex thing and gonna take 30 days.
And you know, I mean which which OK means if it takes 30 days, it's a
different story. But I want to make sure that we are not, we're not
just replicating.
Until you with their data, with their configuration in this new
environment and try to kind of make changes on it because you know,
whenever we do something like that, we don't realize that there was
some check boxes, there were some things there and when you try to move
into the real develop environment and others.
Start things start breaking up right? So I'm OK. There's no need to
have a version upgrade. Ready. But I don't want to just use one of the
previous environment and call it a new environment. At least I would not
recommend that.
I don't know if that's what we were planning or not.

1:14:55\
No, we're not. We're we're. No, we're setting everything up that we
had that discussion at the beginning. So it was one of our first things
said. So we're setting up we we are using own UAT kind of as the
version that we're going to essentially copy over.

1:15:00\
OK. All right.

1:15:12\
But we are setting up new subscription new Azure resources. All that
side of things new portals, it's all net new. Nothing's being kind of
leveraged from a prior environment is what we're doing.
We did discuss the value of.

1:15:29\
What about the configuration and the data and all of those things?

1:15:34\
Much of it, we're going to have to change, but that that side of it
still can come over from, from UAT. Biggest issue is going to be like
just kind of like organization names and stuff like that and configuring
like that, you know, part of it but.
It's just a bunch of, you know, configuration items that that we'll
have to do, right.

1:15:53\
So now then, is it? Is it possible that the only thing we bring from UAT
is the version of the code, not the configuration, not the database, not
the you know database and all of those thing? It is the only code base
that we are moving.
And we configure the environment from scratch.

1:16:13\
We can do that. Yes, we can deploy the the builds and then we have to
configure that the the data then.

1:16:19\
So we know what we are configuring, right or or what we don't need to
configure. It will. So Christian like if we go that way it takes more
time, but you have the clarity and control over what's there.

1:16:21\
Yes.

1:16:34\
If we just move the configuration from the UAT environment, you don't
even remember what those different checks and things that somebody have
set up somewhere which make things work for now. And then you get stuck
later on.

1:16:48\
I know it's it's a catch 22. I don't know what the right you know
because that some of the stuff that's in there is just, like, totally
irrelevant. Yeah, you can get by and you can kind of like showcase it a
bit, but.
Yeah, it's, it's, it's.

1:17:06\
Honey, based on your prior experience, you know both both are the
options. But what would you recommend?

1:17:13\
See, it depends on how much change we are going to make, right. So
again, having existing data and trying to reuse it for another. Another
demo is usually not something I'm comfortable with now in this
situation, I think that still applies.
As far as the.
The setup is concerned the configuration and the code and everything. If
the functionality is the same and it seems like it is, I think we should
use the code. Probably put it on a blank template database and generate
data. I mean, I know we probably cannot do everything.

1:17:42\
Yeah, yeah, yeah.

1:17:50\
Everything, but maybe we can generate enough that we have enough for a
demo.

1:17:53\
My recommendation? Christian would be we generate sample data, use GPT
to generate sample data. You know, just amazing tools out there now and
we load it up and we get this new environment. Lady, we're going live
with a new customer, right?

1:17:58\
Yeah.
Yeah.

1:18:08\
And three days later, if we realize it's more complex, it's just way
too much. We didn't even thought of. We can always, you know, roll back
some of those things. But I would. I would want to start there versus
what's the UAT data.
From phone environment.

1:18:27\
Right.

1:18:28\
Like there's things like like I should say, said. Like there's things
like when we talk, kind of there's master data, right. But then
there's things like the templates, right, the configuration of the of
the notifications. I don't know if those are considered.

1:18:29\
So then.

1:18:31\
I.

1:18:47\
Code or not, but I think so. So those templates I think need to come
over all the outcomes need to come over because recreating all those
\and and huge
amount of work.

1:18:49\
Those are consider configuration.

1:19:03\
So there's certain parts like that that I think are are potentially
useful and so maybe that does maybe the locations do come over and
everything else and we just kind of we we we overwrite or we create new
and delete you know like.
Something like that, right?

1:19:22\
Nancy, what would you be your recommendation?

1:19:24\
Because because I I don't think. I don't think we want to get into
creating all the templates themselves and those workflows for the user
registration or for the the patients and the patient outcomes like in
the portal like all that works and works really, really well.
And we're able to demo that really well, right?

1:19:43\
All right. Now then, what's your recommendation?

1:19:49\
We can potentially just replicate what we have the your data and then
spend the effort to delete the unwanted data and and make sure in the
demo we have only only the meaningful data.

1:20:04\
But that's remember like that's that's just. Yeah, this is what I
want to try to stay away and recommendation. Right. When you just. I
heard this term demo it's not about demo is demo is not what we're
going after right means we could have just the demo in the current
environment and live our life that's that's not the intent.
It's the actual, you know, it's future build that we're gonna make on
top of it and and also all of the changes, you know, I mean from UA from
from the use case perspective.
Then we're gonna move in. Yeah. For for utilization, for validation
phase, right. It's going to be an important play.
Right. So we need to be ready for solution validation with the build
that eventually will go into development and move from development to
the next level.

1:20:59\
Agreed, this is indeed the right way. We're just trying to match up
like the with the effort and the amount of time we have.

1:21:08\
Yeah. Yeah. So, so that one thing that I want you to.
I know you. You you will start with the effort, right? Everything is
complex. Everything is gonna take a lot of time. So let's follow the
least possible effort way. I would recommend take that approach out for
a minute. Think about what is right for the project.
Right. And if right thing to do for the project is to replicate all of
this capability, which I think Christian mentioned that these are all
critical, then go do follow that model. If right thing for the project
is we selective export information and load it up.
Then follow that model.

1:21:56\
Hmm.

1:21:57\
Because end of the day, we do all of that and then September eight, you
says, OK, we have to restart the project because we should take a
shortcut later, earlier. That's what gonna hurt us.
Makes sense, Madam.

1:22:11\
Right, absolutely yes I am.

1:22:13\
So so I think I will let you know. I mean I think Christian provided his
feedback that it seemed like a lot need to be replicated and if we if we
try to configure everything from scratch, it's redundant work with no
value.
Right. So think about it and send a note back to Annie, Annie and Nadim.
You guys should work together to figure out what is the approach. You
want us to to take? I I'm not pressuring on either wayside Nazim.

1:22:38\
None.

1:22:44\
But I don't want like, oh, it's too complex, so let's just follow a
easier route and they get stuck ourselves later on. That's what I
don't want.

1:22:54\
Yeah, agreed.

1:22:56\
OK, good.
And then just I I said it last time to Nazim, make sure that as we are
creating new subscription you know I mean we work with CSP team and
Kevin to create the subscription in a way that is good for Microsoft.
That's a very important video.

1:23:20\
Does anybody actually know how to functionally do that? Said like we've
been talking about that for like 5 months or four months and nobody
seems to actually know how to do it. Are you sure?

1:23:24\
The CSP team knows it. The CSP team knows it. Yeah, CSP team.
No, no. The CSP team knows it. Kevin needs to just introduce our team.
That's what they said last time. That's they showed it to Microsoft.
All of that. So Kevin should be able to introduce to people person,
whoever was responsible for. So Nazim, you should reach out to Kevin
Castillo.
And and ask him and she should be able to engage with whoever we need to
engage with.

1:23:53\
And.

1:23:55\
OK.

1:23:56\
OK.

1:23:57\
Right, like like 'cause, I can cause decided like I can create a new
subscription like. Right now I just don't know right like don't know
what it you know enter selection or subscription number. Right. Oh, as
your RAC owners da da da budget tags create there's there's nothing in
creating a.

1:23:57\
All righty.

1:24:17\
A subscription.

1:24:19\
There was something that we have run with with run with Microsoft, they
said.

1:24:19\
That I see that I see that I see on our end.
Right.

1:24:26\
Yeah, I'm. I'm gonna debate. Here's. Here's where. Hey, Kevin. Work
with someone in Microsoft to get this sorted. Let's bring Kevin back
and get that sorted.

1:24:37\
Yeah.

1:24:37\
I I don't want Nizar on my tail right there on saying oh, but we were
supposed to do that and all of those things.
Fair enough.

1:24:46\
Unless this is what there, this is this app ID so just this is what I
want to get clarity of.
Right, like creating a subscription takes all of two seconds. I'm going
to type in care 1st. I'm going to select A billing, you know, so that
we gave basically have full access to it, you know advanced. You know
you select your directory and da da, da, DA management group or
whatever, right?

1:25:12\
Just bring. Bring Kevin in and then have him verified somewhere it could
be that one, I don't know.

1:25:13\
So.
Subscription owner.
I'm assuming that it's. I'm assuming that it's probably this thing
'cause they've always talked about entering in an app ID.

1:25:25\
OK. Maybe then that's what it is.

1:25:27\
And that's all I can. That's the only that's the only spot anywhere
anywhere in here.
That literally has anything.
To do unless it's under a billing account but billing account if we. If
you guys create it, it goes under your billing account so that this is
the only thing that I can think of this app ID, but this doesn't make
full sense to me.

1:25:58\
Yeah, it these things never make sense to me. So that's why I have
other people who could figure it out.
OK.

1:26:07\
OK.

1:26:08\
Alright, I'm here. Back to you.

1:26:11\
Amazing. So I think you make a great point, said about timeline and
pacing and whether or not we should have that conversation maybe on
Monday instead around efforts and timelines for the group. Is that a
more, is that reasonable to attain a Monday conversation on that instead
of Wednesday?

1:26:34\
I think at this point we are still in the process of putting the user
stories. I think we'll be in more better position at the end tomorrow.

1:26:36\
Yeah.
And the datum.

1:26:46\
Yeah. Why don't I mean, if I were you, I will just set up a 30 minutes
daily check in for rest of the week, right. If it's done, yeah. If
it's done Monday, great. If it's done Tuesday have have another big
session on Wednesday plan. But let's just, you know, follow through.
The other thing. Team Anas, Anasim mukaram, everyone.

1:26:48\
Yeah.

1:26:51\
It it will be better, yes.

1:26:52\
Great.
True, true.
Perfect.

1:27:05\
If we are manually figuring out what the user's stories are, we are not
leveraging the new technology, right? We should be leveraging, you know,
I mean, scopilot other capabilities to ensure that these things are make
sure we are not going on a general GPT out, right, whatever we are
doing.
Business GPT or we're using copilot to generate those. Generate those
user stories which can pass on to then DevOps.

1:27:37\
OK.

1:27:39\
OK.

1:27:41\
That's why I think that, you know, we should be able to share it on
Monday or soon later.

1:27:41\
Fantastic.

1:27:43\
That makes sense.

1:27:45\
Fantastic. That sounds great. So I'll get those invites in in this
group's calendar and then we'll send out the summary of notes and then
we'll talk to the group tomorrow.

1:27:48\
Alrighty.
OK. Thank you.

1:27:58\
Any other questions of the group before we head out?

1:27:59\
Right.

1:28:04\
No.

1:28:07\
OK, great. Thank you everyone.

1:28:08\
I will send a note to Kevin, so he's expecting.

1:28:18\
OK.
OK.

1:28:22\
All right. Thank you. Bye, bye.

1:28:24\
Amazing. Thank you very much everyone. Bye.

1:28:24\
Yeah, thanks. Thank you, everyone. Bye.

1:28:24\
Alright, thank you. Alright, bye bye.

1:28:25\
Thanks. OK bye.

**Muhammad Mukarrum Siraj** stopped transcription
