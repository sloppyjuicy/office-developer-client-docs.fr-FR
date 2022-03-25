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
ms.openlocfilehash: 5375b891684f3ed600449239267d261034946f71
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63726302"
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

