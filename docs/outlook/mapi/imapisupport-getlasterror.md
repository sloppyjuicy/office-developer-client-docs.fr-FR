---
title: IMAPISupportGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetLastError
api_type:
- COM
ms.assetid: 5b4290d9-230f-416a-9644-188578565c7b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3e641842dd8264c0cd3556c498bd74c77bda32f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577505"
---
# <a name="imapisupportgetlasterror"></a>IMAPISupport::GetLastError

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur d’objet prise en charge précédente. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> [in] Handle vers la valeur d’erreur généré dans l’appel de méthode précédent pour l’objet de prise en charge.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes dans la structure **MAPIERROR** retournée dans le paramètre _lppMAPIError_ sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers la structure **MAPIERROR** qui contient les informations de version, composant et le contexte de l’erreur. Le paramètre _lppMAPIError_ peut être défini sur NULL si une structure **MAPIERROR** avec des informations d’erreur approprié ne peut pas être fournie. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’appel a réussi et renvoyé la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et MAPI ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et prend en charge MAPI uniquement Unicode.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::GetLastError** est implémentée pour tous les objets de prise en charge. Les appelants peuvent fournir leurs utilisateurs avec des informations détaillées sur l’erreur en incluant les données à partir de la structure **MAPIERROR** dans une boîte de dialogue. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Vous pouvez utiliser le pointeur vers la structure **MAPIERROR** , si MAPI fournit un, dans le paramètre _lppMAPIError_ uniquement si **GetLastError** renvoie S_OK. Parfois MAPI ne peut pas déterminer quelle était la dernière erreur, ou il a rien de plus à un rapport sur l’erreur. Dans ce cas, _lppMAPIError_ retourne un pointeur vers la valeur NULL à la place. 
  
Pour plus d’informations sur la méthode **GetLastError** , voir [Erreurs d’étendue MAPI](mapi-extended-errors.md).
  
Pour libérer la mémoire allouée par MAPI, appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour la structure **MAPIERROR** retournée. 
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)


[MAPI �tendue des erreurs](mapi-extended-errors.md)

