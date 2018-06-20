---
title: Parcourir le dossier boîte de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 87fcde5a28a30f08bc2fd5f28fb692a4b4251fbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787385"
---
# <a name="traversing-the-inbox-folder"></a>Parcourir le dossier boîte de réception

  
  
**S’applique à**: Outlook 
  
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
    

