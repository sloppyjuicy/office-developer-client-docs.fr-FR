---
title: Propriété canonique PidTagOriginalSubmitTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubmitTime
api_type:
- COM
ms.assetid: 2e027c0c-2370-437a-ad98-2bbb5e41e525
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 07aea33f54a29d497646b62f1f8bd96a383cbd7b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385731"
---
# <a name="pidtagoriginalsubmittime-canonical-property"></a>Propriété canonique PidTagOriginalSubmitTime

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la date de soumission d’origine et l’heure du message dans le rapport.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINAL_SUBMIT_TIME  <br/> |
|Identificateur :  <br/> |0x004E  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Au premier envoi d’un message, une application cliente doit définir cette propriété à la valeur de la propriété **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)). Il n’est pas modifié lorsque le message est transféré. Il est utilisé dans les rapports uniquement.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.
    
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

