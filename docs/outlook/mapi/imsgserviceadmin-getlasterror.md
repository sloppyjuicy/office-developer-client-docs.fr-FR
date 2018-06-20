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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 7ce81e419a4092bd99e5082810ea9d08cb2cc163
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784234"
---
# <a name="imsgserviceadmingetlasterror"></a>IMsgServiceAdmin::GetLastError

  
  
**S’applique à**: Outlook 
  
Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur la dernière erreur qui s’est produite pour un objet de l’administration de service de message. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> [in] Un type de données HRESULT qui contient la valeur d’erreur générée par l’appel de méthode précédent.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes dans la structure **MAPIERROR** retournée dans le paramètre _lppMAPIError_ sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers la structure **MAPIERROR** retournée qui contient les informations de version, composant et le contexte de l’erreur. Le paramètre _lppMAPIError_ peut être défini sur la valeur NULL s’il n’existe aucune structure **MAPIERROR** pour renvoyer. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’indicateur MAPI_UNICODE a été défini et que l’objet d’administration de service de message ne prend pas en charge Unicode.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin::GetLastError** récupère des informations sur la dernière erreur a été renvoyée par un appel de méthode [IMsgServiceAdmin](imsgserviceadminiunknown.md) . Les clients peuvent fournir leurs utilisateurs avec des informations détaillées sur l’erreur en incluant ces informations dans une boîte de dialogue. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Vous pouvez vous servir de la **MAPIERROR** structure, si MAPI fournit un, désignés par le paramètre _lppMAPIError_ uniquement si **GetLastError** renvoie S_OK. Il est parfois MAPI ne peut pas déterminer la dernière erreur a été ou n’a rien de plus de rapport sur l’erreur. Dans ce cas, **GetLastError** retourne un pointeur null dans _lppMAPIError_ à la place. 
  
Pour plus d’informations sur la méthode **GetLastError** , voir [Erreurs d’étendue à l’aide](mapi-extended-errors.md).
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

