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
ms.openlocfilehash: ef5fee7a2e84133f88a00703f7602831d26e3d3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594725"
---
# <a name="imapicontrolgetlasterror"></a>IMAPIControl::GetLastError

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de contrôle de bouton précédent. 
  
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
  
> [in] Masque de bits d’indicateurs qui contrôle le type des chaînes renvoyées. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes dans la structure **MAPIERROR** retournée dans le paramètre _lppMAPIError_ sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers une structure **MAPIERROR** qui contient les informations de version, composant et le contexte de l’erreur. Le paramètre _lppMAPIError_ peut être défini sur la valeur NULL si le fournisseur ne peut pas fournir une structure **MAPIERROR** avec les informations appropriées. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.
    
## <a name="remarks"></a>Remarques

Fournisseurs de services implémentent la méthode **IMAPIControl::GetLastError** pour fournir des informations relatives à un appel de méthode antérieurs ayant échoué. MAPI peut fournir des utilisateurs des informations détaillées sur l’erreur en affichant les données à partir de la structure **MAPIERROR** dans une zone de message ou de la boîte de dialogue. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Il est inutile de disposer d’informations à inclure dans la structure **MAPIERROR** pour chaque erreur. Il peut être pas possible de déterminer quel est l’erreur précédente. Si vous disposez des informations, renvoie S_OK et les données appropriées dans la structure **MAPIERROR** . Si aucune information n’est disponible, renvoie S_OK et un pointeur null pour le paramètre _lppMAPIError_ . 
  
Pour plus d’informations sur la méthode **GetLastError** , voir [Erreurs d’étendue MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

