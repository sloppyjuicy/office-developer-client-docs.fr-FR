---
title: Traversée du dossier Boîte de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
ms.openlocfilehash: 2e43f715e1ff03197da7aba3ca8ba9001adb0cb9
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375334"
---
# <a name="traversing-the-inbox-folder"></a>Traversée du dossier Boîte de réception

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour passer en cycle tous les messages de la boîte de réception**
  
1. [Appelez IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) pour récupérer l’identificateur d’entrée de la boîte de réception. 
    
2. **Appelez IMAPIFolder::OpenEntry** pour ouvrir la boîte de réception. 
    
3. Appelez la méthode [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) de la boîte de réception pour récupérer la table des matières. 
    
4. Appelez la méthode [IMAPITable::SetColumns](imapitable-setcolumns.md) de la table des matières pour limiter le jeu de colonnes à **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) et à toutes les autres colonnes dont vous avez besoin. 
    
5. [Appelez IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer un groupe de lignes. 
    
6. Jusqu’à ce qu’il n’y a plus de lignes dans la table des matières :
    
1. [Appelez IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir le message représenté par l’identificateur d’entrée de chaque ligne. 
    
2. Affectez  _le paramètre lppUnk_ à un **pointeur d’interface IMessage** local. 
    
3. Travaillez avec les propriétés du message.
    
4. Relâchez le pointeur pointé par  _le paramètre lppUnk_ . 
    
5. [Appelez IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer le groupe de lignes suivant. 
    
7. Relâchez la table des matières.
    

