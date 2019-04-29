---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5b58b71dc4f2441448eb3e0dac2c3c5763675927
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407696"
---
# <a name="showoptions"></a>ShowOptions

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Affiche une boîte de dialogue modale pour collecter des informations auprès de l'utilisateur. Ce point d'entrée est appelé lorsqu'un utilisateur clique sur le bouton **options** en regard de la zone **type de cluster** pour le connecteur de cluster sélectionné dans la boîte de dialogue **Options Excel** (dans la catégorie **avancé** , sous la section **formules** ). Les connecteurs de cluster sont chargés d'implémenter leur propre interface de boîte de dialogue Options et de stocker les données associées dans le registre ou ailleurs. Les options sont internes au connecteur de cluster. Excel ne les prend pas en compte. 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a>Paramètres

_hWndParent_
  
> Handle de la fenêtre Excel.
    
## <a name="return-value"></a>Valeur renvoyée

**xlHpcRetSuccess** si la boîte de dialogue a été affichée; **xlHpcRetCallFailed** si elle n'a pas été affichée. 
  
## <a name="remarks"></a>Remarques

Les connecteurs de cluster peuvent utiliser cette boîte de dialogue pour obtenir des informations, telles que le serveur de cluster à utiliser, de l'utilisateur.
  
## <a name="see-also"></a>Voir aussi

- [Fonctions du connecteur de cluster Excel](excel-cluster-connector-functions.md)

