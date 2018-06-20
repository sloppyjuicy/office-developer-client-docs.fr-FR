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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 162451d000c0b3da42c8fbef5f64459bc5ae23b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786469"
---
# <a name="pidtagprovidersubmittime-canonical-property"></a>Propriété canonique PidTagProviderSubmitTime

  
  
**S’applique à**: Outlook 
  
Contient la date et l’heure de qu'un fournisseur de transport transmis un message à son système de messagerie sous-jacent.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROVIDER_SUBMIT_TIME  <br/> |
|Identificateur :  <br/> |0x0048  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Zone :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est définie par le fournisseur de transport sortant au moment où qu'un message est envoyé.
  
Cette propriété correspond à un attribut X.400 envoi enveloppe par message. 
  
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

