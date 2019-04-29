---
title: Définition d'une position de table avec un signet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f0b041cecca92c0ced32631c67c72fcafdab2a16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422459"
---
# <a name="setting-a-table-position-with-a-bookmark"></a>Définition d'une position de table avec un signet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un signet est une ressource qui indique un emplacement particulier dans un tableau. La définition d'un signet permet de revenir à une position ultérieure, ce qui permet d'améliorer considérablement les performances des opérations de tableau. MAPI définit trois signets standard: 
  
|||
|:-----|:-----|
|BOOKMARK_CURRENT  <br/> |Pointe vers la ligne active dans un tableau.  <br/> |
|BOOKMARK_BEGINNING  <br/> |Pointe vers la première ligne d'un tableau.  <br/> |
|BOOKMARK_END  <br/> |Pointe vers la dernière ligne d'un tableau.  <br/> |
   
Les implémenteurs de tableau doivent prendre en charge ces signets standard et peuvent également prendre en charge d'autres. Toutefois, étant donné que les signets sont des ressources et que les ressources sont limitées, les utilisateurs de signets doivent les libérer dès que possible. 
  
 **Pour définir un signet à la position actuelle du tableau**
  
- Appeler [IMAPITable:: CreateBookmark](imapitable-createbookmark.md). Parfois, il n'y aura pas assez de mémoire disponible pour allouer le nouveau signet, provoquant l'échec de **CreateBookmark** pour renvoyer la valeur d'erreur MAPI_E_UNABLE_TO_COMPLETE. 
    
 **Pour libérer un signet**
  
- Appeler [IMAPITable:: FreeBookmark](imapitable-freebookmark.md).
    
 **Pour déplacer le curseur vers une position avec un signet**
  
- Appeler [IMAPITable:: SeekRow](imapitable-seekrow.md). **SeekRow** établit une nouvelle valeur pour la position BOOKMARK_CURRENT. La fonction **SeekRow** peut être utilisée, par exemple, pour positionner un tableau sur dix lignes à partir de la position actuelle ou au début. Les clients ou fournisseurs de services peuvent rechercher le début, le début ou la fin d'une table ou toute autre position associée à un signet prédéfini. Ils peuvent se déplacer dans une direction vers l'avant ou vers l'arrière et limiter l'opération à un nombre spécifié de lignes. En règle générale, les appelants doivent s'efforcer de ne pas dépasser 50 lignes avec **SeekRow**; [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) doit être utilisé avec un grand nombre de lignes. 
    
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

