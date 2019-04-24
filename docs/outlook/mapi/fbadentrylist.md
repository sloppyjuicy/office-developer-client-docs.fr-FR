---
title: FBadEntryList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadEntryList
api_type:
- HeaderDef
ms.assetid: 270c47c3-ae68-4995-b304-27f861b350d6
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 21ed5a23b96dabdd594547109ecb1e6c048a4844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341068"
---
# <a name="fbadentrylist"></a>FBadEntryList

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide une liste d'identificateurs d'entrée MAPI. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a>Paramètres

 _lpEntryList_
  
> dans Pointeur vers une structure [ENTRYLIST](entrylist.md) qui contient un tableau d'identificateurs d'entrée à valider. 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Un ou plusieurs des identificateurs d'entrée répertoriés ne sont pas valides. 
    
FALSE 
  
> Tous les identificateurs d'entrée répertoriés sont valides.
    
## <a name="remarks"></a>Remarques

La fonction **FBadEntryList** détermine si la liste d'identificateurs d'entrée a été correctement générée. Un exemple d'identificateur non valide est celui pour lequel la mémoire a été incorrectement allouée ou un identificateur de taille incorrecte. 
  

