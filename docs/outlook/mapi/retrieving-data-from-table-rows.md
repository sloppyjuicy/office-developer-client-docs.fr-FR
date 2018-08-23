---
title: Récupération de données à partir des lignes d’un tableau
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7b8690871dbe5b7234645f00cabab9c65706141e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573445"
---
# <a name="retrieving-data-from-table-rows"></a>Récupération de données à partir des lignes d’un tableau

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Récupérer des lignes d’une table implique :
  
- Obtention de valeurs de propriété pour toutes les colonnes.
    
- Modification de la position actuelle.
    
Une des colonnes dans la plupart des tables requis est un identificateur d’entrée, la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) — qui peut être utilisé pour ouvrir l’objet qui représente la ligne. Cet identificateur d’entrée est généralement un identificateur d’entrée à court terme, qui ne conserve pas au-delà de la durée de vie de la table. Toutefois, il peut être un identificateur à long terme si l’implémentation de la table uniquement le fournisseur de services prend en charge un seul type d’identificateur d’entrée.
  
Clients et fournisseurs de services peut-il un des appels pour récupérer des lignes suivantes :
  
|||
|:-----|:-----|
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Récupère un nombre spécifié de lignes en commençant par la ligne active dans une direction avancer ou reculer.  <br/> |
|[HrQueryAllRows](hrqueryallrows.md) <br/> |Récupère toutes les lignes d’un tableau.  <br/> |
|[ITableData::HrQueryRow](itabledata-hrqueryrow.md) <br/> |Récupère une ligne dans une table en fonction de la valeur de sa colonne d’index. **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) est généralement la colonne d’index pour une table.  <br/> |
   
Lorsqu’une propriété facultative est incluse en tant qu’une des colonnes dans une table, certaines lignes peut-être les valeurs valides pour la colonne alors que d’autres personnes risque de ne pas. Existence d’une valeur valide pour une colonne dépend de si l’objet qui fournit les informations de la ligne définit la propriété. En fonction de l’implémentation de l’objet, une propriété inexistante peut être représentée dans la table en tant que **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) ou une valeur arbitraire. Les utilisateurs de tableaux doivent être prudent de faire la distinction entre les propriétés qui n’existent pas et ont des valeurs sans signification et des propriétés qui existent et ont des valeurs valides. 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

