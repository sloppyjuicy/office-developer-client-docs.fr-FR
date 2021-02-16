---
title: ScLocalPathFromUNC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScLocalPathFromUNC
api_type:
- COM
ms.assetid: ef5eb5c6-251e-4a3a-8855-7c28804a29ab
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e7607a57da5b618a20d6c8e360c7e3cb4f933856
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432232"
---
# <a name="sclocalpathfromunc"></a>ScLocalPathFromUNC

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recherche un chemin d’accès local équivalent au chemin d’accès UNC (Universal Naming Convention) donné. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a>Paramètres

 _szUNC_
  
> [in] Un chemin d’accès au format \\ [ _serveur_] \[ _partage_] \[ _chemin_] d’un fichier ou d’un répertoire.
    
 _szLocal_
  
> [out] Chemin d’accès au format [ _lecteur :_] chemin ] du même fichier ou répertoire que pour le \[ paramètre _szUNC._ 
    
 _cchLocal_
  
> [in] Taille de la mémoire tampon pour la chaîne de sortie.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Un chemin d’accès local a été localisé.
    
MAPI_E_TOO_BIG
  
>  _szLocal n’était_ pas assez grand pour contenir le résultat. 
    
S_FALSE
  
> La chaîne UNC était déjà un chemin d’accès local.
    
MAPI_E_NOT_FOUND
  
> Un chemin d’accès local n’a pas été trouvé.
    
## <a name="see-also"></a>Voir aussi



[ScUNCFromLocalPath](scuncfromlocalpath.md)

