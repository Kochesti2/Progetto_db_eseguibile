# Progetto_db_eseguibile
Contiene solo eseguibili del progetto DataBase. Db del management del magazzino.

Gli strumenti che servono:

- JVM (versione 1.8 non dovrebbe andare bene, quindi aggiornare almeno a 9)
- Postgres SQL DataBase.

Come inizializzare:

- Creare un servrer(localhost:5432) usando PgAdmin o un altro tool per postgreSQL database management
  IMPORTANTE: - Ricordarsi credenziali dell'Admin. ES: postgres postgres
              - Ricordarsi il nome del database creato. ES: project

Come inizializzare DB:

- Lanciare db_init: java -jar db_init.jar <Nome DB> <username> <password>
                    ES: java -jar db_init.jar project postgres postgres
  usare l'interfaccia con l'opzione 1 per caricare i dati.
  Troubleshooting: Il database potrebbe non andare se si conette con JDBC per prima volta. Quindi connettersi da PgAdmin cliccando      semplicemente sul database creato in precedenza.
  
- Lanciare progetto.jar
   java -jar progetto.jar <Nome DB>
   ES: java -jar progetto.jar project
   
   credenziali: Per Admin sono quelli di postgres.
                Per gli altri utenti vedere define_users nella cartella db_init_exec
                username: codice fiscale
                Password: prime 3 lettere del codice fiscale
