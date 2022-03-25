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
ms.openlocfilehash: ccf77e015282da108566a9ee299510131702f7b2
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63782922"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a>GetDefCachedModeDownloadPubFoldFavs

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique si le mode Exchange mis en cache pour le dossier Favoris du dossier **public** est activé et s’il est appliqué par la stratégie. 
  
## <a name="quick-info"></a>Informations rapides

|Propriété|Valeur|
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

