---
title: Propri t canonique PidLidResponseStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidResponseStatus
api_type:
- COM
ms.assetid: e56142fd-204b-497e-83b9-59f9acda6cb4
description: Spécifie l’état de réponse d’un participant pour Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: d49315721a40c7269b04d0b73767225f5688c610
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63763522"
---
# <a name="pidlidresponsestatus-canonical-property"></a>Propri t canonique PidLidResponseStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie l’état de réponse d’un participant.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidResponseStatus  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID long (LID) :  <br/> |0x00008218  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Réunions  <br/> |
   
## <a name="remarks"></a>Remarques

L’état de la réponse doit être l’une des valeurs du tableau ci-dessous.
  
|**État de la réponse**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|respNone  <br/> |0x00000000  <br/> |Aucune réponse n’est requise pour cet objet. C’est le cas pour les objets de rendez-vous et les objets de réponse de réunion. |
|respOrganized  <br/> |0x00000001  <br/> |Cette réunion appartient à l’organisateur. |
|respTentative  <br/> |0x00000002  <br/> |Cette valeur sur la réunion du participant indique que le participant a provisoirement accepté la demande de réunion. |
|respAccepted  <br/> |0x00000003  <br/> |Cette valeur sur la réunion du participant indique que le participant a accepté la demande de réunion. |
|respDeclined  <br/> |0x00000004  <br/> |Cette valeur sur la réunion du participant indique que le participant a refusé la demande de réunion. |
|respNotResponded  <br/> |0x00000005  <br/> |Cette valeur sur la réunion du participant indique que le participant n’a pas encore répondu. Cette valeur est sur la demande de réunion, la mise à jour de réunion et l’annulation de la réunion. |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

