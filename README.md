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

### create table Animal_Breed_Dog( 
  id serial, 
  
  dog_breed varchar, 
  
  primary key(id) 

);

insert into Animal_Breed_Dog (dog_breed) values 

('husky'), 

('shiba inu'), 

('shepherd'), 

('pomeranian'), 

('corgi') 

;

### create table Animal_Breed_Cat( 
  id serial, 
  
  cat_breed varchar, 
  
  primary key(id) 

);

insert into Animal_Breed_Cat (cat_breed) values 

('siamese'), 

('shorthair'), 

('persian'), 

('sphynx') 

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

('lazy') 

;

### create table Animal ( 
  name varchar, 
  
  type_id int,
  
  dogbreed_id int,
  
  catbreed_id int,
  
  gender_id int, 
  
  personality_id int, 
  
  age int, 
  
  constraint fk_type_id foreign key(type_id) references Animal_Type(id), 
  
  constraint fk_dogbreed_id foreign key(dogbreed_id) references Animal_Breed_dog(id),
  
  constraint fk_catbreed_id foreign key(catbreed_id) references Animal_Breed_cat(id),
  
  constraint fk_gender_id foreign key (gender_id) references Animal_Gender(id),       
 
 constraint fk_personality_id foreign key(personality_id) references Animal_Personality(id) );

insert into Animal (name, type_id, dogbreed_id, catbreed_id, gender_id, personality_id, age) values 

('Richard', 1, 1, 1, 2, 5, 12) ;

## SQL-Queries 

select id, organization, budget as dollar_budget, housing as square_footage from Animal_Shelter_Name
