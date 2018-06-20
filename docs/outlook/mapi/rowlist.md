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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d0427e36d07d1cdc4f88e471f9ca006e737b73f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787033"
---
# <a name="rowlist"></a>ROWLIST

  
  
**S’applique à**: Outlook 
  
Contient un tableau de structures [ROWENTRY](rowentry.md) représentant les lignes et les opérations sont effectuées sur les lignes d’une table par le biais de l’interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) . 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a>Membres

 **cEntries**
  
> Nombre d’entrées dans le tableau spécifié par le membre **aEntries** . 
    
 **aEntries [MAPI_DIM]**
  
> Tableau de structures **ROWENTRY** qui contient les lignes et les opérations sont effectuées sur les lignes de la table. 
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |Permet de créer une liste de règles sélectionnées pour les actions suivantes **ModifyTable** .  <br/> |
   
## <a name="see-also"></a>Voir aussi



[ROWENTRY](rowentry.md)
  
[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Structures MAPI](mapi-structures.md)

