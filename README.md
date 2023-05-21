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

create table Animal ( 
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
('Stanley', 1, 1, 1, 1, 1, 1),
('Cheddar', 1, 1, 1, 3, 2, 6),
('hotdoh', 1, 1, 1, 2, 3, 7),
('Xael', 2, 63, 2, 6, 1, 5),
('Yujiro',2 , 81, 1, 1, 2, 10),
('Richard', 2, 99, 2, 5, 3, 12),
('Mr. Lam', 1, 104, 1, 4, 2, ceiling(RANDOM()*10)),

('No-Name', 2, ceiling(RANDOM()*60 + 60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('No-Name', 2, ceiling(RANDOM()*60 + 60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('No-Name', 2, ceiling(RANDOM()*60 + 60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('No-Name', 2, ceiling(RANDOM()*60 + 60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('No-Name', 2, ceiling(RANDOM()*60 + 60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('No-Name', 2, ceiling(RANDOM()*60 + 60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('No-Name', 2, ceiling(RANDOM()*60 + 60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('No-Name', 2, ceiling(RANDOM()*60 + 60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('No-Name', 2, ceiling(RANDOM()*60 + 60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('No-Name', 2, ceiling(RANDOM()*60 + 60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('No-Name', 1, ceiling(RANDOM()*60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('No-Name', 1, ceiling(RANDOM()*60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('No-Name', 1, ceiling(RANDOM()*60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('No-Name', 1, ceiling(RANDOM()*60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('No-Name', 1, ceiling(RANDOM()*60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('No-Name', 1, ceiling(RANDOM()*60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('No-Name', 1, ceiling(RANDOM()*60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('No-Name', 1, ceiling(RANDOM()*60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('No-Name', 1, ceiling(RANDOM()*60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('No-Name', 1, ceiling(RANDOM()*60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),

('Pumpkin', 1, ceiling(RANDOM()*60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('Rowan', 1, ceiling(RANDOM()*60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('Riley', 1, ceiling(RANDOM()*60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('Reese', 1, ceiling(RANDOM()*60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('Kai', 1, ceiling(RANDOM()*60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('Milo', 1, ceiling(RANDOM()*60), 1, ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('Nala', 1, ceiling(RANDOM()*60), 2, ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('Felix', 1, ceiling(RANDOM()*60), 1, ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('Lucy', 1, ceiling(RANDOM()*60), 2, ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('Cleo', 1, ceiling(RANDOM()*60), 1, ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),

('Maske', 2, ceiling(RANDOM()*60 + 60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('Michael', 2, ceiling(RANDOM()*60 + 60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('Coco', 2, ceiling(RANDOM()*60 + 60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('Arbiter', 2, ceiling(RANDOM()*60 + 60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('Clam', 2, ceiling(RANDOM()*60 + 60), ceiling(RANDOM()*2), ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('Daisy', 2, 66, 2, ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('Holly', 2, ceiling(RANDOM()*60 + 60), 2, ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('Cooper', 2, ceiling(RANDOM()*60 + 60), 1, ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('Billy', 2, ceiling(RANDOM()*60 + 60), 1, ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15)),
('Preston', 2, ceiling(RANDOM()*60 + 60), 1, ceiling(RANDOM()*10), ceiling(RANDOM()*3), ceiling(RANDOM()*15))
;

## SQL-Queries 
### Filtering: Finds all of the animals in house (adoptable). Shows all available pets for adoption.
select name, Animal_Type.type, Animal_Breed.breed, Animal_Gender.gender, Animal_Personality.personality, Animal_Adoption.state, age from Animal

join Animal_Type on Animal.type_id = Animal_Type.id
join Animal_Breed on Animal.breed_id = Animal_Breed.id
join Animal_Gender on Animal.gender_id = Animal_Gender.id
join Animal_Personality on Animal.personality_id = Animal_Personality.id
join Animal_Adoption on Animal.state_id = Animal_Adoption.id

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
