> create function sqarea1(len int)return int is
  2      area int(5,3);
  3      begin
  4      area:=(len*len);
  5      return area;
  6      end;
  7    /

Function created.

SQL> Function created
SP2-0734: unknown command beginning "Function c..." - rest of line ignored.
SQL>  begin
  2    dbms_output.Put_line('area='||sqarea1(4));
  3    end;
  4    /
area=16

PL/SQL procedure successfully completed.

SQL> DECLARE
  2  a number;
  3  b number;
  4  c number;
  5  FUNCTION findMax(x IN number,y IN number)
  6  RETURN number
  7     IS
  8         z number;
  9     BEGIN
 10        IF x > y THEN
 11           z:= x;
 12        ELSE
 13           Z:= y;
 14        END IF;
 15         RETURN z;
 16     END;
 17     BEGIN
 18        a:= 23;
 19        b:= 45;
 20         c := findMax(a, b);
 21        dbms_output.put_line(' Maximum of (23,45): ' || c);
 22     END;
 23     /
Maximum of (23,45): 45

PL/SQL procedure successfully completed.

SQL> create table customers(id int,name varchar(20),dpmt varchar(20),salary int);

Table created.

SQL> Table created.
SP2-0734: unknown command beginning "Table crea..." - rest of line ignored.
SQL> insert into customers values(1,'sam','cs',2000);

1 row created.

SQL> 1 row created.
SQL>  insert into customers values(2,'tam','it',3000);

1 row created.

SQL> 1 row created.
SQL> insert into customers values(3,'ram','ec',2500);

1 row created.

SQL> 1 row created.
SQL>  insert into customers values(4,'kam','mca',5000);

1 row created.

SQL> 1 row created.
SQL> select * from customers;

        ID NAME                 DPMT                     SALARY
---------- -------------------- -------------------- ----------
         1 sam                  cs                         2000
         2 tam                  it                         3000
         3 ram                  ec                         2500
         4 kam                  mca                        5000

SQL> CREATE OR REPLACE FUNCTION totalCustomers
  2          RETURN number IS
  3             total number(2) := 0;
  4          BEGIN
  5             SELECT count(*) into total
  6             FROM customers;
  7              RETURN total;
  8         END;
  9        /

Function created.

SQL>
SQL>   DECLARE
  2            c number(2);
  3          BEGIN
  4             c := totalCustomers();
  5             dbms_output.put_line('Total no. of Customers: ' || c);
  6          END;
  7          /
Total no. of Customers: 4

PL/SQL procedure successfully completed.
