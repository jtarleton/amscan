# amscan
Amscan Evaluation
Web Application Developer - Take Home Assignment

Balloon Inflation and Assembly Management 
Our balloon business is extremely hot right now and getting hotter. So much so we have hit a record number of Balloon sales and in turn a record number of Scheduled Balloon Inflations/Assembly orders. The stores paper solution is outdated and has become a bottleneck and needs to be replaced with a digital version.
The store operation team has partnered with Application Development team to Mockup a Mobile WebAPP solution for the stores to use as a replacement for the paper solution. To be a worthy replacement the App must accomplish the following: 
1.	Display all balloon orders that are to be picked up for the current day, in the order they need to be inflated and or assembled to be ready for the customer pickup 1 hour before the scheduled pickup time.
2.	Allow for the ability to see all the orders scheduled for the following day to allow for planning.

 


 
Listing UI Mock
1.	Day Selector(dropdown)
a.	Today (default option):
i.	Is the default 
ii.	Shows all orders scheduled for pickup on the current day the “list of orders” table at lower section of the screen. 
b.	Tomorrow (second option of the dropdown):
i.	Shows all orders scheduled for pick up the day after the current day within the “list of orders” table at the lower section of the screen.
2.	Total Number of Balloons for the day
a.	Balloon Inflations (Section label)
i.	Foil Totals (label): 1000
1.	The sum of all balloons that will need to be inflated for that day
ii.	Latex Totals (label):  1000
1.	The sum of all Latex Balloons that will need to be inflated that day.
b.	Assembly Total: 4
i.	Total of all columns, and bouquets that must be assembled (assembly service SKUs) for the day
3.	List of orders (Table)
a.	Order Fields
i.	Balloons: Sum of all balloons in the order
ii.	Start Inflation: 
1.	The time inflation/assembly should start in order to be completed 
2.	Start must be padded by 1 hr. so that orders are ready for pick up 1hr before the scheduled pickup time
iii.	Pickup: The time the customer expects to pickup the inflated and or assembled balloon order
iv.	Customer
1.	First initial
2.	Last name
v.	Inflation/assembly time
1.	The calculated time it will take to inflate all balloons, and or assemble a bouquet or column on an order plus the buffer time (1hr before pickup)
vi.	ASM
1.	Total Columns, and Bouquets to be assembled(assembly service skus) for the order

 
Balloon Products/Inventory
Sku	Desc	Package Qty

	Inflation/ Assembly time(secs)	Material	Sku Type
01111111	12” inch Green latex Balloon	1	0	Latex	Balloon
222222	15 Pack 12” green latex	15	0	Latex	Balloon
333333	36” White Latex Balloon	1	0	Latex	Balloon
444444	18” Pink Round Foil	1	0	Foil	Balloon
555555	18” Purple Round Foil	1	0	Foil	Balloon
666666	36” Giant Red Flower	1	0	Foil	Balloon
777777	62 Balloon LG Green and White Column Assembly	1	3600	Null	Assembly Service
999999	Small Garland Assembly	1	2000	null	Assembly Service
10101010	Latex inflation LG	1	60	Latex	Inflation Service
111111111	Latex Inflation SM	1	30	Latex 	Inflation Service
12121212	Foil Inflation LG	1	110	Foil	Inflation Service
13131313	Foil inflation SM	1	30	Foil	Inflation Service


How Customers order
Customers Order Balloons in few ways
1.	Balloons without inflation
a.	Assumptions
i.	Balloons skus are used to describe the balloon products and qty being purchased
ii.	As there is no inflation requested by the customer these orders will not be handled by the app
2.	Balloons with inflation
a.	Assumptions
i.	Balloons skus are used to describe the products and qty being purchased
ii.	Inflation skus are used to determine the qty and type of balloons to be inflated on an order.
 
3.	Balloons with inflation, and Assembly into an arrangement (column, Boquet, etc.)
a.	Assumptions
i.	Balloons skus are used to describe the products and qty being purchased
ii.	Inflation skus are used to determine the qty and type of balloons to be inflated on and order.
iii.	Assembly skus are used determine if the balloons included on the order are to be arranged in the form of Column, or Bouquet
iv.	Included on the order will be the balloon skus  and the appropriate qty necessary to assembly arrangement identified by the Assembly sku


Some Order Examples for testing with 
Lrg Green and White Column 
Fname	John
Lname	Doe
Pickup Date	7/30
Pickup Time	6:00
Store#	1999

	

Sku 	Order Qty
011111	2
22222	4
77777	1
111111	62


2x Small Flower Bouquet
Fname	Darth
Lname	Vader
Pickup Date	7/30
Pickup Time	7:00
Store#	1999

	

Sku	Order Qty
444444	4
555555	4
999999	2
13131313	8


 
Bunch of Balloons with Inflation Only
Fname	Luke
Lname	Skywalker
Pickup Date	7/30
Pickup Time	7:30
Store#	1999

	

Sku	Order Qty
6666666	4
12121212	4
 
Assignment 
You have been asked to create a Minimum Viable Product (MVP) / prototype of the Mobile webAPP solution. MVP Must include the following.
1.	A new API endpoint to accept an order, then perform the following.
a.	Calculate the time it takes to inflate the entire order using the inflation time for skus found in the inventory information provided above
b.	Determine what time the inflation and or assembly should start to get the order ready for pickup and hour before the scheduled pickup time.
c.	Determine the total (split by material) number of balloons for the order. Note, we do sell 15 packs of balloons so account for pack SKUs.
d.	Store the order
2.	List Page listing all Balloon orders for the current day along with all the information shown in the Mock and outline 
a.	Order the list using the order’s Start time ASC: Start time is the time the inflation should be started to complete the inflation and or assembly of the balloon order in time for customer pickup.
b.	Start time must be padded so that inflation and or assembly can be completed 1 hour before the Scheduled pickup time.
3.	List all Balloon orders for the following day (Tomorrow Dropdown: using above listing criteria in 1)

Tech Stack (Preferred Tech Stack), architecture.
While this project is meant to be a prototype, we would like it built and ready to be deployed to a 3+ tiered architecture including a Data layer/Storage, Middleware API, and UI / FE client, ideally using all or most of following technologies.  For demonstration purposes a development machine or demo cloud account are great.. 
•	Front-end to be coded in PHP(frameworks are ok)
•	PHP client that reaches out the api to fetch data
•	MySQL  backup to store the order


•	Guidelines
1.	Candidate will be given up to few days to work on the project with a meeting scheduled immediately
2.	Hiring team will make every attempt to be available to answer questions vis email or an arrange meeting via teams.  
3.	The candidate is permitted to make requirement changes if in-line with 2 stated solution points of the project/app and so that the prototype can accomplish the 3 key objectives for the demo under the assignment section above.
4.	Candidate should be prepared for the following  
a.	A screenshare, walk through, and explanation of the components and code.
b.	Questions around 
i.	Best practices
ii.	Choices in libraries
iii.	Performance options or not 
iv.	Enhancements that could be made
	….


