---
title: FBadEntryList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FBadEntryList
api_type:
- HeaderDef
ms.assetid: 270c47c3-ae68-4995-b304-27f861b350d6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 333cbf047ebefd13c6da39f4d05ab349318d6ccf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576295"
---
# <a name="fbadentrylist"></a>FBadEntryList

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide une liste d’identificateurs d’entrée MAPI. 
  
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
  
> [in] Pointeur vers une structure [ENTRYLIST](entrylist.md) qui contient un tableau d’identificateurs d’entrée à valider. 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Un ou plusieurs identificateurs d’entrée répertoriés ne sont pas valides. 
    
FALSE 
  
> Tous les identificateurs d’entrée répertoriés sont valides.
    
## <a name="remarks"></a>Remarques

La **fonction FBadEntryList** détermine si la liste d’identificateurs d’entrée a été correctement générée. Un exemple d’identificateur non valide est un identificateur pour lequel la mémoire a été allouée de manière incorrecte ou un identificateur de taille incorrecte. 
  

