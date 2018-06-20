---
title: Propriété canonique PidTagOriginatorCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorCertificate
api_type:
- COM
ms.assetid: 65f890d8-9d25-408e-ab29-89991278b92d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 871ce5f594a75b9441d0434c3be47b2718540576
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786359"
---
# <a name="pidtagoriginatorcertificate-canonical-property"></a>Propriété canonique PidTagOriginatorCertificate

  
  
**S’applique à**: Outlook 
  
Contient un certificat ASN.1 pour l’expéditeur du message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINATOR_CERTIFICATE  <br/> |
|Identificateur :  <br/> |0 x 0022  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est une copie de la propriété **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) de l’expéditeur.
  
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

