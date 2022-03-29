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
description: Convertit la partie spécifiée d’une représentation de chaîne d’un nombre hexadécimal en nombre binaire.
ms.openlocfilehash: 65b33a95333f429a0368099e0377c7b101de362a
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455537"
---
# <a name="scbinfromhexbounded"></a>ScBinFromHexBounded

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Convertit la partie spécifiée d’une représentation de chaîne d’un nombre hexadécimal en nombre binaire. 
  
|Propriété |Valeur |
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
  
> [in] Taille, en octets, du  _paramètre pb_ . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> La conversion a réussi.
    
MAPI_E_CALL_FAILED
  
> Des caractères non valides ont été rencontrés.
    
## <a name="see-also"></a>Voir aussi



[FBinFromHex](fbinfromhex.md)

