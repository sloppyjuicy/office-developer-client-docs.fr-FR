---
title: FtNegFt
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dc78701c7cfbb95455bbd92f101afaf15f08a62e
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63781305"
---
# <a name="ftnegft"></a>FtNegFt

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Calcule le complément des deux d’un nombre integer 64 bits non signé. 
  
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

 _ft_
  
> [in] Structure [FILETIME](filetime.md) qui contient l’ensemble non signé 64 bits pour lequel calculer le complément des deux. 
    
## <a name="return-value"></a>Valeur renvoyée

La **fonction FtNegFt** renvoie une structure **FILETIME** qui contient le complément de l’ensemble des deux. Le paramètre d’entrée reste inchangé. 
  

