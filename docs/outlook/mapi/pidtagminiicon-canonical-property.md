---
title: Propriété canonique PidTagMiniIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMiniIcon
api_type:
- HeaderDef
ms.assetid: a436b590-63f3-413c-a9c2-7664567e0ff0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ea7f9e0ed57c56b48399b9ffd1ea42db28daf249
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356230"
---
# <a name="pidtagminiicon-canonical-property"></a>Propriété canonique PidTagMiniIcon

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une image bitmap d'une icône de demi-taille pour un formulaire.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MINI_ICON  <br/> |
|Identificateur :  <br/> |0x0FFC  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient une image 32 × 32 pixels d'une icône, le même que le contenu d'un. Fichier. ICO, mais seuls les 16 × 16 pixels du coin supérieur gauche sont considérés comme significatifs. Cette propriété est généralement copiée à partir du. Fichier. ICO spécifié dans la ligne SmallIcon de la section [Description] appropriée du fichier de configuration du formulaire.
  
 **Note** Certaines plateformes ne prennent pas en charge les icônes 16 x 16 pixels. Le format 32 × 32 de cette propriété est utilisable dans ce cas, mais les applications clientes doivent être conscientes des incohérences d'affichage. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagIcon](pidtagicon-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

