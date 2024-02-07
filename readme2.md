Utilizzando lo stesso database di ieri, eseguite le query in allegato. Obbligatoriamente ne dovete fare 3 per il group by e tre per le JOIN.
Caricate un secondo file nella stessa repo di ieri (db-university) con le query di oggi.


QUERY CON GROUP BY:
1. Contare quanti iscritti ci sono stati ogni anno:

    SELECT YEAR(enrolment_date) AS "anno_iscrizione", COUNT(*) AS "numero_iscritti"
    FROM `students`
    GROUP BY YEAR(enrolment_date)
    

2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio:

    SELECT `office_address`, COUNT(*) AS "numero_docenti_per_ufficio" 
    FROM `teachers`
    GROUP BY `office_address`;

3. Calcolare la media dei voti di ogni appelo d'esame:


4. Contare quanti corsi di laurea ci sono per ogni dipartimento:

    SELECT `department_id`, COUNT(*) AS "numero_corsi_laurea_per_dipartimento" 
    FROM `degrees`
    GROUP BY `department_id`;





QUERY CON JOIN:
1. Selezionare tutti gli studenti iscritti al corso di laurea di economia:

    SELECT `students`.`name`, `students`.`surname`, `students`.`date_of_birth`
    FROM `students`
    JOIN `degrees`
    ON `degrees`.`name` = "Corso di Laurea in Economia";

2. Selezionare tutti i corsi di laurea magistrale del dipartimento di neuroscienze:

    SELECT `degrees`.`name`, `degrees`.`address`, `degrees`.`email`, `degrees`.`website`
    FROM `degrees`
    JOIN `departments`
    ON `departments`.`name` = "Dipartimento di Neuroscienze"
    WHERE `degrees`.`level` = "magistrale";

3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44):

    SELECT `courses`.* 
    FROM `courses`
    INNER JOIN `course_teacher` ON `course_id` = `course_teacher`.`course_id`
    INNER JOIN `teachers` ON `course_teacher`.`teacher_id` = `teachers`.`id`
    WHERE `teachers`.`id` = 44;


4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome  nome:



5. Selezionare tutti i corsi di laurea con i relativi corsi ed insegnanti:


6. Selezionare tutti i docenti che insegnano nel dipartimento di matematica:


7. BONUS. Selezionare per ogni studente il numero di tentativi sostenuti per ogni esame, stampando anche il voto massimo. Successivamente, filtrare i tentativi con voto minimo 18.
