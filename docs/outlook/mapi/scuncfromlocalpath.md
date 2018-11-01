---
title: ScUNCFromLocalPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScUNCFromLocalPath
api_type:
- COM
ms.assetid: cc4abf1a-c08c-4462-9d7c-6af506dc07c9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: faba91d813d27f7ea45e978724ce0d4707803cba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590105"
---
# <a name="scuncfromlocalpath"></a>ScUNCFromLocalPath

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Localise un équivalent chemin d’accès UNC (convention) d’affectation de noms universels pour le chemin d’accès local donné.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a>Paramètres

 _szLocal_
  
> [in] Un chemin d’accès dans le format [ _lecteur :_]\[ _chemin d’accès_] d’un fichier ou un répertoire.
    
 _szUNC_
  
> [out] Un chemin d’accès au format \\[ _server_]\[ _partager_]\[ _chemin d’accès_] du même fichier ou répertoire que pour le paramètre _szLocal_ . 
    
 _cchUNC_
  
> [in] Taille de la mémoire tampon de la chaîne de sortie.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L’équivalent du chemin d’accès UNC a été trouvé.
    
MAPI_E_INVALID_PARAMETER
  
> Un ou plusieurs paramètres ne sont pas valides.
    
MAPI_E_TOO_BIG
  
>  _szUNC_ n’était pas suffisante pour contenir le résultat. 
    
S_FALSE
  
> Le chemin d’accès local a déjà une chaîne UNC.
    
## <a name="see-also"></a>Voir aussi



[ScLocalPathFromUNC](sclocalpathfromunc.md)

