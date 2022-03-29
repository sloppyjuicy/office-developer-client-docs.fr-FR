---
title: ScLocalPathFromUNC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScLocalPathFromUNC
api_type:
- COM
ms.assetid: ef5eb5c6-251e-4a3a-8855-7c28804a29ab
description: Recherche un chemin d’accès local équivalent au chemin d’accès UNC (Universal Naming Convention) donné pour Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: dc0b34b951d0c121954fa9c50be2826270644e9d
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455523"
---
# <a name="sclocalpathfromunc"></a>ScLocalPathFromUNC

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recherche un chemin d’accès local équivalent au chemin d’accès UNC (Universal Naming Convention) donné. 
  
|Propriété |Valeur |
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
  
> [in] Chemin d’accès au format \\[_serveur_]\[ _partage_]\[ d’un fichier ou d’un répertoire.
    
 _szLocal_
  
> [out] Chemin d’accès au format [ _lecteur:_]\[ _du_ même fichier ou répertoire que pour le paramètre  _szUNC_ . 
    
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

