## Classi

Serve per raggruppare variabili e funzioni, nei programmi, in modo che possano essere riutilizzabili.
Grazie alle classi posso definire le prorpietà di ciascun elemento della classe, ed assegnare ad esso degli attrubuti personali. Una classe è una "fabbrica" di oggetti. Ciascun oggetto della classe è detto "istanza". 
In python per creare una classe si usa la funzione "class".

Es. class studente:
	def _init_(self, nome, cognome, corso_di_studi):
		self.nome = nome
        	self.cognome = cognome
        	self.corso_di_studi = corso_di_studi

"self" rappresenta una referenza a ciascun oggetto creato dalla classe. Il meotdo INIT inizializza e attiva le varie proprietà di ciascun oggetto/istanza. Self è il termine utilizzato, CONVENZIONALMENTE, per rappresentare una referenza (collegamento) a ciascuna istanza della classe.
Gli attibuti con "self." (self.nome, self.cognome, ecc.) vengono detti "variabili dell'istanza".
A ciascun metodo viene passata, prima di ogni cosa, l'istanza "self"; essa restituisce la scheda personale del singolo oggetto.
Un "istanza" è un oggetto prodotto dalla classe modello, da cui prende gli attributi generici e i metodi(funzioni) associati.

# Notazione

class nomeclasse:
	def __init__(self, attributo1, attributo2, ...):
		self.attributo1 = attributo1
		...
		
	def funzione2(self):
		---faccio robbe---
		return risultato_che_voglio

#Chiamata della funzione o degli elementi
{self.attributo1} per richiamare l'attributo1 della classe nomeclasse 


