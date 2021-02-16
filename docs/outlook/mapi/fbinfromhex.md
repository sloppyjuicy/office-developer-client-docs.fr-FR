---
title: FBinFromHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBinFromHex
api_type:
- COM
ms.assetid: 47e6c576-bd99-4410-8e41-7dd3159b23b7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 55c7deec9d29ae22a07b2f5ccd1c832d56782c03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414934"
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

