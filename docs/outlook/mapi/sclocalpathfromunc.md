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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e94692ac4eb401109fcb522e6224c8748bef37f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787079"
---
# <a name="sclocalpathfromunc"></a>ScLocalPathFromUNC

  
  
**S’applique à**: Outlook 
  
Localise un équivalent du chemin d’accès local pour le chemin UNC (convention) d’affectation de noms universels. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
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
    
## <a name="return-value"></a>Valeur renvoy�e

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

