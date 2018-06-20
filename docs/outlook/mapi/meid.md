---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Dernière modification : 03 juillet 2012'
ms.openlocfilehash: 1b725dc5151f1f088f2547a1ef82d322c8458b6e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784904"
---
# <a name="meid"></a>MEID

 
  
**S’applique à**: Outlook 
  
Identificateur pour un élément Outlook. Il contient un identificateur d’entrée et d’autres informations pertinentes.
  
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
  
> identificateur d’entrée de 4 octets pour l’élément Outlook. Pour plus d’informations sur les identificateurs d’entrée MAPI, voir **[ENTRYID](entryid.md)**. 
    
 _muid_
  
> GUID qui identifie le fournisseur de banque. Voir mapidefs.h pour la définition du type de **MAPIUID**. 
    
 _espace réservé_
  
> Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.
    
 _ltidFld_
  
> ID à long terme du dossier.
    
 _ltidMsg_
  
> ID à long terme de l’élément Outlook.
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)
  
[Sur l’ordinateur de l’état de réplication](about-the-replication-state-machine.md)
  
[LTID](ltid.md)
  
[SYNCHRONISATION](sync.md)
  
[UPMSG](upmsg.md)

