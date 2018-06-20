---
title: Propriété canonique PidTagOriginalSensitivity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSensitivity
api_type:
- COM
ms.assetid: 70a87cf8-2011-4669-90fd-2711c3352e30
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6d461c88e96a3f749595b3e071737107480472aa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786345"
---
# <a name="pidtagoriginalsensitivity-canonical-property"></a>Propriété canonique PidTagOriginalSensitivity

  
  
**S’applique à**: Outlook 
  
Contient la valeur de sensibilité attribuée par l’expéditeur de la première version d’un message, le message avant d’être transférés ou une réponse.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINAL_SENSITIVITY  <br/> |
|Identificateur :  <br/> |0x002E  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Une application cliente doit définir cette propriété sur la même valeur que la propriété **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) lorsque le message est le premier envoyé. Il ne doit jamais être modifié par la suite.
  
Cette propriété est utilisée par le fournisseur de transport pour protéger la sensibilité sur les entrées copiées. Elle lui permet, par exemple, pour empêcher la modification du texte des messages d’origine dans un transfert d’ou une réponse à un message qui a été initialement marqué **SENSITIVITY_PRIVATE**.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.
    
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

