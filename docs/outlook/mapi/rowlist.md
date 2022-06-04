---
title: ROWLIST
description: Décrit comment ROWLIST contient un tableau de structures ROWENTRY représentant des lignes et les opérations effectuées sur ces lignes.
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
ms.openlocfilehash: 6ff338ffa30f853d8d187fd757184cc7e2bef3db
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65893647"
---
# <a name="rowlist"></a>ROWLIST

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures [ROWENTRY](rowentry.md) représentant des lignes et les opérations effectuées sur ces lignes dans une table via l’interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) . 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a>Members

 **cEntries**
  
> Nombre d’entrées dans le tableau spécifié par le membre **aEntries** . 
    
 **aEntries[MAPI_DIM]**
  
> Tableau de structures **ROWENTRY** qui contient les lignes et les opérations effectuées sur ces lignes dans la table. 
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |Utilisé pour créer une liste de règles sélectionnées pour les actions **ModifyTable suivantes** . |
   
## <a name="see-also"></a>Voir aussi



[ROWENTRY](rowentry.md)
  
[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Structures MAPI](mapi-structures.md)

