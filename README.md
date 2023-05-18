# SQL-Relational-Databases
## SQL-Tables

create table Animal_Type(
 id serial,
 type varchar,
 breed varchar,
 primary key(id)
);

insert into Animal_Type (type, breed) values
('dog', 'husky'),
('dog', 'shiba inu'),
('dog', 'chihuahua'),
('dog', 'shepherd'),
('dog', 'pomeranian'),
('dog', 'corgi')
;


## SQL-Queries 

select id, organization, budget as dollar_budget, housing as square_footage from Animal_Shelter_Name
