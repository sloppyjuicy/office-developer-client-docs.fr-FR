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
- fonction fdialog [excel 2007], fonction fDialog12 [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 554b76d2d316110286e83158acfff33aa68e19c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782121"
---
# <a name="fdialogfdialog12"></a><span data-ttu-id="92d10-104">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="92d10-104">fDialog/fDialog12</span></span>

 <span data-ttu-id="92d10-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="92d10-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="92d10-106">Exemple définies par l’utilisateur de commande qui montre comment créer un Microsoft Excel BENNE Traînante (boîte de dialogue définie par l’utilisateur) dans une DLL en utilisant les fonctionnalités de boîte de dialogue de l’API C.</span><span class="sxs-lookup"><span data-stu-id="92d10-106">Example user-defined command that demonstrates how to create a Microsoft Excel UDD (user-defined dialog box) within a DLL by using the dialog box capabilities in the C API.</span></span> <span data-ttu-id="92d10-107">Lorsque GENERIC.xll est chargé, il crée un menu défini par l’utilisateur, générique, par le biais de laquelle cette commande est accessible.</span><span class="sxs-lookup"><span data-stu-id="92d10-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="92d10-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92d10-108">Parameters</span></span>

<span data-ttu-id="92d10-109">La fonction ne prend aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="92d10-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="92d10-110">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="92d10-110">Property value/Return value</span></span>

<span data-ttu-id="92d10-111">La fonction renvoie toujours 1.</span><span class="sxs-lookup"><span data-stu-id="92d10-111">The function always returns 1.</span></span>
  
### <a name="example"></a><span data-ttu-id="92d10-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="92d10-112">Example</span></span>

<span data-ttu-id="92d10-113">Voir `\SAMPLES\GENERIC\GENERIC.C` pour le code source pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="92d10-113">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="92d10-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92d10-114">See also</span></span>



[<span data-ttu-id="92d10-115">Fonctions de la DLL générique</span><span class="sxs-lookup"><span data-stu-id="92d10-115">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

