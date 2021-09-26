---
title: Extraction de données à partir de lignes de tableau
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 902aa6b0471de78a5946b5fc89cbe87c874ce404
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624334"
---
# <a name="retrieving-data-from-table-rows"></a>Extraction de données à partir de lignes de tableau

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La récupération de lignes à partir d’un tableau implique les opérations ci-après :
  
- Obtention des valeurs de propriété pour toutes les colonnes.
    
- Modification de la position actuelle.
    
L’une des colonnes requises dans la plupart des tableaux est un identificateur d’entrée ( propriété PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) qui peut être utilisé pour ouvrir l’objet qui **représente** la ligne. Cet identificateur d’entrée est généralement un identificateur d’entrée à court terme, qui ne persiste pas au-delà de la durée de vie du tableau. Toutefois, il peut s’agit d’un identificateur à long terme si le fournisseur de services qui implémente la table ne prend en charge qu’un seul type d’identificateur d’entrée.
  
Les clients et les fournisseurs de services peuvent effectuer l’un des appels suivants pour récupérer des lignes :
  
|||
|:-----|:-----|
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Extrait un nombre spécifié de lignes commençant par la ligne en cours dans une direction avant ou arrière.  <br/> |
|[HrQueryAllRows](hrqueryallrows.md) <br/> |Récupère toutes les lignes d’un tableau.  <br/> |
|[ITableData::HrQueryRow](itabledata-hrqueryrow.md) <br/> |Extrait une ligne d’un tableau en fonction de la valeur de sa colonne d’index. **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) est généralement la colonne d’index d’une table.  <br/> |
   
Lorsqu’une propriété facultative est incluse comme une des colonnes d’un tableau, certaines lignes peuvent avoir des valeurs valides pour la colonne, tandis que d’autres peuvent ne pas l’être. L’existence d’une valeur valide pour une colonne varie selon que l’objet fournissant les informations de la ligne définit la propriété. Selon l’implémentation de l’objet, une propriété inexistante peut être représentée dans la table sous la PR_NULL **(** [PidTagNull](pidtagnull-canonical-property.md)) ou une valeur arbitraire. Les utilisateurs de tables doivent faire la distinction entre les propriétés qui n’existent pas et qui ont des valeurs sans signification et qui existent et qui ont des valeurs valides. 
  
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

