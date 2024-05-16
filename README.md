1. Selezionare tutti gli studenti nati nel 1990 (160)
SELECT * FROM `students` WHERE YEAR(`date_of_birth`)=1990;
2. Selezionare tutti i corsi che valgono più di 10 crediti (479)
SELECT * FROM `courses` WHERE `cfu`> 10;
3. Selezionare tutti gli studenti che hanno più di 30 anni
SELECT * FROM `students` WHERE TIMESTAMPDIFF(YEAR,`date_of_birth`,CURRENT_DATE())>30;
4. Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di
laurea (286)
SELECT * FROM `courses` WHERE `period` = 'I semestre' AND `year` =1;
5. Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del
20/06/2020 (21)
SELECT * FROM `exams` WHERE `hour` > '14:00:00' AND `date` = '2020-06-20';
6. Selezionare tutti i corsi di laurea magistrale (38)
SELECT * FROM `degrees` WHERE `level` = 'magistrale';
7. Da quanti dipartimenti è composta l'università? (12)
SELECT COUNT(*) FROM `departments`;
8. Quanti sono gli insegnanti che non hanno un numero di telefono? (50)
SELECT COUNT(*) FROM `teachers` WHERE `phone`IS NULL;








1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia
SELECT * FROM `students` INNER JOIN `degrees` ON `students`.`degree_id` = `degrees`.`id` WHERE `degrees`.`name`= 'Corso di Laurea in Economia';
2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di
Neuroscienze
3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)
4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui
sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e
nome
5. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti
6. Selezionare tutti i docenti che insegnano nel Dipartimento di
Matematica (54)
