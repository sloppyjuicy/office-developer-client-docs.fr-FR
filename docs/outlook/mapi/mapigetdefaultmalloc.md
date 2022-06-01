---
title: MAPIGetDefaultMalloc
description: La fonction MAPIGetDefaultMalloc récupère l’adresse de la fonction d’allocation de mémoire MAPI par défaut.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPIGetDefaultMalloc
api_type:
- HeaderDef
ms.assetid: 148695dd-d886-4a06-9cfe-749059ae91ed
ms.openlocfilehash: 66f8c681180d0d2db388d2fe226e2f67abacd632
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817059"
---
# <a name="mapigetdefaultmalloc"></a>MAPIGetDefaultMalloc

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Récupère l’adresse de la fonction d’allocation de mémoire MAPI par défaut.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a>Paramètres

Aucun. 
  
## <a name="return-value"></a>Valeur renvoyée

La fonction **MAPIGetDefaultMalloc** retourne un pointeur vers la fonction d’allocation de mémoire MAPI par défaut. 
  

