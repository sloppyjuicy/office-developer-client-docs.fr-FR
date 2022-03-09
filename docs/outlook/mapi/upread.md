---
title: UPREAD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 568f2336-cb4d-3f2c-a304-d29cdb0bcbcc
ms.openlocfilehash: 7beab4fdfde5a538aaba4924df0ee9bc1521c55f
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63368726"
---
# <a name="upread"></a>UPREAD

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations pour le chargement de l’état de lecture des éléments pendant l’état de [lecture du chargement](upload-read-status-state.md).
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a>Membres

 _pupre_
  
> [out] Vecteur des **[entrées UPREADE](upreade.md)** . 
    
 _cEnt_
  
> [out] Nombre **d’entrées UPREADE** . 
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[UPREADE](upreade.md)

