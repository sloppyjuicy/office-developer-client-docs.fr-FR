---
title: IMAPISyncProgressCallbackDone
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Done
api_type:
- COM
ms.assetid: aaa8eb56-f22f-4c5a-a224-807ff001e0ca
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: cdd3db3f3779c2078b90352e19f8da6b29cffb8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573206"
---
# <a name="imapisyncprogresscallbackdone"></a>IMAPISyncProgressCallback::Done

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
 Informe Microsoft Outlook que la synchronisation est terminée. 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a>Paramètres

 **hThreadDoneEvent**
  
> Un événement qui est passé précédent pour permettre à Microsoft Outlook fermer le handle. Il peut être NULL.
    
 **hResult**
  
> Une valeur HRESULT indiquant l’état final de la progression.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="see-also"></a>Voir aussi



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

