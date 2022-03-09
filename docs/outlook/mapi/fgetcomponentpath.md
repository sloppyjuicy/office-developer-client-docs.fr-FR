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
ms.openlocfilehash: b7456311e3ad9d0e091221f75fcca20450457fe9
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381753"
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
  
> [in] Clé de registre MSIComponentID décrite dansMapi32.dll [ registre Stub Paramètres](https://msdn.microsoft.com/library/dd162409.aspx).
    
 _szQualifier_
  
> [in] Sous-clé MSIApplicationLCID ou MSIOfficeLCID décrite dans Choisir une version spécifique de [MAPI à charger](how-to-choose-a-specific-version-of-mapi-to-load.md). Les appelants peuvent passer la **valeur null** s’il n’existe aucun qualificateur. 
    
 _szDllPath_
  
> [in] Chemin d’accès au Mapi32.dll privé, qui dispose de toutes les fonctionnalités MAPI (les mêmes exportations que le Mapi32.dll).
    
 _cchBufferSize_
  
> [in] Taille de  _szDllPath_, en caractères.
    
 _fInstall_
  
> [in] Indique à MAPI d’installer le Mapi32.dll privé s’il est absent.
    
## <a name="return-value"></a>Valeur renvoyée

 **true**
  
> Le chemin d’accès a été trouvé.
    
 **false**
  
> Le chemin d’accès est in trouvé.
    
## <a name="remarks"></a>Remarques

Utilisez la **fonction FGetComponentPath** lorsque vous avez besoin d’obtenir le chemin d’accès à la Mapi32.dll. 
  
## <a name="see-also"></a>Voir aussi



[Choisir une version spécifique de MAPI à charger](how-to-choose-a-specific-version-of-mapi-to-load.md)


[Mapi32.dll registre Stub Paramètres](https://msdn.microsoft.com/library/dd162409.aspx)

