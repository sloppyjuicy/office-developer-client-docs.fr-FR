---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: dbf6f0f50e9f7fa988e83f3b58012e9deac13eac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782191"
---
# <a name="showoptions"></a>ShowOptions

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Affiche la boîte de dialogue modale pour collecter des informations à partir de l’utilisateur. Ce point d’entrée est appelé lorsqu’un utilisateur clique sur le bouton **Options** en regard de la zone **type de Cluster** pour le connecteur de cluster sélectionné dans la boîte de dialogue **Options Excel** (dans la catégorie **Avancé** , dans la section **formules** ). Connecteurs de cluster sont responsables de leur propre interface de la boîte de dialogue options de mise en œuvre et de stockage des données connexes dans le Registre ou un autre emplacement. Les options sont des utilisateurs internes pour le connecteur de cluster. Excel n’a pas connaissance d’eux. 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a>Paramètres

_hWndParent_
  
> Un handle vers la fenêtre Excel.
    
## <a name="return-value"></a>Valeur renvoy�e

**xlHpcRetSuccess** si la boîte de dialogue a été affichée ; **xlHpcRetCallFailed** si elle n’était pas affichée. 
  
## <a name="remarks"></a>Remarques

Connecteurs de cluster peuvent utiliser cette boîte de dialogue pour obtenir des informations, telles que le serveur de cluster à utiliser, à partir de l’utilisateur.
  
## <a name="see-also"></a>Voir aussi

- [Fonctions du connecteur de Cluster Excel](excel-cluster-connector-functions.md)

