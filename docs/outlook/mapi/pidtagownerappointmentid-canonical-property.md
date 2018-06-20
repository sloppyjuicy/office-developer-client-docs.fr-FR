---
title: Propriété canonique PidTagOwnerAppointmentId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOwnerAppointmentId
api_type:
- COM
ms.assetid: b5eea554-6bca-42d1-b943-1327f0d70584
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a6fc194a3ef7d82be656a8d6c3f5fb9ad8326ceb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786383"
---
# <a name="pidtagownerappointmentid-canonical-property"></a>Propriété canonique PidTagOwnerAppointmentId

  
  
**S’applique à**: Outlook 
  
Contient un identificateur pour un rendez-vous du calendrier du propriétaire.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PROPRIÉTÉ PR_OWNER_APPT_ID  <br/> |
|Identificateur :  <br/> |0x0062  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Rendez-vous  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée dans les demandes de réunion. Il ne représente pas un identificateur d’entrée, mais un entier long qui identifie de manière unique le rendez-vous au sein de la planification de l’expéditeur.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagOriginalAuthorSearchKey](pidtagoriginalauthorsearchkey-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

