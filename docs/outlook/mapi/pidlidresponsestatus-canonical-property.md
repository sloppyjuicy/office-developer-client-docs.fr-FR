---
title: Propriété canonique PidLidResponseStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidResponseStatus
api_type:
- COM
ms.assetid: e56142fd-204b-497e-83b9-59f9acda6cb4
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0bfa3a01613c49b122e92e4ac281e5b20b5f07ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785385"
---
# <a name="pidlidresponsestatus-canonical-property"></a>Propriété canonique PidLidResponseStatus

  
  
**S’applique à**: Outlook 
  
Spécifie l’état de la réponse d’un participant.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidResponseStatus  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID de type long (capot) :  <br/> |0x00008218  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Réunions  <br/> |
   
## <a name="remarks"></a>Remarques

L’état de réponse doit être une des valeurs dans le tableau ci-dessous.
  
|**État de réponse**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|respNone  <br/> |0x00000000  <br/> |Aucune réponse n’est requise pour cet objet. C’est le cas pour les objets de rendez-vous et des objets de réponse de réunion.  <br/> |
|respOrganized  <br/> |0x00000001  <br/> |Cette réunion appartient à l’organisateur.  <br/> |
|respTentative  <br/> |0x00000002  <br/> |Cette valeur sur la réunion du participant indique que le participant a provisoirement accepté la demande de réunion.  <br/> |
|respAccepted  <br/> |0 x 00000003  <br/> |Cette valeur t de réunion du participant indique que le participant a accepté la demande de réunion.  <br/> |
|respDeclined  <br/> |0 x 00000004  <br/> |Cette valeur sur la réunion du participant indique que le participant a refusé la demande de réunion.  <br/> |
|respNotResponded  <br/> |0 x 00000005  <br/> |Cette valeur sur la réunion du participant indique que le participant n’a pas encore répondu. Cette valeur est dans la demande de réunion, mise à jour de la réunion, l’annulation de réunion.  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

