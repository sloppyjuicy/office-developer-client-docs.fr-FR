---
title: IProfAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetLastError
api_type:
- COM
ms.assetid: bb161d7b-ae5b-4f8e-a506-8346ac5e583d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b6964ecde3a78bd1e9ce0ae1dcab0342c5a21a03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430772"
---
# <a name="iprofadmingetlasterror"></a>IProfAdmin::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur précédente qui s'est produite sur un objet d'administration de profil. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> dans Un type de données HRESULT qui contient la valeur d'erreur générée lors de l'appel de la méthode précédente.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le type de chaînes renvoyées. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les chaînes de la structure [MAPIERROR](mapierror.md) renvoyées dans le paramètre _lppMAPIError_ sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> remarquer Pointeur vers un pointeur vers la structure **MAPIERROR** qui contient les informations de version, de composant et de contexte pour l'erreur. Le paramètre _lppMAPIError_ peut être défini sur null s'il n'existe aucune structure **MAPIERROR** à renvoyer. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.
    
## <a name="remarks"></a>Remarques

La méthode **IProfAdmin:: GetLastError** extrait des informations sur la dernière erreur renvoyée par un appel de méthode pour l'objet d'administration des profils. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez utiliser la structure **MAPIERROR** , si la fonction MAPI fournit un, pointée par le paramètre _LppMAPIError_ uniquement si **GetLastError** renvoie S_OK. Parfois, MAPI ne peut pas déterminer quelle est la dernière erreur ou n'a rien d'autre pour signaler l'erreur. Dans ce cas, un pointeur vers NULL est renvoyé dans _lppMAPIError_. 
  
Pour libérer toute la mémoire allouée par MAPI pour la structure **MAPIERROR** , appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Pour plus d'informations sur la méthode **GetLastError** , consultez la rubrique [utilisation d'erreurs étendues](mapi-extended-errors.md).
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

