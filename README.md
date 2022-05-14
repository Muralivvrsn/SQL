# SQL
pl/sql
Set serveroutput on;
begin
     dbms_output.put_line('Hello world');
end;
-------------------------------------------------------------------------------------------------------------------
set serveroutput on;
declare
    n int:=&n;
begin
    if mod(n,2)=0 then
           dbms_output.put_line('given number is even');
    else
          dbms_output.put_line('Given number is odd');
    end if;
end;
-------------------------------------------------------------------------------------------------------------------
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

