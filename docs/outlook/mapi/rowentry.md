---
title: ROWENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWENTRY
api_type:
- COM
ms.assetid: bd6c0d8e-68cc-4d60-9029-13ed81c816cd
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 243ab1e926171ee66b95cfd8e969cd77e2b31faf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279600"
---
# <a name="rowentry"></a>ROWENTRY

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une ligne et l'opération exécutée sur cette ligne dans un tableau via l'interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) . 
  
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
  
> Une des opérations suivantes à effectuer sur les données: 
    
  - ROW_ADD: ajouter les données à la table en tant que nouvelle ligne.
      
  - ROW_MODIFY: modifiez cette ligne dans le tableau.
      
  - ROW_REMOVE: supprimez cette ligne du tableau.
      
  - ROW_EMPTY: n'ajoutez pas les données de ligne à la table. (La ligne est vide.)
    
**cValues**
  
> Nombre de valeurs de propriété dans **rgPropvals**.
    
**rgPropVals**
  
> Tableau de structures [SPropValue](spropvalue.md) représentant les valeurs de colonnes à insérer dans le tableau. 
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|RulesDlg. cpp  <br/> |CRulesDlg:: GetSelectedItems  <br/> |Permet de créer une liste de règles sélectionnées pour les actions **ModifyTable** suivantes.  <br/> |
   
## <a name="see-also"></a>Voir aussi
  
- [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
- [Structures MAPI](mapi-structures.md)

