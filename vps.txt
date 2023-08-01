drop table Invoice;
drop table Customer;
drop table Movie;
create table Movie(
mvno varchar2(5) primary key,
title varchar2(25),
type varchar2(20),
actor varchar2(20),
price number(4),
year number(4));

create Table Customer(
custid varchar2(6) primary key, 
cname varchar2(15), 
area varchar2(15), 
phone number(10), 
age number(2)
);

create table Invoice(
invno varchar2(5) primary key,
mvno varchar2(5),
custid varchar2(6),
issuedate Date,
returndate Date,
fine number(3),
foreign key (mvno) references Movie(mvno) on delete cascade,
foreign key (custid) references customer(custid ) on delete cascade);


insert into Movie(mvno, title, type, actor, price, year) values('M0100','Welcome','Comedy','Akshay Kumar',350,2007);

insert into Movie(mvno, title, type, actor, price, year) values('M0045','Dhoom 3','Action','Amir Khan',500,2013);

insert into Movie(mvno, title, type, actor, price, year) values('M0002','The Martian','Sci Fi','Matt Damon',1000,2016);

insert into Movie(mvno, title, type, actor, price, year) values('M0072','Kung Fu Panda','Animated','Jack Black',398,2008);

insert into Movie(mvno, title, type, actor, price, year) values('M0132','Raja Hindusthani','Romance','Amir Khan',220,1996);

insert into Movie(mvno, title, type, actor, price, year) values('M0087','Chak De India','Sports Drama','Shah Rukh Khan',411,2007);

insert into Movie(mvno, title, type, actor, price, year) values('M0022','The Theory ','Biographical Drama','Eddie Redmayne',732,2014);

insert into Movie(mvno, title, type, actor, price, year) values('M0041','Special 26','Thriller','Akshay Kumar',480,2013);

insert into Movie(mvno, title, type, actor, price, year) values('M0112','A Beautiful Mind','Biographical Drama','Russel Crowe',515,2001);

insert into Movie(mvno, title, type, actor, price, year) values('M0050','Interstellar','Sci Fi','Matthew McConaughey',800,2014);


select *from Movie;


insert into Customer(custid,cname,area,phone,age) values('C0027','P. Sinha','Ajoynagar',9436745122,41);

insert into Customer(custid,cname,area,phone,age) values('C0052','R. Basak','Kalikapur',9834361275,17);

insert into Customer(custid,cname,area,phone,age) values('C0072','M. Sengupta','Behala',9231742893,36);

insert into Customer(custid,cname,area,phone,age) values('C0086','S. Banerjee','Dum Dum',9432632737,22);

insert into Customer(custid,cname,area,phone,age) values('C0031','A. Dasgupta','Jadavpur',7436548262,51);

insert into Customer(custid,cname,area,phone,age) values('C0107','c. Dey','Kasba',9764374952,33);

insert into Customer(custid,cname,area,phone,age) values('C0087','S. Chowdhury','Park Street',9836457241,37);

insert into Customer(custid,cname,area,phone,age) values('C0009','R. Kapoor','Howrah',9237752263,19);

insert into Customer(custid,cname,area,phone,age) values('C0012','K. Verma','Salt Lake',9437710200,44);

insert into Customer(custid,cname,area,phone,age) values('C0044','T. Paul','Park Circus',9036745211,25);

select *from Customer;

insert into Invoice(invno,mvno,custid,issuedate,returndate,fine) values('I0002','M0045','C0012','28-APR-2015','03-MAY-2015',0);

insert into Invoice(invno,mvno,custid,issuedate,returndate,fine) values('I0043','M0087','C0086','15-MAR-2012','22-MAR-2012',100);

insert into Invoice(invno,mvno,custid,issuedate,returndate,fine) values('I0078','M0050','C0044','18-JUN-2014','26-JUN-2014',0);

insert into Invoice(invno,mvno,custid,issuedate,returndate,fine) values('I0033','M0022','C0009','02-JAN-2015','10-JAN-2015',100);

insert into Invoice(invno,mvno,custid,issuedate,returndate,fine) values('I0021','M0112','C0044','16-FEB-2013','25-FEB-2013',100);

insert into Invoice(invno,mvno,custid,issuedate,returndate,fine) values('I0062','M0132','C0087','21-JUN-2011','01-MAR-2011',50);

insert into Invoice(invno,mvno,custid,issuedate,returndate,fine) values('I0011','M0022','C0027','15-DEC-2014','22-DEC-2014',0);

insert into Invoice(invno,mvno,custid,issuedate,returndate,fine) values('I0059','M0041','C0086','15-JUN-2014','29-JUN-2014',50);

insert into Invoice(invno,mvno,custid,issuedate,returndate,fine) values('I0006','M0112','C0031','19-MAY-2012','26-MAY-2012',100);

insert into Invoice(invno,mvno,custid,issuedate,returndate,fine) values('I0042','M0002','C0044','02-FEB-2016','09-FEB-2016',0);

select *from Invoice;




