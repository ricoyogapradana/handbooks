# Handbook's SQL Command!

Penggunaan cli sangat direkomendasikan dibandingkan menggunakan phpmyadmin, karena dapat meminimalisir percobaan masuk kedalam database melalui web.

---

**DATABASE**

Melihat database yang ada dalam server

    show databases;

Membuat database

    create database nama_database;

Masuk kedalam database

    use nama_database;

---

**Create User**

    CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'password';

Berikut adalah daftar singkat dari kemungkinan izin umum lainnya yang dapat dinikmati pengguna.

    GRANT ALL PRIVILEGES ON * . * TO 'newuser'@'localhost';

> ALL PRIVILEGES- seperti yang kita lihat sebelumnya, ini akan
> memungkinkan pengguna MySQL akses penuh ke database yang ditunjuk
> (atau jika tidak ada database yang dipilih, akses global di seluruh
> sistem)
>
> CREATE- memungkinkan mereka untuk membuat tabel atau database baru
>
> DROP- memungkinkan mereka untuk menghapus tabel atau database
>
> DELETE- memungkinkan mereka untuk menghapus baris dari tabel
>
> INSERT- memungkinkan mereka untuk memasukkan baris ke dalam tabel
>
> SELECT- memungkinkan mereka untuk menggunakan perintah SELECT untuk
> membaca database
>
> UPDATE- izinkan mereka memperbarui baris tabel
>
> GRANT OPTION- memungkinkan mereka untuk memberikan atau menghapus hak
> istimewa pengguna lain

    FLUSH PRIVILEGES;

---

**TABLE**

Membuat table

    CREATE TABLE table_name (column_name column_type(length) attribute_type);

Insert data Ke table pada database

    INSERT into table_name (column_name, column_name ) value ('data','data');

Melihat isi data pada kolim

    SELECT * from table_name; //mengambil semua data yang ada pada table
    SELECT * from table_name WHERE column_name = value; //mengambil isi table berdasarkan column_name dan value atau isi.

Menambah kolom pada table

    ALTER TABLE table_name ADD column_name char(12); //menambah kolom pada kolom akhir
    ALTER TABLE table_name ADD column_name CHAR (12) FIRST; //menambah kolom pada kolom awal
    ALTER TABLE table_name ADD column_name CHAR (12) AFTER column_name; //menambah kolom setelah kolom yang telah diset

Merubah tipe data pada table

    alter table table_name MODIFY column_name VARCHAR(10);

Menghapus kolom pada table

    alter table table_name DROP column column_name;

Mengubah nama kolom

    alter table table_name CHANGE column_name_old column_name_new VARCHAR (60);

Memindahkan posisi kolom

    alter table table_name MODIFY COLUMN column_name_old VARCHAR (60) AFTER column_name;

Update data

    UPDATE table_name SET column_name ='dataupdate' WHERE coloum_name_pk='data';

Delete table

    DELETE from table_name where column_name ='value';

---

**Import & Export**

Export database

    mysqldump -u NAMAUSER -p NAMADATABASE > dbexport.sql

Import database

    mysql -u NAMAUSER -p NAMADATABASE < dbexport.sql

referensi :

[https://www.tutorialspoint.com/mysql/mysql-create-tables.htm](https://www.blogger.com/blog/post/edit/6043742386678456086/8460083480081098394?hl=en#)

[https://www.digitalocean.com/community/tutorials/how-to-create-a-new-user-and-grant-permissions-in-mysql](https://www.blogger.com/blog/post/edit/6043742386678456086/3529120736751043949?hl=en#)

Materi 5 (Manipulasi Data) - [SRI SUMARLINDA](https://www.blogger.com/blog/post/edit/6043742386678456086/8460083480081098394?hl=en#) (dosen UDB)
