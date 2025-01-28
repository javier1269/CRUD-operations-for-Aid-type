CREATE TABLE aid_types (
    aid_type_id SERIAL PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    description TEXT
);

INSERT INTO aid_types (aid_type_id, name, description) 
VALUES ('1','Food', 'Basic food supplies including rice, flour, and canned goods.');

SELECT * FROM aid_types;
UPDATE aid_types 
SET description = 'Essential food supplies for survival.' 
WHERE aid_type_id = 1;

DELETE FROM aid_types WHERE aid_type_id = 1;

SELECT * FROM public.aid_types
ORDER BY aid_type_id ASC 
