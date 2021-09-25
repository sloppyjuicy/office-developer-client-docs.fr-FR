---
title: Types de restrictions
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0d3bd58b-7100-4117-91ac-27139715c85b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3fd12f2bed213bf48db18b8dacafc8d522439140
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590897"
---
# <a name="types-of-restrictions"></a>Types de restrictions

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe de nombreux types de restrictions, certaines se concentrent sur des colonnes spécifiques. Toutes les implémentations de tableau sont prévues pour prendre en charge les restrictions sur les colonnes de l’ensemble de colonnes actuel. Toutefois, pour ajouter de la valeur, les implémenteurs de tableau peuvent également prendre en charge des restrictions basées sur des propriétés d’objet qui ne sont pas actuellement dans l’affichage Tableau.
  
Certaines restrictions peuvent être combinées à l’aide d’une restriction qui effectue une opération **logique AND,** **OR** ou **NOT.** Par exemple, la plupart des restrictions de propriété doivent être jointes à des restrictions existantes à l’aide des restrictions **AND.** Il existe quelques exceptions, par exemple lorsque la propriété utilisée dans la restriction de propriété est la propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) ou lorsqu’il s’agit d’une colonne obligatoire dans une table. Les restrictions de construction d’un client pour limiter son affichage doivent utiliser des restrictions existantes avec ses restrictions de propriété, car MAPI ne spécifie pas comment les fournisseurs de services doivent évaluer les restrictions de propriété lorsqu’une propriété n’existe pas. Il est raisonnable et recommandé que les fournisseurs de services échouent à la restriction, mais il n’y a aucune exigence. 
  
Une restriction est définie à l’aide de la structure de données [SRestriction](srestriction.md) qui contient une union de structures de restriction plus spécialisées et un indicateur du type de structure inclus dans l’union. 
  
Chacune des structures de restriction spécialisées dans l’union représente un type de restriction différent. Les types de restrictions et leurs structures de données associées sont :
  
|**Type de restriction**|**Structure de données associée**|**Description**|
|:-----|:-----|:-----|
|Compare, propriété  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |Compare deux propriétés du même type.  <br/> |
|**AND** <br/> |[SAndRestriction](sandrestriction.md) <br/> |Effectue une opération **LOGIQUE AND** sur au moins deux restrictions.  <br/> |
|**OR** <br/> |[SOrRestriction](sorrestriction.md) <br/> |Effectue une opération **LOGIQUE OR** sur au moins deux restrictions.  <br/> |
|**NOT** <br/> |[SNotRestriction](snotrestriction.md) <br/> |Effectue une opération **NOT** logique sur au moins deux restrictions.  <br/> |
|Content  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |Recherche les données spécifiées.  <br/> |
|Property  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |Spécifie une valeur de propriété particulière en tant que critères de correspondance. Peut être utilisé, par exemple, pour rechercher un type particulier de pièce jointe.  <br/> |
|Bitmask  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |Applique un masque de bits à une propriété PT_LONG, généralement pour déterminer si des indicateurs particuliers sont définies.  <br/> |
|Size  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |Teste la taille d’une propriété à l’aide d’opérateurs relationnels standard.  <br/> |
|Exist  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |Teste si un objet a une valeur pour une propriété.  <br/> |
|Subobject  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |Utilisé pour rechercher des sous-objets ou des objets qui ne sont pas accessibles avec un identificateur d’entrée, tels que les destinataires et les pièces jointes. Peut être utilisé, par exemple, pour rechercher des messages pour un destinataire particulier.  <br/> |
|Commentaire  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |Associe un objet à un ensemble de propriétés nommées.  <br/> |
   
Certaines restrictions utilisent des expressions régulières et MAPI prend en charge une forme limitée de notation d’expression régulière dans le style utilisé par de nombreuses applications de texte.
  
La restriction de commentaire est utilisée par les clients qui enregistrent les restrictions sur le disque pour conserver les informations spécifiques à l’application avec la restriction. Par exemple, un client qui sauvegarde le nom d’une propriété nommée utilisée dans une restriction de propriété peut le faire avec une restriction de commentaire. L’enregistrement du nom n’est pas possible dans une restriction de propriété ; La structure [de données SPropertyRestriction](spropertyrestriction.md) contient uniquement la balise de propriété. Les restrictions de commentaire sont ignorées par [IMAPITable::Restrict](imapitable-restrict.md) en ce sens qu’elles n’ont aucun effet sur les lignes renvoyées par [IMAPITable::QueryRows](imapitable-queryrows.md) après qu’un appel **Restrict** a été effectué. 
  
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

