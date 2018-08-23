---
title: IMAPITableQueryColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryColumns
api_type:
- COM
ms.assetid: d6341acc-c6ca-4605-93af-77230040339d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 86dfaa8fbc9ff24d38472f1339a22534086d890b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593745"
---
# <a name="imapitablequerycolumns"></a>IMAPITable::QueryColumns

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Renvoie une liste de colonnes pour la table.
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui indique la colonne dans laquelle la valeur doit être retournée. Vous pouvez définir l’indicateur suivant :
    
TBL_ALL_COLUMNS 
  
> Le tableau doit renvoyer toutes les colonnes disponibles.
    
 _lpPropTagArray_
  
> [out] Pointeur vers une structure [SPropTagArray](sproptagarray.md) contenant les balises de propriété pour la colonne valeur. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’ensemble de la colonne a été renvoyée avec succès.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche la colonne définie opération de récupération de démarrage. L’opération en cours doit être autorisée à effectuer ou il doit être arrêté.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::QueryColumns** peut être appelée pour récupérer : 
  
- La colonne par défaut d’un tableau.
    
- La colonne en cours défini pour une table, comme ouverte par un appel à la méthode [IMAPITable::SetColumns](imapitable-setcolumns.md) . 
    
- La colonne complète d’une table, les colonnes qui sont disponibles, mais pas nécessairement partie de l’ensemble actuel.
    
## <a name="notes-to-callers"></a>Notes aux appelants

Si vous ne définissez pas l’indicateur TBL_ALL_COLUMNS, **IMAPITable::QueryColumns** renvoie d’une table par défaut ou ensemble de colonnes en cours, selon que le tableau a été affecté par un appel à **IMAPITable::SetColumns**. **SetColumns** modifie l’ordre et la sélection des colonnes dans un ensemble de colonnes d’une table. 
  
Si vous définissez l’indicateur TBL_ALL_COLUMNS, **QueryColumns** renvoie toutes les colonnes qui sont susceptibles d’être dans l’ensemble de colonnes de la table. 
  
Libérer de la mémoire pour le tableau de balise de propriété indiqué par le paramètre _lpPropTagArray_ en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoSetColumns  <br/> |MFCMAPI utilise la méthode **IMAPITable::QueryColumns** pour récupérer la colonne en cours d’une table afin que l’utilisateur peut le modifier.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

