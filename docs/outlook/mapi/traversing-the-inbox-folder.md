---
title: Navigation dans le dossier de boîte de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5e93dbed0fe56ada5fc41c3e2e51aa3d0c3bef6d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594487"
---
# <a name="traversing-the-inbox-folder"></a>Navigation dans le dossier de boîte de réception

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
 **Pour passer en revue tous les messages dans la boîte de réception**
  
1. Appelez [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) pour récupérer l’identificateur d’entrée de la boîte de réception. 
    
2. Appelez **IMAPIFolder::OpenEntry** pour ouvrir la boîte de réception. 
    
3. Appelez la méthode de [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) de la boîte de réception pour récupérer la table des matières. 
    
4. Appelez le contenu [IMAPITable::SetColumns](imapitable-setcolumns.md) méthode table pour limiter la colonne valeur **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) et les autres colonnes que vous avez besoin. 
    
5. Appelez [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer un groupe de lignes. 
    
6. Jusqu'à ce qu’il ne sont plus toutes les lignes de la table des matières :
    
1. Appelez [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir le message représenté par l’identificateur d’entrée de chaque ligne. 
    
2. Affecter le paramètre _lppUnk_ à un pointeur d’interface **IMessage** local. 
    
3. Utiliser les propriétés du message.
    
4. Libérer le pointeur vers laquelle pointé le paramètre _lppUnk_ . 
    
5. Appelez [IMAPITable::QueryRows](imapitable-queryrows.md) pour extraire le groupe de lignes suivant. 
    
7. Version de la table des matières.
    

