---
title: Propriété canonique PidTagAttachContentBase
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentBase
api_type:
- HeaderDef
ms.assetid: 35c10264-6998-4c46-8cef-82708c96d9c7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ec1db68d9168e7260a32aaf7708897df6124725a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398975"
---
# <a name="pidtagattachcontentbase-canonical-property"></a>Propriété canonique PidTagAttachContentBase

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’en-tête de base de contenu d’une pièce jointe du message Multipurpose Internet Mail Extensions (MIME).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A, PR_ATTACH_CONTENT_BASE_W  <br/> |
|Identificateur :  <br/> |0x3711  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont utilisées pour la prise en charge MHTML. Ils représentent l’en-tête de base de contenu pour le composant de corps MIME approprié. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
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

