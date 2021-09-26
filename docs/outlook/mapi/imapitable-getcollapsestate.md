---
title: IMAPITableGetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.GetCollapseState
api_type:
- COM
ms.assetid: fd4ea496-4c83-49cd-854e-f373cc1ed2af
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 64a63e860f423b7de56bce277f778576c2ed44c1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620834"
---
# <a name="imapitablegetcollapsestate"></a>IMAPITable::GetCollapseState

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie les données nécessaires pour reconstruire l’état actuel, réduire ou développé, d’une table classée.
  
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
  
> Réservé ; doit être zéro.
    
 _cbInstanceKey_
  
> [in] Nombre d’octets dans la clé d’instance pointée par _le paramètre lpbInstanceKey._ 
    
 _lpbInstanceKey_
  
> [in] Pointeur vers la **propriété PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) de la ligne à laquelle l’état actuellement réduire ou développé doit être reconstruit. Le  _paramètre lpbInstanceKey ne_ peut pas être NULL. 
    
 _lpcbCollapseState_
  
> [out] Pointeur vers le nombre de structures pointées par _le paramètre lppbCollapseState._ 
    
 _lppbCollapseState_
  
> [out] Pointeur vers un pointeur vers des structures qui contiennent des données décrivent l’affichage tableau actuel.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’état de la table classée a été enregistré avec succès.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche le démarrage de l’opération. L’opération en cours doit être autorisée ou arrêtée.
    
MAPI_E_NO_SUPPORT 
  
> Le tableau ne prend pas en charge la catégorisation et les affichages développés et réduire.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPITable::GetCollapseState** fonctionne avec la méthode [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) pour modifier l’affichage d’une table classée par l’utilisateur. **GetCollapseState** enregistre les données nécessaires à l’utilisation de **SetCollapseState** pour reconstruire les affichages appropriés des catégories d’une table classée. Les fournisseurs de services déterminent les données à enregistrées. Toutefois, la plupart des fournisseurs de services implémentant **GetCollapseState** enregistrent les données suivantes : 
  
- Clés de tri (colonnes standard et colonnes de catégorie).
    
- Informations sur la ligne représentée par la clé d’instance.
    
- Informations pour restaurer les catégories collapsed et expanded du tableau.
    
Pour plus d’informations sur les tableaux classés, voir [Tri et catégorisation.](sorting-and-categorization.md)
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Stockez l’état actuel de tous les nodes d’une table dans le _paramètre lppbCollapseState._ 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Toujours appeler **GetCollapseState** avant d’appeler **SetCollapseState**. 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

