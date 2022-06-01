---
title: FtNegFt
description: Décrit FtNegFt et fournit la syntaxe, les paramètres et la valeur de retour.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FtNegFt
api_type:
- COM
ms.assetid: 639a408c-aed1-456b-9f75-9d6fb8dcb33b
ms.openlocfilehash: 2344e31520fa07058b70473af78e8d433d1a7147
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816954"
---
# <a name="ftnegft"></a>FtNegFt

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Calcule le complément d’un entier 64 bits non signé. 
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a>Paramètres

 _Ft_
  
> [in] Structure [FILETIME](filetime.md) qui contient l’entier 64 bits non signé pour lequel calculer le complément des deux. 
    
## <a name="return-value"></a>Valeur renvoyée

La fonction **FtNegFt** retourne une structure **FILETIME** qui contient le complément de l’entier des deux. Le paramètre d’entrée reste inchangé. 
  

