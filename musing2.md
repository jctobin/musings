Data Science is a Rebrand of Data Analytics  
At some point data and nerd became a cool/okay thing
probably the time when people realized that using data to make decisions tended to yield greater profits
so we said 'we need to analyze data' --> data analyst
you paid them decent salaries, but they were just analyzing, 
not actually making the decisions, 
not directly fueling business decisions, 
just being treated like a dev of 'make feature X', but 'tell me the average market share'
or in less common situations 'how are our sales forcasting out for the next quarter'
i wasn't part of the industry at that time, but you still see the remnants of that to this day with a large of 'data analysts' and 'data scientists' alike. 
the simple 'find out X.'
At some point managerial folks let go of the reins a little, perhaps bc of the general shifts in the industries, 
  maybe bc they could afford to try new things? 
  maybe due to the literature that started appearing about 'how to raise kids.' 
ya know, the stuff about not being super strict, letting them 'discover things for themselves', etc
anyway, instead of being told to 'find me the average from last month' the question was, check out the data from last month and tell me what's up with it
or maybe due to the advances in technology, this just became (hopefully) a relatively easy task in most organizations
data had been being collected and moved into DBs, more people were familiar with DBs, 
mainframes started to go away, sql became a big thing
data just became easier
idk if y'all have tried to work in a mainframe context, but it just kinda sucks
by no means have i delved too deep into that space, but ive had to do Some stuff with it and its just unpleasant
nothing is customizable, as a linux terminal lover, nothing just felt intuitive, movement was weird, etc
but now we have RDBMSs, there are various flavors of SQL, but set standards for the globe across all the systems
`select * from table` works Almost everywhere
we're even now putting sql layers on top of nosql DBs, im looking at you phoenix
so maybe 20 years ago, something like calculate the mean last month was a task that would take a few hours
find the right spreadsheet/file or collection of files
do a 2x check that that data all actually fell within those months, (bc it wasn't Easy)
to put it in perspective, the first commercial Oracle DB came out in 1979. 
there are still MANY people working, that were working when the FIRST oracle db came out. the first. 
the very first MS sql server came out in 1989!!! 
30 years ago. 30. that's it. 
and we know that organizations/enterprises dont move at the same speed as the tech they use, 
they cant. an organization has far too many moving parts to hope to stay  at the absolute bleeding edge of every tech in their stack
they probably wouldnt want to either, for security, bugs, etc 
Let's take a second and think about how many semi-major updates that means. 
quarterly updates for 30 years? 120 updates. that's it
120 cycles 
now we have fancy 'sprints' and 2 week cycles, continous integration and continous deployment
but for a long while, and still at a VERY large number of places. its waterfall planning. bi-annual releases (maybe quarterly, maybe monthly, but still, even then, 12*30 = 360 updates
idk how much work yall can accomplish or get done in an 'update' of your code, especially things that you have to work with cross-collaboration, but what ive seen is that 1 update may only contain max(10) truly different/better updates/upgrades
that's it
so over the span of 30 years, and 360 updates, you get 3600 'things' that are better (or at least not broken)
back to the main story
technology got better, makes things easier, now we can do a simple thing like
`select customerId, sum(sales) from customer join sales where sale_time = last_month`
and the month after? just run the same thing, if you want 2 months ago, `sale_time = 2_months ago`
because the data is all there, we're just storing it and using our new fancy tools
at about that time 
