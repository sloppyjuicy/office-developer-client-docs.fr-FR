---
title: IMAPITableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetLastError
api_type:
- COM
ms.assetid: 832e2c18-ddba-4d18-a391-710d21fe23e6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2444ea7e05367423e7920be3a871c2ab68aad76d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419001"
---
# <a name="imapitablegetlasterror"></a>IMAPITable::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une structure [MAPIERROR](mapierror.md) contenant des informations sur l’erreur précédente sur le tableau. 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
> [in] HRESULT contenant l’erreur générée dans l’appel de méthode précédent.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type des chaînes renvoyées. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les chaînes de la structure **MAPIERROR renvoyées** dans le paramètre  _lppMAPIError_ sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers la structure **MAPIERROR renvoyée** contenant les informations de version, de composant et de contexte de l’erreur. Le  _paramètre lppMAPIError_ peut être définie sur NULL si une structure **MAPIERROR** avec les informations appropriées ne peut pas être fournie. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’indicateur MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPITable::GetLastError** renvoie des informations détaillées, si elles sont disponibles, sur un appel de méthode antérieur qui a échoué. Ces informations peuvent être affichées dans un message ou une boîte de dialogue. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez **GetLastError chaque** fois que vous avez besoin d’afficher des informations sur une erreur à l’utilisateur. 
  
Vous pouvez utiliser la structure [MAPIERROR](mapierror.md) pointée par le paramètre  _lppMAPIError_ si l’objet table en fournit un uniquement si **GetLastError** renvoie S_OK. Parfois, l’implémentation de la table ne peut pas déterminer la dernière erreur ou n’a rien d’autre à signaler à propos de l’erreur. Dans ce cas, le pointeur de  _lppMAPIError_ est définie sur NULL. 
  
Pour libérer toute la mémoire allouée à la structure **MAPIERROR,** appelez la [fonction MAPIFreeBuffer.](mapifreebuffer.md) 
  
Pour plus d’informations **sur la méthode GetLastError,** voir [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

