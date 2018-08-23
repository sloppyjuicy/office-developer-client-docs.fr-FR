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
ms.openlocfilehash: 887c66277b54e2e14c7f67c76b8e9dd4fa8bc719
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589230"
---
# <a name="upread"></a>UPREAD

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Informations de téléchargement de l’état de lecture des éléments pendant le [téléchargement lire l’état de l’état](upload-read-status-state.md).
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a>Members

 _pupre_
  
>  [out] Vecteur d’entrées **[UPREADE](upreade.md)** . 
    
 _cEnt_
  
>  [out] Nombre d’entrées **UPREADE** . 
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[UPREADE](upreade.md)

