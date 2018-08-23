---
title: Propriété canonique PidLidCategories
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCategories
api_type:
- COM
ms.assetid: 6ad2aedc-405b-475e-ac76-7ecbbef28f73
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 6893afa11cc08b335b0ffb39b725e26478dae22f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574838"
---
# <a name="pidlidcategories-canonical-property"></a>Propriété canonique PidLidCategories

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Spécifie une liste de catégories pour un élément.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidCategories  <br/> |
|Jeu de propriétés :  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ID de type long (capot) :  <br/> |0x00002328  <br/> |
|Type de données :  <br/> |PT_MV_UNICODE  <br/> |
|Domaine :  <br/> |Common  <br/> |
   
## <a name="remarks"></a>Remarques

Pour générer un champ d’en-tête de mots clés, les clients doivent définir la valeur de cette propriété avec les valeurs souhaitées. Cette propriété a plusieurs chaînes ; chaque catégorie doit être mappé à un mot clé unique.
  
Les auteurs Multipurpose Internet Mail Extensions (MIME) doivent copier chaque valeur sous-sites de cette propriété à un mot clé distinct dans le champ en-tête de mots clés, avec une virgule (U + 002 C) et espace (U + 0020) séparant chaque mot clé. Rédacteurs MIME peuvent supprimer cette propriété au lieu de la copier dans le champ en-tête de mots clés, afin d’éviter les conflits entre les différentes catégories dans différentes organisations.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit une définition de propriété et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet aux objets de message.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

