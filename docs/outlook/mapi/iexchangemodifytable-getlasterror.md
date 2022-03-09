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
ms.openlocfilehash: 21c6b8471ed358ebe0ca162289fafdf4dd29157c
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374410"
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

