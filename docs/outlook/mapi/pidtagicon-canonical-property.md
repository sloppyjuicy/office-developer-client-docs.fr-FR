---
title: Propriété canonique PidTagIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIcon
api_type:
- HeaderDef
ms.assetid: 815dabf3-3cac-40e1-b6ff-51db2ff5096a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0aa5873d98b7ae9dea1bdaffc37f7996262b6062
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786078"
---
# <a name="pidtagicon-canonical-property"></a>Propriété canonique PidTagIcon

  
  
**S’applique à**: Outlook 
  
Contient un bitmap d’une icône de toute taille d’un formulaire. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ICON  <br/> |
|Identificateur :  <br/> |0x0FFD  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |MAPI non transmissible  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient une image de 32 x 32 pixels d’une icône, le même que le contenu d’un. Fichier ICO. Cette propriété est normalement copiée à partir de la. Fichier ICO spécifié dans la ligne LargeIcon de la section [Description] appropriée du fichier de configuration du formulaire. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagMiniIcon](pidtagminiicon-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

