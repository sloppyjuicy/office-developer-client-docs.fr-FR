---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Dernière modification : 02 juillet 2012'
ms.openlocfilehash: 3e534f91863e2a1300e03d112d1f532f486eedd9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588306"
---
# <a name="feid"></a>FEID

 
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Identificateur d’un dossier. Il contient un identificateur d’entrée et d’autres informations pertinentes.
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a>Members

 _abFlags_
  
> identificateur d’entrée de 4 octets pour le dossier. Pour plus d’informations sur les identificateurs d’entrée MAPI, voir **[ENTRYID](entryid.md)**. 
    
 _muid_
  
> GUID qui identifie le fournisseur de banque. Voir mapidefs.h pour la définition du type de **MAPIUID**. 
    
 _espace réservé_
  
> Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.
    
 _ltid_
  
> ID à long terme du dossier.
    
## <a name="see-also"></a>Voir aussi



[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[LTID](ltid.md)
  
[UPFLD](upfld.md)
  
[SYNC](sync.md)

