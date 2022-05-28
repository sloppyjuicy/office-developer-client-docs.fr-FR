---
title: Propriété canonique PidTagFormDesignerGuid
description: Décrit la propriété canonique PidTagFormDesignerGuid, qui contient l’identificateur unique de l’objet utilisé pour concevoir un formulaire.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagFormDesignerGuid
api_type:
- HeaderDef
ms.assetid: 8d7f5789-610c-47f6-a109-5513d677ef60
ms.openlocfilehash: f63e9bc79a7bd0eed18c003508bb505532db48cb
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770543"
---
# <a name="pidtagformdesignerguid-canonical-property"></a>Propriété canonique PidTagFormDesignerGuid

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’identificateur unique de l’objet utilisé pour concevoir un formulaire.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FORM_DESIGNER_GUID  <br/> |
|Identificateur :  <br/> |0x3309  <br/> |
|Type de données :  <br/> |PT_GUID  <br/> |
|Domaine :  <br/> |MAPI commun  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient généralement l’identificateur global unique (GUID) du programme de conception utilisé pour créer le formulaire. Cette propriété peut être vide. 
  
La structure [MAPIUID](mapiuid.md) contient la définition de l’identificateur unique. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

