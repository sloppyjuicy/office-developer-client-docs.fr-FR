---
title: IMAPITableGetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetCollapseState
api_type:
- COM
ms.assetid: fd4ea496-4c83-49cd-854e-f373cc1ed2af
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 97575a65cd6825e07d6f11c813beec539f99f53a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328925"
---
# <a name="imapitablegetcollapsestate"></a>IMAPITable::GetCollapseState

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie les données nécessaires pour recréer l'État réduit ou développé actuel d'une table catégorisée.
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> MSR doit être égal à zéro.
    
 _cbInstanceKey_
  
> dans Nombre d'octets dans la clé d'instance vers laquelle pointe le paramètre _lpbInstanceKey_ . 
    
 _lpbInstanceKey_
  
> dans Pointeur vers la propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) de la ligne à laquelle l'État réduit ou développé actuel doit être reconstruit. Le paramètre _lpbInstanceKey_ ne peut pas être null. 
    
 _lpcbCollapseState_
  
> remarquer Pointeur vers le nombre de structures vers lesquelles pointe le paramètre _lppbCollapseState_ . 
    
 _lppbCollapseState_
  
> remarquer Pointeur vers un pointeur vers des structures qui contiennent des données qui décrivent la vue de tableau actuelle.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'état de la table catégorisée a été enregistré avec succès.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours, ce qui empêche le démarrage de l'opération. L'opération en cours doit être autorisée ou elle doit être arrêtée.
    
MAPI_E_NO_SUPPORT 
  
> Le tableau ne prend pas en charge la catégorisation, ni les vues développées et réduites.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable:: GetCollapseState** fonctionne avec la méthode [IMAPITable:: SetCollapseState](imapitable-setcollapsestate.md) pour modifier l'affichage de l'utilisateur d'une table catégorisée. **GetCollapseState** enregistre les données nécessaires à **SetCollapseState** pour recréer les vues appropriées des catégories d'une table classée. Les fournisseurs de services déterminent les données à enregistrer. Toutefois, la plupart des fournisseurs de services qui implémentent **GetCollapseState** enregistrent les éléments suivants: 
  
- Les clés de tri (colonnes standard et colonnes de catégorie).
    
- Informations sur la ligne représentée par la clé d'instance.
    
- Informations permettant de restaurer les catégories réduites et développées du tableau.
    
Pour plus d'informations sur les tables classées, reportez-vous à la rubrique [Tri et catégorisation](sorting-and-categorization.md).
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Stockez l'état actuel de tous les nœuds d'une table dans le paramètre _lppbCollapseState_ . 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez toujours **GetCollapseState** avant d'appeler **SetCollapseState**. 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

