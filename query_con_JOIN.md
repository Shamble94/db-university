1. Selezionare tutti gli stundenti iscritti al Corso di Laurea in Economia:

SELECT `students`.`name`, `students`.`surname`
FROM `students`
JOIN `degrees`
ON `students`.`degree_id` = `degrees`.`id`
WHERE `degrees`.`name` = "Corso di Laurea in Economia";