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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328839"
---
# <a name="imapitableseekrowapprox"></a>IMAPITable::SeekRowApprox

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Place le curseur sur une position fractionnaire approximative dans le tableau. 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a>Paramètres

 _ulNumerator_
  
> dans Pointeur vers le numérateur de la fraction représentant la position de la table. Si le paramètre _ulNumerator_ est égal à zéro, le curseur est positionné au début de la table, quelle que soit la valeur du dénominateur. Si _ulNumerator_ est égal au paramètre _ulDenominator_ , le curseur est positionné après la dernière ligne de tableau. 
    
 _ulDenominator_
  
> dans Pointeur vers le dénominateur de la fraction représentant la position de la table. Le paramètre _ulDenominator_ ne peut pas être égal à zéro. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'opération Seek a réussi.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours, ce qui empêche le démarrage de l'opération de recherche de ligne. L'opération en cours doit être autorisée ou elle doit être arrêtée.
    
## <a name="remarks"></a>Remarques

La position du curseur dans un tableau après un appel à la méthode **IMAPITable:: SeekRowApprox** est la fraction de manière heuristique et peut ne pas être exacte. Par exemple, certains fournisseurs peuvent implémenter une table en haut d'une arborescence binaire, en traitant le point central de la table en tant que haut de l'arborescence pour des raisons de performances. Si l'arborescence n'est pas équilibrée, le point central utilisé peut ne pas être exactement au milieu de la table. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez **SeekRowApprox** pour fournir les données d'une implémentation de barre de défilement. Par exemple, si l'utilisateur positionne la case de défilement 2/3 vers le bas dans la barre de défilement, vous pouvez modéliser cette action en appelant **SeekRowApprox** et en transmettant une valeur fractionnaire équivalente à l'aide de _UlNumerator_ et de _ulDenominator_. La recherche **SeekRowApprox** est toujours absolue à partir du début de la table. Pour accéder à la fin de la table, les valeurs dans _ulNumerator_ et _ulDenominator_ doivent être identiques. 
  
Utilisez un modèle de nombre approprié. Autrement dit, pour rechercher une position à mi-parcours de la table, vous pouvez spécifier 1/2, 10/20 ou 50/100. 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable : IUnknown](imapitableiunknown.md)

