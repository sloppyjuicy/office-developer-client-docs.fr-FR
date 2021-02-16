---
title: THEMERESTORE, fonction
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ca7e6621-f39b-64dd-3594-41d74da21a94
description: Stocke la valeur de mise en forme locale d’une forme lorsque vous appliquez un thème afin de pouvoir restaurer la mise en forme locale si l’utilisateur supprime ensuite le thème.
ms.openlocfilehash: 628e246f91172f136dd1a70807fca2abc1ff5bdd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404287"
---
# <a name="themerestore-function"></a>Fonction THEMERESTORE

Stocke la valeur de mise en forme locale d’une forme lorsque vous appliquez un thème afin que vous pouvez restaurer la mise en forme locale si l’utilisateur supprime ensuite le thème.
  
## <a name="syntax"></a>Syntaxe

THEMERESTORE()
  
## <a name="example"></a>Exemple

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

Restaure la mise en forme de couleur de remplissage locale appliquée précédemment à une forme si le thème actif est supprimé.
  

