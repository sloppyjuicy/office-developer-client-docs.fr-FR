---
title: UFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.UFromSz
api_type:
- COM
ms.assetid: 4a67faa2-8c2e-49a7-8c92-690a0a65c8f7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 49f921ddd26fc78cea9b9b1e5ad99e248f4409ac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609249"
---
# <a name="ufromsz"></a>UFromSz

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Convertit une chaîne de chiffres décimales terminée par null en un nombre non signé. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a>Paramètres

 _lpsz_
  
> [in] Pointeur vers la chaîne terminée par null à convertir. Le  _paramètre lpsz_ ne doit pas dépasser 65 536 caractères. 
    
## <a name="return-value"></a>Valeur renvoyée

 **UFromSz** renvoie un integer non signé. Si la chaîne ne commence pas par au moins un chiffre décimal, zéro est renvoyé. 
  
## <a name="remarks"></a>Remarques

La **fonction UFromSz** cesse de se convertir lorsqu’elle atteint le premier caractère de la chaîne qui n’est pas un chiffre décimal. Par exemple, étant donné la chaîne « 55 », **UFromSz** renvoie la valeur d’ensemble 55. Étant donné la chaîne « 5a5b », la fonction renvoie la valeur d’ensemble 5. Étant donné la chaîne « a5b5 », **UFromSz** renvoie zéro. 
  
 **UFromSz est** sensible aux différences diacritiques. Les chaînes aux formats Unicode et DBCS sont pris en charge. La limite de longueur sur  _lpsz est_ en caractères, pas nécessairement en octets. 
  

