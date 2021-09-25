---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 174320928f94992c010e5c4349ba66e2ec6457cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614163"
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

## <a name="parameters"></a>Paramètres

 _pfPolicy_
  
> [out] **true** si la valeur de retour est appliquée par la stratégie, **false** si ce n’est pas le cas. 
    
## <a name="return-values"></a>Valeurs de retour

 **true**
  
- La mise en cache est activée.
    
 **false**
  
- La mise en cache est désactivée.
    
## <a name="see-also"></a>Voir aussi



[GetDefCachedModeDownloadPubFoldFavs](getdefcachedmodedownloadpubfoldfavs.md)

