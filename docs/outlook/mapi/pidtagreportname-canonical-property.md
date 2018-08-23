---
title: Propriété canonique PidTagReportName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportName
api_type:
- COM
ms.assetid: 4ec3100f-7cf1-4702-b326-e6da586a7bb2
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3c1a848eec84c7d81792a95baa3f47fa6779e95f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569581"
---
# <a name="pidtagreportname-canonical-property"></a>Propriété canonique PidTagReportName

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient le nom complet pour le destinataire qui doit obtenir des rapports de ce message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W  <br/> |
|Identificateur :  <br/> |0x003A  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont des exemples de propriétés d’adresse du destinataire l’expéditeur a délégué pour recevoir les rapports générés pour ce message.
  
Une application cliente qui doit router les rapports à un autre utilisateur doit définir ces propriétés au moment d’envoi de message. Si elles ne sont pas définies, les rapports sont envoyés à l’expéditeur du message.
  
## <a name="related-resources"></a>Ressources connexes

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

