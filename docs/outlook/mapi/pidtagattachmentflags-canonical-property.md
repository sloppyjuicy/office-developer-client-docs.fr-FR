---
title: Propriété canonique PidTagAttachmentFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachmentFlags
api_type:
- HeaderDef
ms.assetid: 42981aac-f9e7-45dd-91a2-15d9784f30aa
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d494f1f14daff75be55e910da56204ecb3dbcf83
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345799"
---
# <a name="pidtagattachmentflags-canonical-property"></a>Propriété canonique PidTagAttachmentFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique une gestion spéciale pour cet objet Attachment.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACHMENT_FLAGS  <br/> |
|Identificateur :  <br/> |0x7FFD  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Doit être 0x00000000, sauf en cas de non-lieu par d’autres protocoles qui étendent le protocole d’objet de message et de pièce jointe, comme indiqué dans [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

