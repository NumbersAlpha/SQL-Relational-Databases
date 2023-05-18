# SQL-Relational-Databases
## SQL-Tables

create table Animal_Type(
 id serial,
 name  varchar,
 gender varchar,
 type varchar,
 age int,
 breed varchar,
 primary key(id)
);

insert into Animal_Type (name, gender, type, age, breed) values
('Charlie', 'male', 'dog', 1, 'husky')
;


create table Animal_Shelter_Name(
  id serial,
  organization varchar,
  budget int,
  housing int,
  primary key(id)
);

insert into Animal_Shelter_Name (organization, budget, housing) values
('Quackers', 123000, 5000)
;

## SQL-Queries 

select id, organization, budget as dollar_budget, housing as square_footage from Animal_Shelter_Name
