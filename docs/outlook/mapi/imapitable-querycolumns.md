---
title: IMAPITableQueryColumns
description: Décrit la syntaxe, les paramètres et la valeur de retour d’IMAPITable QueryColumns, qui retourne une liste de colonnes pour la table.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.QueryColumns
api_type:
- COM
ms.assetid: d6341acc-c6ca-4605-93af-77230040339d
ms.openlocfilehash: 862cfe101238692c8acba1d24b5d93c08a47d5e2
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827827"
---
# <a name="imapitablequerycolumns"></a>IMAPITable::QueryColumns

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne une liste de colonnes pour la table.
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui indique quel jeu de colonnes doit être retourné. L’indicateur suivant peut être défini :
    
TBL_ALL_COLUMNS 
  
> La table doit retourner toutes les colonnes disponibles.
    
 _lpPropTagArray_
  
> [out] Pointeur vers une structure [SPropTagArray](sproptagarray.md) contenant les balises de propriété pour l’ensemble de colonnes. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’ensemble de colonnes a été retourné avec succès.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche le démarrage de l’opération de récupération du jeu de colonnes. Soit l’opération en cours doit être autorisée à se terminer, soit elle doit être arrêtée.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::QueryColumns** peut être appelée pour récupérer : 
  
- Jeu de colonnes par défaut pour une table.
    
- Colonne actuelle définie pour une table, telle qu’établie par un appel à la méthode [IMAPITable::SetColumns](imapitable-setcolumns.md) . 
    
- Ensemble de colonnes complet pour une table, colonnes disponibles, mais pas nécessairement partie de l’ensemble actuel.
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si vous ne définissez pas l’indicateur TBL_ALL_COLUMNS, **IMAPITable::QueryColumns** retourne l’ensemble de colonnes par défaut ou actuel d’une table, selon que la table a été affectée par un appel à **IMAPITable::SetColumns**. **SetColumns** modifie l’ordre et la sélection des colonnes dans l’ensemble de colonnes d’une table. 
  
Si vous définissez l’indicateur TBL_ALL_COLUMNS, **QueryColumns** retourne toutes les colonnes capables d’être dans le jeu de colonnes de la table. 
  
Libérez la mémoire du tableau de balises de propriétés pointé par le paramètre  _lpPropTagArray_ en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oSetColumns  <br/> |MFCMAPI utilise la méthode **IMAPITable::QueryColumns** pour récupérer le jeu de colonnes actuel pour une table afin que l’utilisateur puisse la modifier. |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

