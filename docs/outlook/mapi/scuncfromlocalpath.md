---
title: ScUNCFromLocalPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScUNCFromLocalPath
api_type:
- COM
ms.assetid: cc4abf1a-c08c-4462-9d7c-6af506dc07c9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4cb47ae7f880985c625e61a4ca6fc02ba1477441
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591191"
---
# <a name="scuncfromlocalpath"></a>ScUNCFromLocalPath

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recherche un chemin d’accès UNC (Universal Naming Convention) équivalent au chemin local donné.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a>Paramètres

 _szLocal_
  
> [in] Chemin d’accès au format [ _lecteur :_] \[ _chemin_] d’un fichier ou d’un répertoire.
    
 _szUNC_
  
> [out] Un chemin d’accès au format [ serveur ] partage ] chemin ] du même fichier ou répertoire que pour le \\  \[ paramètre \[  _szLocal._ 
    
 _cchUNC_
  
> [in] Taille de la mémoire tampon pour la chaîne de sortie.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L’équivalent du chemin d’accès UNC a été correctement localisé.
    
MAPI_E_INVALID_PARAMETER
  
> Un ou plusieurs paramètres ne sont pas valides.
    
MAPI_E_TOO_BIG
  
>  _szUNC_ n’était pas assez grand pour contenir le résultat. 
    
S_FALSE
  
> Le chemin d’accès local était déjà une chaîne UNC.
    
## <a name="see-also"></a>Voir aussi



[ScLocalPathFromUNC](sclocalpathfromunc.md)

