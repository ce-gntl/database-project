#### LOGICAL DESIGN AND IMPLEMENTATION

The first step involves restructuring the ER schema of our animal shelter. The generalization between the parent entity PERSONALE and the child entities DIPENDENTE and RICERCATORE is resolved by merging the parent entity into the child entities. The RICERCATORE and DIPENDENTE will both have the badge number as their primary key, since this differs in the two entities and is a valid unique identification code.

The generalization between the parent entity STANZA and the subset STANZA DI STABULAZIONE is resolved by replacing the generalization with a new association IT IS ONE. The entity STANZA DI STABULAZIONE is identified externally by the entity STANZA. As regards the entity DIPENDENTE and the multi-valued attribute POSIZIONE RICOPERTA, a new entity POSIZIONE RICOPERTA is considered to be created and associated with DIPENDENTE through the relationship RICOPRE.  
As regards the entity RICERCATORE and the multi-valued attribute ENTE DI RIFERIMENTO, it is considered to create a new entity ENTE DI RIFERIMENTO and associate it with RICERCATORE through the ASSOCIATO relation.

#### LOGICAL SCHEME:

Ente (Id ente, nome ente, città, indirizzo, nazione);  
Posizione ricoperta(Codice posizione, descrizione);  
Registro (Codice registro, orario di entrata, orario di uscita);  
Stanza (Numero stanza, nome stanza, descrizione);  
Stanza per la stabulazione (Numero stanza, capienza, specie animale);  
Dipendente (Codice badge, nome, cognome, cf, data di nascita, email, numero  
di telefono, posizione ricoperta, stanza);  
Ricercatore (Codice badge, nome, cognome, cf, data di nascita, email, numero  
di telefono,corso di formazione, Progetto di ricerca, ente);  
Progetto di ricerca (Codice progetto, titolo, data di approvazione, data di fine  
progetto, veterinario responsabile);  
Animale (Id animale, specie, data di arrivo, Id ceppo, nome venditore, Id  
stanza, progetto di ricerca, trattamento, data assegnazione, data fine);  
Prenota (codice\_prenotazione, codice badge, numero stanza, data  
prenotazione);  
Annota in ( Codice registro, codice badge, data entrata);  
Referente (Titolare progetto, codice progetto);