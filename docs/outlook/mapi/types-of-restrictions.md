---
title: Types de Restrictions
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d3bd58b-7100-4117-91ac-27139715c85b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7e3459c639cac449cdc03361949c9618827515b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787387"
---
# <a name="types-of-restrictions"></a>Types de Restrictions

  
  
**S’applique à**: Outlook 
  
Il existe de nombreux types de restrictions, certains spécialisés sur des colonnes spécifiques. Toutes les implémentations de tableau doivent prendre en charge des restrictions sur les colonnes dans le jeu actuel de la colonne. Toutefois, pour ajouter la valeur, l’implémentation de la table peut prennent également en charge les restrictions basées sur les propriétés de l’objet qui ne sont pas actuellement dans l’affichage tableau.
  
Certaines restrictions peuvent être combinées à l’aide d’une restriction qui effectue une opération logique **et**, **ou**ou **pas** . Par exemple, la propriété la plupart des restrictions doivent être associées existe restrictions à l’aide **et** restrictions. Il existe quelques exceptions, telles que lorsque la propriété utilisée dans la restriction de propriété est la propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) ou lorsqu’il est une colonne obligatoire dans un tableau. Un client de création des restrictions pour limiter l’affichage doit utiliser existe restrictions avec des restrictions de propriété MAPI ne spécifie pas comment les fournisseurs de services doivent évaluer les restrictions de propriété lorsqu’une propriété n’existe pas. Il est raisonnable et recommandé de fournisseurs de services de faire échouer la restriction, mais il n’existe aucune exigence. 
  
Une restriction est définie à l’aide de la structure de données [SRestriction](srestriction.md) qui contient une union des structures de restriction plus spécialisés et un indicateur du type de structure inclus dans l’union. 
  
Chacune des structures restriction spécialisés dans l’union représente un autre type de restriction. Les types de restrictions et les structures de données associées sont les suivants :
  
|**Type de restriction**|**Structure de données associée**|**Description**|
|:-----|:-----|:-----|
|La propriété  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |Compare deux propriétés du même type.  <br/> |
|**AND** <br/> |[SAndRestriction](sandrestriction.md) <br/> |Effectue une opération **AND** logique sur deux ou plusieurs restrictions.  <br/> |
|**OU** <br/> |[SOrRestriction](sorrestriction.md) <br/> |Effectue une opération **OR** logique sur deux ou plusieurs restrictions.  <br/> |
|**NOT** <br/> |[SNotRestriction](snotrestriction.md) <br/> |Effectue une opération **NOT** logique sur deux ou plusieurs restrictions.  <br/> |
|Content  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |Recherche de données spécifié.  <br/> |
|Property  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |Spécifie une valeur de propriété particulière comme critères pour la correspondance. Peut être utilisé, par exemple, pour rechercher un type particulier de pièce jointe.  <br/> |
|Masque de bits  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |Applique un masque de bits à une propriété PT_LONG, généralement pour déterminer si les indicateurs particuliers sont définis.  <br/> |
|Size  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |Teste la taille d’une propriété à l’aide des opérateurs de relation standard.  <br/> |
|Il existe  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |Vérifie si un objet a une valeur d’une propriété.  <br/> |
|Sous-objet  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |Utilisé pour la recherche par le biais de sous-objets ou des objets qui ne sont pas accessibles avec un identificateur d’entrée, tels que les destinataires et les pièces jointes. Peut être utilisé, par exemple, pour rechercher des messages pour un destinataire particulier.  <br/> |
|Commentaires  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |Associe un objet à un jeu de propriétés nommées.  <br/> |
   
Certaines restrictions utilisent des expressions régulières et MAPI prend en charge un type d’expression régulière la notation de style qui est utilisé de nombreuses applications de texte.
  
La restriction de commentaire est utilisée par les clients qui enregistrent des restrictions sur disque pour conserver les informations spécifiques à l’application avec la restriction. Par exemple, un client de l’enregistrement du nom d’une propriété nommée utilisé dans une restriction de propriété permettre le faire avec une restriction de commentaire. Enregistrez le nom n’est pas possible dans une restriction de propriété ; la structure de données [SPropertyRestriction](spropertyrestriction.md) conserve uniquement la balise de propriété. Restrictions de commentaire sont ignorées par [IMAPITable](imapitable-restrict.md) en ce sens qu’ils n’ont aucun effet sur les lignes renvoyées par [IMAPITable::QueryRows](imapitable-queryrows.md) après qu’un appel **Restrict** a été effectué. 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

