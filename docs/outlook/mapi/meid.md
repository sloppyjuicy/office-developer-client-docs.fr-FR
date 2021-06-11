---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: a9aea0db700de9c82aa2a41a443ebf03da8ce9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430307"
---
# <a name="meid"></a>MEID

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Identificateur d’Outlook’élément. Il contient un identificateur d’entrée et d’autres informations pertinentes.
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct MEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltidFld; 
    LTID ltidMsg; 
};
```

## <a name="members"></a>Membres

 _abFlags_
  
> Identificateur d’entrée de 4 Outlook’élément. Pour plus d’informations sur les identificateurs d’entrée MAPI, voir **[ENTRYID](entryid.md)**. 
    
 _muid_
  
> GUID qui identifie le fournisseur du magasin. Voir mapidefs.h pour la définition de type **de MAPIUID**. 
    
 _espace réservé_
  
> Ce membre est réservé à l’utilisation interne de Outlook et n’est pas pris en charge.
    
 _ltidFld_
  
> ID à long terme du dossier.
    
 _ltidMsg_
  
> ID à long terme de l’Outlook’élément.
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[LTID](ltid.md)
  
[SYNC](sync.md)
  
[UPMSG](upmsg.md)

