---
title: IMAPIControlGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetLastError
api_type:
- COM
ms.assetid: 83290b8e-fffc-41c8-a01e-578d130b65c5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 10ac4e33b3f734ec2ce3205aa1897e0418cb563d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421150"
---
# <a name="imapicontrolgetlasterror"></a>IMAPIControl::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de contrôle de bouton précédente. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> [in] Handle vers la valeur d’erreur générée dans l’appel de méthode précédent.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type des chaînes renvoyées. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les chaînes de la structure **MAPIERROR renvoyées** dans le paramètre  _lppMAPIError_ sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers une structure **MAPIERROR** qui contient les informations de version, de composant et de contexte de l’erreur. Le  _paramètre lppMAPIError_ peut être définie sur NULL si le fournisseur ne peut pas fournir une structure **MAPIERROR** avec les informations appropriées. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> L’indicateur MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de services implémentent la méthode **IMAPIControl::GetLastError** pour fournir des informations sur un appel de méthode antérieur qui a échoué. MAPI peut fournir aux utilisateurs des informations détaillées sur l’erreur en affichant les données de la structure **MAPIERROR** dans un message ou une boîte de dialogue. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Il n’est pas nécessaire d’inclure des informations dans la structure **MAPIERROR** pour chaque erreur. Il n’est peut-être pas possible de déterminer la raison de l’erreur précédente. Si vous avez des informations, renvoyez S_OK données appropriées dans la structure **MAPIERROR.** Si aucune information n’est disponible, renvoyez S_OK et un pointeur vers NULL pour _le paramètre lppMAPIError._ 
  
Pour plus d’informations **sur la méthode GetLastError,** voir [MAPI Extended Errors](mapi-extended-errors.md).
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

