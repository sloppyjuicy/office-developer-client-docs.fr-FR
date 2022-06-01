---
title: FEID
description: Décrit FEID et fournit la syntaxe et les membres.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
ms.openlocfilehash: 3e2a7f79bd1d7035379755d4acf43853787d1fb8
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817934"
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
  
> Identificateur d’entrée de 4 octets pour le dossier. Pour plus d’informations sur les identificateurs d’entrée MAPI, consultez **[ENTRYID](entryid.md)**. 
    
 _muid_
  
> GUID qui identifie le fournisseur du magasin. Consultez mapidefs.h pour connaître la définition de type **mapIUID**. 
    
 _Espace réservé_
  
> Ce membre est réservé à l’utilisation interne de Outlook et n’est pas pris en charge.
    
 _ltid_
  
> ID à long terme du dossier.
    
## <a name="see-also"></a>Voir aussi



[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[LTID](ltid.md)
  
[UPFLD](upfld.md)
  
[SYNCHRONISATION](sync.md)

