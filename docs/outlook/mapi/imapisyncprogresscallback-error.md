---
title: IMAPISyncProgressCallbackError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISyncProgressCallback.Error
api_type:
- COM
ms.assetid: 4860992d-65d7-4cb0-a874-ceccb153dbac
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d70dc611a7756c8dca15e1c173e5702a7fc86f63
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575749"
---
# <a name="imapisyncprogresscallbackerror"></a>IMAPISyncProgressCallback::Error

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit des détails affichés dans la boîte de dialogue d’envoi/réception. Si des erreurs se sont rencontrées lors de la synchronisation, le fournisseur de magasins appelle cette fonction.
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a>Paramètres

 **hResult**
  
> HRESULT de l’erreur ou de l’avertissement.
    
 **pwcszErrorStr**
  
> Pointeur vers la chaîne associée à l’erreur à afficher.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="see-also"></a>Voir aussi



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

