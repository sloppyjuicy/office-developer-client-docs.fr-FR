---
title: IProfAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.GetLastError
api_type:
- COM
ms.assetid: bb161d7b-ae5b-4f8e-a506-8346ac5e583d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 61da9b3eb173c8d33dfc0d2c29d39f03895f47c1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587887"
---
# <a name="iprofadmingetlasterror"></a>IProfAdmin::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite sur un objet d’administration de profil. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> [in] Type de données HRESULT qui contient la valeur d’erreur générée dans l’appel de méthode précédent.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les chaînes de la structure [MAPIERROR renvoyées](mapierror.md) dans le paramètre  _lppMAPIError_ sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers la structure **MAPIERROR** qui contient les informations de version, de composant et de contexte de l’erreur. Le  _paramètre lppMAPIError_ peut avoir la valeur NULL s’il n’existe aucune structure **MAPIERROR** à renvoyer. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’indicateur MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.
    
## <a name="remarks"></a>Remarques

La **méthode IProfAdmin::GetLastError** récupère des informations sur la dernière erreur renvoyée par un appel de méthode pour l’objet d’administration de profil. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez utiliser la structure **MAPIERROR,** si MAPI en fournit un, pointée par le paramètre  _lppMAPIError_ uniquement si **GetLastError** renvoie S_OK. Parfois, MAPI ne peut pas déterminer la dernière erreur ou n’a rien d’autre à signaler sur l’erreur. Dans ce cas, un pointeur vers NULL est renvoyé dans  _lppMAPIError_. 
  
Pour libérer toute la mémoire allouée par MAPI pour la structure **MAPIERROR,** appelez la [fonction MAPIFreeBuffer.](mapifreebuffer.md) 
  
Pour plus d’informations sur **la méthode GetLastError,** voir [Using Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

