---
title: Propriété canonique PidTagOwnerAppointmentId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOwnerAppointmentId
api_type:
- COM
ms.assetid: b5eea554-6bca-42d1-b943-1327f0d70584
description: Contient un identificateur pour un rendez-vous dans la planification du propriétaire. Cette propriété est utilisée dans les demandes de réunion.
ms.openlocfilehash: 8e030d8dd41640566b16025b6be8b3a0e3e945e7
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524000"
---
# <a name="pidtagownerappointmentid-canonical-property"></a>Propriété canonique PidTagOwnerAppointmentId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un identificateur pour un rendez-vous dans la planification du propriétaire.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_OWNER_APPT_ID  <br/> |
|Identificateur :  <br/> |0x0062  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Rendez-vous  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée dans les demandes de réunion. Il ne représente pas un identificateur d’entrée, mais un long integer qui identifie de manière unique le rendez-vous dans la planification de l’expéditeur.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convertit les objets RFC2445, RFC2446 et RFC2447 de l’IETF, ainsi que les objets de rendez-vous et de réunion.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode les objets de message et de pièce jointe dans une représentation de flux efficace.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagOriginalAuthorSearchKey](pidtagoriginalauthorsearchkey-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

