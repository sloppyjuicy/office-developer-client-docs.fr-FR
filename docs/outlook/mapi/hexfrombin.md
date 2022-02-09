---
title: HexFromBin
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a6a326d49548e59a0476942b3465b1cef19355d4
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62461686"
---
# <a name="hexfrombin"></a>HexFromBin

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Convertit un nombre binaire en une représentation sous forme de chaîne d’un nombre hexadécimal. 
  
|||
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
  
> [in] Taille, en octets, des données binaires pointées par le  _paramètre pb_ . 
    
 _sz_
  
> [out] Pointeur vers une chaîne ASCII terminée par null représentant les données binaires en chiffres hexadécimals.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

La **fonction HexFromBin** prend un pointeur vers une unité de données binaires dont la taille est indiquée par le  _paramètre cb_ . Elle renvoie dans la chaîne _sz_ , dans (2*  _cb_)+1 octets de mémoire, une représentation de ces informations binaires en nombres hexadécimals. Si la valeur d’octet est décimale 10, par exemple, la chaîne hexadécimale sera 0A, de sorte qu’un octet est converti en deux octets dans la chaîne. 
  

