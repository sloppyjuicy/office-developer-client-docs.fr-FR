---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7595fac4346a537eed86550432f56a761c27c0ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783436"
---
# <a name="getdefcachedmode"></a>GetDefCachedMode

  
  
**S’applique à**: Outlook 
  
Indique si le Mode Exchange mis en cache pour la banque Exchange privée est activé, et si cela est appliqué par la stratégie.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exportés par :  <br/> |Msmapi32.dll  <br/> |
|Appelée par :  <br/> |Client  <br/> |
|Implémentée par :  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

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



[GetDefCachedModeDownloadPubFoldFavs](getdefcachedmodedownloadpubfoldfavs.md)

