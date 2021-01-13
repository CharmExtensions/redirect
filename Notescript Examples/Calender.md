# Calenders
````
[note] < google-search | https://www.google.com/search?q=how+many+days+are+in+this+month
 - google-search ----- ^ | [return] > day "from" > google-search | answer = 2
[note] < calender | calender: /d/{date}=/$/?=d{day}/s{seconds}/m{minutes}/h{hours}/d{days}/m{months}/y{years}
calender == array |
  - [h:m,d,y,]  _ ^

list: calender > array / list "date" | google-search | answer=2 //returns the second answer.
````
