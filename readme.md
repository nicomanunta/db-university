Esercizio di oggi: DB UNiversity
nome repo: db-university
Dopo aver creato un nuovo database nel vostro phpMyAdmin e aver importato lo schema allegato (non dovete scompattare il file zip, semplicemente andate nella sezione importa, e fate drag and drop oppure prendetelo dai file delle vostre cartelle, esattamente come visto a lezione), eseguite le query del file allegato.
Cosa consegnare?
Dopo aver testato le vostre query con phpMyAdmin, riportatele in un file txt, md o altro e caricatelo nella vostra repo.
BONUS:
Selezionare nome, descrizione e periodo di tutti i corsi che hanno sito web diverso da null, cfu compresi tra 9 e 12 e che sono del primo anno ed ordinarli in ordine decrescente
P.S. Ad ogni query fatta corrisponde un push.


1. Selezionare tutti gli studenti nati nel 1990:

    SELECT *
    FROM `students`
    WHERE YEAR(date_of_birth) =  1990;

2. Selezionare tutti i corsi che valgono più di 10 crediti:

3. Selezionare tutti gli studenti che hanno più di 30 anni:

4. Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di laurea:

5. Selezionare tutti gli appelli di esame che avvengono nel pomeriggio (dopo le 14) del 20/06/2020:

6. Selezionare tutti i corsi di laurea magistrale: 

7. Da quanti dipartimenti è composta l'università:

8. Quanti sono gli insegnanti che non hanno un numero di telefono:


