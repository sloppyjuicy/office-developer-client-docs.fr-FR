---
title: Types de restrictions
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d3bd58b-7100-4117-91ac-27139715c85b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 28159dfb947b4fb0ea54680627588b7c10bee3b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356566"
---
# <a name="types-of-restrictions"></a>Types de restrictions

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe de nombreux types de restrictions, qui se concentrent sur des colonnes spécifiques. Toutes les implémentations de table sont censées prendre en charge des restrictions sur les colonnes dans le jeu de colonnes actuel. Toutefois, pour ajouter de la valeur, les implémenteurs de tableaux peuvent également prendre en charge des restrictions basées sur les propriétés de l'objet qui ne sont pas actuellement dans l'affichage tableau.
  
Certaines restrictions peuvent être combinées à l'aide d'une restriction qui effectue une opération **and**, **or**ou **not** . Par exemple, la plupart des restrictions de propriété doivent être jointes avec des restrictions Exists à l'aide **de et des** restrictions. Il existe quelques exceptions, par exemple lorsque la propriété utilisée dans la restriction de propriété est la propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) ou lorsqu'il s'agit d'une colonne obligatoire dans un tableau. Les restrictions de création d'un client pour limiter sa vue doivent utiliser des restrictions Exists avec ses restrictions de propriété car MAPI ne spécifie pas comment les fournisseurs de services doivent évaluer les restrictions de propriété lorsqu'une propriété n'existe pas. Il est raisonnable et recommandé que les fournisseurs de services échouent à la restriction, mais qu'il n'y a pas de configuration requise. 
  
Une restriction est définie à l'aide de la structure de données [SRestriction](srestriction.md) qui contient une Union de structures de restriction spécialisées plus spécialisées et un indicateur du type de structure inclus dans l'Union. 
  
Chacune des structures de restriction spécialisées de l'Union représente un type différent de restriction. Les types de restrictions et leurs structures de données associées sont les suivants:
  
|**Type de restriction**|**Structure de données associée**|**Description**|
|:-----|:-----|:-----|
|Compare, propriété  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |Compare deux propriétés du même type.  <br/> |
|**AND** <br/> |[SAndRestriction](sandrestriction.md) <br/> |Effectue une opération **and** logique sur au moins deux restrictions.  <br/> |
|**OU** <br/> |[SOrRestriction](sorrestriction.md) <br/> |Effectue une opération **or** logique sur au moins deux restrictions.  <br/> |
|**NOT** <br/> |[SNotRestriction](snotrestriction.md) <br/> |Effectue une opération **not** logique sur deux ou plusieurs restrictions.  <br/> |
|Contenu  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |Localise les données spécifiées.  <br/> |
|Propriété  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |Spécifie une valeur de propriété particulière comme critère de correspondance. Peut être utilisé, par exemple, pour rechercher un type particulier de pièce jointe.  <br/> |
|Composé  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |Applique un masque de réactivation à une propriété PT_LONG, généralement pour déterminer si des indicateurs spécifiques sont définis.  <br/> |
|Taille  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |Teste la taille d'une propriété à l'aide d'opérateurs relationnels standard.  <br/> |
|Présent  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |Teste si un objet a une valeur pour une propriété.  <br/> |
|Sous-objet  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |Utilisé pour effectuer des recherches dans des sous-objets ou des objets qui ne sont pas accessibles avec un identificateur d'entrée, comme des destinataires et des pièces jointes. Peut être utilisé, par exemple, pour rechercher des messages pour un destinataire particulier.  <br/> |
|Commentaire  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |Associe un objet à un ensemble de propriétés nommées.  <br/> |
   
Certaines restrictions utilisent des expressions régulières et MAPI prend en charge une forme limitée de notation d'expression régulière dans le style utilisé par de nombreuses applications de texte.
  
La restriction de commentaire est utilisée par les clients qui enregistrent des restrictions sur le disque pour conserver les informations spécifiques à l'application avec la restriction. Par exemple, un client enregistrant le nom d'une propriété nommée utilisée dans une restriction de propriété peut le faire avec une restriction de commentaire. L'enregistrement du nom n'est pas possible dans une restriction de propriété; la structure de données [SPropertyRestriction](spropertyrestriction.md) contient uniquement la balise de propriété. Les restrictions de commentaire sont ignorées par la fonction [IMAPITable:: Restrict](imapitable-restrict.md) dans la limite du fait qu'elles n'ont aucun effet sur les lignes renvoyées par la fonction [IMAPITable:: QueryRows](imapitable-queryrows.md) après qu'un appel de **restriction** a été effectué. 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

