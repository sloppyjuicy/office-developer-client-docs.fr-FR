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
ms.openlocfilehash: bb2d347d218a7c33a2184bf1fcf181a11fa7d8fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783300"
---
# <a name="feid"></a>FEID

 
  
**S’applique à**: Outlook 
  
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

## <a name="members"></a>Membres

 _abFlags_
  
> identificateur d’entrée de 4 octets pour le dossier. Pour plus d’informations sur les identificateurs d’entrée MAPI, voir **[ENTRYID](entryid.md)**. 
    
 _muid_
  
> GUID qui identifie le fournisseur de banque. Voir mapidefs.h pour la définition du type de **MAPIUID**. 
    
 _espace réservé_
  
> Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.
    
 _ltid_
  
> ID à long terme du dossier.
    
## <a name="see-also"></a>Voir aussi



[Sur l’ordinateur de l’état de réplication](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[LTID](ltid.md)
  
[UPFLD](upfld.md)
  
[SYNCHRONISATION](sync.md)

