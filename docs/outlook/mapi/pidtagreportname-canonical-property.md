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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 33a7545f9b2719615617d46e2d5ed1f6952b5522
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422312"
---
# <a name="pidtagreportname-canonical-property"></a>Propriété canonique PidTagReportName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom complet du destinataire qui doit obtenir des rapports pour ce message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W  <br/> |
|Identificateur :  <br/> |0x003A  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont des exemples de propriétés d’adresse pour le destinataire que l’expéditeur a délégué pour recevoir tous les rapports générés pour ce message.
  
Une application cliente qui doit router les rapports vers un autre utilisateur doit définir ces propriétés au moment de l’envoi du message. S’ils ne sont pas définies, les rapports sont envoyés à l’expéditeur du message.
  
## <a name="related-resources"></a>Ressources connexes

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

