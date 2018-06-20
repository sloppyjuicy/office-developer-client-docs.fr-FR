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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e26acb8415df007a7f3fb5901521da7222ae40ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783397"
---
# <a name="ftnegft"></a>FtNegFt

  
  
**S’applique à**: Outlook 
  
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
  

