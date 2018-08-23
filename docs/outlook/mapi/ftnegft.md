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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 37dc92a40043657cb791359d543ef52c77dbd8ce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589237"
---
# <a name="ftnegft"></a>FtNegFt

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Calcule des deux complément d’un nombre entier non signé 64 bits. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a>Paramètres

 _FT_
  
> [in] Une structure [FILETIME](filetime.md) qui contient l’entier non signé de 64 bits pour lequel calculer les compléments des deux. 
    
## <a name="return-value"></a>Valeur renvoy�e

La fonction **FtNegFt** renvoie une structure **FILETIME** qui contient des deux complément de l’entier. Le paramètre d’entrée reste inchangé. 
  

