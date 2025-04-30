#Documentazione sulle funzioni
Posso scrivere la documentazione della mia funzione, ovvero la spiegazione di come funziona, usando tre virgolette singole '''. Quando poi eseguo il comando help(nomefunzione), in output avrò quello che ho scritto dentro la coppia di '''. 

#Es

def f():
	'''documentazione della funzione '''
	operazioni...
	return...
	
#Funzioni di script esterni
Importo la libreria (cioè lo script intero), oppure una funzione di questa libreria, per poterla utilizzare nel mio script. Per farlo utilizzo:
	-from nomelibreria import * (tutta)
	-from nomelibreria import nomefunnzione (solo la
	funzione che mi serve)
	
#if __name__ == "__main__"
Suppongo di aver creato uno script (script1), che utilizzerò come libreria in un altro script (script2), del tipo:

Script1 :
	
	def funzione1():
		.....
		return ...	
	
	def funzione2():
		.....
		return ...
	def funzione3():
		.....
		return ...
	
	funzione1() --> viene eseguito (è "sempre attivo")
	
#N.B: c'è un problema
Quando in script2, dopo aver importato script1 (from script1 import *), eseguirò una funzione dello script ( script1.funzione2() ), oltre alla funzione2 verrà eseguita "funzione1" che nello script1 risulta sempre "attiva". Quindi, per ogni chiamata di funzione dello Script1 verrà eseguito funzione1()


# Come si risolve?
Per risolvere questo problema baste mettere nello Script1, al posto di funzione1(), il metodo if__name__=="__main__":

Script1 :
	
	def funzione1():
		.....
		return ...	
	
	def funzione2():
		.....
		return ...
	def funzione3():
		.....
		return ...
	
	if __name__ == "__main__"
	funzione1() --> viene eseguito solo nello script1
	ma non quando uso deelle funzioni dello script1
	nello script2.


