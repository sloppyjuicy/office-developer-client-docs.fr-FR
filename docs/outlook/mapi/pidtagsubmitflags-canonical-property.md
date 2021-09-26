---
title: Propriété canonique PidTagSubmitFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSubmitFlags
api_type:
- COM
ms.assetid: 9ea1c029-d53c-4c28-b413-560083b6215a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 90a3807a4dd5edc5a0a18baebbc9754bd35ea1fc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624425"
---
# <a name="pidtagsubmitflags-canonical-property"></a>Propriété canonique PidTagSubmitFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de bits d’indicateurs indiquant des détails sur l’envoi d’un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SUBMIT_FLAGS  <br/> |
|Identificateur :  <br/> |0x0E14  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |MAPI non transmetteable  <br/> |
   
## <a name="remarks"></a>Remarques

Un ou plusieurs des indicateurs suivants peuvent être définies pour PR_SUBMIT_FLAGS **masque** de bits : 
  
SUBMITFLAG_LOCKED 
  
> Lepooler MAPI a actuellement le message verrouillé. 
    
SUBMITFLAG_PREPROCESS 
  
> Le message doit être prétraité. Lorsque lepooler MAPI a terminé le prétraitement de ce message, il doit appeler la méthode [IMessage::SubmitMessage.](imessage-submitmessage.md) Le fournisseur de magasin de messages reconnaît que lepooler, plutôt que l’application cliente, a appelé **SubmitMessage,** effacer l’indicateur et continue l’envoi du message.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convertit les objets RFC2445, RFC2446 et RFC2447 de l’IETF, ainsi que les objets de rendez-vous et de réunion.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[IMsgStore::SetLockState](imsgstore-setlockstate.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

