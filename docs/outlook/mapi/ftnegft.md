---
title: FtNegFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtNegFt
api_type:
- COM
ms.assetid: 639a408c-aed1-456b-9f75-9d6fb8dcb33b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: db208dad8697060e394b3ee037ea658cefbab669
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423383"
---
# <a name="ftnegft"></a>FtNegFt

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Calcule le complément à deux d'un entier non signé 64 bits. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a>Paramètres

 _pied_
  
> dans Une structure [fileTime](filetime.md) qui contient l'entier non signé 64 bits pour lequel calculer le complément à deux. 
    
## <a name="return-value"></a>Valeur renvoyée

La fonction **FtNegFt** renvoie une structure **fileTime** qui contient le complément à deux de l'entier. Le paramètre d'entrée reste inchangé. 
  

