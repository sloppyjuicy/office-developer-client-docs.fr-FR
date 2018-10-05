---
title: Propriété canonique PidTagReportSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportSearchKey
api_type:
- COM
ms.assetid: d4f4c40b-b6a8-45f3-b750-07b92c535322
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 889b43bb606cbe9c96d52c8a21ffda5dfcebb1da
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383505"
---
# <a name="pidtagreportsearchkey-canonical-property"></a>Propriété canonique PidTagReportSearchKey

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la clé de recherche pour le destinataire qui doit obtenir des rapports de ce message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_REPORT_SEARCH_KEY  <br/> |
|Identificateur :  <br/> |0x0054  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est une des propriétés d’adresse du destinataire l’expéditeur a délégué pour recevoir les rapports générés pour ce message.
  
Une application cliente qui doit router les rapports à un autre utilisateur doit définir cette propriété à l’heure d’envoi de message. Si elle n’est pas définie, les rapports sont envoyés à l’expéditeur du message.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les messages électroniques.
    
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

