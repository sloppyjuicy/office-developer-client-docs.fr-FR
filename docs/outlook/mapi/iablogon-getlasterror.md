---
title: IABLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.GetLastError
api_type:
- COM
ms.assetid: d157e29e-7731-4e47-b4a7-e8622b223001
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a6cd6750e2b0e9479b619ff1ae0f2f22738dc843
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62464195"
---
# <a name="iablogongetlasterror"></a>IABLogon::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de fournisseur de carnet d’adresses précédente. 
  
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
  
> [out] Pointeur vers un pointeur vers une structure **MAPIERROR** qui contient les informations de version, de composant et de contexte de l’erreur. Le  _paramètre lppMAPIError_ peut être définie sur NULL si le fournisseur ne peut pas fournir une structure **MAPIERROR** avec les informations appropriées. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’indicateur MAPI_UNICODE a été définie et le fournisseur de carnet d’adresses ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et le fournisseur de carnet d’adresses prend uniquement en charge Unicode.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de carnet d’adresses **implémentent la méthode GetLastError** pour fournir des informations sur un appel de méthode antérieur qui a échoué. Les appelants peuvent fournir à leurs utilisateurs des informations détaillées sur l’erreur en incluant les données de la structure **MAPIERROR** dans une boîte de dialogue. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez utiliser la structure **MAPIERROR** pointée par le paramètre  _lppMAPIError_ si le fournisseur de carnet d’adresses fournit la structure et uniquement si **GetLastError** renvoie S_OK. Parfois, le fournisseur de carnet d’adresses ne peut pas déterminer la dernière erreur ou n’a rien d’autre à signaler à propos de l’erreur. Dans ce cas, le fournisseur de carnet d’adresses renvoie un pointeur vers NULL dans  _lppMAPIError_ à la place. 
  
Pour plus d’informations **sur la méthode GetLastError** , voir [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

