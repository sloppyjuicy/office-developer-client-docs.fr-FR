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
- fdialog function [excel 2007],fDialog12 function [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 58d0df500c38534ec1315d2dab1517c1f5272ad5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431525"
---
# <a name="fdialogfdialog12"></a><span data-ttu-id="9e0bb-104">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="9e0bb-104">fDialog/fDialog12</span></span>

 <span data-ttu-id="9e0bb-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9e0bb-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9e0bb-106">Exemple de commande définie par l’utilisateur qui montre comment créer un UDD Microsoft Excel (boîte de dialogue définie par l’utilisateur) dans une DLL à l’aide des fonctionnalités de la boîte de dialogue dans l’API C.</span><span class="sxs-lookup"><span data-stu-id="9e0bb-106">Example user-defined command that demonstrates how to create a Microsoft Excel UDD (user-defined dialog box) within a DLL by using the dialog box capabilities in the C API.</span></span> <span data-ttu-id="9e0bb-107">Lorsque GENERIC.xll est chargé, il crée un menu défini par l’utilisateur, Generic, via lequel cette commande est accessible.</span><span class="sxs-lookup"><span data-stu-id="9e0bb-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="9e0bb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e0bb-108">Parameters</span></span>

<span data-ttu-id="9e0bb-109">La fonction ne prend aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9e0bb-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="9e0bb-110">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="9e0bb-110">Property value/Return value</span></span>

<span data-ttu-id="9e0bb-111">La fonction renvoie toujours 1.</span><span class="sxs-lookup"><span data-stu-id="9e0bb-111">The function always returns 1.</span></span>
  
### <a name="example"></a><span data-ttu-id="9e0bb-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="9e0bb-112">Example</span></span>

<span data-ttu-id="9e0bb-113">Voir  `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="9e0bb-113">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9e0bb-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e0bb-114">See also</span></span>



[<span data-ttu-id="9e0bb-115">Fonctions dans le fichier DLL générique</span><span class="sxs-lookup"><span data-stu-id="9e0bb-115">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

