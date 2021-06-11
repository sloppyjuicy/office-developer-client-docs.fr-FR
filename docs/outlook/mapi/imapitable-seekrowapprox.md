---
title: IMAPITableSeekRowApprox
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRowApprox
api_type:
- COM
ms.assetid: ce5e8c43-06af-4afc-9138-5cc51d8fc401
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bbb79097d03a8ea09cb4aff374231ee780e15395
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412148"
---
# <a name="imapitableseekrowapprox"></a>IMAPITable::SeekRowApprox

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Déplace le curseur vers une position fractionnaire approximative dans le tableau. 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a>Parameters

 _ulNumerator_
  
> [in] Pointeur vers le numérateur de la fraction représentant la position du tableau. Si le  _paramètre ulNumerator_ est zéro, le curseur est placé au début de la table, quelle que soit la valeur du dénominateur. Si  _ulNumerator est_ égal au paramètre  _ulDenominator,_ le curseur est placé après la dernière ligne du tableau. 
    
 _ulDenominator_
  
> [in] Pointeur vers le dénominateur de la fraction représentant la position du tableau. Le  _paramètre ulDenominator ne peut_ pas être zéro. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’opération de recherche a réussi.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche le démarrage de l’opération de recherche de lignes. L’opération en cours doit être autorisée ou arrêtée.
    
## <a name="remarks"></a>Remarques

La position du curseur dans une table après un appel à la méthode **IMAPITable::SeekRowApprox** est heuristiquement la fraction et peut ne pas être exacte. Par exemple, certains fournisseurs peuvent implémenter un tableau au-dessus d’une arborescence binaire, en traitant le point à mi-chemin de la table comme le haut de l’arborescence pour des raisons de performances. Si l’arborescence n’est pas équilibrée, le point à mi-chemin utilisé risque de ne pas être exactement à mi-chemin du tableau. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez **SeekRowApprox** pour fournir les données d’une implémentation de barre de défilement. Par exemple, si l’utilisateur place la case de défilement 2/3 vers le bas de la barre de défilement, vous pouvez modéliser cette action en appelant **SeekRowApprox** et en passant une valeur fractionnaire équivalente à l’aide  _d’ulNumerator_ et  _ulDenominator_. La **recherche SeekRowApprox** est toujours absolue à partir du début du tableau. Pour aller à la fin du tableau, les valeurs dans  _ulNumerator_ et  _ulDenominator_ doivent être identiques. 
  
Utilisez n’importe quel schéma de nombres approprié. Autrement dit, pour rechercher une position à mi-chemin du tableau, vous pouvez spécifier 1/2, 10/20 ou 50/100. 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable : IUnknown](imapitableiunknown.md)

