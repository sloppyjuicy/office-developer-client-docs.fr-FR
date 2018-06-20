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
ms.openlocfilehash: aae2e97b987414fc5e46b410465d3232b61f1ffe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783275"
---
# <a name="fbadentrylist"></a>FBadEntryList

  
  
**S’applique à**: Outlook 
  
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
  

