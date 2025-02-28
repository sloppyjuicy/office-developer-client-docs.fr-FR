---
title: IPSTOVERPLATEEQRegisterTrustedPSTOverrideHandler
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
description: 'Dernière modification : 24 février 2013'
ms.openlocfilehash: ac8fd8ff7e943a59325351f1cace0c495000ed15
ms.sourcegitcommit: 600f0dc552b725f98f3354d42feefc39be9c354c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2022
ms.locfileid: "66577364"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a>IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lance la procédure de déverrouillage pour un fichier Dossiers personnels (.pst).
  
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
  
> [in] Pointeur vers les données clientes, qui sera passé par le fournisseur PST dans les appels suivants à la fonction HrTrustedPSTOverrideHandlerCallback de la DLL. Ces données clientes peuvent être utilisées par la DLL pour vous aider à vérifier si le PST doit être déverrouillé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L’appel de fonction a réussi.
    
## <a name="remarks"></a>Remarques

La DLL spécifiée par le paramètre wzDllPath doit être signée à l’aide d’un certificat numérique. La DLL doit également exporter une fonction avec la signature suivante.
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

Cette fonction sera appelée avec un pointeur vers l’objet IMsgStore pour le PST, un pointeur vers un objet IUnknown qui implémente l’interface IPSTOVERRIDE1 et un pointeur vers les données fournies à l’origine via pvClientData.
  
<!-- For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).
   -->
## <a name="see-also"></a>Voir aussi



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

