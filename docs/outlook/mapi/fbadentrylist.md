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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 113628ef5487bc66a07d1367c938ed178a8e32ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582909"
---
# <a name="fbadentrylist"></a>FBadEntryList

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Valide une liste d’identificateurs d’entrée MAPI. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a>Paramètres

 _lpEntryList_
  
> [in] Pointeur vers une structure [ENTRYLIST](entrylist.md) qui contient un tableau d’identificateurs d’entrée à valider. 
    
## <a name="return-value"></a>Valeur renvoy�e

TRUE 
  
> Un ou plusieurs des identificateurs d’entrée répertoriés ne sont pas valides. 
    
FALSE 
  
> Tous les identificateurs d’entrée répertoriés sont valides.
    
## <a name="remarks"></a>Remarques

La fonction **FBadEntryList** détermine si la liste Identificateur d’entrée a été correctement générée. Un exemple d’un identificateur non valide est 1 qui a été incorrectement allouer de la mémoire ou un identificateur pour une taille incorrecte. 
  

