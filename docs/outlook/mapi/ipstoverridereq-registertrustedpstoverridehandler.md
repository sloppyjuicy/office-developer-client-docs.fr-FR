---
title: IPSTOVERRIDEREQRegisterTrustedPSTOverrideHandler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTOVERRIDEREQ.RegisterTrustedPSTOverrideHandler
api_type:
- COM
ms.assetid: 4a73c77c-7e32-4302-bffe-a1ea13574731
description: 'Last modified: February 24, 2013'
ms.openlocfilehash: c7c074bbfb365d8a975bee12c5611c4d0809dc1e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620533"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a>IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lance la procédure de déverrouillage pour un fichier de dossiers personnels (.pst).
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a>Paramètres

 _pwzDllPath_
  
> [in] Pointeur vers le chemin d’accès d’une bibliothèque de liens dynamiques (DLL) tierce.
    
 _pvClientData_
  
> [in] Pointeur vers les données client, qui seront transmises par le fournisseur PST dans les appels ultérieurs à la fonction HrTrustedPSTOverrideHandlerCallback de la DLL. Ces données client peuvent être utilisées par la DLL pour vous aider à vérifier si le PST doit être déverrouillé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L’appel de fonction a réussi.
    
## <a name="remarks"></a>Remarques

La DLL spécifiée par le paramètre wzDllPath doit être signée à l’aide d’un certificat numérique. La DLL doit également exporter une fonction avec la signature suivante.
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

Cette fonction est appelée avec un pointeur vers l’objet IMsgStore pour le PST, un pointeur vers un objet IUnknown qui implémente l’interface IPSTOVERRIDE1 et un pointeur vers les données fournies à l’origine par pvClientData.
  
Pour plus d’informations, voir Comment implémenter un handler de remplacement PST pour contourner la stratégie [PSTDisableGrow dans Outlook 2007](https://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Voir aussi



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

