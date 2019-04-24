---
title: IMAPIViewContextGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetLastError
api_type:
- COM
ms.assetid: 3306e37a-2500-4281-96c3-ca0d5c81909d
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: bcd8e977d924bae170dcad27c672b963189cfa94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351395"
---
# <a name="imapiviewcontextgetlasterror"></a>IMAPIViewContext::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur précédente qui s'est produite dans l'objet de contexte d'affichage. 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> dans Type de données HRESULT qui contient la valeur d'erreur générée lors de l'appel de la méthode précédente.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le type de chaînes renvoyées. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les chaînes de la structure **MAPIERROR** renvoyées dans le paramètre _lppMAPIError_ sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> remarquer Pointeur vers un pointeur vers la structure **MAPIERROR** renvoyée qui contient les informations de version, de composant et de contexte pour l'erreur. Ce paramètre peut être défini sur NULL s'il n'existe aucune structure **MAPIERROR** à renvoyer. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et **GetLastError** ne prend pas en charge Unicode, ou MAPI_UNICODE n'est pas défini et **GetLastError** ne prend en charge que le format Unicode. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIViewContext:: GetLastError** fournit des informations sur un appel de méthode précédent qui a échoué. Les appelants peuvent fournir à leurs utilisateurs des informations détaillées sur l'erreur en incluant les données de la structure **MAPIERROR** dans une boîte de dialogue. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez utiliser la structure **MAPIERROR** vers laquelle pointe le paramètre _lppMAPIError_ si MAPI en fournit un uniquement si **GetLastError** renvoie S_OK. Parfois, MAPI ne peut pas déterminer quelle est la dernière erreur ou n'a rien d'autre pour signaler l'erreur. Dans ce cas, un pointeur vers une valeur NULL est renvoyé dans _lppMAPIError_ à la place. 
  
Pour plus d'informations sur la méthode **GetLastError** , consultez la rubrique [erreurs étendues MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

