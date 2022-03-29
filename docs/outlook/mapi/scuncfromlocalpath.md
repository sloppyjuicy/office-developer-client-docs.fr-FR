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
description: Recherche un chemin d’accès UNC (Universal Naming Convention) équivalent au chemin local donné pour Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: 532bbc92509fabcc02d6d9379ccc1591aa6fb877
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455040"
---
# <a name="scuncfromlocalpath"></a>ScUNCFromLocalPath

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recherche un chemin d’accès UNC (Universal Naming Convention) équivalent au chemin local donné.
  
|Propriété |Valeur |
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
  
> [in] Chemin d’accès au format [ _lecteur:__]_\[ d’un fichier ou d’un répertoire.
    
 _szUNC_
  
> [out] Chemin d’accès au format \\[ _serveur_]\[ _partage_]\[ _du_ même fichier ou répertoire que pour le  _paramètre szLocal_ . 
    
 _cchUNC_
  
> [in] Taille de la mémoire tampon pour la chaîne de sortie.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L’équivalent du chemin d’accès UNC a été localisé avec succès.
    
MAPI_E_INVALID_PARAMETER
  
> Un ou plusieurs paramètres ne sont pas valides.
    
MAPI_E_TOO_BIG
  
>  _szUNC_ n’était pas assez grand pour contenir le résultat. 
    
S_FALSE
  
> Le chemin d’accès local était déjà une chaîne UNC.
    
## <a name="see-also"></a>Voir aussi



[ScLocalPathFromUNC](sclocalpathfromunc.md)

