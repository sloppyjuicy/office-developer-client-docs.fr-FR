---
title: FGetComponentPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FGetComponentPath
api_type:
- COM
ms.assetid: 2a303458-3283-409a-bc3b-b891f3fcfc22
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 3456d81935a0a94bc2158eefd321da968dda9983
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335209"
---
# <a name="fgetcomponentpath"></a>FGetComponentPath

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie le chemin d'accès au fichier Mapi32. dll privé.
  
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
  
> dans La clé Reg MSIComponentID décrite dans les [paramètres du Registre stub Mapi32. dll](https://msdn.microsoft.com/library/dd162409.aspx).
    
 _szQualifier_
  
> dans La sous-clé MSIApplicationLCID ou MSIOfficeLCID décrite dans [Choose a specific version of MAPI to load](how-to-choose-a-specific-version-of-mapi-to-load.md). Les appelants peuvent transmettre la **valeur null** s'il n'y a aucun qualificateur. 
    
 _szDllPath_
  
> dans Chemin d'accès au fichier Mapi32. dll privé, qui dispose de la fonctionnalité MAPI complète (les mêmes exportations que Mapi32. dll).
    
 _cchBufferSize_
  
> dans Taille de _szDllPath_, en caractères.
    
 _fInstall_
  
> dans Indique à MAPI d'installer le composant privé Mapi32. dll s'il est absent.
    
## <a name="return-value"></a>Valeur renvoyée

 **true**
  
> Le chemin d'accès a été trouvé.
    
 **true**
  
> Le chemin d'accès est introuvable.
    
## <a name="remarks"></a>Remarques

Utilisez la fonction **FGetComponentPath** lorsque vous devez obtenir le chemin d'accès au fichier Mapi32. dll privé. 
  
## <a name="see-also"></a>Voir aussi



[Choisir une version spécifique de MAPI à charger](how-to-choose-a-specific-version-of-mapi-to-load.md)


[Paramètres de Registre stub Mapi32. dll](https://msdn.microsoft.com/library/dd162409.aspx)

