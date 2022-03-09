---
title: IMAPISessionGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.GetLastError
api_type:
- COM
ms.assetid: 38cb3692-a5f8-403a-9615-9bd5868af23c
ms.openlocfilehash: f7a251a25a1c8f2b20c8a03f5e5ad4f0bcbf7683
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379940"
---
# <a name="imapisessiongetlasterror"></a>IMAPISession::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de session précédente. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> [in] Handle vers la valeur d’erreur générée dans l’appel de méthode précédent.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les chaînes de la structure **MAPIERROR renvoyées** dans le paramètre _lppMAPIError_ sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers une structure **MAPIERROR** qui contient les informations de version, de composant et de contexte de l’erreur. Le  _paramètre lppMAPIError_ peut avoir la valeur NULL si MAPI ne peut pas fournir les informations appropriées pour une structure **MAPIERROR** . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> L MAPI_UNICODE a été définie et la session ne prend pas en charge Unicode.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISession::GetLastError** récupère des informations sur la dernière erreur renvoyée par un appel de méthode **IMAPISession** . Les clients peuvent fournir à leurs utilisateurs des informations détaillées sur l’erreur en incluant ces informations dans une boîte de dialogue. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez utiliser la structure **MAPIERROR** , si MAPI en fournit un, pointée par le paramètre  _lppMAPIError_ uniquement si **GetLastError** renvoie S_OK. Parfois, MAPI ne peut pas déterminer la dernière erreur, ou il n’a rien d’autre à signaler à propos de l’erreur. Dans ce cas, **GetLastError** renvoie un pointeur vers NULL dans  _lppMAPIError_ à la place. 
  
Pour plus d’informations **sur la méthode GetLastError** , voir [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[Erreurs étendues MAPI](mapi-extended-errors.md)

