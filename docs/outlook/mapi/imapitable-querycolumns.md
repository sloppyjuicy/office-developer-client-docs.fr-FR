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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d142e19fc4721cec4dde0df7fc030a001121da63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328881"
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
  
> dans Masque de des indicateurs qui indique quel jeu de colonnes doit être renvoyé. L'indicateur suivant peut être défini:
    
TBL_ALL_COLUMNS 
  
> Le tableau doit renvoyer toutes les colonnes disponibles.
    
 _lpPropTagArray_
  
> remarquer Pointeur vers une structure [SPropTagArray](sproptagarray.md) contenant les balises de propriété pour le jeu de colonnes. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le jeu de colonnes a été renvoyé avec succès.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours, ce qui empêche le démarrage de l'opération de récupération du jeu de colonnes. L'opération en cours doit être autorisée ou elle doit être arrêtée.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable:: QueryColumns** peut être appelée pour extraire les éléments suivants: 
  
- Colonne par défaut définie pour un tableau.
    
- La colonne actuelle définie pour une table, telle qu'établie par un appel à la méthode [IMAPITable:: SetColumns](imapitable-setcolumns.md) . 
    
- La colonne complète d'un tableau, les colonnes qui sont disponibles, mais qui ne font pas nécessairement partie de l'ensemble actuel.
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si vous ne définissez pas l'indicateur TBL_ALL_COLUMNS, **IMAPITable:: QueryColumns** renvoie le jeu de colonnes par défaut ou par défaut d'une table, selon que la table a été affectée ou non par un appel de la méthode **IMAPITable:: SetColumns**. **SetColumns** modifie l'ordre et la sélection des colonnes dans le jeu de colonnes d'un tableau. 
  
Si vous définissez l'indicateur TBL_ALL_COLUMNS, **QueryColumns** renvoie toutes les colonnes susceptibles de se situer dans le jeu de colonnes de la table. 
  
Libérez de la mémoire pour le tableau de balises de propriété pointé par le paramètre _lpPropTagArray_ en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl::D oSetColumns  <br/> |MFCMAPI utilise la méthode **IMAPITable:: QueryColumns** pour récupérer le jeu de colonnes actuel d'une table de sorte que l'utilisateur puisse le modifier.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

