---
title: Propriété canonique PidTagAttachMimeSequence
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d85e13b6b8217bbe0d77304525b740a96e2816fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563853"
---
# <a name="pidtagattachmimesequence-canonical-property"></a>Propriété canonique PidTagAttachMimeSequence

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le numéro de séquence MIME d’une pièce jointe de message MIME.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_MIME_SEQUENCE  <br/> |
|Identificateur :  <br/> |0x3710  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Propriétés des pièces jointes des messages  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée pour la prise en charge MHTML. Il représente le numéro de séquence de la pièce jointe dans la partie du corps en plusieurs parties MIME parent du message MIME.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

