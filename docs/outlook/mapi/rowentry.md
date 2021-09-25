---
title: ROWENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ROWENTRY
api_type:
- COM
ms.assetid: bd6c0d8e-68cc-4d60-9029-13ed81c816cd
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7620f62cc67b99e863a6fa7442056e29f470f1e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591282"
---
# <a name="rowentry"></a>ROWENTRY

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une ligne et l’opération effectuée sur cette ligne dans un tableau via l’interface [IExchangeModifyTable.](iexchangemodifytableiunknown.md) 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a>Members

**ulRowFlags**
  
> L’une des opérations suivantes à effectuer sur les données : 
    
  - ROW_ADD : ajoutez les données au tableau en tant que nouvelle ligne.
      
  - ROW_MODIFY : modifiez cette ligne dans le tableau.
      
  - ROW_REMOVE : supprimez cette ligne du tableau.
      
  - ROW_EMPTY : n’ajoutez pas les données de ligne au tableau. (La ligne est vide.)
    
**cValues**
  
> Nombre de valeurs de propriété dans **rgPropvals**.
    
**rgPropVals**
  
> Tableau de structures [SPropValue](spropvalue.md) représentant les valeurs de colonnes à insérer dans le tableau. 
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |Utilisé pour créer une liste de règles sélectionnées pour les actions **ModifyTable suivantes.**  <br/> |
   
## <a name="see-also"></a>Voir aussi
  
- [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
- [Structures MAPI](mapi-structures.md)

