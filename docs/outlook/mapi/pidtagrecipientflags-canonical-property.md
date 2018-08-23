---
title: Propriété canonique PidTagRecipientFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientFlags
api_type:
- COM
ms.assetid: 9fbe537f-b5fe-48a2-803c-653c50c82efd
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 0e84f1361e9ca3d95b4297c01801e649a9f86ced
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569231"
---
# <a name="pidtagrecipientflags-canonical-property"></a>Propriété canonique PidTagRecipientFlags

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Spécifie un champ de bits qui décrit l’état du destinataire.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECIPIENT_FLAGS  <br/> |
|Identificateur :  <br/> |0x5FFD  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Destinataire de transport  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété n’est pas requise. Voici les indicateurs individuels qui peuvent être définies.
  
|**Valeur**|**Description**|
|:-----|:-----|
|S (recipSendable, 0 x 00000001)  <br/> |Le destinataire est un participant **Sendable** . Cet indicateur est utilisé uniquement dans la propriété **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)).  <br/> |
|O (recipOrganizer, 0x0000002)  <br/> |Le **RecipientRow** sur lequel il est défini représente l’organisateur de la réunion.  <br/> |
|Restauration d’urgence (recipExceptionalResponse, 0 x 00000010)  <br/> |Indique que le participant a donné une réponse de l’exception sur lequel réside cette **RecipientRow** . Cet indicateur est utilisé uniquement dans un **RecipientRow** d’un objet de messages incorporés d’exception de l’objet de réunion de l’organisateur.  <br/> |
|ED (recipExceptionalDeleted, 0 x 00000020)  <br/> |Indique que bien que l' **RecipientRow** existe, il doit être traitée comme si le destinataire n’a pas. Cet indicateur est utilisé uniquement dans un **RecipientRow** d’un objet de messages incorporés d’exception de l’objet de réunion de l’organisateur.  <br/> |
|X (0 x 00000040 réservés,)  <br/> |Ne doit pas être définie.  <br/> |
|X (0x00000080 réservés,)  <br/> |Ne doit pas être définie.  <br/> |
|G (recipOriginal, 0 x 00000100)  <br/> |Indique que le destinataire est un participant d’origine. Cet indicateur est utilisé uniquement dans la propriété **dispidApptUnsendableRecips** .  <br/> |
|X (0 x 00000200 réservés,)  <br/> |Réservé.  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

