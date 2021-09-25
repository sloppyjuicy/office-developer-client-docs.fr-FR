---
title: IMAPIViewContextGetPrintSetup
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewContext.GetPrintSetup
api_type:
- COM
ms.assetid: eaf3bafb-975d-42c8-99ea-7f9ef9c934ba
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 58eccafa4faec96de0acacd4338798dba9f110d2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556461"
---
# <a name="imapiviewcontextgetprintsetup"></a>IMAPIViewContext::GetPrintSetup

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Récupère les informations d’impression actuelles.
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type des chaînes renvoyées. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les chaînes renvoyées sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _lppFormPrintSetup_
  
> [out] Pointeur vers un pointeur vers une structure qui contient les informations d’impression.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les informations d’impression ont été récupérées avec succès.
    
## <a name="remarks"></a>Remarques

Les objets form appellent la méthode **IMAPIViewContext::GetPrintSetup** pour récupérer des informations sur la configuration de l’imprimante avant d’essayer d’imprimer le message actuel. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Allouez **les membres hDevMode** et **hDevName** de la structure [FORMPRINTSETUP](formprintsetup.md) à l’aide de la fonction Win32 **GlobalAlloc**.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si vous attendez que les membres **hDevMode** et **hDevName** de la structure **FORMPRINTSETUP** pointés par le paramètre  _lppFormPrintSetup_ soient des chaînes Unicode, définissez  _ulFlags_ sur MAPI_UNICODE. Sinon, **GetPrintSetup** retournera ces chaînes au format ANSI. 
  
Libérez **les membres hDevMode** et **hDevName** de la structure **FORMPRINTSETUP** en appelant la fonction Win32 **GlobalFree**. Libérez toute la structure **FORMPRINTSETUP** en appelant [MAPIFreeBuffer](mapifreebuffer.md). 
  
## <a name="see-also"></a>Voir aussi



[FORMPRINTSETUP](formprintsetup.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

