---
title: IMAPISessionGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetLastError
api_type:
- COM
ms.assetid: 38cb3692-a5f8-403a-9615-9bd5868af23c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 34de52693d8484abb28d2ee2f7b86f15e8bd037b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574102"
---
# <a name="imapisessiongetlasterror"></a>IMAPISession::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de session précédente. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> [in] Handle vers la valeur d’erreur généré lors de l’appel de méthode précédent.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes dans la structure **MAPIERROR** retournée dans le paramètre _lppMAPIError_ sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers une structure **MAPIERROR** qui contient les informations de version, composant et le contexte de l’erreur. Le paramètre _lppMAPIError_ peut être défini sur la valeur NULL si MAPI ne peut pas fournir les informations appropriées pour une structure **MAPIERROR** . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’indicateur MAPI_UNICODE a été défini et que la session ne prend pas en charge Unicode.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::GetLastError** récupère des informations sur la dernière erreur a été renvoyée par un appel de la méthode **IMAPISession** . Les clients peuvent fournir leurs utilisateurs avec des informations détaillées sur l’erreur en incluant ces informations dans une boîte de dialogue. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Vous pouvez utiliser la structure **MAPIERROR** , si MAPI en fournit une, désignés par if seul paramètre _lppMAPIError_ **GetLastError** renvoie S_OK. Parfois MAPI ne peut pas déterminer quelle était la dernière erreur, ou il a rien de plus de rapport sur l’erreur. Dans ce cas, **GetLastError** retourne un pointeur null dans _lppMAPIError_ à la place. 
  
Pour plus d’informations sur la méthode **GetLastError** , voir [Erreurs d’étendue MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MAPI �tendue des erreurs](mapi-extended-errors.md)

