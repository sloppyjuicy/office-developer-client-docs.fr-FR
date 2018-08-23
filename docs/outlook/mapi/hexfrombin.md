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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 8f68de5e18d84c728241c188b932f99456f5be8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584834"
---
# <a name="hexfrombin"></a>HexFromBin

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Convertit un nombre binaire en une représentation de chaîne d’un nombre hexadécimal. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
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
  
> [in] Taille, en octets, des données binaires vers laquelle pointe le paramètre _po_ . 
    
 _sz_
  
> [out] Pointeur vers une chaîne qui représente les données binaires de chiffres hexadécimaux ASCII terminée.
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

La fonction **HexFromBin** prend un pointeur vers une unité de données binaires dont la taille est indiquée par le paramètre _cb_ . Elle renvoie au sein de la chaîne _sz_ , (2 * _cb_) + 1 octets de mémoire, une représentation de ces informations binaires en nombre hexadécimal. Si la valeur d’octet est 10 décimal, par exemple, la chaîne hexadécimale sera 0, 1 octet tel convertit sur deux octets dans la chaîne. 
  

