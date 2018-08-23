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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: fb0bfaba1ca0a0d7d34096b3b0b1db9863207097
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576266"
---
# <a name="rowentry"></a>ROWENTRY

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient une ligne et l’opération est effectuée sur la ligne dans une table par le biais de l’interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) . 
  
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
  
> Une des opérations à effectuer sur les données suivantes : 
    
  - ROW_ADD : Ajoutez les données dans le tableau en tant qu’une nouvelle ligne.
      
  - ROW_MODIFY : Modifiez cette ligne dans le tableau.
      
  - ROW_REMOVE : Supprimer cette ligne de la table.
      
  - ROW_EMPTY : N’ajoutez pas les données de ligne à la table. (La ligne est vide).
    
**cValues**
  
> Le nombre de valeurs de propriété dans **rgPropvals**.
    
**rgPropVals**
  
> Tableau des structures [SPropValue](spropvalue.md) représentant les valeurs de colonnes à insérer dans le tableau. 
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |Permet de créer une liste de règles sélectionnées pour les actions suivantes **ModifyTable** .  <br/> |
   
## <a name="see-also"></a>Voir aussi
  
- [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
- [Structures MAPI](mapi-structures.md)

