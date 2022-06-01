---
title: HexFromBin
description: La fonction HexFromBin convertit un nombre binaire en une représentation sous forme de chaîne d’un nombre hexadécimal.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HexFromBin
api_type:
- COM
ms.assetid: 12b95657-1926-4a24-be63-40305ea6f990
ms.openlocfilehash: ce4eff171dcb1295d91507f70390ed1a9ba8b7c1
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815169"
---
# <a name="hexfrombin"></a>HexFromBin

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Convertit un nombre binaire en une représentation sous forme de chaîne d’un nombre hexadécimal. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
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
  
> [in] Pointeur vers les données binaires à convertir. 
    
 _cb_
  
> [in] Taille, en octets, des données binaires pointées par le paramètre  _pb_ . 
    
 _Sz_
  
> [out] Pointeur vers une chaîne ASCII terminée par une valeur Null représentant les données binaires en chiffres hexadécimals.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

La fonction **HexFromBin** prend un pointeur vers une unité de données binaires dont la taille est indiquée par le paramètre  _cb_ . Elle retourne dans la chaîne _sz_ , dans (2*  _cb_)+1 octets de mémoire, une représentation de ces informations binaires en nombres hexadécimals. Si la valeur d’octet est décimale 10, par exemple, la chaîne hexadécimale est 0A, un octet est converti en deux octets dans la chaîne. 
  

