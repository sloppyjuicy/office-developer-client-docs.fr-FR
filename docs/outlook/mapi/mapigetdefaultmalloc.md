---
title: MAPIGetDefaultMalloc
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7ffffdae05799ce573beabe1379ff66b059fb63d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616788"
---
# <a name="mapigetdefaultmalloc"></a>MAPIGetDefaultMalloc

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Récupère l’adresse de la fonction d’allocation de mémoire MAPI par défaut.
  
|||
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

La **fonction MAPIGetDefaultMalloc** renvoie un pointeur vers la fonction d’allocation de mémoire MAPI par défaut. 
  

