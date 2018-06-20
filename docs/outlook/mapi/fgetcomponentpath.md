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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e4bce7f122522532023d18b43fe4bfdeda84af9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783291"
---
# <a name="fgetcomponentpath"></a>FGetComponentPath

  
  
**S’applique à**: Outlook 
  
Renvoie le chemin d’accès pour le fichier Mapi32.dll privé.
  
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
  
> [in] La clé de Registre MSIComponentID décrite dans les [Paramètres de Registre Stub Mapi32.dll](http://msdn.microsoft.com/en-us/library/dd162409.aspx).
    
 _szQualifier_
  
> [in] La sous-clé MSIApplicationLCID ou MSIOfficeLCID décrite dans la zone [Choisissez une Version spécifique de MAPI à charge](how-to-choose-a-specific-version-of-mapi-to-load.md). Les appelants peuvent passer **null** s’il n’existe aucun qualificateur. 
    
 _szDllPath_
  
> [in] Le chemin d’accès pour le fichier Mapi32.dll privée, qui comprend toutes les fonctionnalités MAPI (exportations même en tant que le fichier Mapi32.dll).
    
 _cchBufferSize_
  
> [in] Taille de _szDllPath_, en caractères.
    
 _fInstall_
  
> [in] Indique à MAPI pour installer le composant Mapi32.dll privé si elle est absente.
    
## <a name="return-value"></a>Valeur renvoy�e

 **valeur True**
  
> Le chemin d’accès a été trouvé.
    
 **False**
  
> Le chemin d’accès est introuvable.
    
## <a name="remarks"></a>Remarques

Utilisez la fonction **FGetComponentPath** lorsque vous avez besoin obtenir le chemin d’accès pour le fichier Mapi32.dll privé. 
  
## <a name="see-also"></a>Voir aussi



[Choisissez une Version spécifique de MAPI à charge](how-to-choose-a-specific-version-of-mapi-to-load.md)


[Paramètres de Registre Stub Mapi32.dll](http://msdn.microsoft.com/en-us/library/dd162409.aspx)

