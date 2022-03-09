---
title: IMAPIPropGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.GetLastError
api_type:
- COM
ms.assetid: f64a765d-c653-4eef-a0fc-24a54968757c
ms.openlocfilehash: 686d15cb9a1d0468d3c6440c100a80a3a373cbce
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379688"
---
# <a name="imapipropgetlasterror"></a>IMAPIProp::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> [in] Handle vers le code d’erreur généré dans l’appel de méthode précédent.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui indique le format du texte renvoyé dans la structure **MAPIERROR** pointée par  _lppMAPIError_. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les chaînes doivent être au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes doivent être au format ANSI.
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers la structure **MAPIERROR** qui contient les informations de version, de composant et de contexte de l’erreur. Le  _paramètre lppMAPIError_ peut être définie sur NULL s’il n’existe aucune information d’erreur à renvoyer. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les informations d’erreur ont été renvoyées.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIProp::GetLastError** fournit des informations sur un appel de méthode antérieur qui a échoué. Les clients peuvent fournir à leurs utilisateurs des informations détaillées sur l’erreur en incluant les données de la structure **MAPIERROR** dans une boîte de dialogue. 
  
Toutes les implémentations de **GetLastError** fournies par MAPI sont des implémentations ANSI, à l’exception de l’implémentation [IAddrBook](iaddrbookimapiprop.md) . La **méthode GetLastError incluse** avec **IAddrBook** prend en charge Unicode. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Les détails de l’implémentation de cette méthode par un fournisseur de transport distant et les messages qu’elle renvoie sont dus au fournisseur de transport, car les conditions d’erreur particulières qui entraînent diverses valeurs HRESULT sont différentes pour différents fournisseurs de transport.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez utiliser la structure **MAPIERROR** pointée par le paramètre  _lppMAPIError_ , si **GetLastError** en fournit un, uniquement si la valeur de retour est S_OK. Parfois **, GetLastError ne** peut pas déterminer la dernière erreur ou n’a rien d’autre à signaler à propos de l’erreur. Dans ce cas, un pointeur vers NULL est renvoyé dans  _lppMAPIError_ à la place. 
  
Pour libérer la mémoire de la structure **MAPIERROR** , appelez la [fonction MAPIFreeBuffer](mapifreebuffer.md) . 
  
Pour plus d’informations **sur la méthode GetLastError** , voir [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Voir aussi



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Erreurs étendues MAPI](mapi-extended-errors.md)

