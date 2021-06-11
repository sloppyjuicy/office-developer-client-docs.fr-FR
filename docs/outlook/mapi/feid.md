---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: 88716719857cfd623d30a3684fc997ea8019455e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409810"
---
# <a name="feid"></a>FEID

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
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
  
> Identificateur d’entrée de 4 byte pour le dossier. Pour plus d’informations sur les identificateurs d’entrée MAPI, voir **[ENTRYID](entryid.md)**. 
    
 _muid_
  
> GUID qui identifie le fournisseur du magasin. Voir mapidefs.h pour la définition de type **de MAPIUID**. 
    
 _espace réservé_
  
> Ce membre est réservé à l’utilisation interne de Outlook et n’est pas pris en charge.
    
 _ltid_
  
> ID à long terme du dossier.
    
## <a name="see-also"></a>Voir aussi



[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[LTID](ltid.md)
  
[UPFLD](upfld.md)
  
[SYNC](sync.md)

