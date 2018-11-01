---
title: UFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UFromSz
api_type:
- COM
ms.assetid: 4a67faa2-8c2e-49a7-8c92-690a0a65c8f7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7513e361f4c1c1bcc93cc420f3a1987e0d817c54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580501"
---
# <a name="ufromsz"></a>UFromSz

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Convertit une chaîne de chiffres décimaux en entier non signé. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a>Paramètres

 _lpsz_
  
> [in] Pointeur vers la chaîne à convertir. Le paramètre _lpsz_ ne doit pas dépasser 65536 caractères. 
    
## <a name="return-value"></a>Valeur renvoyée

 **UFromSz** renvoie un entier non signé. Si la chaîne ne commence pas par au moins un chiffre, zéro est renvoyé. 
  
## <a name="remarks"></a>Remarques

La fonction **UFromSz** cesse de conversion lorsqu’elle atteint le premier caractère de la chaîne qui n’est pas un nombre décimal. Par exemple, si la chaîne « 55 », **UFromSz** renvoie la valeur d’entier 55. Si la chaîne « 5a5b », la fonction renvoie la valeur entière 5. Si la chaîne « a5b5 », **UFromSz** renvoie zéro. 
  
 **UFromSz** est sensible aux différences diacritiques. Chaînes dans les formats Unicode et DBCS sont pris en charge. La limite de longueur _lpsz_ est en caractères, pas nécessairement octets. 
  

