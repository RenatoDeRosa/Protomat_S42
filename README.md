# Protomat_S42
Questa repository punta a diffondere le competenze necessarie a operare macchinari della lpkf protomat, in particolare in questo documento discuteremo della protomat S42,
macchinario a controllo numerico per la prototipazione di circuiti stampati, e ai software a questo corredati, quali, CircuitCam software di CAM(Computer Aided Manufacturing) e
a Boardmaster software utilizzato per operare il macchinario.

Il macchinario inizialmente si trovava in stato di inutilizzo, a causa della non operabilità dell'asse Z rendendo il macchinario inutilizzabile, grazie alla coordinazione di vari professori
che mi hanno permesso di assentarmi durate determinate ore di lezione, ho avuto la possibilità di tentare e di riuscire a portare in vita il macchinario.
![Protomat_S42](https://github.com/user-attachments/assets/516e50e7-f114-4863-9997-c0e784f4d568)
![Screenshot (4)](https://github.com/user-attachments/assets/d93d0a22-a2a2-467e-a408-d9e9a261da38)

## Il documento si divide in 3 punti principali
   __1. Funzionamento Hardware e componenti che consentono l'operabilità del macchinario, e come è stato diagnosticato il problema__
   
   __2. Funzionamento e utilizzo dei software principali (BM e CircuitCam)__
   
   __3. Design e Prototipazione di una scheda STM32, seguendo le linee guida del produttore__

# Struttura e Funzionamento base del macchinario
   ## Struttura testa e switch di limite
   Qui possiamo vedere come il funzionamento base della macchina sia dettato dagli switch di limite che vanno a settare i parametri di base per le assi X e Y durante l'inizzializzazione della macchina, possiamo anche
   vedere come l'asse Z al contrario delle assi X e Y è azionata da un solenoide che ha la funzione di abbassare la struttura del mandrino, successivamente per avere un movimento ascensionale
   della struttura si utilizza un sistema composto da una molla in acciaio con trazione regolabile questo perchè c'è la possibilità di montare una telecamera che facilità
   l'utilizzo della macchina e rende possibile la realizzazione di PCB a doppio strato tramite il sistema (di cui parleremo in seguito) di buchi referenziali

![Protomat_42_Schematics_1](https://github.com/user-attachments/assets/f49a32e9-4557-433c-9969-6609ffc4387a)

XXX FOTO STRUTTURA DI RITORNO TESTA xxx
   ## Struttura di movimento delle assi
   Le assi sono controllare da 2 motori passo-passo COD. C9783-9212K, che vanno a controllare i due assi ,tramite un meccanismo a vite a ricircolo di sfere(Ball Screw) e a delle guide lineari, motori passo-passo di ricambio sono disponibili a un prezzo molto contenuto (intorno ai 100 euro cad.) anche se è improbabile una problematica in questi ultimi
   ![Protomat_42_Schematics_2](https://github.com/user-attachments/assets/46ac16c5-b4ae-402b-b0fb-f9cbe28cb19c)
   
XXX FOTO STRUTTURA BALL SCREW E SERVOMOTORI XXX

## Struttura di protezione e isolamento acustico, aspiratore e telecamera
   La macchina ha vari optional tra cui 
  ### Custodia di protezione e isolamento acustico
   Una custodia che funge da protezione e da isolante acustico, abbiamo la fortuna di avere una macchina con questo tipo di optional
## Telecamera per creazione di buchi referenziali
   purtroppo per quanto riguarda  la telecamera non ne siamo in possesso
   la funzione della telecamera può essere facilmente sostituito da una telecamera generica USB e da un software come openPNP per gestire l'offset della telecamera ed averla
   perfettamente all'ineata alla punta (cosa che andremo a montare e trattare successivamente)
   
   ![fiducial camera](https://github.com/user-attachments/assets/16099803-8641-44bc-84db-1c4dcf4e1ae5)

   
## Aspiratore polveri di vetronita (Rame e Fibra di vetro mischiata a resina)
   Mentre la telecamera è facilmente sostituibile con soluzioni relativamente economiche, l'aspiratore dovendo filtrare materiale quale polveri di vetronite, materiale che può
   provocare danni alle vie respiratorie necessità di essere equipaggiato con filtri adatti al tipo di polveri che andrà a rimuovere, sembrerebbe essere sostituibile con un 
   JetStream Dust Collector by quatro, l'unità originale sembrerebbe essere un rebrand e i filtri usati appartengono a questa casa produttrice, ma qualsiasi estrattore con un
   sistema di filtraggio adeguato è adatto
  
   ![vacuum](https://github.com/user-attachments/assets/709ce684-95ca-42df-b70b-fae999fa515f)

