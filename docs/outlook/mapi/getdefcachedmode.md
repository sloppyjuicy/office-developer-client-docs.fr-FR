---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8e8a6ac07e14af52337b6e280fa58274df453c65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412743"
---
# <a name="getdefcachedmode"></a>GetDefCachedMode

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique si le mode Exchange mis en cache pour le magasin Exchange privé est activé et s’il est appliqué par la stratégie.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exporté par :  <br/> |msmapi32.dll  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a>Parameters

 _pfPolicy_
  
> [out] **true** si la valeur de retour est appliquée par la stratégie, **false** si ce n’est pas le cas. 
    
## <a name="return-values"></a>Valeurs de retour

 **true**
  
- La mise en cache est activée.
    
 **false**
  
- La mise en cache est désactivée.
    
## <a name="see-also"></a>Voir aussi



[GetDefCachedModeDownloadPubFoldFavs](getdefcachedmodedownloadpubfoldfavs.md)

