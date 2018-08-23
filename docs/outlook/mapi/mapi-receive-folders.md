---
title: MAPI re�oivent des dossiers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e1287a3-0f15-4d9a-b7ee-738fce9cd51f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a305b9c9ea2802ac63a22118b55274bcdff23617
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569007"
---
# <a name="mapi-receive-folders"></a>MAPI re�oivent des dossiers

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Un dossier de r�ception conserve les messages entrants d'une classe de message particulier. Recevoir le dossier associations peuvent �tre �tablies par les clients, par le fournisseur de banque de messages ou MAPI. MAPI a deux par d�faut � recevoir des dossiers : le dossier racine de la banque de messages et le dossier bo�te de r�ception de la sous-arborescence message interpersonnel (IPM). Le dossier racine de la banque de messages est le dossier pour tous les messages de communication interprocessus (IPC) de r�ception de la valeur par d�faut.
  
 Le dossier bo�te de r�ception est cr�� par MAPI pour chaque nouvelle banque de messages et agit en tant que valeur par d�faut recevoir des dossiers pour les classes de message suivants : 
  
- La classe de message IPM.
    
- La classe de message de rapport.
    
- Une classe vide ou manquante.
    
Tous les messages d'�tat, y compris ceux envoy�s en r�ponse � un message IPC, sont plac�s dans le dossier bo�te de r�ception. Les applications clientes IPC qui traitent leurs propres rapports doivent ajouter explicitement un dossier de r�ception pour la classe sp�cifique du rapport. Par exemple, si un client attend de recevoir des messages avec la classe IPC. Paper.Order, elle doit appeler la m�thode [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) pour �tablir un dossier de r�ception des rapports avec la classe Report.IPC.Paper.Order. 
  
Dossier associations sont bas�es sur la structure hi�rarchique des classes de message de r�ception. Les clients peuvent explicitement �tablir une association entre un dossier de r�ception et une classe de message ou utiliser les dossiers de r�ception par d�faut MAPI. En r�gle g�n�rale, les clients d�signer un dossier de recevoir des messages pour une classe de base et toutes ses sous-classes. Par exemple, un client typique permettrait d'�tablir une association pour les messages avec la classe **MyClass**. Si le client a re�u les messages avec les classes **MyClass.Home** ou **MyClass.Home.Kitchen.Computer**, ces messages seraient acc�dez au dossier de r�ception pour la classe de base, **MyClass**.
  
Il existe trois message m�thodes magasin que les clients utilisent pour travailler avec re�oivent des dossiers :
  
- [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)
    
- [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)
    
- [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md)
    
Le tableau de dossier de r�ception vous trouverez des informations sur tous les dossiers de r�ception �tablis pour une banque de messages. Son jeu de colonne obligatoire inclut la classe de message, la cl� d'enregistrement et identificateur d'entr�e.
  
To retrieve a receive folder for a particular message class, clients pass the message class string to the [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) method. The message store provider returns an entry identifier for the corresponding folder. To implement **GetReceiveFolder**, a message store provider should use an algorithm that selects the folder whose associated message class matches the longest possible prefix of the specified message class. For example, assume the message store has the following associations between receive folders and message classes in its receive folder table:
  
- **IPM** les messages sont plac�s dans le dossier bo�te de r�ception. 
    
- **IPM.Note.Sample** les messages sont plac�s dans le dossier Samples. 
    
Le tableau suivant montre comment les messages avec plusieurs classes doivent �tre achemin�s vers appropri�s re�oit un dossier.
  
|**Classe de message entrant**|**Dossier de r�ception**|
|:-----|:-----|
|**IPM. Note.Sample.Simple** <br/> |Dossier d'exemples  <br/> |
|**IPM.Note** <br/> |Dossier bo�te de r�ception  <br/> |
|**IPM. Feuille de présence** <br/> |Dossier bo�te de r�ception  <br/> |
|**IPM. Note.Sample.Simple.Totally** <br/> |Dossier d'exemples  <br/> |
   
Clients appellent la m�thode **SetReceiveFolder** pour �mettre une association entre une classe de message particuli�re explicite et recevoir des dossiers. Lorsqu'un message est remis � une classe de message vide, MAPI place le message dans le dossier de r�ception n'est d�fini pour un pr�fixe de la classe vide. Par exemple, si votre client dispose d'un dossier de r�ception �tabli pour les messages avec la classe **IPM** et la remise d'un message avec la classe **IPM.Note.Test**, ce message sera plac� dans le dossier de r�ception pour la classe de message **IPM**. 
  
Dans l'appel **SetReceiveFolder**, clients transmettre g�n�ralement une cha�ne de classe de message et l'identificateur d'entr�e du nouveau dossier de r�ception. Toutefois, les clients peuvent passer de NULL pour une ou deux de ces param�tres. Le tableau suivant d�crit le comportement qui se traduit � partir de la sp�cification NULL pour les param�tres d'identificateur de classe et d'entr�e de message. 
  
|**param�tre de  _SetReceiveFolder_**|**Comportement r�sultant**|
|:-----|:-----|
|Identificateur d'entr�e la valeur NULL  <br/> |La banque de messages supprime l'association entre le texte sp�cifi� de classe et de ses existants de dossier de r�ception de message. Recevoir un nouveau dossier n'est pas �tablie. <br/> Les appels ult�rieurs � **GetReceiveFolder** � cette classe de message renverra le dossier de r�ception pour un pr�fixe de la classe de message ; de nouvelles banques de message, **GetReceiveFolder** retournera la bo�te de r�ception dans la sous-arborescence IPM.  <br/> |
|Classe de message la valeur NULL  <br/> |La banque de messages modifie l'association de la classe de message vide dans le dossier indiqu�. Les messages entrants dont la classe n'est pas reconnue dans le cas contraire seront dirig�s vers ce dossier.  <br/> |
|Identificateur d'entr�e et de la classe de message la valeur NULL  <br/> |La banque de messages supprime l'association de la classe/dossier pour la classe de message vide. Vous ne devez pas d�finir les deux param�tres � la valeur NULL, car elle r�duit g�n�ralement dans les messages entrants plac�es dans le dossier racine de la banque de messages, un dossier qui est invisible dans le client.  <br/> |
   
Bien que les classes d'un message ne doivent jamais �tre vide, une classe de message vide peut se produire. Il incombe de la banque de messages pour affecter la classe de message � **IPM** pour les nouveaux messages sortants qui ont une classe vide ; Il incombe du fournisseur de transport pour affecter **IPM.Note** comme classe pour les messages entrants ayant n'importe quelle classe vide. 
  
## <a name="see-also"></a>Voir aussi



[Dossiers MAPI](mapi-folders.md)

