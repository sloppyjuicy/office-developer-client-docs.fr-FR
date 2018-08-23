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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e6de4be29811dafaf5288b2ccb39c0342a314bad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584624"
---
# <a name="ulfromszhex"></a>UlFromSzHex

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Convertit une chaîne de chiffres hexadécimaux en entier long non signé. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a>Paramètres

 _lpsz_
  
> [in] Pointeur vers la chaîne à convertir. Le paramètre _lpsz_ ne doit pas dépasser 65536 caractères. 
    
## <a name="return-value"></a>Valeur renvoy�e

 **UlFromSzHex** renvoie un entier long non signé. Si la chaîne ne commence pas par au moins un chiffre hexadécimal, zéro est renvoyé. 
  
## <a name="remarks"></a>Remarques

La fonction **UlFromSzHex** cesse de conversion lorsqu’elle atteint le premier caractère de la chaîne n’est pas un chiffre hexadécimal. Par exemple, si la chaîne « 5 », **UlFromSzHex** renvoie la valeur d’entier 90. Si la chaîne « 5g5h », la fonction renvoie la valeur entière 5. Si la chaîne « g5h5 », **UlFromSzHex** renvoie zéro. 
  
 **UlFromSzHex** est sensible aux différences diacritiques mais « a » à « f » et « A » à « F » pour les chiffres hexadécimaux. Chaînes dans les formats Unicode et DBCS sont pris en charge. La limite de longueur _lpsz_ est en caractères, pas nécessairement octets. 
  

