---
title: Propriété canonique PidTagOriginalMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalMessageClass
api_type:
- COM
ms.assetid: 49deb153-03c6-4be2-a3a5-53cca01accba
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: a0abd3618f7a1586d8ca786fc1b6802c17e0f0f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573116"
---
# <a name="pidtagoriginalmessageclass-canonical-property"></a>Propriété canonique PidTagOriginalMessageClass

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient la classe du message d’origine pour une utilisation dans un rapport.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIG_MESSAGE_CLASS, PR_ORIG_MESSAGE_CLASS_A, PR_ORIG_MESSAGE_CLASS_W  <br/> |
|Identificateur :  <br/> |0x004B  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Sécuriser les propriétés de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés contiennent une copie de la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) du message pour lequel le rapport est généré.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

