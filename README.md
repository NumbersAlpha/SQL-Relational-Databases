# SQL-Relational-Databases
## SQL-Tables

### create table Animal_Type( 
  id serial, 
  type varchar, 
  primary key(id) 
);

insert into Animal_Type (type) values 
('dog'),
('cat')
;

### create table Animal_Breed( 
  id serial, 
  breed varchar, 
  primary key(id) 
);

insert into Animal_Breed (breed) values 
('siamese'), 
('shorthair'), 
('persian'), 
('sphynx'),
('birman'),

('Chow Chow'),
('corgi'),
('Dalmatian'),
('Dachshund'),
('shepherd'), 
 
('Abyssinian'),
('Burmese'),
('Bombay'),
('Siberian'),
('Munchkin'),

('shiba inu'), 
('Havanese'),
('Husky'),
('Maltese'),
('Pomeranian')
;

### create table Animal_Gender( 
  id serial, 
  gender varchar, 
  primary key(id) 
);

 insert into Animal_Gender (gender) values
 ('male'),
 ('female')
 ;
### create table Animal_Personality( 
  id serial, 
  personality varchar, 
  primary key(id) 
);

insert into Animal_Personality (personality) values 
('short tempered'), 
('polite'), 
('shy'), 
('anxious'), 
('joyous'), 
('lazy'),
('happy'),
('firecracker'),
('Sassy'),
('philosophical')
;

### create table Animal_Adoption(
  id serial,
  state varchar,
  primary key(id)
  );
  
 insert into Animal_Adoption (state) values
 ('adopted'),
 ('housed'),
 ('in action')
 ;

### create table Animal ( 
  name varchar, 
  type_id int,
  breed_id int,
  gender_id int, 
  personality_id int, 
  age int, 
  state_id int,
  
  
  constraint fk_type_id foreign key(type_id) references Animal_Type(id),
  constraint fk_breed_id foreign key(breed_id) references Animal_Breed(id),
  constraint fk_gender_id foreign key (gender_id) references Animal_Gender(id),       
  constraint fk_personality_id foreign key(personality_id) references Animal_Personality(id),
  constraint fk_state_id foreign key(state_id) references Animal_Adoption(id)
  );

insert into Animal (name, type_id, breed_id, gender_id, personality_id, state_id, age) values 

('Stanley', 1, 8, 1, 1, 1, 1),
('Cheddar', 1, 10, 1, 3, 2, 6),
('hotdoh', 1, 7, 1, 2, 3, 7),
('Xael', 2, 2, 2, 6, 1, 55),
('Yujiro', 2, 4, 1, 1, 2, 10),
('Richard', 2, 1, 2, 5, 1, 12)
;

## SQL-Queries 

### Basic Test
select id, organization, budget as dollar_budget, housing as square_footage from Animal_Shelter_Name

### finds all related names, breeds, genders, and personalities of Animals
select name, Animal_Breed_Dog.dog_breed, Animal_Breed_cat.cat_breed, Animal_Gender.gender, Animal_Personality.personality from Animal

join Animal_Breed_Dog on Animal.dogbreed_id = Animal_Breed_Dog.id

join Animal_Breed_Cat on Animal.catbreed_id = Animal_Breed_Cat.id

join Animal_Gender on Animal.gender_id = Animal_Gender.id

join Animal_Personality on Animal.personality_id = Animal_Personality.id

