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
description: 'Dernière modification : 25 juin 2012'
ms.openlocfilehash: ff13866139bf422f071eaba2c146aa1140ccd1ab
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565045"
---
# <a name="iattachmentsecurityisattachmentblocked"></a>IAttachmentSecurity::IsAttachmentBlocked

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Vérifie si une pièce jointe spécifiée est bloquée par Microsoft Outlook 2010 ou Microsoft Outlook 2013 pour l’affichage et l’indexation.
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a>Paramètres

 _pwszFileName_
  
> [in] Pointeur vers le nom de fichier d’une pièce jointe.
    
 _pfBlocked_
  
> [out] Pointeur vers une valeur indiquant **la valeur true** si la pièce jointe spécifiée est bloquée ; Sinon, **false**.
    
## <a name="see-also"></a>Voir aussi



[Constantes MAPI](mapi-constants.md)
  
[Vérifiez la que pièce jointe est bloquée](how-to-verify-an-attachment-is-blocked.md)

