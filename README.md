# Databasdrop table if exists libros;

create table libros(
  codigo int unsigned auto_increment,
  titulo varchar(40) not null,
  autor varchar(30),
  editorial varchar(15),
  precio decimal(5,2) unsigned,
  primary key (codigo)
 );

insert into libros (titulo,autor,editorial,precio)
  values('El aleph','Borges','Planeta',15);
insert into libros (titulo,autor,editorial,precio)
  values('Satanas','Mario Mendoza','Planeta',50);
insert into libros (titulo,autor,editorial,precio)
  values('Antologia poetica','Borges','Planeta',40.000);
insert into libros (titulo,autor,editorial,precio)
  values('Relato de un Asesino','Mario Mendoza','Planeta',70.000);
insert into libros (titulo,autor,editorial,precio)
  values('Cervantes y el quijote','Borges','Dos Caras',36.000);
insert into libros (titulo,autor,editorial,precio)
  values('El dueño del viento', 'Patxi Irurzun Ilundain', 'Dos Caras',50);
insert into libros (titulo,autor,editorial,precio)
  values('Harry Potter y la piedra filosofal','J.K. Rowling','Dos Caras',50);
insert into libros (titulo,autor,editorial,precio)
  values('Harry Potter y la camara secreta','J.K. Rowling','Dos Caras',50.000);
insert into libros (titulo,autor,editorial,precio)
  values('Alicia en el pais de las maravillas','Lewis Carroll','Dos Caras',null);

select * from libros limit 0,4;

select * from libros limit 5,4;

select * from libros limit 8;

select * from libros limit 6,10000;

delete from libros
  order by precio
  limit 2;

insert into libros (titulo,autor,editorial,precio)
  values('El aleph','Borges','Planeta',15);

insert into libros (titulo,autor,editorial,precio)
  values('El aleph','Borges','Planeta',15);
insert into libros (titulo,autor,editorial,precio)
  values('El aleph','Borges','Planeta',15);

select * from libros
  where titulo='El aleph' and
  autor='Borges' and
  editorial='Planeta';

delete from libros
  where titulo='El aleph' and
  autor='Borges' and
  editorial='Planeta'
  limit 2;

select * from libros
  where titulo='El aleph' and
  autor='Borges' andes
