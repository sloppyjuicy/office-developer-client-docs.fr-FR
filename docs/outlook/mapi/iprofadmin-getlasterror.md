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
ms.openlocfilehash: 65bf7debcae1367ccad9e109242fd4a72839a94e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584925"
---
# <a name="iprofadmingetlasterror"></a>IProfAdmin::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente s’est produite pour un objet d’administration de profil. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> [in] Un type de données HRESULT qui contient la valeur d’erreur générée lors de l’appel de méthode précédent.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes dans la structure [MAPIERROR](mapierror.md) retournée dans le paramètre _lppMAPIError_ sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers la structure **MAPIERROR** qui contient les informations de version, composant et le contexte de l’erreur. Le paramètre _lppMAPIError_ peut être défini sur la valeur NULL s’il n’existe aucune structure **MAPIERROR** pour renvoyer. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.
    
## <a name="remarks"></a>Remarques

La méthode **IProfAdmin::GetLastError** récupère des informations sur la dernière erreur renvoyée par un appel de méthode de l’objet d’administration de profil. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Vous pouvez utiliser la structure **MAPIERROR** , si MAPI en fournit une, désignés par if seul paramètre _lppMAPIError_ **GetLastError** renvoie S_OK. Il est parfois MAPI ne peut pas déterminer la dernière erreur a été ou n’a rien de plus de rapport sur l’erreur. Dans ce cas, un pointeur vers la valeur NULL est retourné dans _lppMAPIError_. 
  
Pour libérer la mémoire allouée par MAPI pour la structure **MAPIERROR** , appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Pour plus d’informations sur la méthode **GetLastError** , voir [Erreurs d’étendue à l’aide](mapi-extended-errors.md).
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

