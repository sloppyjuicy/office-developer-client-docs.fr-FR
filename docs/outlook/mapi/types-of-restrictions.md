---
title: Types de restrictions
description: Décrit les types de restrictions, dont certains se concentrent sur des colonnes spécifiques. Cela s’applique à Outlook 2013 et Outlook 2016.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0d3bd58b-7100-4117-91ac-27139715c85b
ms.openlocfilehash: 1f39672cb0240129a8eca9b0175ebce928f3c43c
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894879"
---
# <a name="types-of-restrictions"></a>Types de restrictions

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe de nombreux types de restrictions, certains se concentrant sur des colonnes spécifiques. Toutes les implémentations de table sont censées prendre en charge les restrictions sur les colonnes du jeu de colonnes actuel. Toutefois, pour ajouter de la valeur, les implémenteurs de table peuvent également prendre en charge les restrictions basées sur les propriétés d’objet qui ne sont pas actuellement dans la vue de table.
  
Certaines restrictions peuvent être combinées à l’aide d’une restriction qui effectue une opération **LOGIQUE AND**, **OR** ou **NOT** . Par exemple, la plupart des restrictions de propriété doivent être jointes à des restrictions existantes à l’aide de restrictions **AND** . Il existe quelques exceptions, par exemple lorsque la propriété utilisée dans la restriction de propriété est la propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) ou lorsqu’il s’agit d’une colonne obligatoire dans une table. Une restriction de construction de client pour limiter son affichage doit utiliser des restrictions existantes avec ses restrictions de propriété, car MAPI ne spécifie pas comment les fournisseurs de services doivent évaluer les restrictions de propriété lorsqu’une propriété n’existe pas. Il est raisonnable et recommandé que les fournisseurs de services ne respectent pas la restriction, mais il n’existe aucune exigence. 
  
Une restriction est définie à l’aide de la structure de données [SRestriction](srestriction.md) qui contient une union de structures de restriction plus spécialisées et un indicateur du type de structure inclus dans l’union. 
  
Chacune des structures de restriction spécialisées dans l’union représente un type de restriction différent. Les types de restrictions et leurs structures de données associées sont les suivants :
  
|**Type de restriction**|**Structure de données associée**|**Description**|
|:-----|:-----|:-----|
|Comparer la propriété  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |Compare deux propriétés du même type. |
|**AND** <br/> |[SAndRestriction](sandrestriction.md) <br/> |Effectue une opération **AND** logique sur deux restrictions ou plus. |
|**OR** <br/> |[SOrRestriction](sorrestriction.md) <br/> |Effectue une opération **OR** logique sur deux restrictions ou plus. |
|**NOT** <br/> |[SNotRestriction](snotrestriction.md) <br/> |Effectue une opération **NOT** logique sur deux restrictions ou plus. |
|Contenu  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |Localise les données spécifiées. |
|Propriété  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |Spécifie une valeur de propriété particulière comme critère de correspondance. Peut être utilisé, par exemple, pour rechercher un type particulier de pièce jointe. |
|Bitmask  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |Applique un masque de bits à une propriété PT_LONG, généralement pour déterminer si des indicateurs particuliers sont définis. |
|Size  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |Teste la taille d’une propriété à l’aide d’opérateurs relationnels standard. |
|Existe  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |Teste si un objet a une valeur pour une propriété. |
|Sous-objet  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |Utilisé pour la recherche par le biais de sous-objets ou d’objets qui ne sont pas accessibles avec un identificateur d’entrée, tels que des destinataires et des pièces jointes. Peut être utilisé, par exemple, pour rechercher des messages pour un destinataire particulier. |
|Commentaire  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |Associe un objet à un ensemble de propriétés nommées. |
   
Certaines restrictions utilisent des expressions régulières, et MAPI prend en charge une forme limitée de notation d’expression régulière dans le style utilisé dans de nombreuses applications de texte.
  
La restriction de commentaire est utilisée par les clients qui enregistrent les restrictions sur le disque pour conserver les informations spécifiques à l’application avec la restriction. Par exemple, un client qui enregistre le nom d’une propriété nommée utilisée dans une restriction de propriété peut le faire avec une restriction de commentaire. L’enregistrement du nom n’est pas possible dans une restriction de propriété ; La structure de données [SPropertyRestriction](spropertyrestriction.md) contient uniquement la balise de propriété. Les restrictions de commentaire sont ignorées par [IMAPITable::Restrict](imapitable-restrict.md) , car elles n’ont aucun effet sur les lignes retournées par [IMAPITable::QueryRows](imapitable-queryrows.md) après qu’un appel **Restrict** a été effectué. 
  
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

