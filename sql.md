# Database
## database design pattern:  
1. atomicity
2. non-primary key must rely on primary key
3. the rely relation must be direct relation

## E-R model  
square: table  
circlr: field  
diamond: relation  


## database engine
1. innoDB  (support transact -sql)
2. MYISAM  (fast, but not support innoDB)

### change db engine:
```sql
alter table students engine = 'MyISAM'
```

## transact-sql:  
only apply if all sql success  
ACID(atomicity, consistency, isolation, durability)  
default will autocommit all transaction.  

```sql
set autocommit=0 --temperory set auto commit 0 (re connect will reset to 1)
XXXXXXXXXXXXXXXXXXX
commit
--rollback
```

start a transaction
```sql
begin;
XXXXXXXXXXXXXXXXXXXXXX(transaction code)
commit;
```


# Index
primary key will automaticly add index
foreign key will also automaticly add index
create a index = create a file, will occupy disk space

## joint index
will save disk space.  

***the left most column must inside the query string***  

## notes
1. update often table, no index  
2. data size small, no index  
3. duplicate value too much, no index  