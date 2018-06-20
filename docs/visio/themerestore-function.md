---
title: THEMERESTORE, fonction
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ca7e6621-f39b-64dd-3594-41d74da21a94
description: Stocke la valeur mise en forme locale d’une forme lorsque vous appliquez un thème pour que vous pouvez restaurer la mise en forme locale si l’utilisateur supprime ensuite le thème.
ms.openlocfilehash: f22f603cad1d310adc59d19e9b3e3882bd797fce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789901"
---
# <a name="themerestore-function"></a>THEMERESTORE, fonction

Stocke la valeur mise en forme locale d’une forme lorsque vous appliquez un thème pour que vous pouvez restaurer la mise en forme locale si l’utilisateur supprime ensuite le thème.
  
## <a name="syntax"></a>Syntaxe

THEMERESTORE()
  
## <a name="example"></a>Exemple

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

Restaure la mise en forme de couleur de remplissage locale appliquée précédemment à une forme si le thème actif est supprimé.
  

