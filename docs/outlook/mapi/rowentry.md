---
title: ROWENTRY
description: Décrit comment ROWENTRY contient une ligne et l’opération effectuée sur cette ligne dans une table via l’interface IExchangeModifyTable.
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
ms.openlocfilehash: 4fd41928d911f92cddf617f3b8f10afc77e269ee
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894270"
---
# <a name="rowentry"></a>ROWENTRY

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une ligne et l’opération qui est effectuée sur cette ligne dans une table via l’interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) . 
  
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
    
  - ROW_ADD : ajoutez les données à la table en tant que nouvelle ligne.
      
  - ROW_MODIFY : modifiez cette ligne dans la table.
      
  - ROW_REMOVE : Supprimez cette ligne de la table.
      
  - ROW_EMPTY : n’ajoutez pas les données de ligne à la table. (La ligne est vide.)
    
**cValues**
  
> Nombre de valeurs de propriété dans **rgPropvals**.
    
**rgPropVals**
  
> Tableau de structures [SPropValue](spropvalue.md) représentant les valeurs de colonnes à insérer dans la table. 
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |Utilisé pour créer une liste de règles sélectionnées pour les actions **ModifyTable suivantes** . |
   
## <a name="see-also"></a>Voir aussi
  
- [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
- [Structures MAPI](mapi-structures.md)

