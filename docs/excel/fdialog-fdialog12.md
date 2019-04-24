---
title: fDialog/fDialog12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDialog
- fDialog12
keywords:
- fonction fdialog [Excel 2007], fonction fDialog12 [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 58d0df500c38534ec1315d2dab1517c1f5272ad5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304066"
---
# <a name="fdialogfdialog12"></a><span data-ttu-id="b9808-104">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="b9808-104">fDialog/fDialog12</span></span>

 <span data-ttu-id="b9808-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b9808-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b9808-106">Exemple de commande définie par l'utilisateur montrant comment créer une UDD Microsoft Excel (boîte de dialogue définie par l'utilisateur) dans une DLL à l'aide des fonctionnalités de la boîte de dialogue de l'API C.</span><span class="sxs-lookup"><span data-stu-id="b9808-106">Example user-defined command that demonstrates how to create a Microsoft Excel UDD (user-defined dialog box) within a DLL by using the dialog box capabilities in the C API.</span></span> <span data-ttu-id="b9808-107">Lorsque GENERIC. xll est chargé, il crée un menu défini par l'utilisateur, générique, par le biais duquel cette commande est accédée.</span><span class="sxs-lookup"><span data-stu-id="b9808-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="b9808-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9808-108">Parameters</span></span>

<span data-ttu-id="b9808-109">La fonction ne prend aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b9808-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="b9808-110">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="b9808-110">Property value/Return value</span></span>

<span data-ttu-id="b9808-111">La fonction renvoie toujours 1.</span><span class="sxs-lookup"><span data-stu-id="b9808-111">The function always returns 1.</span></span>
  
### <a name="example"></a><span data-ttu-id="b9808-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="b9808-112">Example</span></span>

<span data-ttu-id="b9808-113">Voir `\SAMPLES\GENERIC\GENERIC.C` pour obtenir le code source de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="b9808-113">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b9808-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9808-114">See also</span></span>



[<span data-ttu-id="b9808-115">Fonctions dans le fichier DLL générique</span><span class="sxs-lookup"><span data-stu-id="b9808-115">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

