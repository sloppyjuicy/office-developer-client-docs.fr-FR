---
title: MEID
description: MEID est un identificateur pour un élément Outlook. Il contient un identificateur d’entrée et d’autres informations pertinentes.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
ms.openlocfilehash: 49574cf1f82fa8269e065f7d395f5f12b583acb8
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828226"
---
# <a name="meid"></a>MEID

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Identificateur d’un élément Outlook. Il contient un identificateur d’entrée et d’autres informations pertinentes.
  
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
  
> Identificateur d’entrée de 4 octets pour l’élément Outlook. Pour plus d’informations sur les identificateurs d’entrée MAPI, consultez **[ENTRYID](entryid.md)**. 
    
 _muid_
  
> GUID qui identifie le fournisseur du magasin. Consultez mapidefs.h pour connaître la définition de type **mapIUID**. 
    
 _Espace réservé_
  
> Ce membre est réservé à l’utilisation interne de Outlook et n’est pas pris en charge.
    
 _ltidFld_
  
> ID à long terme du dossier.
    
 _ltidMsg_
  
> ID à long terme de l’élément Outlook.
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[LTID](ltid.md)
  
[SYNCHRONISATION](sync.md)
  
[UPMSG](upmsg.md)

