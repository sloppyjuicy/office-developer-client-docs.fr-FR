---
title: ROWLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWLIST
api_type:
- COM
ms.assetid: ce0be0d5-4962-4d53-828f-c93d1c5aae32
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c13b741b1e0ddfd964b9325d736a26dac4bff2af
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419183"
---
# <a name="rowlist"></a>ROWLIST

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures [ROWENTRY](rowentry.md) représentant les lignes et les opérations effectuées sur les lignes d'une table via l'interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) . 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a>Members

 **cEntries**
  
> Nombre d'entrées dans le tableau spécifié par le membre **aEntries** . 
    
 **aEntries [MAPI_DIM]**
  
> Tableau de structures **ROWENTRY** qui contient les lignes et les opérations effectuées sur ces lignes dans le tableau. 
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|RulesDlg. cpp  <br/> |CRulesDlg:: GetSelectedItems  <br/> |Permet de créer une liste de règles sélectionnées pour les actions **ModifyTable** suivantes.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[ROWENTRY](rowentry.md)
  
[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Structures MAPI](mapi-structures.md)

