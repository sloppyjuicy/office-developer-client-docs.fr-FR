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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ae6d8b2f0b95641678947e9bd75daa2237b080b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782135"
---
# <a name="fshowdialog"></a><span data-ttu-id="0081b-104">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="0081b-104">fShowDialog</span></span>

 <span data-ttu-id="0081b-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0081b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0081b-106">Exemple définies par l’utilisateur de commande qui charge et affiche une boîte de dialogue Windows native exemple.</span><span class="sxs-lookup"><span data-stu-id="0081b-106">Example user-defined command that loads and displays an example native Windows dialog box.</span></span> <span data-ttu-id="0081b-107">Lorsque GENERIC.xll est chargé, il crée un menu défini par l’utilisateur, générique, par le biais de laquelle cette commande est accessible.</span><span class="sxs-lookup"><span data-stu-id="0081b-107">When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="0081b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0081b-108">Parameters</span></span>

<span data-ttu-id="0081b-109">La fonction ne prend aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0081b-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="0081b-110">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0081b-110">Property value/Return value</span></span>

<span data-ttu-id="0081b-111">La fonction retour entier entre zéro pour indiquer la réussite de l’opération</span><span class="sxs-lookup"><span data-stu-id="0081b-111">The function return integer zero to indicate successful completion</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0081b-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="0081b-112">Remarks</span></span>

<span data-ttu-id="0081b-113">Les étapes pour afficher la boîte de dialogue Windows native sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0081b-113">The steps to display the native Windows dialog box are as follows:</span></span>
  
1. <span data-ttu-id="0081b-114">Obtenir le handle Windows principal Microsoft Excel à l’aide de **GetHwnd**.</span><span class="sxs-lookup"><span data-stu-id="0081b-114">Obtain the Microsoft Excel main Windows handle using **GetHwnd**.</span></span>
    
2. <span data-ttu-id="0081b-115">Connecter la fenêtre principale de Excel à l’aide de **HookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="0081b-115">Hook the Excel main window using **HookExcelWindow**.</span></span>
    
3. <span data-ttu-id="0081b-116">Afficher la boîte de dialogue à l’aide de **DialogBox**.</span><span class="sxs-lookup"><span data-stu-id="0081b-116">Display the dialog box using **DialogBox**.</span></span>
    
4. <span data-ttu-id="0081b-117">Décrocher la fenêtre principale de Excel à l’aide de **UnhookExcelWindow**.</span><span class="sxs-lookup"><span data-stu-id="0081b-117">Unhook the Excel main window using **UnhookExcelWindow**.</span></span>
    
### <a name="example"></a><span data-ttu-id="0081b-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="0081b-118">Example</span></span>

<span data-ttu-id="0081b-119">Voir `\SAMPLES\GENERIC\GENERIC.C` pour le code source pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="0081b-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0081b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0081b-120">See also</span></span>



[<span data-ttu-id="0081b-121">Fonctions de la DLL générique</span><span class="sxs-lookup"><span data-stu-id="0081b-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

