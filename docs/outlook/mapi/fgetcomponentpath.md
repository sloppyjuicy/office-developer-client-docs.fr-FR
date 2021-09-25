---
title: FGetComponentPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FGetComponentPath
api_type:
- COM
ms.assetid: 2a303458-3283-409a-bc3b-b891f3fcfc22
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 0ad1e8ef09b3f41c46c0c321e0e3699e9e6020bc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621100"
---
# <a name="fgetcomponentpath"></a>FGetComponentPath

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie le chemin d’accès au Mapi32.dll.
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a>Paramètres

 _szComponent_
  
> [in] La clé de registre MSIComponentID décrite dans [Mapi32.dll registre Stub Paramètres](https://msdn.microsoft.com/library/dd162409.aspx).
    
 _szQualifier_
  
> [in] La sous-clé MSIApplicationLCID ou MSIOfficeLCID décrite dans [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md). Les appelants peuvent passer la **valeur null** s’il n’existe aucun qualificateur. 
    
 _szDllPath_
  
> [in] Chemin d’accès au Mapi32.dll privé, qui dispose de toutes les fonctionnalités MAPI (les mêmes exportations que le Mapi32.dll).
    
 _cchBufferSize_
  
> [in] Taille de  _szDllPath,_ en caractères.
    
 _fInstall_
  
> [in] Indique à MAPI d’installer le Mapi32.dll privé s’il est absent.
    
## <a name="return-value"></a>Valeur renvoyée

 **true**
  
> Le chemin d’accès a été trouvé.
    
 **false**
  
> Le chemin d’accès est in trouvé.
    
## <a name="remarks"></a>Remarques

Utilisez la **fonction FGetComponentPath** lorsque vous avez besoin d’obtenir le chemin d’accès au Mapi32.dll. 
  
## <a name="see-also"></a>Voir aussi



[Choisir une version spécifique de MAPI à charger](how-to-choose-a-specific-version-of-mapi-to-load.md)


[Mapi32.dll registre Stub Paramètres](https://msdn.microsoft.com/library/dd162409.aspx)

