---
title: Propriété canonique PidTagFormDesignerGuid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormDesignerGuid
api_type:
- HeaderDef
ms.assetid: 8d7f5789-610c-47f6-a109-5513d677ef60
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: db3bc9dacb0756f3ed9f16969b95245950b947fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786019"
---
# <a name="pidtagformdesignerguid-canonical-property"></a>Propriété canonique PidTagFormDesignerGuid

  
  
**S’applique à**: Outlook 
  
Contient l’identificateur unique de l’objet qui est utilisé pour créer un formulaire.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FORM_DESIGNER_GUID  <br/> |
|Identificateur :  <br/> |0x3309  <br/> |
|Type de données :  <br/> |PT_GUID  <br/> |
|Zone :  <br/> |MAPI courantes  <br/> |
   
## <a name="remarks"></a>Remarques

Généralement, cette propriété contient l’identificateur global unique (GUID) du programme de conception qui est utilisé pour créer le formulaire. Cette propriété peut être vide. 
  
La structure [MAPIUID](mapiuid.md) contient la définition de l’identificateur unique. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

