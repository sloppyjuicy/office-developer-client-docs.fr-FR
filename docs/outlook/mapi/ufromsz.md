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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9947558975098316a547abfaefcdf5e7d4cd2f41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346535"
---
# <a name="ufromsz"></a>UFromSz

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
ConVertit une chaîne terminée par un caractère null de chiffres décimaux en un entier non signé. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a>Paramètres

 _lpsz_
  
> dans Pointeur vers la chaîne terminée par un caractère null à convertir. Le paramètre _lpsz_ ne doit pas dépasser 65536 caractères. 
    
## <a name="return-value"></a>Valeur renvoyée

 **UFromSz** renvoie un entier non signé. Si la chaîne ne commence pas par au moins un chiffre décimal, zéro est renvoyé. 
  
## <a name="remarks"></a>Remarques

La fonction **UFromSz** arrête la conversion lorsqu'elle atteint le premier caractère de la chaîne qui n'est pas un chiffre décimal. Par exemple, en fonction de la chaîne «55», **UFromSz** renvoie la valeur entière 55. Étant donné la chaîne «5a5b», la fonction renvoie la valeur entière 5. Étant donné la chaîne «A5B5», **UFromSz** renvoie zéro. 
  
 **UFromSz** est sensible aux différences diacritiques. Les chaînes au format Unicode et DBCS sont prises en charge. La limite de longueur sur _lpsz_ est exprimée en caractères, pas nécessairement en octets. 
  

