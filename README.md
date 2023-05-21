# SQL-Relational-Databases
## SQL-Tables

create table Animal_Type( 
  id serial, 
  type varchar, 
  primary key(id) 
);

insert into Animal_Type (type) values 
('cat'),
('dog')
;

create table Animal_Breed( 
  id serial, 
  breed varchar, 
  primary key(id) 
);

insert into Animal_Breed (breed) values 
('Abyssinian'),
('Aegean'),
('American Bobtail'),
('American Curl'),
('American Shorthair'),
('American Wirehair'),
('Aphrodite Giant'),
('Arabian Mau'),
('Ashera'),
('Asian Longhair'),
('Asian Shorthair'),
('Australian Mist'),
('Aztec'),
('Balinese'),
('Balinese Modern'),
('Bambino'),
('Bengal'),
('Birman'),
('Bombay'),
('Bramble'),
('Brazilian Shorthair'),
('British Longhair'),
('British Shorthair'),
('Burmese'),
('Burmilla'),
('Chartreux'),
('Chausie'),
('Cornish Rex'),
('Cyprus'),
('Devon Rex'),
('Domestic Long Hair'),
('Domestic Shorthair'),
('Dragon Li'),
('Egyptian Mau'),
('Exotic'),
('Himalayan'),
('Javanese'),
('Korat'),
('LaPerm'),
('Lykoi'),
('Maine Coon'),
('Manx'),
('Minskin'),
('Norwegian Forest Cat'),
('Ocicat'),
('Oriental Longhair'),
('Oriental Shorthair'),
('Persian Modern'),
('Persian Traditional'),
('Ragamuffin'),
('Ragdoll'),
('Russian Blue'),
('Scottish Fold'),
('Selkirk Rex'),
('Siamese'),
('Siamese Modern'),
('Siberian'),
('Singapura'),
('Snowshoe'),
('Sphynx'),
('Tonkinese'),

('Affenpinscher'),
('Akita'),
('Alaskan Klee Kai'),
('Bassugg'),
('Bavarian Mountain Hound'),
('Beagle'),
('Bracco Italiano'),
('Bugg'),
('Cairn Terrier'),
('Cheagle'),
('Chesapeake Bay Retriever'),
('Cirneco Dell"Etna'),
('Curly Coated Retriever'),
('Dachshund'),
('Dalmatian'),
('Doxiepoo'),
('Dutch Shepherd'),
('English Bulldog'),
('French Bulldog'),
('Frug'),
('Giant Schnauzer'),
('Glen Of Imaal Terrier'),
('Goberian'),
('Golden Retriever'),
('Hamiltonstovare'),
('Havanese'),
('Horgi'),
('Ibizan Hound'),
('Italian Spinone'),
('Jackahuahua'),
('Johnson American Bulldog'),
('Jug'),
('Keeshond'),
('King Charles Spaniel'),
('Korean Jindo'),
('Labradoodle'),
('Löwchen'),
('Lurcher'),
('Mal-Shi'),
('Maltese'),
('Nova Scotia Duck Tolling Retriever'),
('Otterhound'),
('Papillon'),
('Petit Basset Griffon Vendeen'),
('Picardy Sheepdog'),
('Pugzu'),
('Rat Terrier'),
('Rough Collie'),
('Schipperke'),
('Shar Pei'),
('Swedish Lapphund'),
('Tibetan Mastiff'),
('Treeing Walker Coonhound'),
('Turkish Kangal Dog'),
('Weimaraner'),
('Welsh Springer Spaniel'),
('Welsh Terrier'),
('West Highland White Terrier'),
('Yorkie Russell'),
('Yorkshire Terrier'),
('Zuchon')
;

create table Animal_Gender( 
  id serial, 
  gender varchar, 
  primary key(id) 
);

 insert into Animal_Gender (gender) values
 ('male'),
 ('female')
 ;
