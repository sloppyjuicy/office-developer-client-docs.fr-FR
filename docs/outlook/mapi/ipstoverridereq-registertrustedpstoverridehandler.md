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
description: 'Dernière modification : 24 février 2013'
ms.openlocfilehash: 4fc3b7427fc13a024aab38c7b7df1d940a4730ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784432"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a>IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler

 
  
**S’applique à**: Outlook 
  
Lance la procédure de déverrouillage pour un fichier de dossiers personnels (.pst).
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a>Paramètres

 _pwzDllPath_
  
> [in] Pointeur vers le chemin d’accès d’une bibliothèque de liens dynamiques (DLL) tiers.
    
 _pvClientData_
  
> [in] Pointeur vers les données clientes qui sont passés par le fournisseur PST dans les appels suivants à la fonction la DLL HrTrustedPSTOverrideHandlerCallback. Ces données client peuvent être utilisées par la DLL pour vous aider à vérifier si le fichier PST doit être déverrouillé.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK
  
> L’appel de fonction a réussi.
    
## <a name="remarks"></a>Remarques

La DLL spécifiée par le paramètre wzDllPath doit être signée à l’aide d’un certificat numérique. La DLL doit également exporter une fonction avec la signature suivante.
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

Cette fonction est appelée avec un pointeur vers l’objet IMsgStore pour le fichier PST, un pointeur vers un objet IUnknown qui implémente l’interface IPSTOVERRIDE1 et un pointeur vers les données fournies par le biais de pvClientData.
  
Pour plus d’informations, voir [comment implémenter un gestionnaire de substitution PST pour contourner la stratégie PSTDisableGrow dans Outlook 2007](http://support.microsoft.com/kb/956070).
  
## <a name="see-also"></a>Voir aussi



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

