---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 602d9ce178c0d88192d3eaba899b15f6c2445c8d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580173"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a>GetDefCachedModeDownloadPubFoldFavs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique si le mode Exchange mis en cache pour le dossier Favoris des **dossiers** publics est activé et si cela est appliqué par la stratégie. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exporté par :  <br/> |msmapi32.dll  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

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



[GetDefCachedMode](getdefcachedmode.md)

