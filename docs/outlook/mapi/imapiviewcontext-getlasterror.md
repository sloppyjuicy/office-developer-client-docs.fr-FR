---
title: IMAPIViewContextGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewContext.GetLastError
api_type:
- COM
ms.assetid: 3306e37a-2500-4281-96c3-ca0d5c81909d
ms.openlocfilehash: 46ef6524e83df24c06b6442ee7cac64e97970287
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376804"
---
# <a name="imapiviewcontextgetlasterror"></a>IMAPIViewContext::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite sur l’objet de contexte d’affichage. 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> [in] Type de données HRESULT qui contient la valeur d’erreur générée dans l’appel de méthode précédent.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les chaînes de la structure **MAPIERROR renvoyées** dans le paramètre _lppMAPIError_ sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers la structure **MAPIERROR** renvoyée qui contient les informations de version, de composant et de contexte de l’erreur. Ce paramètre peut être définie sur NULL s’il n’existe aucune structure **MAPIERROR** à renvoyer. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’MAPI_UNICODE a été définie et **GetLastError** ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et **GetLastError** prend uniquement en charge Unicode. 
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIViewContext::GetLastError** fournit des informations sur un appel de méthode antérieur qui a échoué. Les appelants peuvent fournir à leurs utilisateurs des informations détaillées sur l’erreur en incluant les données de la structure **MAPIERROR** dans une boîte de dialogue. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez utiliser la structure **MAPIERROR** pointée par le paramètre  _lppMAPIError_ si MAPI en fournit un uniquement si **GetLastError** renvoie S_OK. Parfois, MAPI ne peut pas déterminer la dernière erreur ou n’a rien d’autre à signaler sur l’erreur. Dans ce cas, un pointeur vers NULL est renvoyé dans  _lppMAPIError_ à la place. 
  
Pour plus d’informations **sur la méthode GetLastError** , voir [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

