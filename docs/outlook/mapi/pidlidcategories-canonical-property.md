---
title: Propri t canonique PidLidCategories
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidCategories
api_type:
- COM
ms.assetid: 6ad2aedc-405b-475e-ac76-7ecbbef28f73
description: Spécifie une liste de catégories pour un élément.
ms.openlocfilehash: bb6632b15a6f83c42ee7483316d12232ebf3a9b7
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64406252"
---
# <a name="pidlidcategories-canonical-property"></a>Propri t canonique PidLidCategories

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie une liste de catégories pour un élément. Pour générer un champ d’en-tête de mots clés, les clients doivent définir la valeur de cette propriété sur les valeurs souhaitées.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidCategories  <br/> |
|Jeu de propriétés :  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ID long (LID) :  <br/> |0x00002328  <br/> |
|Type de données :  <br/> |PT_MV_UNICODE  <br/> |
|Domaine :  <br/> |Courant  <br/> |
   
## <a name="remarks"></a>Remarques

Pour générer un champ d’en-tête de mots clés, les clients doivent définir la valeur de cette propriété sur les valeurs souhaitées. Cette propriété possède plusieurs chaînes ; chaque catégorie doit être mappée à un mot clé unique.
  
Les rédacteurs MIME (Multipurpose Internet Mail Extensions) doivent copier chaque sous-valeur de cette propriété dans un mot clé distinct dans le champ d’en-tête Keywords, avec une virgule (U+002C) et un espace (U+0020) séparant chaque mot clé. Les rédacteurs MIME peuvent abandonner cette propriété au lieu de la copier dans le champ d’en-tête des mots clés, afin d’éviter tout conflit entre différents ensembles de catégories dans différentes organisations.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit une définition de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet en objets de message.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

