---
title: Propriété canonique PidTagRecipientFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRecipientFlags
api_type:
- COM
ms.assetid: 9fbe537f-b5fe-48a2-803c-653c50c82efd
description: Spécifie un champ de bits qui décrit l’état du destinataire. Cette propriété n’est pas obligatoire.
ms.openlocfilehash: 02272de12404309af1dfa353cfbf8fa33449fa77
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64405957"
---
# <a name="pidtagrecipientflags-canonical-property"></a>Propriété canonique PidTagRecipientFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie un champ de bits qui décrit l’état du destinataire.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECIPIENT_FLAGS  <br/> |
|Identificateur :  <br/> |0x5FFD  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Destinataire de transport  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété n’est pas obligatoire. Voici les indicateurs individuels qui peuvent être définies.
  
|**Valeur**|**Description**|
|:-----|:-----|
|S (recipSendable, 0x00000001)  <br/> |Le destinataire est un **participant à l’envoi** . Cet indicateur est utilisé uniquement dans la propriété **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)). |
|O (recipOrganizer, 0x0000002)  <br/> |Le **RecipientRow** sur lequel cet indicateur est définie représente l’organisateur de la réunion. |
|ER (recipExceptionalResponse, 0x00000010)  <br/> |Indique que le participant a donné une réponse pour l’exception sur laquelle réside **ce RecipientRow** . Cet indicateur est utilisé uniquement dans **un RecipientRow** d’un objet message incorporé d’exception de l’objet de réunion de l’organisateur. |
|ED (recipExceptionalDeleted, 0x00000020)  <br/> |Indique que bien que **recipientRow** existe, il doit être traité comme si le destinataire correspondant ne le fait pas. Cet indicateur est utilisé uniquement dans **un RecipientRow** d’un objet message incorporé d’exception de l’objet de réunion de l’organisateur. |
|X (réservé, 0x00000040)  <br/> |Ne doit pas être définie. |
|X (réservé, 0x00000080)  <br/> |Ne doit pas être définie. |
|G (recipOriginal, 0x00000100)  <br/> |Indique que le destinataire est un participant d’origine. Cet indicateur est utilisé uniquement dans la **propriété dispidApptUnsendableRecips** . |
|X (réservé, 0x00000200)  <br/> |Réservé. |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

