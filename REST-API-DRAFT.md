#Draft 
Rest API q.uote.me URL (GET)  

/quotes -> gives last 10 quotes by date desc  
/quotes/{int}/asc -> gives first {nb} quotes by date asc  
/quotes/.../a-> gives last 10 quotes from author by date desc  

*Rest API q.uote.me stats URL*

```
stats/quotes -> gives stats about quotes  
/{...}/posted -> gives nb quotes posted  
/{...}/delivered -> gives nb quotes delivered  
/{...}/{...}/{lastYear|lastMonth|lastWeek|yesterday|today} -> gives nb quotes last year, last month, last week, yesterday or today  
/{...}/{...}/{year} -> (int 4) gives nb for {year}  
/{...}/{...}/{year}/{month} -> (int 2) gives nb for {month}  
/{...}/{...}/{year}/{month}/{day} -> (int 2) gives nb for {day}  
/{...}/{...}/{...}/{user} -> filter search by user {user}  
```

*Backend for non url rewrite:*

```
stats?method=quotes -> gives stats about quotes  
{...}&type=posted -> gives nb quotes posted  
{...}&type=delivered -> gives nb quotes delivered  
&when={lastYear|lastMonth|lastWeek|yesterday|today} -> gives nb quotes last year, last month, last week, yesterday or today  
&year={year} -> (int 4) gives nb for {year}  
&year={year}&month={month} -> (int 2) gives nb for {month}  
&year={year}&month={month}&day={day} -> (int 2) gives nb for {day}  
&user={user} -> filter search by user {user}  
```