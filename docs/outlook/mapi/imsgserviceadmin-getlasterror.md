---
title: IMsgServiceAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetLastError
api_type:
- COM
ms.assetid: 9e3c8d6e-74be-46a7-94ed-74a969caf165
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 302aebd0be78c833acf4f82d2bb815ba46ae6f77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412141"
---
# <a name="imsgserviceadmingetlasterror"></a>IMsgServiceAdmin::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur la dernière erreur survenue pour un objet d'administration de service de messagerie. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> dans Un type de données HRESULT qui contient la valeur d'erreur générée par l'appel de méthode précédent.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le type de chaînes renvoyées. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les chaînes de la structure **MAPIERROR** renvoyées dans le paramètre _lppMAPIError_ sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> remarquer Pointeur vers un pointeur vers la structure **MAPIERROR** renvoyée qui contient les informations de version, de composant et de contexte pour l'erreur. Le paramètre _lppMAPIError_ peut être défini sur null s'il n'existe aucune structure **MAPIERROR** à renvoyer. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et l'objet d'administration du service de messagerie ne prend pas en charge Unicode.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin:: GetLastError** extrait des informations sur la dernière erreur renvoyée par un appel de la méthode [IMsgServiceAdmin](imsgserviceadminiunknown.md) . Les clients peuvent fournir à leurs utilisateurs des informations détaillées sur l'erreur en incluant ces informations dans une boîte de dialogue. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez utiliser la structure **MAPIERROR** , si la fonction MAPI en fournit une, pointée par le paramètre _LppMAPIError_ uniquement si **GetLastError** renvoie S_OK. Parfois, MAPI ne peut pas déterminer quelle est la dernière erreur ou n'a rien d'autre pour signaler l'erreur. Dans ce cas, **GetLastError** renvoie un pointeur vers une valeur null dans _lppMAPIError_ à la place. 
  
Pour plus d'informations sur la méthode **GetLastError** , consultez la rubrique [utilisation d'erreurs étendues](mapi-extended-errors.md).
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

