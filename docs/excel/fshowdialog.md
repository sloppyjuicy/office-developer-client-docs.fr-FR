---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- fonction fshowdialog [excel 2007]
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6122e4b99c69cd1bd878c9267ff85f59d0f61998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433590"
---
# <a name="fshowdialog"></a><span data-ttu-id="781c6-104">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="781c6-104">fShowDialog</span></span>

 <span data-ttu-id="781c6-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="781c6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="781c6-106">Exemple de commande définie par l’utilisateur qui charge et affiche un exemple de boîte de dialogue Windows native.</span><span class="sxs-lookup"><span data-stu-id="781c6-106">Example user-defined command that loads and displays an example native Windows dialog box.</span></span> <span data-ttu-id="781c6-107">Lorsque GENERIC.xll est chargé, il crée un menu défini par l’utilisateur, Generic, via lequel cette commande est accessible.</span><span class="sxs-lookup"><span data-stu-id="781c6-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="781c6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="781c6-108">Parameters</span></span>

<span data-ttu-id="781c6-109">La fonction ne prend aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="781c6-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="781c6-110">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="781c6-110">Property value/Return value</span></span>

<span data-ttu-id="781c6-111">La fonction retourne l’integer zéro pour indiquer l’achèvement réussi</span><span class="sxs-lookup"><span data-stu-id="781c6-111">The function return integer zero to indicate successful completion</span></span>
  
## <a name="remarks"></a><span data-ttu-id="781c6-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="781c6-112">Remarks</span></span>

<span data-ttu-id="781c6-113">Les étapes d’affichage de la boîte de dialogue Windows native sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="781c6-113">The steps to display the native Windows dialog box are as follows:</span></span>
  
1. <span data-ttu-id="781c6-114">Obtenez le handle Windows principal De Microsoft Excel à **l’aide de GetHwnd**.</span><span class="sxs-lookup"><span data-stu-id="781c6-114">Obtain the Microsoft Excel main Windows handle using **GetHwnd**.</span></span>
    
2. <span data-ttu-id="781c6-115">Hook the Excel main window using **HookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="781c6-115">Hook the Excel main window using **HookExcelWindow**.</span></span>
    
3. <span data-ttu-id="781c6-116">Afficher la boîte de dialogue à l’aide **de DialogBox**.</span><span class="sxs-lookup"><span data-stu-id="781c6-116">Display the dialog box using **DialogBox**.</span></span>
    
4. <span data-ttu-id="781c6-117">Unhook the Excel main window using **UnhookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="781c6-117">Unhook the Excel main window using **UnhookExcelWindow**.</span></span>
    
### <a name="example"></a><span data-ttu-id="781c6-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="781c6-118">Example</span></span>

<span data-ttu-id="781c6-119">Voir  `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="781c6-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="781c6-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="781c6-120">See also</span></span>



[<span data-ttu-id="781c6-121">Fonctions dans le fichier DLL générique</span><span class="sxs-lookup"><span data-stu-id="781c6-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

