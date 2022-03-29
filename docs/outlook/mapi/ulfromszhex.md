---
title: UlFromSzHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.UlFromSzHex
api_type:
- COM
ms.assetid: e2d6b6bf-f96d-460c-859a-21961ac9237c
description: Convertit une chaîne de chiffres hexadécimals terminée par null en un nombre long non signé.
ms.openlocfilehash: bcc0367f9c45fada5fdbc595e755a229cdbc41bc
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64454998"
---
# <a name="ulfromszhex"></a>UlFromSzHex

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Convertit une chaîne de chiffres hexadécimals terminée par null en un nombre long non signé. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a>Paramètres

 _lpsz_
  
> [in] Pointeur vers la chaîne terminée par null à convertir. Le  _paramètre lpsz_ ne doit pas dépasser 65 536 caractères. 
    
## <a name="return-value"></a>Valeur renvoyée

 **UlFromSzHex** renvoie un long integer non signé. Si la chaîne ne commence pas par au moins un chiffre hexadécimal, zéro est renvoyé. 
  
## <a name="remarks"></a>Remarques

La **fonction UlFromSzHex** cesse de se convertir lorsqu’elle atteint le premier caractère de la chaîne qui n’est pas un chiffre hexadécimal. Par exemple, étant donné la chaîne « 5a », **UlFromSzHex** renvoie la valeur d’ensemble 90. Étant donné la chaîne « 5g5h », la fonction renvoie la valeur d’ensemble 5. Étant donné la chaîne « g5h5 », **UlFromSzHex** renvoie zéro. 
  
 **UlFromSzHex** est sensible aux différences diacritiques, mais permet à la fois « a » à « f » et « A » à « F » pour les chiffres hexadécimals. Les chaînes aux formats Unicode et DBCS sont pris en charge. La limite de longueur sur  _lpsz est_ en caractères, pas nécessairement en octets. 
  

