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
('rat'),
('bunny'),
('hampster')
;

create table Animal_Breed(
  id serial,
  breed varchar,
  primary key(id)
  );
  
 insert into Animal_Breed (breed) values
 ('male'),
 ('female')
 ;
 


## SQL-Queries 

select id, organization, budget as dollar_budget, housing as square_footage from Animal_Shelter_Name
