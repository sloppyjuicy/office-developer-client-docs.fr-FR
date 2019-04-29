---
title: IAttachmentSecurityIsAttachmentBlocked
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity.IsAttachmentBlocked
api_type:
- COM
ms.assetid: 6986d27a-9602-e44a-0797-4c47f2184ef7
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: d255d7b6e80fe0c080fa0a27a7976db758a8c2ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439778"
---
# <a name="iattachmentsecurityisattachmentblocked"></a>IAttachmentSecurity::IsAttachmentBlocked

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Vérifie si une pièce jointe spécifiée est bloquée par Microsoft Outlook 2010 ou par Microsoft Outlook 2013 pour l'affichage et l'indexation.
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a>Paramètres

 _pwszFileName_
  
> dans Pointeur vers le nom de fichier d'une pièce jointe.
    
 _pfBlocked_
  
> remarquer Pointeur vers une valeur indiquant **true** si la pièce jointe spécifiée est bloquée; Sinon, **false**.
    
## <a name="see-also"></a>Voir aussi



[Constantes MAPI](mapi-constants.md)
  
[Vérifier qu'une pièce jointe est bloquée](how-to-verify-an-attachment-is-blocked.md)

