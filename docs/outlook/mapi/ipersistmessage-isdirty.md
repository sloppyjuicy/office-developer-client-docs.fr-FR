---
title: IPersistMessageIsDirty
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPersistMessage.IsDirty
api_type:
- COM
ms.assetid: 57f688db-3a1c-49ff-a15a-8508bda5de68
ms.openlocfilehash: bd37c173aadb12a7f329d93005a8d9aeea9839e3
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370357"
---
# <a name="ipersistmessageisdirty"></a>IPersistMessage::IsDirty

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recherche dans le formulaire les modifications apportées depuis le dernier sauvegarde.
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a>Paramètres

Aucun
  
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le formulaire a des modifications qui ont été apportées depuis son dernier enregistré.
    
S_FALSE 
  
> Le formulaire ne comprend pas de modifications qui ont été apportées depuis son dernier enregistré.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IPersistMessage::IsDirty** pour déterminer si le message possède des données nonavées. 
  
## <a name="see-also"></a>Voir aussi



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

