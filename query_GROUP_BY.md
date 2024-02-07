1. Contare quanti iscritti ci sono stati ogni anno:

SELECT COUNT(*) AS iscritti_per_anno
FROM `students`
GROUP BY YEAR(`enrolment_date`);

2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio:

SELECT COUNT(*) AS insegnanti
FROM `teachers`
WHERE `teachers`.`office_address` = `teachers`.`office_address`
GROUP BY `teachers`.`office_address`;

3. Calcolare la media dei voti di ogni appello d'esame:

SELECT `exams`.`id`, ((SELECT SUM(vote)) / (SELECT COUNT(vote))) as media_voti
FROM `exams`
JOIN `exam_student`
ON `exam_student`.`exam_id` = `exams`.`id`
GROUP BY `exams`.`id`;