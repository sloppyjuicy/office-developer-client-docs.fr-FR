---
title: IAttachmentSecurityIsAttachmentBlocked
description: Vérifie si une pièce jointe spécifiée est bloquée par Microsoft Outlook 2010 ou Microsoft Outlook 2013 pour l’affichage et l’indexation.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAttachmentSecurity.IsAttachmentBlocked
api_type:
- COM
ms.assetid: 6986d27a-9602-e44a-0797-4c47f2184ef7
ms.openlocfilehash: bf5cdf9ce325d033b43f4c1fed446cf4f6d4eb1a
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65818207"
---
# <a name="iattachmentsecurityisattachmentblocked"></a>IAttachmentSecurity::IsAttachmentBlocked

**S’applique à** : Outlook 2013 | Outlook 2016
  
Vérifie si une pièce jointe spécifiée est bloquée par Microsoft Outlook 2010 ou Microsoft Outlook 2013 pour l’affichage et l’indexation.
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a>Paramètres

 _pwszFileName_
  
> [in] Pointeur vers le nom de fichier d’une pièce jointe.

 _pfBlocked_
  
> [out] Pointeur vers une valeur indiquant **true** si la pièce jointe spécifiée est bloquée ; sinon, **false**.

## <a name="see-also"></a>Voir aussi

[Constantes MAPI](mapi-constants.md)
  
[Vérifier qu’une pièce jointe est bloquée](how-to-verify-an-attachment-is-blocked.md)
