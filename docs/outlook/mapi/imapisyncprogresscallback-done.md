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
ms.openlocfilehash: 8d397e12b8b24c5031e6e6d89d98134d487a815b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422347"
---
# <a name="imapisyncprogresscallbackdone"></a>IMAPISyncProgressCallback::Done

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Informe Microsoft Outlook que la synchronisation est terminée. 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a>Paramètres

 **hThreadDoneEvent**
  
> Un événement qui est renvoyé pour permettre à Microsoft Outlook de fermer le descripteur. Elle peut être NULL.
    
 **hResult**
  
> HRESULT indiquant l'état final de la progression.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="see-also"></a>Voir aussi



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

