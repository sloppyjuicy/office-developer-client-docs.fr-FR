---
title: IABLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetLastError
api_type:
- COM
ms.assetid: d157e29e-7731-4e47-b4a7-e8622b223001
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 311299b00143667b3f2fb22bd7be6c3a52c7141d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434248"
---
# <a name="iablogongetlasterror"></a>IABLogon::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur du fournisseur de carnet d'adresses précédent. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> dans Handle de la valeur d'erreur générée lors de l'appel de méthode précédent.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le type de chaînes renvoyées. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les chaînes de la structure **MAPIERROR** renvoyées dans le paramètre _lppMAPIError_ sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> remarquer Pointeur vers un pointeur vers une structure **MAPIERROR** qui contient les informations de version, de composant et de contexte pour l'erreur. Le paramètre _lppMAPIError_ peut être défini sur null si le fournisseur ne peut pas fournir une structure **MAPIERROR** avec les informations appropriées. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et le fournisseur de carnet d'adresses ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et le fournisseur de carnet d'adresses prend en charge uniquement Unicode.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de carnets d'adresses implémentent la méthode **GetLastError** pour fournir des informations sur un appel de méthode précédent qui a échoué. Les appelants peuvent fournir à leurs utilisateurs des informations détaillées sur l'erreur en incluant les données de la structure **MAPIERROR** dans une boîte de dialogue. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez utiliser la structure **MAPIERROR** vers laquelle pointe le paramètre _lppMAPIError_ si le fournisseur de carnet d'adresses fournit la structure et uniquement si **GetLastError** renvoie S_OK. Parfois, le fournisseur de carnets d'adresses ne peut pas déterminer la dernière erreur ou n'a rien de plus à signaler à propos de l'erreur. Dans ce cas, le fournisseur de carnet d'adresses renvoie un pointeur vers une valeur NULL dans _lppMAPIError_ à la place. 
  
Pour plus d'informations sur la méthode **GetLastError** , consultez la rubrique [erreurs étendues MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

