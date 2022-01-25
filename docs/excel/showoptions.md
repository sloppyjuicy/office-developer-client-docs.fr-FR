---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
ms.openlocfilehash: 024ec7d80bd026b3c8228a32efa70b266577ab96
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62199275"
---
# <a name="showoptions"></a>ShowOptions

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Affiche une boîte de dialogue modale pour collecter des informations auprès de l’utilisateur. Ce point d’entrée est appelé lorsqu’un utilisateur clique sur le bouton **Options** en dessous de la zone  de **type** cluster pour le connecteur de cluster sélectionné dans la boîte de dialogue **Options Excel** (dans la catégorie Avancé sous la section **Formules).** Les connecteurs de cluster sont chargés d’implémenter leur propre interface de boîte de dialogue d’options et de stocker les données associées dans le Registre ou ailleurs. Les options sont internes au connecteur de cluster. Excel ne les connaît pas. 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a>Paramètres

_hWndParent_
  
> Poignée vers la fenêtre Excel fenêtre.
    
## <a name="return-value"></a>Valeur renvoyée

**xlHpcRetSuccess si** la boîte de dialogue était affichée ; **xlHpcRetCallFailed s’il** n’a pas été affiché. 
  
## <a name="remarks"></a>Remarques

Les connecteurs de cluster peuvent utiliser cette boîte de dialogue pour obtenir des informations, telles que le serveur de cluster à utiliser, de l’utilisateur.
  
## <a name="see-also"></a>Voir aussi

- [Fonctions du connecteur de cluster Excel](excel-cluster-connector-functions.md)

