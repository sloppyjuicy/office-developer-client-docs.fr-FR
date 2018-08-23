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
ms.openlocfilehash: e6803c54ddd60c1bcebbe7a139c2edf2e7f4449d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572086"
---
# <a name="imapitableseekrowapprox"></a>IMAPITable::SeekRowApprox

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Déplace le curseur à une position en fraction approximative dans le tableau. 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a>Paramètres

 _ulNumerator_
  
> [in] Pointeur vers le numérateur de la fraction qui représente la position de la table. Si le paramètre _ulNumerator_ est égale à zéro, le curseur est positionné au début de la table indépendamment de la valeur du dénominateur. Si _ulNumerator_ est égal au paramètre _ulDenominator_ , le curseur est positionné après la dernière ligne du tableau. 
    
 _ulDenominator_
  
> [in] Pointeur vers le dénominateur de la fraction qui représente la position de la table. Le paramètre _ulDenominator_ ne peut pas être égal à zéro. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’opération de recherche a réussi.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche la ligne opération de démarrage de recherche. L’opération en cours doit être autorisée à effectuer ou il doit être arrêté.
    
## <a name="remarks"></a>Remarques

La position du curseur dans une table après un appel à la méthode **IMAPI::SeekRowApprox** correspond à la fraction heuristique et peuvent ne pas être exacte. Par exemple, certains fournisseurs peuvent implémenter une table par-dessus un arbre binaire, traitement mi-chemin la table en tant que la partie supérieure de l’arborescence pour des raisons de performances. Si l’arborescence n’est pas équilibrée, le point à mi-chemin utilisé ne peut pas être exactement au cours de la table. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Appelez **SeekRowApprox** pour fournir les données pour une implémentation de barre de défilement. Par exemple, si l’utilisateur place le défilement zone 2/3 vers le bas de la barre de défilement, vous pouvez modéliser cette action en appelant **SeekRowApprox** et en passant une valeur décimale équivalente à l’aide de _ulNumerator_ et _ulDenominator_. La recherche **SeekRowApprox** est toujours absolue depuis le début de la table. Pour déplacer vers la fin de la table, les valeurs dans _ulNumerator_ et _ulDenominator_ doivent être identiques. 
  
Utilisez le modèle de numéros est approprié. Autrement dit, pour rechercher une position à mi-chemin par le biais de la table, vous pouvez spécifier 1/2, 10/20 ou 50/100. 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable : IUnknown](imapitableiunknown.md)

