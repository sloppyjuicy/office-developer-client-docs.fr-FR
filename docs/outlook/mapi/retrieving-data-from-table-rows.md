---
title: Récupération de données à partir de lignes de table
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2f389d26ec80b9af3ed28c5eb85b589c9cbb26c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328657"
---
# <a name="retrieving-data-from-table-rows"></a>Récupération de données à partir de lignes de table

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'extraction de lignes d'une table implique les opérations suivantes:
  
- Obtention des valeurs de propriété pour toutes les colonnes.
    
- Modification de la position actuelle.
    
L'une des colonnes obligatoires dans la plupart des tables est un identificateur d'entrée, la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), qui peut être utilisée pour ouvrir l'objet qui représente la ligne. Cet identificateur d'entrée est généralement un identificateur d'entrée à court terme, un identifiant qui ne persiste pas au-delà de la durée de vie de la table. Toutefois, il peut s'agir d'un identificateur à long terme si le fournisseur de services implémentant la table ne prend en charge qu'un seul type d'identificateur d'entrée.
  
Les clients et fournisseurs de services peuvent effectuer l'un des appels suivants pour récupérer des lignes:
  
|||
|:-----|:-----|
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Récupère un nombre spécifié de lignes en commençant par la ligne active dans une direction vers l'avant ou vers l'arrière.  <br/> |
|[HrQueryAllRows](hrqueryallrows.md) <br/> |Récupère toutes les lignes d'un tableau.  <br/> |
|[ITableData::HrQueryRow](itabledata-hrqueryrow.md) <br/> |Récupère une ligne dans un tableau en fonction de la valeur de sa colonne d'index. **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) est généralement la colonne d'index d'un tableau.  <br/> |
   
Lorsqu'une propriété facultative est incluse dans l'une des colonnes d'un tableau, certaines lignes peuvent avoir des valeurs valides pour la colonne tandis que d'autres ne le peuvent pas. L'existence d'une valeur valide pour une colonne varie selon que l'objet qui fournit les informations sur la ligne définit la propriété. En fonction de l'implémentation de l'objet, une propriété qui n'existe pas peut être représentée dans le tableau en tant que **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) ou une valeur arbitraire. Les utilisateurs de tables doivent veiller à faire la différence entre les propriétés qui ne sont pas existantes et qui ont des valeurs incompréhensibles et des propriétés qui existent et qui ont des valeurs valides. 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

