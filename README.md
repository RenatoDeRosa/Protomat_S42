# Protomat_S42
Questa repository punta a diffondere le competenze necessarie a operare macchinari della lpkf protomat, in particolare in questo documento discuteremo della protomat S42,
macchinario a controllo numerico per la prototipazione di circuiti stampati, e ai software a questo corredati, quali, CircuitCam software di CAM(Computer Aided Manufacturing) e
a Boardmaster software utilizzato per operare il macchinario.

Il macchinario inizialmente si trovava in stato di inutilizzo, a causa della non operabilità dell'asse Z rendendo il macchinario inutilizzabile, grazie alla coordinazione di vari professori
che mi hanno permesso di assentarmi durate determinate ore di lezione, ho avuto la possibilità di tentare di portare in vita il macchinario.

In questo documento ricapitolando andremo a coprire 3 punti principali
1. Funzionamento Hardware e componenti che consentono l'operabilità del macchinario, e come è stato diagnosticato il problema
2. Funzionamento e utilizzo dei software principali (BM e CircuitCam)
3. Design e Prototipazione di una scheda STM32, seguendo le linee guida del produttore

1. Struttura e Funzionamento base del macchinario
   Qui possiamo vedere come il funzionamento base della macchina sia dettato dagli switch di limite che vanno a settare i parametri di base per le assi X e Y, possiamo anche
   vedere come l'asse Z al contrario è azionata da un solenoide che ha la funzione di abbassare la struttura del mandrino, successivamente per avere un movimento ascensionale
   della struttura si utilizza un sistema composto da una molla in acciaio con trazione regolabile questo perchè c'è la possibilità di montare una telecamera che facilità
   l'utilizzo della macchina e rende possibile la realizzazione di PCB a doppio strato tramite il sistema (di cui parleremo in seguito) di buchi referenziali
![Protomat_42_Schematics_1](https://github.com/user-attachments/assets/f49a32e9-4557-433c-9969-6609ffc4387a)


