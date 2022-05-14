# SQL
pl/sql
BASIC
Set serveroutput on;
begin
     dbms_output.put_line('Hello world');
end;
-------------------------------------------------------------------------------------------------------------------
IF ELSE
set serveroutput on;
declare
    n int:=&n;// IN SYSTEM WE DON'T USE '&' INSTEAD WE USE ':'
begin
    if mod(n,2)=0 then
           dbms_output.put_line('given number is even');
    else
          dbms_output.put_line('Given number is odd');
    end if;
end;
-------------------------------------------------------------------------------------------------------------------
IF ELSE LADDER
set serveroutput on;
declare
    n int:=&n;
    n1 int:=&n1;
    n2 int:=&n2;
begin
    if n>n1 and n>n2 then
           dbms_output.put_line('n is greater');
    elsif n1>n and n1>n2 then
          dbms_output.put_line('n1 is greater');
    else
          dbms_output.put_line('n2 is greater');
    end if;
end;
------------------------------------------------------------------------------------------------------------------
BASIC LOOP
set serveroutput on;
declare
    n int:=&n;
    i int:=1;
    s int:=0;
begin
    loop 
        if i=n then
            s:=s+i;
            exit;
        end if;
        s:=s+i;
        i:=i+1;
   end loop;
   dbms_output.put_line('sum of  '||n||' natural numers  is '||s);
end;
-----------------------------------------------------------------------------------------------------------------------
FOR LOOP
set serveroutput on;
declare
    n int:=&n;
    s int:=0;
begin
    for i in 1..n
    loop
       s:=s+i;
    end loop;
   dbms_output.put_line('sum of  '||n||' natural numers  is '||s);
end;
------------------------------------------------------------------------------------------------------------------------
WHILE LOOP
set serveroutput on;
declare
    n int:=&n;
    s int:=0;
    i int:=1;
begin
    while i<=n
    loop
       s:=s+i;
       i:=i+1;
    end loop;
   dbms_output.put_line('sum of  '||n||' natural numers  is '||s);
end;
----------------------------------------------------------------------------------------------------------------------------
MULTIPLICATION TABLE USING BASIC LOOP
set serveroutput on;
declare
    n int:=&n;
    s int:=0;
    i int:=1;
begin
    loop
         s:=(n*i);
         dbms_output.put_line(n||'*'||i||'='||s);
         exit when i=10;
         i:=i+1;
   end loop;
end;
----------------------------------------------------------------------------------------------------------------------------------\
MULTIPLICATION TABLE USING FOR LOOP
set serveroutput on;
declare
    n int:=&n;
    s int:=0;
begin
    for i in 1..10
    loop
         s:=(n*i);
         dbms_output.put_line(n||'*'||i||'='||s);
   end loop;
end;
