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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 55c7deec9d29ae22a07b2f5ccd1c832d56782c03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341642"
---
# <a name="fbinfromhex"></a>FBinFromHex

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
ConVertit une représentation sous forme de chaîne d'un nombre hexadécimal en données binaires. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a>Paramètres

 _t_
  
> dans Pointeur vers la chaîne ASCII terminée par un caractère null à convertir. Il ne s'agit pas d'une chaîne Unicode. Les caractères valides incluent les caractères hexadécimaux 0 à 9, ainsi que les caractères majuscules et minuscules A à F.
    
 _pb_
  
> remarquer Pointeur vers le nombre binaire renvoyé.
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> La chaîne a été convertie correctement en un nombre binaire. 
    
FALSE 
  
> La chaîne d'entrée contient des caractères hexadécimaux ASCII non valides.
    
## <a name="see-also"></a>Voir aussi



[ScBinFromHexBounded](scbinfromhexbounded.md)

