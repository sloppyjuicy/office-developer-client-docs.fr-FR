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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 8d5d4895e4440945896ee4f2212c5fca6da8610d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350861"
---
# <a name="iexchangemodifytablegetlasterror"></a>IExchangeModifyTable::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie des informations sur la dernière erreur qui s'est produite dans un objet table.
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> dans Valeur renvoyée par la méthode qui a échoué.
    
 _ulFlags_
  
> dans Non utilisé, défini sur 0 (zéro).
    
 _lppMAPIError_
  
> remarquer Pointe vers une structure [MAPIERROR](mapierror.md) MAPI qui contient des informations sur la dernière erreur survenue pour un objet table. 
    
## <a name="see-also"></a>Voir aussi



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[MAPIERROR](mapierror.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

