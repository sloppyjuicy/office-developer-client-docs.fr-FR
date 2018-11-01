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
ms.openlocfilehash: e303361f4f0dd3a08dbb362096d07b8b391a6d97
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594417"
---
# <a name="sclocalpathfromunc"></a>ScLocalPathFromUNC

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Localise un équivalent du chemin d’accès local pour le chemin UNC (convention) d’affectation de noms universels. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a>Paramètres

 _szUNC_
  
> [in] Un chemin d’accès au format \\[ _server_]\[ _partager_]\[ _chemin d’accès_] d’un fichier ou un répertoire.
    
 _szLocal_
  
> [out] Un chemin d’accès dans le format [ _lecteur :_]\[ _chemin d’accès_] du même fichier ou répertoire que pour le paramètre _szUNC_ . 
    
 _cchLocal_
  
> [in] Taille de la mémoire tampon de la chaîne de sortie.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Un chemin d’accès local a été trouvé.
    
MAPI_E_TOO_BIG
  
>  _szLocal_ n’était pas suffisante pour contenir le résultat. 
    
S_FALSE
  
> La chaîne UNC est déjà un chemin d’accès local.
    
MAPI_E_NOT_FOUND
  
> Un chemin d’accès local est introuvable.
    
## <a name="see-also"></a>Voir aussi



[ScUNCFromLocalPath](scuncfromlocalpath.md)

