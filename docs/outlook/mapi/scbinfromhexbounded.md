---
title: ScBinFromHexBounded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScBinFromHexBounded
api_type:
- COM
ms.assetid: edac715c-6edb-4b05-82e5-c08c3c7cb6d4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4afb140d8c273d274b4d8e7417c39e6dffb97764
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599038"
---
# <a name="scbinfromhexbounded"></a>ScBinFromHexBounded

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Convertit la partie spécifiée d’une représentation de chaîne d’un nombre hexadécimal en nombre binaire. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a>Paramètres

 _sz_
  
> [in] Pointeur vers la chaîne terminée par null à convertir. Les caractères valides incluent les caractères hexadécimals 0 à 9, ainsi que les caractères en minuscules et en minuscules a à f.
    
 _pb_
  
> [out] Pointeur vers le nombre binaire renvoyé.
    
 _cb_
  
> [in] Taille, en octets, du _paramètre pb._ 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> La conversion a réussi.
    
MAPI_E_CALL_FAILED
  
> Des caractères non valides ont été rencontrés.
    
## <a name="see-also"></a>Voir aussi



[FBinFromHex](fbinfromhex.md)

