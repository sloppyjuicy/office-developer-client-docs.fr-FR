---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: 81bc97456d0b8ed3cce7071afdd445583a6f0a1d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571422"
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

