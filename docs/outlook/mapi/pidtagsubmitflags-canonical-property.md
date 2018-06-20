---
title: Propriété canonique PidTagSubmitFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubmitFlags
api_type:
- COM
ms.assetid: 9ea1c029-d53c-4c28-b413-560083b6215a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 444d98c4e8e32e0cc7d2eb8af753a394af1f020c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786861"
---
# <a name="pidtagsubmitflags-canonical-property"></a>Propriété canonique PidTagSubmitFlags

  
  
**S’applique à**: Outlook 
  
Contient un masque de bits d’indicateurs indiquant le plus d’informations sur un envoi de message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SUBMIT_FLAGS  <br/> |
|Identificateur :  <br/> |0x0E14  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |MAPI non transmissible  <br/> |
   
## <a name="remarks"></a>Remarques

Un ou plusieurs des indicateurs suivants peuvent être définies pour le masque de bits **PR_SUBMIT_FLAGS** : 
  
SUBMITFLAG_LOCKED 
  
> Le spouleur MAPI a actuellement le message verrouillé. 
    
SUBMITFLAG_PREPROCESS 
  
> Le message doit prétraitement. Lorsque le spouleur MAPI est terminé prétraitement ce message, il doit appeler la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) . Le fournisseur de banque de messages reconnaît que le spouleur, plutôt que l’application cliente, a appelé **SubmitMessage**, efface l’indicateur et continue d’envoi du message.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[IMsgStore::SetLockState](imsgstore-setlockstate.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

