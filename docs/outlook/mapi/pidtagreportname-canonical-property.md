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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4d3a38f55fa2869df3f8afa1301cf1ad0c7b0737
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786592"
---
# <a name="pidtagreportname-canonical-property"></a>Propriété canonique PidTagReportName

  
  
**S’applique à**: Outlook 
  
Contient le nom complet pour le destinataire qui doit obtenir des rapports de ce message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W  <br/> |
|Identificateur :  <br/> |0x003A  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Zone :  <br/> |Enveloppe MAPI  <br/> |
   
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
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

