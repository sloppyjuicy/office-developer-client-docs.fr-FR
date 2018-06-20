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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 1c817f7ec02e79b956cdd0090ea54ea4528022ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783683"
---
# <a name="iexchangemodifytablegetlasterror"></a>IExchangeModifyTable::GetLastError

  
  
**S’applique à**: Outlook 
  
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

