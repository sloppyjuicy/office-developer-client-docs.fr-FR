---
title: IMAPIViewContextGetPrintSetup
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetPrintSetup
api_type:
- COM
ms.assetid: eaf3bafb-975d-42c8-99ea-7f9ef9c934ba
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a58e723113f70c10b5c8468f5bdd0d8d9014bd2c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425126"
---
# <a name="imapiviewcontextgetprintsetup"></a>IMAPIViewContext::GetPrintSetup

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Récupère les informations d'impression actuelles.
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de des indicateurs qui contrôlent le type des chaînes renvoyées. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les chaînes renvoyées sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.
    
 _lppFormPrintSetup_
  
> remarquer Pointeur vers un pointeur vers une structure qui contient les informations d'impression.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les informations d'impression ont été correctement récupérées.
    
## <a name="remarks"></a>Remarques

Les objets de formulaire appellent la méthode **IMAPIViewContext:: GetPrintSetup** pour récupérer des informations sur la configuration de l'imprimante avant d'essayer d'imprimer le message en cours. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

AlLouez les membres **hDevMode** et **hDevName** de la structure [FORMPRINTSETUP](formprintsetup.md) à l'aide de la fonction Win32 **GlobalAlloc**.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si vous souhaitez que les membres **hDevMode** et **hDevName** de la structure **FORMPRINTSETUP** vers laquelle pointe le paramètre _LppFormPrintSetup_ soient des chaînes Unicode, définissez _ulFlags_ sur MAPI_UNICODE. Dans le cas contraire, **GetPrintSetup** renverra ces chaînes au format ANSI. 
  
Libérez les membres **hDevMode** et **hDevName** de la structure **FORMPRINTSETUP** en appelant la fonction Win32 **GlobalFree**. Libérez toute la structure **FORMPRINTSETUP** en appelant [MAPIFreeBuffer](mapifreebuffer.md). 
  
## <a name="see-also"></a>Voir aussi



[FORMPRINTSETUP](formprintsetup.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

