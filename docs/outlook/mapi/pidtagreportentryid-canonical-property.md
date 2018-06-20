---
title: Propriété canonique PidTagReportEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportEntryId
api_type:
- COM
ms.assetid: ea2bcc06-0089-4999-b115-06a14de4a0f1
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a1d81581afa3bb9df8bd7aded5c265dfa8f04676
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786584"
---
# <a name="pidtagreportentryid-canonical-property"></a>Propriété canonique PidTagReportEntryId

  
  
**S’applique à**: Outlook 
  
Contient l’identificateur d’entrée pour le destinataire qui doit recevoir des rapports de ce message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_REPORT_ENTRYID  <br/> |
|Identificateur :  <br/> |0x0045  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est une des propriétés d’adresse pour le destinataire que l’expéditeur a délégué pour recevoir les rapports générés pour ce message.
  
Une application cliente qui doit router les rapports à un autre utilisateur doit définir cette propriété à l’heure d’envoi de message. Si elle n’est pas définie, les rapports sont envoyés à l’expéditeur du message.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les messages électroniques.
    
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

