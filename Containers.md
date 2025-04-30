#		Containers
Sono, in python, l'equivalente delle strutture per C e C++.
Nei containers posso: mettere delle variabili, mettere altri containers. I containers sono anche loro dei tipi di variabili. Tipi di containers sono: 
	1. liste: ordinate, modificabili, permettono copie, gli oggetti al loro interno sono indicizzati.
	2. tuple: ordinate, NON modificabili, permettono copie, gli oggetti al loro interno sono indicizzati.
	3. set: NON ordinate, NON modificabili, non permettono copie di valori.
	4. dictionary: gli oggetti sono rappresentati tramite "parole chiave", sono ordinate secondo la "chiave" (a partire da python 3.7), non permettono duplicati di oggetti al loro interno.
	
	1] es. [1,2,3]
	2] es. (1,2,3)
	3] es. {1,2,3}
	4] es. 'parolachiave':'valore' {'a':1, 'b':2, 'c':3}

## Gestione delle variabili
Quando vene creata una nuova variabile si susseguono 3 passi: viene reato un oggetto in memoria che contiene il valore assegnato, viene creata la variabile python (se non già esistente), viene collegata la variabile al nuovo oggetto.
Le variabili son di due tipi: mutabili (liste, set, user-defined classes, dizionari), immutabili (int, float, bool, stringhe, tuple).

## Liste

Si possono creare con le parentesi[] oppure con la funzione list().
	
* list("hello") crea una lista contenente le lettere della parola "hello"
* list(range(10)) crea una lista contenente inumeri da 1 a 10
* list[i] seleziono l'elemento di posto i della lista
* l2.append(7) aggiunge 7 come ultimo elemento della lista l2
* Slicing: la logica dello slicing è list[start:stop:step]. Se volessi includere anche l'ultimo elemento, baste non mettere 'stop'. Se 'step' viene omesso, in automatico si avrà step==1
* len(lista1) restituisce la lunghezza della lista1
* list_from_range + list_from_string combina le due liste (senza spazio)
* del l1[5] elimina l'elemento di indice cinque della lista l1
* l1.remove(10) rimuove dalla lista l1 l'elemento che ha come valore 10
* l1.count(8) conta il numero degli elementi della lista l1 che hanno valore 8
* l1.index(a, b, c) riporta l'indice del primo valore 'a' che si trova dopo 'b' e prima di 'c' (ovvero nel range (b,c)) 
* l1.index(a) riposta l'indice del primo valore 'a'

#Funzioni Sort e Sorted (e sorreta)
'Sorted' restituisce una nuova lista che è la copia di quella precedente ma ordinata.
'Sort' invece, modifica direttamente la lista che gli stiamo mandando mettendola in ordine.

## Tuple
...vedi github...
# Tuple vs Liste
le tuple occupano meno memoria e sono più veloci

## Dizionari
Proprietà e regole per il buon uso:
* unordered set of pairs key:value
* elements are accessed by key and not by offset (like lists and tuples)
* le key devono essere immutabili (e.g., boolean, integer, float, tuple, string, not list)
* i dizionari sono modificabili, quindi posso aggiungere e/o eliminare e/o cambiare i loro elementi 'key:value'
* sono molto ottimizzati

Comandi utili:
	
* a = dict() crea un dizionario e lo chiama 'a'
* list(a.items()) fa una lista degli elementi (key) del dizionario 'a' con i rispettivi numeri (value) associati
* zip(a,b) la funzione "zip" prende due containers e li associa in tuple di due elementi (come se stessi facendo il prodotto cartesiano di due spazi vettoriali accoppiando il primo elemento del primo spazio con il primo elemento del secondo spazio, e cos' via). Se i due containers hanno diversa dimensione, la funzione zip si ferma alla minima dimensione fra le due.
* posso lavorare con un elemento del dizionario come faccio con le liste. In questo caso però, l'indice non sarà un numero ma la 'key'. Es. a['key1'] = 5 + 8
* a["ciao"] = 55 aggiungo al dictionary un elemento con la key = ciao e il value = 55
* print("Eggs" a) darà il valore True se la key 'Eggs' è presente nel dictionary a; altrimenti False
* del a['ciao'] elimina l'elemento che ha key 'ciao'

	
Posso costruire dei dictionaries all'interno delle liste/tuple, mettedo ('key', value) [la parola chiave va messa tra le virgolette singole]

Di default, non posso accedere ad elementi della lista che non esistono; quindi è importnate, all'interno del codice, scrivere in modo corretto le 'key' a cui si fa riferimento e, in primis, dare ad esse un nome breve ma comprensibile.

Posso creare un dictionary all'interno di un altro dictionary: es. fridge_dict = {'Yogurt': 4, 'Tofu': 2, 'Vegetables': {'celeriac': 0.5, 'onions': 2, 'cherry_tomatoes': 42}}. la categoria 'Vegetables' ha un dizionario ad essa collegato. Se volessi eliminare un elemento di solo questa categoria dovrei usare il comando:
	
* del fridge_dict['Vegetables':['celeriac']]

# Sets
Sono come i dictionaries ma senza valori (solo key) e sono disordinati. Sono usati per sapere se qualcosa esiste/è presente evitando ripetizioni. Soto ottimizzati per operazioni matematiche tra insiemi.

* Creazione: a = set()
* dati due set a e b, come negli insiemi in matematica, posso unirli col comando: c = a.union(b) creando così il set 'c' che è l'unione di a e b.
* Intersezione: d = a.intersection(b)
* differenza: e = a - b

