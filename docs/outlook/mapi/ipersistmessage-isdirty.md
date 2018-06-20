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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e748427b39418a80cae88e98b4aa7eef6df24393
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784366"
---
# <a name="ipersistmessageisdirty"></a>IPersistMessage::IsDirty

  
  
**S’applique à**: Outlook 
  
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

