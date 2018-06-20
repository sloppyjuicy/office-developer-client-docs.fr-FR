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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 7fdf76bc56feb7e46370e7fcf66c55d229933eca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784126"
---
# <a name="imapiviewcontextgetprintsetup"></a>IMAPIViewContext::GetPrintSetup

  
  
**S’applique à**: Outlook 
  
Récupère les informations d’impression en cours.
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type des chaînes renvoyées. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes retournées sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _lppFormPrintSetup_
  
> [out] Pointeur vers un pointeur vers une structure qui contient les informations d’impression.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Les informations d’impression a été récupérées correctement.
    
## <a name="remarks"></a>Remarques

Objets formulaire appeler la méthode **IMAPIViewContext::GetPrintSetup** pour extraire des informations sur la configuration de l’imprimante avant d’imprimer le message en cours. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Allouer les membres **hDevMode** et **hDevName** de la structure [FORMPRINTSETUP](formprintsetup.md) à l’aide de la fonction Win32 **GlobalAlloc**.
  
## <a name="notes-to-callers"></a>Notes aux appelants

Si vous envisagez l' **hDevMode** et **hDevName** les membres de la structure **FORMPRINTSETUP** désignés par le paramètre _lppFormPrintSetup_ chaînes Unicode, la valeur _ulFlags_ MAPI_UNICODE. Dans le cas contraire, **GetPrintSetup** renverra ces chaînes au format ANSI. 
  
Libérer les membres **hDevMode** et **hDevName** de la structure **FORMPRINTSETUP** en appelant la fonction Win32 **GlobalFree**. Libérez de l’intégralité de la structure **FORMPRINTSETUP** en appelant [MAPIFreeBuffer](mapifreebuffer.md). 
  
## <a name="see-also"></a>Voir aussi



[FORMPRINTSETUP](formprintsetup.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

