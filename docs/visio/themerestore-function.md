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
# <a name="themerestore-function"></a><span data-ttu-id="32d20-103">Fonction THEMERESTORE</span><span class="sxs-lookup"><span data-stu-id="32d20-103">THEMERESTORE Function</span></span>

<span data-ttu-id="32d20-104">Stocke la valeur de mise en forme locale d’une forme lorsque vous appliquez un thème afin de pouvoir restaurer la mise en forme locale si l’utilisateur supprime ensuite le thème.</span><span class="sxs-lookup"><span data-stu-id="32d20-104">Stores the local formatting value of a shape when you apply a theme so that you can restore the local formatting if the user subsequently removes the theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="32d20-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32d20-105">Syntax</span></span>

<span data-ttu-id="32d20-106">THEMERESTORE()</span><span class="sxs-lookup"><span data-stu-id="32d20-106">THEMERESTORE()</span></span>
  
## <a name="example"></a><span data-ttu-id="32d20-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="32d20-107">Example</span></span>

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

<span data-ttu-id="32d20-108">Restaure la mise en forme de couleur de remplissage locale appliquée précédemment à une forme si le thème actif est supprimé.</span><span class="sxs-lookup"><span data-stu-id="32d20-108">Restores local fill color formatting previously applied to a shape when the current theme is removed.</span></span>
  

