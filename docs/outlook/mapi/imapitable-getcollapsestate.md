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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 46d993060d03b8c22c2d6c083c05f023648e6642
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589664"
---
# <a name="imapitablegetcollapsestate"></a>IMAPITable::GetCollapseState

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne les données nécessaires à la recréation en cours réduit ou développé état d’une table, voir.
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> Réservé ; doit être égal à zéro.
    
 _cbInstanceKey_
  
> [in] Le nombre d’octets dans la clé de l’instance indiqué par le paramètre _lpbInstanceKey_ . 
    
 _lpbInstanceKey_
  
> [in] Un pointeur vers la propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) de la ligne à laquelle actuel réduit ou développé état doit être reconstruit. Le paramètre _lpbInstanceKey_ ne peut pas être NULL. 
    
 _lpcbCollapseState_
  
> [out] Un pointeur vers le nombre de structures indiqué par le paramètre _lppbCollapseState_ . 
    
 _lppbCollapseState_
  
> [out] Pointeur vers un pointeur vers les structures qui contiennent des données qui décrit l’affichage tableau actuel.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’état de la table par catégorie a été enregistré avec succès.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche l’opération de démarrage. L’opération en cours doit être autorisée à effectuer ou il doit être arrêté.
    
MAPI_E_NO_SUPPORT 
  
> Le tableau ne gère pas la catégorisation et vues développée et réduite.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::GetCollapseState** fonctionne avec la méthode [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) pour modifier l’affichage de l’utilisateur d’une table, voir. **GetCollapseState** enregistre les données nécessaires pour **SetCollapseState** à utiliser pour reconstruire les affichages des catégories d’une table, voir appropriés. Fournisseurs de services de déterminent les données à enregistrer. Toutefois, la plupart des fournisseurs de services de mise en œuvre **GetCollapseState** enregistrement les éléments suivants : 
  
- Les clés de tri (colonnes standards et les colonnes de catégorie).
    
- Plus d’informations sur la ligne qui représente la clé d’instance.
    
- Informations pour restaurer les catégories de réduction et le développement de la table.
    
Pour plus d’informations sur les tables, voir, consultez [tri et catégorisation](sorting-and-categorization.md).
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Stocker l’état actuel de tous les nœuds d’un tableau dans le paramètre _lppbCollapseState_ . 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Toujours appeler **GetCollapseState** avant d’appeler **SetCollapseState**. 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

