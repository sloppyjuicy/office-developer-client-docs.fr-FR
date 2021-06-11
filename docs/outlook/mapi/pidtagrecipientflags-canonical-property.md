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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7b791d75c2a76ea1a504c0d8862dd20f5365b475
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356699"
---
# <a name="pidtagrecipientflags-canonical-property"></a>Propriété canonique PidTagRecipientFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie un champ de bits qui décrit l’état du destinataire.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECIPIENT_FLAGS  <br/> |
|Identificateur :  <br/> |0x5FFD  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Destinataire de transport  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété n’est pas obligatoire. Voici les indicateurs individuels qui peuvent être définies.
  
|**Valeur**|**Description**|
|:-----|:-----|
|S (recipSendable, 0x00000001)  <br/> |Le destinataire est un **participant à l’envoi.** Cet indicateur est utilisé uniquement dans la propriété **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)).  <br/> |
|O (recipOrganizer, 0x0000002)  <br/> |La **recipientRow** sur laquelle cet indicateur est définie représente l’organisateur de la réunion.  <br/> |
|ER (recipExceptionalResponse, 0x00000010)  <br/> |Indique que le participant a donné une réponse pour l’exception sur laquelle réside **ce RecipientRow.** Cet indicateur est utilisé uniquement dans **un RecipientRow** d’un objet message incorporé d’exception de l’objet de réunion de l’organisateur.  <br/> |
|ED (recipExceptionalDeleted, 0x00000020)  <br/> |Indique que bien que **recipientRow** existe, il doit être traité comme si le destinataire correspondant ne le fait pas. Cet indicateur est utilisé uniquement dans **un RecipientRow** d’un objet message incorporé d’exception de l’objet de réunion de l’organisateur.  <br/> |
|X (réservé, 0x00000040)  <br/> |Ne doit pas être définie.  <br/> |
|X (réservé, 0x00000080)  <br/> |Ne doit pas être définie.  <br/> |
|G (recipOriginal, 0x00000100)  <br/> |Indique que le destinataire est un participant d’origine. Cet indicateur est utilisé uniquement dans la **propriété dispidApptUnsendableRecips.**  <br/> |
|X (réservé, 0x00000200)  <br/> |Réservé.  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
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

