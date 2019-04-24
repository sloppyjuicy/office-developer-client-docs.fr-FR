---
title: IPersistMessageIsDirty
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.IsDirty
api_type:
- COM
ms.assetid: 57f688db-3a1c-49ff-a15a-8508bda5de68
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 91985d3dc8a7816c3da3215e505097c57c63e035
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309610"
---
# <a name="ipersistmessageisdirty"></a>IPersistMessage::IsDirty

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Vérifie si le formulaire a été modifié depuis le dernier enregistrement.
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a>Paramètres

Aucun
  
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le formulaire comporte des modifications qui ont été effectuées depuis son dernier enregistrement.
    
S_FALSE 
  
> Le formulaire ne comporte pas de modifications effectuées depuis son dernier enregistrement.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IPersistMessage:: IsDirty** pour déterminer si le message contient des données non enregistrées. 
  
## <a name="see-also"></a>Voir aussi



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

