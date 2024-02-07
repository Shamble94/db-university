1. Selezionare tutti gli stundenti iscritti al Corso di Laurea in Economia:

SELECT `students`.`name`, `students`.`surname`
FROM `students`
JOIN `degrees`
ON `students`.`degree_id` = `degrees`.`id`
WHERE `degrees`.`name` = "Corso di Laurea in Economia";

2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze: 

SELECT `degrees`.`name`, `degrees`.`level`, `departments`.`name`
FROM `degrees`
JOIN `departments`
ON `degrees`.`department_id` = `departments`.`id`
WHERE `degrees`.`level` = "Magistrale" and `departments`.`name` = "Dipartimento di Neuroscienze";

3. Selezionare tutti i corsi in cui insegna Fulvio amato (id=44):

SELECT *
FROM `courses`
JOIN `course_teacher`
ON `course_teacher`.`course_id` = `courses`.`id`
WHERE `course_teacher`.`teacher_id` = 44;