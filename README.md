# JSONServer-test

https://github.com/typicode/json-server

GET SINGLE AUTHOR OR ARTICLE
http://localhost:3000/authors/1 This will give us the author with id 1
http://localhost:3000/articles/1 This will give us the article with id 1

GET ALL ARTICLES BY AUTHOR
http://localhost:3000/authors/1/articles This will return all articles by author with id 1

FILTER AUTHORS BY ID, FIRST NAME, ...
http://localhost:3000/authors?id=1 This will return all authors with id 1
http://localhost:3000/authors?firstName=Albert This will return all authors with firstName of Albert

FILTER ARTICLES BY ID, DESCRIPTION, ...
http://localhost:3000/articles?id=1
http://localhost:3000/articles?description=Mathematics
http://localhost:3000/articles?date=June 18, 2019 will turn into http://localhost:3000/articles?date=June%2018,%202019

PAGINATION AND LIMIT
http://localhost:3000/articles?_page=1&_limit=10 this will give us the first 10 results in page 1
http://localhost:3000/articles?_page=2&_limit=10 this will give us the next 10 results in page 2 (if there are enough)

SORT
http://localhost:3000/authors?_sort=firstName&_order=asc Sorts authors by first name in ascending order
http://localhost:3000/authors?_sort=firstName&_order=desc Sorts authors by first name in descending order
http://localhost:3000/authors?_sort=id&_order=desc Sorts authors by id number in descending order
http://localhost:3000/articles?_sort=date&_order=desc
The sorting only takes into account the initial digit or char so in ex. 1, 10, 2, 3, ...

RANGE
http://localhost:3000/articles?id_gte=2 articles with an id of 2 or more
http://localhost:3000/articles?id_gte=2&id_lte=5 articles with an id of 2 and less or equal than 5

FULL TEXT SEARCH
http://localhost:3000/articles?q=math searches all the fields for whatever keyword we use