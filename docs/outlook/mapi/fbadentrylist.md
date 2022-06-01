---
title: FBadEntryList
description: FBadEntryList valide une liste d’identificateurs d’entrée MAPI. Cet article décrit sa syntaxe, ses paramètres, sa valeur de retour et ses remarques.
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
ms.openlocfilehash: 93bd79751cb95d206080214d5cd45a5ddb7df1e4
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817094"
---
# <a name="fbadentrylist"></a>FBadEntryList

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valide une liste d’identificateurs d’entrée MAPI. 
  
|Propriété |Valeur |
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
  
> Un ou plusieurs des identificateurs d’entrée répertoriés ne sont pas valides. 
    
FALSE 
  
> Tous les identificateurs d’entrée répertoriés sont valides.
    
## <a name="remarks"></a>Remarques

La fonction **FBadEntryList** détermine si la liste d’identificateurs d’entrée a été correctement générée. Un exemple d’identificateur non valide est celui pour lequel la mémoire a été allouée de manière incorrecte ou un identificateur d’une taille incorrecte. 
  

