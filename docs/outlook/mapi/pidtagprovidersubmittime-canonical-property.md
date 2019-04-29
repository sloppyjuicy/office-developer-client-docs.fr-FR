---
title: Propriété canonique PidTagProviderSubmitTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderSubmitTime
api_type:
- COM
ms.assetid: 9e5161d9-fefe-4a12-b7f7-5600f1d2e95b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c5e840250da7ba3b95150f2e83e1eb08b0c61ab5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409019"
---
# <a name="pidtagprovidersubmittime-canonical-property"></a>Propriété canonique PidTagProviderSubmitTime

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la date et l'heure auxquelles un fournisseur de transport a passé un message à son système de messagerie sous-jacent.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROVIDER_SUBMIT_TIME  <br/> |
|Identificateur :  <br/> |0x0048  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est définie par le fournisseur de transport sortant lors de l'envoi d'un message.
  
Cette propriété correspond à l'attribut d'enveloppe de soumission X. 400 par message. 
  
## <a name="related-resources"></a>Ressources connexes

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

