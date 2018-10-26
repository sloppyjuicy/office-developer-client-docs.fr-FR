---
title: IMAPIFormFactoryGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.GetLastError
api_type:
- COM
ms.assetid: 4b1d85f6-7996-4839-b985-abf83e305651
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b4d9838846a124b1c81ec9f9fc6309dcd37c7f2d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578142"
---
# <a name="imapiformfactorygetlasterror"></a>IMAPIFormFactory::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente à l’objet de fabrique de formulaire. 
  
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
  
> Les chaînes dans la structure **MAPIERROR** retournée dans le paramètre _lppMAPIError_ sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers la structure **MAPIERROR** retournée qui contient les informations de version, composant et le contexte de l’erreur. Ce paramètre peut être défini sur la valeur NULL s’il n’existe aucune structure **MAPIERROR** pour renvoyer. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et **GetLastError** ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et **GetLastError** prend en charge Unicode uniquement. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFormFactory::GetLastError** fournit des informations sur un appel de méthode antérieurs ayant échoué. Les appelants peuvent fournir leurs utilisateurs avec des informations détaillées sur l’erreur en incluant les données à partir de la structure **MAPIERROR** dans une boîte de dialogue. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Vous pouvez vous servir de la **MAPIERROR** structure indiquée par le paramètre _lppMAPIError_ si MAPI fournit une uniquement si **GetLastError** renvoie S_OK. Il est parfois MAPI ne peut pas déterminer la dernière erreur a été ou n’a rien de plus de rapport sur l’erreur. Dans ce cas, un pointeur vers la valeur NULL est retourné dans _lppMAPIError_ à la place. 
  
Pour plus d’informations sur la méthode **GetLastError** , voir [Erreurs d’étendue à l’aide](mapi-extended-errors.md).
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)