create table Animal_Personality( 
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

create table Animal_Adoption(
  id serial,
  state varchar,
  primary key(id)
  );
  
 insert into Animal_Adoption (state) values
 ('adopted'),
 ('housed'),
 ('in action')
 ;
 
 create table Company_BASE (
  id serial,
  org_name varchar,
  org_space int,
  org_funds int,
  primary key(id)
  );
  
  insert into Company_BASE (org_name, org_space, org_funds) values
  ('Quackers', 10000, 2450000),
  ('Simply Shelters', 14500, 3240000),
  ('Bones on Bones', 20000, 5125000)
  ;

create table AnimalORG_one ( 
  id serial,
  name varchar,
  org_id int,
  type_id int,
  breed_id int,
  gender_id int, 
  personality_id int, 
  age int, 
  state_id int,
  primary key(id),
  
  constraint fk_org_id foreign key(org_id) references Company_BASE(id),
  constraint fk_type_id foreign key(type_id) references Animal_Type(id),
  constraint fk_breed_id foreign key(breed_id) references Animal_Breed(id),
  constraint fk_gender_id foreign key (gender_id) references Animal_Gender(id),       
  constraint fk_personality_id foreign key(personality_id) references Animal_Personality(id),
  constraint fk_state_id foreign key(state_id) references Animal_Adoption(id)
  );


insert into AnimalORG_one (name, org_id, type_id, breed_id, gender_id, personality_id, state_id, age) values 
('Stanley', 1, 1, 1, 1, 1, 1, 1),
('Cheddar', 1, 1, 1, 1, 3, 2, 6),
('hotdoh', 1, 1, 1, 1, 2, 2, 7),
('Xael', 1, 2, 63, 2, 6, 1, 5),
('Yujiro', 1, 2, 81, 1, 1, 2, 10),
('Richard', 1, 2, 99, 2, 5, 2, 12),
('Mr. Lam', 1, 1, 104, 1, 4, 2, ceiling(RANDOM()*10)),

('Pumpkin', 1, 1, ceiling(RANDOM()*60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*2), ceiling(RANDOM()*15)),
('Rowan', 1, 1, ceiling(RANDOM()*60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*2), ceiling(RANDOM()*15)),
('Riley', 1, 1, ceiling(RANDOM()*60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*2), ceiling(RANDOM()*15)),
('Reese', 1, 1, ceiling(RANDOM()*60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*2), ceiling(RANDOM()*15)),
('Kai', 1, 1, ceiling(RANDOM()*60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*2), ceiling(RANDOM()*15)),
('Milo', 1, 1, ceiling(RANDOM()*60), 1, ceiling(RANDOM()*10), ceiling(RANDOM()*2), ceiling(RANDOM()*15)),
('Nala', 1, 1, ceiling(RANDOM()*60), 2, ceiling(RANDOM()*10), ceiling(RANDOM()*2), ceiling(RANDOM()*15)),
('Felix', 1, 1, ceiling(RANDOM()*60), 1, ceiling(RANDOM()*10), ceiling(RANDOM()*2), ceiling(RANDOM()*15)),
('Lucy', 1, 1, ceiling(RANDOM()*60), 2, ceiling(RANDOM()*10), ceiling(RANDOM()*2), ceiling(RANDOM()*15)),
('Cleo', 1, 1, ceiling(RANDOM()*60), 1, ceiling(RANDOM()*10), ceiling(RANDOM()*2), ceiling(RANDOM()*15)),

('Maske', 1, 2, ceiling(RANDOM()*60 + 60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*2), ceiling(RANDOM()*15)),
('Michael', 1, 2, ceiling(RANDOM()*60 + 60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*2), ceiling(RANDOM()*15)),
('Coco', 1, 2, ceiling(RANDOM()*60 + 60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*2), ceiling(RANDOM()*15)),
('Arbiter', 1, 2, ceiling(RANDOM()*60 + 60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*2), ceiling(RANDOM()*15)),
('Clam', 1, 2, ceiling(RANDOM()*60 + 60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*2), ceiling(RANDOM()*15)),
('Daisy', 1, 2, 66, 2, ceiling(RANDOM()*10), ceiling(RANDOM()*2), ceiling(RANDOM()*15)),
('Holly', 1, 2, ceiling(RANDOM()*60 + 60), 2, ceiling(RANDOM()*10), ceiling(RANDOM()*2), ceiling(RANDOM()*15)),
('Cooper', 1, 2, ceiling(RANDOM()*60 + 60), 1, ceiling(RANDOM()*10), ceiling(RANDOM()*2), ceiling(RANDOM()*15)),
('Billy', 1, 2, ceiling(RANDOM()*60 + 60), 1, ceiling(RANDOM()*10), ceiling(RANDOM()*2), ceiling(RANDOM()*15)),
('Preston', 1, 2, ceiling(RANDOM()*60 + 60), 1, ceiling(RANDOM()*10), ceiling(RANDOM()*2), ceiling(RANDOM()*15))
;

## SQL-Queries 
### Filtering: Finds all of the animals in house (adoptable). Shows all available pets for adoption.
select name, Company_BASE.org_name, Animal_Type.type, Animal_Breed.breed, Animal_Gender.gender, Animal_Personality.personality, Animal_Adoption.state, age from AnimalORG_one

join Company_BASE on AnimalORG_one.org_id = Company_BASE.id
join Animal_Type on AnimalORG_one.type_id = Animal_Type.id
join Animal_Breed on AnimalORG_one.breed_id = Animal_Breed.id
join Animal_Gender on AnimalORG_one.gender_id = Animal_Gender.id
join Animal_Personality on AnimalORG_one.personality_id = Animal_Personality.id
join Animal_Adoption on AnimalORG_one.state_id = Animal_Adoption.id

where Animal_Adoption.state = 'housed'

### Sorting: Orders all the adoptable animals from youngest to oldest. If you want a younger pet.
select name, Animal_Type.type, Animal_Breed.breed, Animal_Gender.gender, Animal_Personality.personality, Animal_Adoption.state, age from Animal

join Animal_Type on Animal.type_id = Animal_Type.id
join Animal_Breed on Animal.breed_id = Animal_Breed.id
join Animal_Gender on Animal.gender_id = Animal_Gender.id
join Animal_Personality on Animal.personality_id = Animal_Personality.id
join Animal_Adoption on Animal.state_id = Animal_Adoption.id

where Animal_Adoption.state = 'housed'
order by age

### Aggregation + Grouping: Finds the average age of a female / male cat and dog. If you get influenced by other people.

select Animal_Type.type, Animal_Gender.gender, count(*), Animal_Adoption.state, avg(age) from Animal

join Animal_Type on Animal.type_id = Animal_Type.id
join Animal_Gender on Animal.gender_id = Animal_Gender.id
join Animal_Adoption on Animal.state_id = Animal_Adoption.id

where state = 'housed'

group by Animal_type.type, Animal_Gender.gender, Animal_Adoption.state

### Percentage of housed animals

select Animal_Type.type, Animal_Gender.gender, 

((sum(Animal.state_id) - count(*))*100/count(*)) as Housed_Percentage

from Animal

join Animal_Gender on Animal.gender_id = Animal_Gender.id
join Animal_Type on Animal.type_id = Animal_Type.id


group by  Animal_Gender.gender, Animal_Type.type

### Percentage of adopted animals

select Animal_Type.type, Animal_Gender.gender, 

abs(((sum(Animal.state_id) - count(*))*100/count(*))-100) as Adoption_Percentage

from Animal

join Animal_Gender on Animal.gender_id = Animal_Gender.id
join Animal_Type on Animal.type_id = Animal_Type.id


group by  Animal_Gender.gender, Animal_Type.type
