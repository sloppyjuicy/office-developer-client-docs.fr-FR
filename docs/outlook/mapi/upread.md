---
title: UPREAD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 568f2336-cb4d-3f2c-a304-d29cdb0bcbcc
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7338edc13227e303ec5fa47da4a5d9ee611c6749
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419883"
---
# <a name="upread"></a>UPREAD

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations pour le chargement de l’état de lecture des éléments pendant l’état de [lecture du chargement.](upload-read-status-state.md)
  
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
  
>  [out] Vecteur des **[entrées UPREADE.](upreade.md)** 
    
 _cEnt_
  
>  [out] Nombre **d’entrées UPREADE.** 
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[UPREADE](upreade.md)

