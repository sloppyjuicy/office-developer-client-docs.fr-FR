---
title: FBinFromHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FBinFromHex
api_type:
- COM
ms.assetid: 47e6c576-bd99-4410-8e41-7dd3159b23b7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 021336f54d6ca7b00ee6ccb434edc91067075a15
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596462"
---
# <a name="fbinfromhex"></a>FBinFromHex

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Convertit une représentation sous forme de chaîne d’un nombre hexadécimal en données binaires. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a>Paramètres

 _sz_
  
> [in] Pointeur vers la chaîne ASCII terminée par null à convertir. Il ne s’agit pas d’une chaîne Unicode. Les caractères valides incluent les caractères hexadécimals de zéro à neuf, ainsi que les caractères en minuscules et en minuscules A à F.
    
 _pb_
  
> [out] Pointeur vers le nombre binaire renvoyé.
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> La chaîne a été convertie en nombre binaire. 
    
FALSE 
  
> La chaîne d’entrée contient des caractères hexadécimals ASCII non valides.
    
## <a name="see-also"></a>Voir aussi



[ScBinFromHexBounded](scbinfromhexbounded.md)

