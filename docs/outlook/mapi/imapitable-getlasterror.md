---
title: IMAPITableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetLastError
api_type:
- COM
ms.assetid: 832e2c18-ddba-4d18-a391-710d21fe23e6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2444ea7e05367423e7920be3a871c2ab68aad76d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419001"
---
# <a name="imapitablegetlasterror"></a>IMAPITable::GetLastError

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une structure [MAPIERROR](mapierror.md) contenant des informations sur l'erreur précédente sur le tableau. 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> dans HRESULT contenant l'erreur générée lors de l'appel de la méthode précédente.
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôlent le type des chaînes renvoyées. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les chaînes de la structure **MAPIERROR** renvoyées dans le paramètre _lppMAPIError_ sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> remarquer Pointeur vers un pointeur vers la structure **MAPIERROR** renvoyée contenant les informations de version, de composant et de contexte pour l'erreur. Le paramètre _lppMAPIError_ peut être défini sur null si une structure **MAPIERROR** avec des informations appropriées ne peut pas être fournie. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable:: GetLastError** renvoie des informations détaillées, si elles sont disponibles, sur un appel de méthode précédent ayant échoué. Ces informations peuvent être affichées dans un message ou une boîte de dialogue. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez **GetLastError** chaque fois que vous devez afficher des informations sur une erreur à l'utilisateur. 
  
Vous pouvez utiliser la structure [MAPIERROR](mapierror.md) vers laquelle pointe le paramètre _lppMAPIError_ si l'objet table en fournit un uniquement si **GetLastError** renvoie S_OK. Parfois, l'implémentation de la table ne peut pas déterminer la dernière erreur ou n'a rien de plus à signaler à propos de l'erreur. Dans ce cas, le pointeur sur _lppMAPIError_ est défini sur null. 
  
Pour libérer toute la mémoire allouée à la structure **MAPIERROR** , appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Pour plus d'informations sur la méthode **GetLastError** , consultez la rubrique [erreurs étendues MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

