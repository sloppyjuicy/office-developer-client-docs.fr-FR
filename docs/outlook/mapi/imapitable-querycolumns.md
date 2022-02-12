---
title: IMAPITableQueryColumns
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 870367f47b0c75e5324f8ef5f9682037a28582be
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62776388"
---
# <a name="imapitablequerycolumns"></a>IMAPITable::QueryColumns

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie une liste de colonnes pour le tableau.
  
```cpp
HRESULT QueryColumns(
ULONG ulFlags,
LPSPropTagArray FAR * lpPropTagArray
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui indique quel jeu de colonnes doit être renvoyé. L’indicateur suivant peut être définie :
    
TBL_ALL_COLUMNS 
  
> Le tableau doit renvoyer toutes les colonnes disponibles.
    
 _lpPropTagArray_
  
> [out] Pointeur vers une structure [SPropTagArray](sproptagarray.md) contenant les balises de propriété pour le jeu de colonnes. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le jeu de colonnes a été renvoyé avec succès.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche le démarrage de l’opération de récupération du jeu de colonnes. L’opération en cours doit être autorisée ou arrêtée.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPITable::QueryColumns** peut être appelée pour récupérer : 
  
- Colonne par défaut définie pour un tableau.
    
- Colonne actuelle définie pour une table, tel qu’établi par un appel à la méthode [IMAPITable::SetColumns](imapitable-setcolumns.md) . 
    
- Ensemble de colonnes complet d’un tableau, colonnes disponibles, mais pas nécessairement partie de l’ensemble actuel.
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si vous ne définissez pas l’indicateur TBL_ALL_COLUMNS, **IMAPITable::QueryColumns** renvoie l’ensemble de colonnes par défaut ou actuel d’une table, selon que la table a été affectée par un appel à **IMAPITable::SetColumns**. **SetColumns modifie l’ordre** et la sélection des colonnes dans le jeu de colonnes d’un tableau. 
  
Si vous définissez l’TBL_ALL_COLUMNS, **QueryColumns** renvoie toutes les colonnes pouvant être dans le jeu de colonnes de la table. 
  
Libérez la mémoire du tableau de balises de propriétés pointé par le paramètre  _lpPropTagArray_ en appelant la [fonction MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oSetColumns  <br/> |MFCMAPI utilise la méthode **IMAPITable::QueryColumns** pour récupérer le jeu de colonnes actuel d’une table afin que l’utilisateur puisse la modifier. |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

