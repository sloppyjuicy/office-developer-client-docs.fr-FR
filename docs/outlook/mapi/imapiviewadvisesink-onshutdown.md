---
title: IMAPIViewAdviseSinkOnShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewAdviseSink.OnShutdown
api_type:
- COM
ms.assetid: c9c3aecf-5e4b-407a-8ea1-6211b4c6e0a5
ms.openlocfilehash: 8bbcbac93d8a61adde6d3818fcf9e4a9641eaf13
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369937"
---
# <a name="imapiviewadvisesinkonshutdown"></a>IMAPIViewAdviseSink::OnShutdown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avertit la visionneuse de formulaire qu’un formulaire est en cours de fermeture.
  
```cpp
HRESULT OnShutdown( void );
```

## <a name="parameters"></a>Paramètres

Aucun
  
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La notification a réussi.
    
## <a name="remarks"></a>Remarques

Pour plus d’informations sur les notifications de formulaire, voir [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

