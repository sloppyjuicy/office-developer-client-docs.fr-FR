---
title: Définition d’une position de table avec un signet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f43e3a7e3376cb437620204a29aed9fb732d3427
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564093"
---
# <a name="setting-a-table-position-with-a-bookmark"></a>Définition d’une position de table avec un signet

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Un signet est une ressource qui indique un emplacement particulier dans une table. Définition d’un signet rend possible revenir à une position à une date ultérieure, une fonctionnalité qui peut améliorer sensiblement les performances des opérations de table. MAPI définit trois signets standards : 
  
|||
|:-----|:-----|
|BOOKMARK_CURRENT  <br/> |Points à la ligne active dans un tableau.  <br/> |
|BOOKMARK_BEGINNING  <br/> |Points à la première ligne dans un tableau.  <br/> |
|BOOKMARK_END  <br/> |Points à la dernière ligne dans une table.  <br/> |
   
L’implémentation de la table est nécessaires pour prendre en charge les signets standards et peut également prendre en charge d’autres personnes. Toutefois, étant donné que les signets sont des ressources et les ressources sont limitées, les utilisateurs de signet doivent libérer les dès que possible. 
  
 **Pour définir un signet à la position actuelle de la table**
  
- Appelez [IMAPITable::CreateBookmark](imapitable-createbookmark.md). Il peut arriver que sera mémoire disponible insuffisante pour allouer le nouveau signet, entraînant **CreateBookmark** renvoyer la valeur d’erreur MAPI_E_UNABLE_TO_COMPLETE. 
    
 **Pour libérer un signet**
  
- Appelez [IMAPITable::FreeBookmark](imapitable-freebookmark.md).
    
 **Pour déplacer le curseur vers une position marquée par un signet**
  
- Appelez [IMAPITable::SeekRow](imapitable-seekrow.md). **SeekRow** établit une nouvelle valeur pour la position BOOKMARK_CURRENT. **SeekRow** peut être utilisé, par exemple, pour positionner un lignes de tableau 10 à partir de la position actuelle ou recommencer au début. Clients ou fournisseurs de services peuvent rechercher en cours, à partir de, ou fin d’une table ou toute autre position qui est associée à un signet prédéfini. Ils peuvent déplacer dans un sens avancer ou reculer et le limite l’opération à un nombre spécifié de lignes. En règle générale, les appelants doivent seek pas plus de 50 lignes avec **SeekRow**; [IMAPI::SeekRowApprox](imapitable-seekrowapprox.md) doit être utilisé avec le plus grand nombre de lignes. 
    
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

