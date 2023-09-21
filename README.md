# NCSL-50-states
1 – We searched for a specific databases from NCSL.org 
2 – used python libraries ( selenium , BeautifulSoup) to connect to the web page and extract the data from the website 
3 – first we scraped all html code from the page using soup from BeautifulSoup
4 – searched for all (bill names, links , bill numbers, year)
5 – searched for (title , status ,  author) of every bill
6 – searched for additional author if existed and associated bills if existed
7- transformed the auther :
•	If independent we put 0 instead 
•	In it was a commite we put 1
•	If it was a government office we put 2
8 – transformed party :
•	Republicans : 0
•	Democrats :  1
•	Independent : 5
•	Nepraska : 7
•	Government office : 8
•	Commite : 8
9 – transformed the status:
•	Adopted : 1
•	Enacted : 2
•	Failed : 3
•	Failed – Adjourned :4
•	Override pending : 5
•	Pending : 6
•	Pending – carryover : 7
•	To governor : 8
•	Voted : 9
9 – calculated total number of supporter from all parties and total number of supporter from the other party
10 – using pandas dropped all bills that was suggested from “PPD” and “PNP” parties
11 -if author party was ( 6 , 7 ,8 ) we transformed total number of supporter and total number of supporter from the other party to (996,997,998) accordingly 
