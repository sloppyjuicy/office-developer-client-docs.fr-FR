---
title: ROWLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ROWLIST
api_type:
- COM
ms.assetid: ce0be0d5-4962-4d53-828f-c93d1c5aae32
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 03b55fd87620eaca1421d4d467b92030aac891e2
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773109"
---
# <a name="rowlist"></a>ROWLIST

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures [ROWENTRY](rowentry.md) représentant des lignes et les opérations effectuées sur ces lignes dans un tableau via l’interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) . 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a>Members

 **cEntries**
  
> Nombre d’entrées dans le tableau spécifié par **le membre aEntries** . 
    
 **aEntries[MAPI_DIM]**
  
> Tableau de structures **ROWENTRY** qui contient les lignes et les opérations effectuées sur ces lignes dans le tableau. 
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |Utilisé pour créer une liste de règles sélectionnées pour les actions **ModifyTable suivantes** . |
   
## <a name="see-also"></a>Voir aussi



[ROWENTRY](rowentry.md)
  
[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Structures MAPI](mapi-structures.md)

