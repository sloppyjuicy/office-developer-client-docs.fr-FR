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
description: Contient des indicateurs indiquant les détails d’une soumission de message, notamment si lepooler MAPI a le message verrouillé et s’il doit être prétraité.
ms.openlocfilehash: c8f5c41b17e76a5a7a9ebeee37edbc8ccce74e2d
ms.sourcegitcommit: c68b7b7f98b3ff9e6de37ee5877adcad2e5e71d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63741556"
---
# <a name="pidtagsubmitflags-canonical-property"></a>Propriété canonique PidTagSubmitFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de bits d’indicateurs indiquant des détails sur l’envoi d’un message.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SUBMIT_FLAGS  <br/> |
|Identificateur :  <br/> |0x0E14  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |MAPI non transmetteable  <br/> |
   
## <a name="remarks"></a>Remarques

Un ou plusieurs des indicateurs suivants peuvent être définies pour **PR_SUBMIT_FLAGS masque de** bits : 
  
SUBMITFLAG_LOCKED 
  
> Lepooler MAPI a actuellement le message verrouillé. 
    
SUBMITFLAG_PREPROCESS 
  
> Le message doit être prétraité. Lorsque lepooler MAPI a terminé le prétraitement de ce message, il doit appeler la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) . Le fournisseur de la boutique de messages reconnaît que lepooler, plutôt que l’application cliente, a appelé **SubmitMessage**, effacer l’indicateur et poursuivre l’envoi du message.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
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

