---
title: THEMERESTORE, fonction
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ca7e6621-f39b-64dd-3594-41d74da21a94
description: Stocke la valeur de mise en forme locale d’une forme lorsque vous appliquez un thème afin de pouvoir restaurer la mise en forme locale si l’utilisateur supprime ensuite le thème.
ms.openlocfilehash: 708dcf51a7a01c0f58dab435dd710208b5cb2ff1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597855"
---
# <a name="themerestore-function"></a>Fonction THEMERESTORE

Stocke la valeur de mise en forme locale d’une forme lorsque vous appliquez un thème afin de pouvoir restaurer la mise en forme locale si l’utilisateur supprime ensuite le thème.
  
## <a name="syntax"></a>Syntaxe

THEMERESTORE()
  
## <a name="example"></a>Exemple

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

Restaure la mise en forme de couleur de remplissage locale appliquée précédemment à une forme si le thème actif est supprimé.
  

