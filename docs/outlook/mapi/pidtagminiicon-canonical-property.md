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
ms.openlocfilehash: 04d78bddc7bae27ba23cccf676eb6e7412ffc0db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786252"
---
# <a name="pidtagminiicon-canonical-property"></a>Propriété canonique PidTagMiniIcon

  
  
**S’applique à**: Outlook 
  
Contient un bitmap d’une icône demi pour un formulaire.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MINI_ICON  <br/> |
|Identificateur :  <br/> |0x0FFC  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient une image de 32 x 32 pixels d’une icône, le même que le contenu d’un. Fichier ICO, mais seuls les pixels du coin supérieur gauche de 16 x 16 sont considérées comme importantes. Cette propriété est normalement copiée à partir de la. Fichier ICO spécifié dans la ligne SmallIcon de la section [Description] appropriée du fichier de configuration du formulaire.
  
 **Remarque** Certaines plateformes de ne pas les icônes prise en charge 16 x 16 pixels. Le format de 32 x 32 de cette propriété est utile dans ce cas, mais les applications clientes doivent être conscients de l’affichage incohérences. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagIcon](pidtagicon-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

