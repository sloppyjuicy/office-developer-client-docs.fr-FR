---
title: Propriété canonique PidTagAttachMimeSequence
description: Décrit la propriété canonique PidTagAttachMimeSequence, qui contient le numéro de séquence MIME d’une pièce jointe de message MIME.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachMimeSequence
api_type:
- HeaderDef
ms.assetid: d2a84f24-b4a5-4e16-9219-7a579a31a8f8
ms.openlocfilehash: 04753294a8907fad19d72e6678c9059fd14873e6
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815302"
---
# <a name="pidtagattachmimesequence-canonical-property"></a>Propriété canonique PidTagAttachMimeSequence

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le numéro de séquence MIME d’une pièce jointe de message MIME.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_MIME_SEQUENCE  <br/> |
|Identificateur :  <br/> |0x3710  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Propriétés de la pièce jointe du message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée pour la prise en charge de MHTML. Il représente le numéro de séquence de la pièce jointe dans la partie du corps en plusieurs parties MIME parente du message MIME.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

