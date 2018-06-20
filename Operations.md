# Operations in Mysql
## 1. create table
### (a) create new table 
> **CREATE** **TABLE** bookstore (bid INT PRIMARY KEY, bookname VARCHAR(10), publishDate DATE);
### (b) create table from other table
> **CREATE** **TABLE** bookDate(bid int PRIMARY KEY, publishDate DATE)  
> **INSERT** **INTO** bookDate  
> **SELECT** bid, publishDate  
> **FROM** bookstore
### (c) create table adding index
> **CREATE** **TABLE** bookstore (bid int PRIMARY KEY,   
                                  bookname VARCHAR(10),   
                                  publishDate DATE,   
                                  **index** pd_index(publishDate))
## 2.drop table
> **DROP** TABLE bookstore
## 3. cast
> cast(timestamp as DATE), cast(responseData as JSON)
## 4. JSON in MYSql
> **JSON_EXTRACT**(**CAST**(responseData **AS** **JSON**), '.$creditRating')
## 5. time comparison
>> SELECT bookname  
FROM bookstore
WHERE publishDate > CAST('1994-09-23' AS DATE)
