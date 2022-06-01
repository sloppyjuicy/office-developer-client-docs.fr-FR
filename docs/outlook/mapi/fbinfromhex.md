---
title: FBinFromHex
description: Décrit FBinFromHex et fournit la syntaxe, les paramètres et la valeur de retour.
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
ms.openlocfilehash: 121521e7c1b4487150ef416ae1d9124462035f39
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815841"
---
# <a name="fbinfromhex"></a>FBinFromHex

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Convertit une représentation sous forme de chaîne d’un nombre hexadécimal en données binaires. 
  
|Propriété |Valeur |
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

 _Sz_
  
> [in] Pointeur vers la chaîne ASCII terminée par la valeur Null à convertir. Il ne s’agit pas d’une chaîne Unicode. Les caractères valides incluent les caractères hexadécimals de zéro à neuf et les caractères majuscules et minuscules A à F.
    
 _pb_
  
> [out] Pointeur vers le nombre binaire retourné.
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> La chaîne a été correctement convertie en nombre binaire. 
    
FALSE 
  
> La chaîne d’entrée contient des caractères hexadécimals ASCII non valides.
    
## <a name="see-also"></a>Voir aussi



[ScBinFromHexBounded](scbinfromhexbounded.md)

