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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bf294c7243ddc3b418c1df9de3b6981c1b950fb8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596049"
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

