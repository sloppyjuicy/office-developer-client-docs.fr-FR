---
title: GetDefCachedMode
description: Décrit GetDefCachedMode et fournit la syntaxe, les paramètres et la valeur de retour.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
ms.openlocfilehash: b3b6709483796edc3e4a569b89e5abe9343ec7f3
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816632"
---
# <a name="getdefcachedmode"></a>GetDefCachedMode

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique si le mode de Exchange mis en cache pour le magasin de Exchange privé est activé et s’il est appliqué par la stratégie.
  
## <a name="quick-info"></a>Informations rapides

|Propriété|Valeur|
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

 **Vrai**
  
- La mise en cache est activée.
    
 **Faux**
  
- La mise en cache est désactivée.
    
## <a name="see-also"></a>Voir aussi



[GetDefCachedModeDownloadPubFoldFavs](getdefcachedmodedownloadpubfoldfavs.md)

