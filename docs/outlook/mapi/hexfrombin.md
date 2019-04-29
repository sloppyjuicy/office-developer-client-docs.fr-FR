---
title: HexFromBin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HexFromBin
api_type:
- COM
ms.assetid: 12b95657-1926-4a24-be63-40305ea6f990
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a1bf02de914865e27c8c018aba8695c858888ae2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412575"
---
# <a name="hexfrombin"></a>HexFromBin

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
ConVertit un nombre binaire en une représentation sous forme de chaîne d'un nombre hexadécimal. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a>Paramètres

 _pb_
  
> dans Pointeur vers les données binaires à convertir. 
    
 _cb_
  
> dans Taille, en octets, des données binaires auxquelles pointe le paramètre _PB_ . 
    
 _t_
  
> remarquer Pointeur vers une chaîne ASCII terminée par un caractère null qui représente les données binaires dans des chiffres hexadécimaux.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

La fonction **HexFromBin** prend un pointeur vers une unité de données binaires dont la taille est indiquée par le paramètre _CB_ . Elle retourne dans la chaîne _SZ_ , dans (2 * _CB_) + 1 octets de mémoire, une représentation de ces informations binaires dans des nombres hexadécimaux. Si la valeur Byte est de 10 décimal, par exemple, la chaîne hexadécimale sera 0A, un octet convertit en deux octets dans la chaîne. 
  

