---
title: IExchangeModifyTableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IExchangeModifyTable.GetLastError
api_type:
- COM
ms.assetid: b850dc08-73c3-4b19-ae29-1892d6a2ff2f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a92089c9df921259b0df638ec94b118fa53276cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613925"
---
# <a name="iexchangemodifytablegetlasterror"></a>IExchangeModifyTable::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie des informations sur la dernière erreur qui s’est produite dans un objet table.
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> [in] Valeur de retour de la méthode qui a échoué.
    
 _ulFlags_
  
> [in] Non utilisé, avec la valeur 0 (zéro).
    
 _lppMAPIError_
  
> [out] Pointe vers une structure [MAPI MAPIERROR](mapierror.md) qui contient des informations sur la dernière erreur qui s’est produite pour un objet table. 
    
## <a name="see-also"></a>Voir aussi



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[MAPIERROR](mapierror.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

