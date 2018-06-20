---
title: Propriété canonique PidTagRecipientTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientTrackStatus
api_type:
- COM
ms.assetid: d619b5e7-2867-44fc-9b42-123bb1bf7bde
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cbc934eec5331a0302ba222108ee92a0dc696b1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786553"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a>Propriété canonique PidTagRecipientTrackStatus

  
  
**S’applique à**: Outlook 
  
Indique l’état de la réponse renvoyée par le participant.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECIPIENT_TRACKSTATUS  <br/> |
|Identificateur :  <br/> |0x5FFF  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Destinataire de transport  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette valeur n’est pas définie, il doit être supposé pour être respNone. Dans le cas contraire, il doit être une des options suivantes :
  
|**État de réponse**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|respNone  <br/> |0x00000000  <br/> |Aucune réponse n’est requise pour cet objet. C’est le cas pour les objets de rendez-vous et des objets de réponse de réunion.  <br/> |
|respTentative  <br/> |0x00000002  <br/> |Cette valeur sur l’objet de réunion du participant indique que le participant a accepté provisoirement la réunion objet de requête.  <br/> |
|respAccepted  <br/> |0 x 00000003  <br/> |Cette valeur sur l’objet de réunion du participant indique que le participant a accepté la réunion objet de requête.  <br/> |
|respDeclined  <br/> |0 x 00000004  <br/> |Cette valeur sur l’objet de réunion du participant indique que le participant a refusé la réunion objet de requête.  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

