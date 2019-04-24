---
title: IMAPIPropGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetLastError
api_type:
- COM
ms.assetid: f64a765d-c653-4eef-a0fc-24a54968757c
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 8c31cbf0472d3d64c7327fcfc80480ef27a1638e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342048"
---
# <a name="imapipropgetlasterror"></a>IMAPIProp::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur précédente. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> dans Handle du code d'erreur généré dans l'appel de méthode précédent.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui indique le format du texte renvoyé dans la structure **MAPIERROR** vers laquelle pointe le _lppMAPIError_. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les chaînes doivent être au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes doivent être au format ANSI.
    
 _lppMAPIError_
  
> remarquer Pointeur vers un pointeur vers la structure **MAPIERROR** qui contient les informations de version, de composant et de contexte pour l'erreur. Le paramètre _lppMAPIError_ peut être défini sur null s'il n'y a aucune information d'erreur à renvoyer. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les informations relatives à l'erreur ont été renvoyées.
    
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIProp:: GetLastError** fournit des informations sur un appel de méthode précédent qui a échoué. Les clients peuvent fournir à leurs utilisateurs des informations détaillées sur l'erreur en incluant les données de la structure **MAPIERROR** dans une boîte de dialogue. 
  
Toutes les implémentations de **GetLastError** fournies par MAPI sont des implémentations ANSI, à l'exception de l'implémentation de [IAddrBook](iaddrbookimapiprop.md) . La méthode **GetLastError** incluse dans **IAddrBook** prend en charge Unicode. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Les détails de l'implémentation d'une méthode par un fournisseur de transport distant et les messages renvoyés par cette méthode sont envoyés au fournisseur de transport, car les conditions d'erreur spécifiques conduisant à diverses valeurs HRESULT diffèrent selon le transport. vide.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez utiliser la structure **MAPIERROR** vers laquelle pointe le paramètre _LppMAPIError_ , si **GetLastError** en fournit un, uniquement si la valeur renvoyée est S_OK. Parfois, **GetLastError** ne peut pas déterminer la dernière erreur ou n'a rien de plus à signaler à propos de l'erreur. Dans ce cas, un pointeur vers une valeur NULL est renvoyé dans _lppMAPIError_ à la place. 
  
Pour libérer la mémoire pour la structure **MAPIERROR** , appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Pour plus d'informations sur la méthode **GetLastError** , consultez la rubrique [erreurs étendues MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>Voir aussi



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Erreurs étendues MAPI](mapi-extended-errors.md)

