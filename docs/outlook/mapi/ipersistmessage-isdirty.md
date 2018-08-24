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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 0d2ae556f4dd98b5f6e274a21c608d4ea364d4ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576203"
---
# <a name="ipersistmessageisdirty"></a>IPersistMessage::IsDirty

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Vérifie le formulaire pour que les modifications qui ont été apportées depuis le dernier enregistrement.
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a>Paramètres

Aucune
  
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le formulaire comporte des modifications qui ont été apportées depuis son dernier enregistrement.
    
S_FALSE 
  
> Le formulaire n’a pas de modifications qui ont été apportées depuis son dernier enregistrement.
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appeler la méthode **IPersistMessage::IsDirty** pour déterminer si le message comporte des données non enregistrées. 
  
## <a name="see-also"></a>Voir aussi



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

