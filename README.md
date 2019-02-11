C:\Users\Notbook>cd..

C:\Users>cd..

C:\>cd xampp\mysql

C:\xampp\mysql>cd..

C:\xampp>cd..

C:\>cd xampp\mysql\bin

C:\xampp\mysql\bin>mysql -u root

MariaDB [(none)]> create database latihan2;

MariaDB [(none)]> use latihan2;

MariaDB [latihan2]> create table mahasiswa (
    -> nim varchar (11),
    -> nama varchar (20),
    -> alamat varchar (30),
    -> kota varchar (50),
    -> kode_Pos varchar (5),
    -> no_hp varchar (12),
    -> jenis_kelamin varchar (2),
    -> tgl_lahir varchar (10),
    -> kode_dosen varchar (5));

MariaDB [latihan2]> insert into mahasiswa (nim,nama,alamat,kota,kode_Pos,no_hp,jenis_kelamin,tgl_lahir,kode_dosen) values
    -> (11223344,"ari santoso","","bekasi","","","L","1998-10-12",""),
    -> (11223345,"ario talib","","cikarang","","","L","1999-11-16",""),
    -> (11223346,"dina malina","","karawang","","","P","1997-12-01",""),
    -> (11223347,"lisa ayu","","bekasi","","","p","1996-01-02",""),
    ->(11223348,"tiara wahidah","","bekasi","","","p","1980-02-05",""),
    ->(11223349,"anton sinaga","","bekasi","","","L","1988-03-10","");
 
select * from mahasiswa;

MariaDB [latihan2]> update mahasiswa set tgl_lahir='1979-08-31' where nim=11223344;

select * from mahasiswa;

MariaDB [latihan2]> delete from mahasiswa where nim=11223346;

select * from mahasiswa;

MariaDB [latihan2]> select * from mahasiswa where tgl_lahir<='1996-1-2';

MariaDB [latihan2]> select * from mahasiswa where kota='bekasi' and jenis_kelamin='P';

MariaDB [latihan2]> select * from mahasiswa where kota='bekasi' and jenis_kelamin='L' or tgl_lahir<='1997-01-02' and jenis_kelamin='P';

MariaDB [latihan2]> select nama,alamat from mahasiswa;

MariaDB [latihan2]> select * from mahasiswa
    -> order by nama asc;
