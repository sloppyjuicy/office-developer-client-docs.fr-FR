---
title: Parcours du dossier boîte de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e954cb2d8029a31e7f69daaa7e8ed55a7953ac02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406555"
---
# <a name="traversing-the-inbox-folder"></a>Parcours du dossier boîte de réception

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour parcourir tous les messages de la boîte de réception**
  
1. Appelez [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) pour récupérer l'identificateur d'entrée de la boîte de réception. 
    
2. Appelez **IMAPIFolder:: OpenEntry** pour ouvrir la boîte de réception. 
    
3. Appelez la méthode [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md) de la boîte de réception pour extraire la table de contenu. 
    
4. Appelez la méthode [IMAPITable:: SetColumns](imapitable-setcolumns.md) de la table contents pour limiter la valeur de la colonne à **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) et toutes les autres colonnes requises. 
    
5. Appeler [IMAPITable:: QueryRows](imapitable-queryrows.md) pour récupérer un groupe de lignes. 
    
6. Jusqu'à ce qu'il n'y ait plus de lignes dans la table Contents:
    
1. Appelez [IMsgStore:: OpenEntry](imsgstore-openentry.md) pour ouvrir le message représenté par l'identificateur d'entrée de chaque ligne. 
    
2. AsSignez le paramètre _lppUnk_ à un pointeur d'interface **IMessage** local. 
    
3. Utiliser les propriétés du message.
    
4. ReLâchez le pointeur pointé par le paramètre _lppUnk_ . 
    
5. Appelez [IMAPITable:: QueryRows](imapitable-queryrows.md) pour extraire le groupe de lignes suivant. 
    
7. Libérez la table des matières.
    

