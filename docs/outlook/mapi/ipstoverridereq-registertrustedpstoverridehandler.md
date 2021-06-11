---
title: IPSTOVERRIDEREQRegisterTrustedPSTOverrideHandler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ.RegisterTrustedPSTOverrideHandler
api_type:
- COM
ms.assetid: 4a73c77c-7e32-4302-bffe-a1ea13574731
description: 'Last modified: February 24, 2013'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279534"
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

## <a name="parameters"></a>Parameters

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

