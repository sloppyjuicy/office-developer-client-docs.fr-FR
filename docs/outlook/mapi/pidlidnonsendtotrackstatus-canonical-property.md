---
title: Propriété canonique PidLidNonSendToTrackStatus
description: Décrit la propriété canonique PidLidNonSendToTrackStatus, qui contient la valeur de chaque participant répertorié dans la propriété dispidNonSendableTo.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidNonSendToTrackStatus
api_type:
- COM
ms.assetid: 50fec332-e7df-4bc6-8c50-59b9ca545f89
ms.openlocfilehash: 7b48941fbe9ffcb04307b56eb5142dca0ae9a95a
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817458"
---
# <a name="pidlidnonsendtotrackstatus-canonical-property"></a>Propriété canonique PidLidNonSendToTrackStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur de chaque participant répertorié dans la propriété **dispidNonSendableTo** ([PidLidNonSendableTo](pidlidnonsendableto-canonical-property.md)).
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |dispidNonSendToTrackStatus  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x00008543  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété n’est requise que lorsque la propriété **dispidNonSendableTo** est définie. Le nombre de valeurs dans cette propriété doit être égal au nombre de valeurs dans **dispidNonSendableTo**. Chaque PT_LONG valeur de cette propriété correspond au participant de la propriété **dispidNonSendableTo** au même index. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit une définition de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

