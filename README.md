# Protomat_S42
Questa repository punta a diffondere le competenze necessarie a operare macchinari della lpkf protomat, in particolare in questo documento discuteremo della protomat S42,
macchinario a controllo numerico per la prototipazione di circuiti stampati, e ai software a questo corredati, quali, CircuitCam software di CAM(Computer Aided Manufacturing) e
a Boardmaster software utilizzato per operare il macchinario.

Il macchinario inizialmente si trovava in stato di inutilizzo, a causa della non operabilità dell'asse Z rendendo il macchinario inutilizzabile, grazie alla coordinazione di vari professori
che mi hanno permesso di assentarmi durate determinate ore di lezione, ho avuto la possibilità di tentare di portare in vita il macchinario.
![Protomat_S42](https://github.com/user-attachments/assets/516e50e7-f114-4863-9997-c0e784f4d568)

## Il documento si divide in 3 punti principali
   __1. Funzionamento Hardware e componenti che consentono l'operabilità del macchinario, e come è stato diagnosticato il problema__
   
   __2. Funzionamento e utilizzo dei software principali (BM e CircuitCam)__
   
   __3. Design e Prototipazione di una scheda STM32, seguendo le linee guida del produttore__

# Struttura e Funzionamento base del macchinario
   ## Struttura testa e switch di limite
   Qui possiamo vedere come il funzionamento base della macchina sia dettato dagli switch di limite che vanno a settare i parametri di base per le assi X e Y durante l'inizzializzazione della macchina, possiamo anche
   vedere come l'asse Z al contrario è azionata da un solenoide che ha la funzione di abbassare la struttura del mandrino, successivamente per avere un movimento ascensionale
   della struttura si utilizza un sistema composto da una molla in acciaio con trazione regolabile questo perchè c'è la possibilità di montare una telecamera che facilità
   l'utilizzo della macchina e rende possibile la realizzazione di PCB a doppio strato tramite il sistema (di cui parleremo in seguito) di buchi referenziali
![Protomat_42_Schematics_1](https://github.com/user-attachments/assets/f49a32e9-4557-433c-9969-6609ffc4387a)
XXX FOTO STRUTTURA DI RITORNO TESTA xxx
   ## Struttura di movimento delle assi
   Le assi sono controllare da 2 servomotori COD. C9783-9212K, che vanno a controllare i due assi ,tramite un meccanismo a vite a ricircolo di sfere(Ball Screw) e a delle guide lineari, servomotori di ricambio sono disponibili a un prezzo molto contenuto (intorno ai 100 euro cad.) anche se è improbabile una problematica in questi servomotori
   ![Protomat_42_Schematics_2](https://github.com/user-attachments/assets/46ac16c5-b4ae-402b-b0fb-f9cbe28cb19c)
XXX FOTO STRUTTURA BALL SCREW E SERVOMOTORI XXX

