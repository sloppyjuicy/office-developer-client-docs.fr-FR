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
ms.openlocfilehash: 64d205ee7f51c0ce6a6eb1e982659c6cda675f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783303"
---
# <a name="fbinfromhex"></a>FBinFromHex

  
  
**S’applique à**: Outlook 
  
Convertit une représentation sous forme de chaîne d’un nombre hexadécimal à des données binaires. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a>Paramètres

 _sz_
  
> [in] Pointeur vers la chaîne ASCII à convertir. Il n’est pas une chaîne Unicode. Caractères valides incluent les caractères hexadécimaux zéro par le biais de neuf et les deux caractères majuscules et minuscules A à F.
    
 _pb_
  
> [out] Pointeur vers le nombre binaire renvoyé.
    
## <a name="return-value"></a>Valeur renvoy�e

TRUE 
  
> La chaîne a été convertie en nombre binaire. 
    
FALSE 
  
> La chaîne d’entrée contient des caractères hexadécimaux ASCII non valides.
    
## <a name="see-also"></a>Voir aussi



[ScBinFromHexBounded](scbinfromhexbounded.md)

