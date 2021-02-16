---
title: ScBinFromHexBounded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScBinFromHexBounded
api_type:
- COM
ms.assetid: edac715c-6edb-4b05-82e5-c08c3c7cb6d4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 813fab28e3e865c9f04f85c854b292ce7229dad5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439757"
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

