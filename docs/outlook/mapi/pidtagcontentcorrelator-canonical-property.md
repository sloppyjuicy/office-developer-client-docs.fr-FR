---
title: Propriété canonique PidTagContentCorrelator
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCorrelator
api_type:
- HeaderDef
ms.assetid: 0bf78879-2f9f-4c29-b1f4-2f4882d8464d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2290e6751778f17defc8d1007ff62c88f1b75465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785847"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a>Propriété canonique PidTagContentCorrelator

  
  
**S’applique à**: Outlook 
  
Contient une valeur de que l’expéditeur du message peut utiliser pour correspondre à un rapport avec le message d’origine.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTENT_CORRELATOR  <br/> |
|Identificateur :  <br/> |0 x 0007  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Remarques

Le contenu de la chaîne binaire est défini par l’expéditeur du message. Si défini sur un message sortant, cette propriété doit être copié sur tous les rapports générés en réponse au message.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

