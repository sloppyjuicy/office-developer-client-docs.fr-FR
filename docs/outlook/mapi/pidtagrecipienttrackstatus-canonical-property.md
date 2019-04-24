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
ms.openlocfilehash: 074bcf7c051b78bc32caf66502747e7fb1ab6b79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355285"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a>Propriété canonique PidTagRecipientTrackStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique l'état de la réponse renvoyée par le participant.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECIPIENT_TRACKSTATUS  <br/> |
|Identificateur :  <br/> |0x5FFF  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Destinataire de transport  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette valeur n'est pas définie, elle doit être supposée être respNone. Sinon, il doit s'agir de l'un des éléments suivants:
  
|**État de la réponse**|**Value**|**Description**|
|:-----|:-----|:-----|
|respNone  <br/> |0x00000000  <br/> |Aucune réponse n'est requise pour cet objet. C'est le cas des objets de rendez-vous et des objets de réponse aux réunions.  <br/> |
|respTentative  <br/> |0x00000002  <br/> |Cette valeur sur l'objet Meeting du participant indique que le participant a provisoirement accepté l'objet de la demande de réunion.  <br/> |
|respAccepted  <br/> |0x00000003  <br/> |Cette valeur sur l'objet Meeting du participant indique que le participant a accepté l'objet de la demande de réunion.  <br/> |
|respDeclined  <br/> |0x00000004  <br/> |Cette valeur sur l'objet Meeting du participant indique que le participant a refusé l'objet de la demande de réunion.  <br/> |
   
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et Attachment.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

