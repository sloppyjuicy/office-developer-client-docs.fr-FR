---
title: FtMulDwDw
description: Décrit FtMulDwDw et fournit la syntaxe, les paramètres et la valeur de retour.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FtMulDwDw
api_type:
- COM
ms.assetid: 8c1a342c-d7ae-4e26-b327-a63cdd3c3ee6
ms.openlocfilehash: 59a64013eea08d54c53806103fd08717d24ca77e
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816443"
---
# <a name="ftmuldwdw"></a>FtMulDwDw

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Multiplie un entier 32 bits non signé par un autre.
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a>Paramètres

 _Multiplicand_
  
> [in] Mot double qui contient l’entier 32 bits non signé à multiplier par la valeur du paramètre _Multiplicateur_ . 
    
 _Multiplicateur_
  
> [in] Mot double qui contient le multiplicateur entier 32 bits non signé.
    
## <a name="return-value"></a>Valeur renvoyée

La fonction **FtMulDwDw** retourne une structure [FILETIME](filetime.md) qui contient le produit des deux entiers. Les deux paramètres d’entrée restent inchangés. 
  

