---
title: IMAPIPropGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetLastError
api_type:
- COM
ms.assetid: f64a765d-c653-4eef-a0fc-24a54968757c
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 67aa5b3d85de3df659b5aa1a351ec0d1dcf90248
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783896"
---
# <a name="imapipropgetlasterror"></a>IMAPIProp::GetLastError

  
  
**S’applique à**: Outlook 
  
Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> [in] Handle vers le code d’erreur généré lors de l’appel de méthode précédent.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui indique le format du texte retourné dans la structure **MAPIERROR** désignée par _lppMAPIError_. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes doivent être au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes doivent être au format ANSI.
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers la structure **MAPIERROR** qui contient les informations de version, composant et le contexte de l’erreur. Le paramètre _lppMAPIError_ peut être défini sur NULL s’il n’existe aucune information d’erreur à renvoyer. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Les informations d’erreur a été renvoyées.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIProp::GetLastError** fournit des informations sur un appel de méthode antérieurs ayant échoué. Les clients peuvent fournir leurs utilisateurs avec des informations détaillées sur l’erreur en incluant les données à partir de la structure **MAPIERROR** dans une boîte de dialogue. 
  
Toutes les implémentations de **GetLastError** fourni par MAPI sont mises en œuvre ANSI, à l’exception de l’implémentation de [IAddrBook](iaddrbookimapiprop.md) . La méthode **GetLastError** incluse avec **IAddrBook** prend en charge Unicode. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Les détails d’une distance de transport du fournisseur d’implémentation de cette méthode et quels sont les messages, que cette méthode retourne le fournisseur de transport, étant donné que les conditions d’erreur spécifique qui mènent à des différentes valeurs HRESULT sera différentes pour le transport différents fournisseurs.
  
## <a name="notes-to-callers"></a>Notes aux appelants

Vous pouvez utiliser la structure **MAPIERROR** désignée par le paramètre _lppMAPIError_ , si **GetLastError** fournit un, uniquement si la valeur renvoyée est S_OK. Il est parfois **GetLastError** ne peut pas déterminer la dernière erreur a été ou n’a rien de plus de rapport sur l’erreur. Dans ce cas, un pointeur vers la valeur NULL est retourné dans _lppMAPIError_ à la place. 
  
Pour libérer de la mémoire pour la structure **MAPIERROR** , appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Pour plus d’informations sur la méthode **GetLastError** , voir [Erreurs d’étendue MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>Voir aussi



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MAPI étendue des erreurs](mapi-extended-errors.md)

