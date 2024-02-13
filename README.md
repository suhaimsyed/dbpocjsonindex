Trying out https://planetscale.com/blog/indexing-json-in-mysql

start the container docker-compose-up

 '''
 mysql> SELECT JSON_UNQUOTE(JSON_EXTRACT(jsonobject, "$.invoiceid")) as invoiceid FROM ordertablenew where JSON_UNQUOTE(JSON_EXTRACT(jsonobject, "$.invoiceid")) = '100030020';
+-----------+
| invoiceid |
+-----------+
| 100030020 |
+-----------+
1 row in set (0.01 sec)

mysql> SELECT JSON_UNQUOTE(JSON_EXTRACT(jsonobject, "$.invoiceid")) as invoiceid FROM ordertable where JSON_UNQUOTE(JSON_EXTRACT(jsonobject, "$.invoiceid")) = '100030020';
+-----------+
| invoiceid |
+-----------+
| 100030020 |
+-----------+
1 row in set (5.22 sec)
 '''
