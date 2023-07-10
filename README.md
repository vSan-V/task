create database BANK;
use bank;
create table CUSTOMERDETIAL(Acc_no int primary key , Acc_name varchar(50) not null,pin_no int unique,pan_no varchar (8)not null unique,balance int not null,address varchar(20),acc_type varchar(20)not null) ;
create table BANKDETIAL(e_id int primary key,bank_name varchar(20),IFSC_CODE int not null,branch varchar (10) not null,Phone_no int not null,pincode int not null,e_salary int not null);
insert into bankdetial values(1,"SBI",12,"vpmalai",999999,606202,20000);
insert into bankdetial values(2,"ICIC",11,"vpmalai",899999,606202,22500);
insert into bankdetial values(3,"HDFC",13,"vpmalai",799999,606202,21000);
insert into CUSTOMERDETIAL values(12345,"Sanjai",1511,"San123",25000,"vpmlai","benificiary");
insert into CUSTOMERDETIAL values(12675,"vignesh",1212,"vicky123",250000,"metur","benificiary");
insert into CUSTOMERDETIAL values(12445,"sudan",1410,"sudanmd123",50000,"tcode","benificiary");
insert into CUSTOMERDETIAL values(1235,"vimal",1507,"vim123",250090,"japuram","Joint");
select * from customerdetial;
select * from bankdetial;
SELECT
  customerdetial.Acc_no,
  customerdetial.Acc_name,
  customerdetial.balance,
  bankdetial.bank_name,
  bankdetial.IFSC_CODE
FROM
  customerdetial
INNER JOIN
  bankdetial
ON
  customerdetial.Acc_no = bankdetial.e_id;
