---
title: IExchangeModifyTableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetLastError
api_type:
- COM
ms.assetid: b850dc08-73c3-4b19-ae29-1892d6a2ff2f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f0d2ad118346dd06788af972b64b10d6f6f6d0fc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594291"
---
# <a name="iexchangemodifytablegetlasterror"></a>IExchangeModifyTable::GetLastError

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Retourne des informations sur la dernière erreur qui s’est produite dans un objet table.
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> [in] La valeur renvoyée par la méthode qui a échoué.
    
 _ulFlags_
  
> [in] Ne pas utilisé, la valeur 0 (zéro).
    
 _lppMAPIError_
  
> [out] Pointe vers une structure MAPI [MAPIERROR](mapierror.md) qui contient des informations sur la dernière erreur qui s’est produite pour un objet table. 
    
## <a name="see-also"></a>Voir aussi



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[MAPIERROR](mapierror.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

