---
title: IAttachmentSecurityIsAttachmentBlocked
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
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: e84b1c992f4b2c743f54194092cf190e4eb4aeed
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63382390"
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
