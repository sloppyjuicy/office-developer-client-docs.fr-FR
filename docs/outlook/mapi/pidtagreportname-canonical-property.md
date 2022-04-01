---
title: Propriété canonique PidTagReportName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagReportName
api_type:
- COM
ms.assetid: 4ec3100f-7cf1-4702-b326-e6da586a7bb2
description: Contient le nom complet du destinataire qui doit obtenir des rapports pour ce message. Une application cliente doit définir cette propriété au moment de la soumission.
ms.openlocfilehash: bc5aa1e419ae38ff6483a9a6f53143293a3ff365
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523284"
---
# <a name="pidtagreportname-canonical-property"></a>Propriété canonique PidTagReportName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom complet du destinataire qui doit obtenir des rapports pour ce message.
  
|Propriété |Valeur |
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

