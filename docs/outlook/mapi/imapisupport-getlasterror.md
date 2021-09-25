---
title: IMAPISupportGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.GetLastError
api_type:
- COM
ms.assetid: 5b4290d9-230f-416a-9644-188578565c7b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 15884634ea80b48dfade4f0ef86f617b60cd6bd4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567458"
---
# <a name="imapisupportgetlasterror"></a>IMAPISupport::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente de l’objet de support. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> [in] Handle vers la valeur d’erreur générée dans l’appel de méthode précédent pour l’objet de support.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les chaînes de la structure **MAPIERROR renvoyées** dans le paramètre  _lppMAPIError_ sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers la structure **MAPIERROR** qui contient les informations de version, de composant et de contexte de l’erreur. Le  _paramètre lppMAPIError_ peut être définie sur NULL si une structure **MAPIERROR** avec des informations d’erreur appropriées ne peut pas être fournie. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a renvoyé la ou les valeurs attendues.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’MAPI_UNICODE a été définie et MAPI ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et MAPI prend uniquement en charge Unicode.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::GetLastError** est implémentée pour tous les objets de prise en charge. Les appelants peuvent fournir à leurs utilisateurs des informations détaillées sur l’erreur en incluant les données de la structure **MAPIERROR** dans une boîte de dialogue. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez utiliser le pointeur vers la structure **MAPIERROR,** si MAPI en fournit un, dans le paramètre  _lppMAPIError_ uniquement si **GetLastError** renvoie S_OK. Parfois, MAPI ne peut pas déterminer la dernière erreur ou il n’a rien d’autre à signaler sur l’erreur. Dans ce cas,  _lppMAPIError_ renvoie un pointeur vers NULL à la place. 
  
Pour plus d’informations **sur la méthode GetLastError,** voir [MAPI Extended Errors](mapi-extended-errors.md).
  
Pour libérer toute la mémoire allouée par MAPI, appelez la [fonction MAPIFreeBuffer](mapifreebuffer.md) pour la structure **MAPIERROR renvoyée.** 
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)


[Erreurs étendues MAPI](mapi-extended-errors.md)

