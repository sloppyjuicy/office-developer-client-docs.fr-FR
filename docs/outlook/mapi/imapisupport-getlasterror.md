---
title: IMAPISupportGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetLastError
api_type:
- COM
ms.assetid: 5b4290d9-230f-416a-9644-188578565c7b
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: c34c175c43ada03e982f08a27f675448ea24a567
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316591"
---
# <a name="imapisupportgetlasterror"></a>IMAPISupport::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur de l'objet de prise en charge précédent. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> dans Handle de la valeur d'erreur générée dans l'appel de méthode précédent pour l'objet support.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le type de chaînes renvoyées. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les chaînes de la structure **MAPIERROR** renvoyées dans le paramètre _lppMAPIError_ sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> remarquer Pointeur vers un pointeur vers la structure **MAPIERROR** qui contient les informations de version, de composant et de contexte pour l'erreur. Le paramètre _lppMAPIError_ peut être défini sur null si une structure **MAPIERROR** avec des informations d'erreur appropriées ne peut pas être fournie. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi et a renvoyé la ou les valeurs attendues.
    
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et MAPI ne prend pas en charge Unicode, ou MAPI_UNICODE n'est pas défini et MAPI ne prend en charge que l'Unicode.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: GetLastError** est implémentée pour tous les objets de prise en charge. Les appelants peuvent fournir à leurs utilisateurs des informations détaillées sur l'erreur en incluant les données de la structure **MAPIERROR** dans une boîte de dialogue. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez utiliser le pointeur vers la structure **MAPIERROR** , si MAPI en fournit un, uniquement dans le paramètre _lppMAPIError_ si **GetLastError** renvoie S_OK. Parfois, MAPI ne peut pas déterminer la dernière erreur ou il n'a rien de plus à signaler à propos de l'erreur. Dans ce cas, _lppMAPIError_ renvoie un pointeur vers null à la place. 
  
Pour plus d'informations sur la méthode **GetLastError** , consultez la rubrique [erreurs étendues MAPI](mapi-extended-errors.md).
  
Pour libérer toute la mémoire allouée par MAPI, appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour la structure **MAPIERROR** renvoyée. 
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)


[Erreurs étendues MAPI](mapi-extended-errors.md)

