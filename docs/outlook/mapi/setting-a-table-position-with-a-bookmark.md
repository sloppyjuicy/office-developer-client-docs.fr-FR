---
title: Définition d’une position de tableau avec un signet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: La définition d’un signet permet de revenir à une position ultérieurement, fonctionnalité qui peut considérablement améliorer les performances des opérations de table.
ms.openlocfilehash: e0b148abc382490064afabfe9d82573e6a26834b
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64454543"
---
# <a name="setting-a-table-position-with-a-bookmark"></a>Définition d’une position de tableau avec un signet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un signet est une ressource qui indique un emplacement particulier dans une table. La définition d’un signet permet de revenir à une position ultérieurement, fonctionnalité qui peut considérablement améliorer les performances des opérations de table. MAPI définit trois signets standard : 
  
|Propriété |Valeur |
|:-----|:-----|
|BOOKMARK_CURRENT  <br/> |Pointe vers la ligne actuelle d’un tableau. |
|BOOKMARK_BEGINNING  <br/> |Pointe vers la première ligne d’un tableau. |
|BOOKMARK_END  <br/> |Pointe vers la dernière ligne d’un tableau. |
   
Les implémenteurs de tableau sont requis pour prendre en charge ces signets standard et peuvent également prendre en charge d’autres. Toutefois, étant donné que les signets sont des ressources et que les ressources sont limitées, les utilisateurs de signets doivent les libérer dès que possible. 
  
 **Pour définir un signet à la position actuelle du tableau**
  
- [Appelez IMAPITable::CreateBookmark](imapitable-createbookmark.md). Parfois, la mémoire disponible pour allouer le nouveau signet est insuffisante, ce qui entraîne le retour de la valeur d’erreur MAPI_E_UNABLE_TO_COMPLETE **CreateBookmark** . 
    
 **Pour libérer un signet**
  
- [Appelez IMAPITable::FreeBookmark](imapitable-freebookmark.md).
    
 **Pour déplacer le curseur vers une position avec signet**
  
- [Appelez IMAPITable::SeekRow](imapitable-seekrow.md). **SeekRow** établit une nouvelle valeur pour la position BOOKMARK_CURRENT position. **SeekRow** peut être utilisé, par exemple, pour positionner un tableau à dix lignes de la position actuelle ou pour recommencer au début. Les clients ou les fournisseurs de services peuvent rechercher l’état actuel, le début ou la fin d’une table, ou toute autre position associée à un signet prédéféré. Ils peuvent se déplacer vers l’avant ou l’arrière et limiter l’opération à un nombre de lignes spécifié. En règle générale, les appelants ne doivent pas rechercher plus de 50 lignes avec **SeekRow** . [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) doit être utilisé avec un plus grand nombre de lignes. 
    
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

