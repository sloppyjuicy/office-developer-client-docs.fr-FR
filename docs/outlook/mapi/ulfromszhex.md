---
title: UlFromSzHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlFromSzHex
api_type:
- COM
ms.assetid: e2d6b6bf-f96d-460c-859a-21961ac9237c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 950f5513696a9dd9d52db7b7ee912d3f7d12cc48
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433051"
---
# <a name="ulfromszhex"></a>UlFromSzHex

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
ConVertit une chaîne terminée par un caractère null de chiffres hexadécimaux en un entier long non signé. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a>Paramètres

 _lpsz_
  
> dans Pointeur vers la chaîne terminée par un caractère null à convertir. Le paramètre _lpsz_ ne doit pas dépasser 65536 caractères. 
    
## <a name="return-value"></a>Valeur renvoyée

 **UlFromSzHex** renvoie un entier long non signé. Si la chaîne ne commence pas par au moins un chiffre hexadécimal, zéro est renvoyé. 
  
## <a name="remarks"></a>Remarques

La fonction **UlFromSzHex** arrête la conversion lorsqu'elle atteint le premier caractère de la chaîne qui n'est pas un chiffre hexadécimal. Par exemple, en fonction de la chaîne «5a», **UlFromSzHex** renvoie la valeur entière 90. Étant donné la chaîne «5g5h», la fonction renvoie la valeur entière 5. Étant donné la chaîne «g5h5», **UlFromSzHex** renvoie zéro. 
  
 **UlFromSzHex** est sensible aux différences diacritiques, mais autorise «a» à «f» et «a» À «f» pour les chiffres hexadécimaux. Les chaînes au format Unicode et DBCS sont prises en charge. La limite de longueur sur _lpsz_ est exprimée en caractères, pas nécessairement en octets. 
  

