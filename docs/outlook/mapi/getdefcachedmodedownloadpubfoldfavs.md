---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ced6f2c6540e04a0bb4945ff98c4fda520322f03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581726"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a>GetDefCachedModeDownloadPubFoldFavs

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Indique si le Mode Exchange mis en cache pour le dossier **Favoris des dossiers publics** est activé, et si cela est appliqué par la stratégie. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exportés par :  <br/> |Msmapi32.dll  <br/> |
|Appelée par :  <br/> |Client  <br/> |
|Implémentée par :  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a>Paramètres

 _pfPolicy_
  
> [out] **true** si la valeur de retour est appliquée par la stratégie, **false** si elle n’est pas. 
    
## <a name="return-values"></a>Valeurs de retour

 **valeur True**
  
- La mise en cache est activé.
    
 **False**
  
- La mise en cache est désactivée.
    
## <a name="see-also"></a>Voir aussi



[GetDefCachedMode](getdefcachedmode.md)

