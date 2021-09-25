---
title: Définition d’une position de tableau avec un signet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5db558aa984c3a794517ec61bd04434e99efe13a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566702"
---
# <a name="setting-a-table-position-with-a-bookmark"></a>Définition d’une position de tableau avec un signet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un signet est une ressource qui indique un emplacement particulier dans une table. La définition d’un signet permet de revenir à une position ultérieurement, fonctionnalité qui peut considérablement améliorer les performances des opérations de table. MAPI définit trois signets standard : 
  
|||
|:-----|:-----|
|BOOKMARK_CURRENT  <br/> |Pointe vers la ligne actuelle d’un tableau.  <br/> |
|BOOKMARK_BEGINNING  <br/> |Pointe vers la première ligne d’un tableau.  <br/> |
|BOOKMARK_END  <br/> |Pointe vers la dernière ligne d’un tableau.  <br/> |
   
Les implémenteurs de tableau sont requis pour prendre en charge ces signets standard et peuvent également prendre en charge d’autres. Toutefois, étant donné que les signets sont des ressources et que les ressources sont limitées, les utilisateurs de signets doivent les libérer dès que possible. 
  
 **Pour définir un signet à la position actuelle du tableau**
  
- Appelez [IMAPITable::CreateBookmark](imapitable-createbookmark.md). Il peut arriver que la mémoire disponible soit  insuffisante pour allouer le nouveau signet, ce qui a pour effet de renvoyer la valeur MAPI_E_UNABLE_TO_COMPLETE’erreur. 
    
 **Pour libérer un signet**
  
- Appelez [IMAPITable::FreeBookmark](imapitable-freebookmark.md).
    
 **Pour déplacer le curseur vers une position avec signet**
  
- Appelez [IMAPITable::SeekRow](imapitable-seekrow.md). **SeekRow** établit une nouvelle valeur pour la position BOOKMARK_CURRENT position. **SeekRow** peut être utilisé, par exemple, pour positionner un tableau à dix lignes de la position actuelle ou pour recommencer au début. Les clients ou les fournisseurs de services peuvent rechercher l’état actuel, le début ou la fin d’une table, ou toute autre position associée à un signet prédéféré. Ils peuvent se déplacer vers l’avant ou l’arrière et limiter l’opération à un nombre de lignes spécifié. En règle générale, les appelants ne doivent pas rechercher plus de 50 lignes avec **SeekRow**; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) doit être utilisé avec un plus grand nombre de lignes. 
    
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

