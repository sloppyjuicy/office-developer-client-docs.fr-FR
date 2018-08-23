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
ms.openlocfilehash: 8b7b1db5bcc718858b01f122f53406c885998741
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593815"
---
# <a name="imapitablegetlasterror"></a>IMAPITable::GetLastError

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Retourne une structure [MAPIERROR](mapierror.md) contenant des informations sur l’erreur précédente dans le tableau. 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Paramètres

 _hResult_
  
> [in] HRESULT contenant l’erreur générée lors de l’appel de méthode précédent.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type des chaînes renvoyées. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes dans la structure **MAPIERROR** retournée dans le paramètre _lppMAPIError_ sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers la structure **MAPIERROR** retournée contenant des informations de version, composant et le contexte de l’erreur. Le paramètre _lppMAPIError_ peut être défini sur NULL si une structure **MAPIERROR** avec les informations appropriées ne peut pas être fournie. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend uniquement en charge Unicode.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::GetLastError** renvoie des informations détaillées, s’il est disponible sur un appel de méthode antérieurs ayant échoué. Ces informations peuvent être affiché dans un message ou d’une boîte de dialogue. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Appeler **GetLastError** dès que vous souhaitez afficher des informations sur une erreur à l’utilisateur. 
  
Vous pouvez vous servir de la [MAPIERROR](mapierror.md) structure indiquée par le paramètre _lppMAPIError_ si l’objet table fournit un uniquement si **GetLastError** renvoie S_OK. Parfois, l’implémentation de la table ne peut pas déterminer la dernière erreur a été ou n’a rien de plus de rapport sur l’erreur. Dans ce cas, le pointeur à _lppMAPIError_ est défini sur NULL. 
  
Pour libérer la mémoire allouée pour la structure **MAPIERROR** , appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Pour plus d’informations sur la méthode **GetLastError** , voir [Erreurs d’étendue MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

