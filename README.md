# SQL-Relational-Databases
## SQL-Tables

create table Animal_Type(
 id serial,
 type varchar,
 primary key(id)
);

insert into Animal_Type (type) values
('dog'),
('cat'),
;

create table Animal_Breed_Dog(
  id serial,
  breed_dog varchar,
  primary key(id)
  );
  
 insert into Animal_Breed_Dog (breed_dog) values
 ('husky'),
 ('shiba inu'),
 ('shepherd'),
 ('pomeranian'),
 ('corgi')
 ;
 
 create table Animal_Breed_Cat(
   id serial,
   breed_cat varchar,
   primary key(id)
   );
   
   insert into Animal_Breed_Cat (breed_cat) values
   ('siamese'),
   ('shorthair'),
   ('persian'),
   ('sphynx')
   ;
   


## SQL-Queries 

select id, organization, budget as dollar_budget, housing as square_footage from Animal_Shelter_Name
