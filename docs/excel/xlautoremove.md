---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- fonction xlautoremove [excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 6e5daac21a6d89472a7d84a25e9aeaea56db1ae1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782220"
---
# <a name="xlautoremove"></a><span data-ttu-id="ff225-104">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="ff225-104">xlAutoRemove</span></span>

 <span data-ttu-id="ff225-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ff225-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ff225-106">Appelée par Microsoft Excel lorsque l’utilisateur désactive le XLL pendant une session Excel à l’aide du Gestionnaire de compléments.</span><span class="sxs-lookup"><span data-stu-id="ff225-106">Called by Microsoft Excel whenever the user deactivates the XLL during an Excel session by using the Add-In Manager.</span></span> <span data-ttu-id="ff225-107">Cette fonction n’est pas appelée lorsqu’une session Excel se ferme, normale ou anormale, avec le complément installé.</span><span class="sxs-lookup"><span data-stu-id="ff225-107">This function is not called when an Excel session closes, normally or abnormally, with the add-in installed.</span></span>
  
<span data-ttu-id="ff225-108">Cette fonction peut être utilisée pour afficher une boîte de dialogue personnalisée pour présenter à l’utilisateur que le complément a été désactivé, ou pour lire ou écrire dans le Registre, par exemple.</span><span class="sxs-lookup"><span data-stu-id="ff225-108">This function can be used to display a custom dialog box telling the user that the add-in has been deactivated, or to read from or write to the registry, for example.</span></span>
  
<span data-ttu-id="ff225-109">Excel ne nécessite pas un ressource XLL à mettre en œuvre et exporter cette fonction.</span><span class="sxs-lookup"><span data-stu-id="ff225-109">Excel does not require an XLL to implement and export this function.</span></span> 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a><span data-ttu-id="ff225-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff225-110">Parameters</span></span>

<span data-ttu-id="ff225-111">Cette fonction prend aucun argument.</span><span class="sxs-lookup"><span data-stu-id="ff225-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="ff225-112">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ff225-112">Property value/Return value</span></span>

<span data-ttu-id="ff225-113">Votre implémentation de cette fonction doit renvoyer 1 (**int**).</span><span class="sxs-lookup"><span data-stu-id="ff225-113">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ff225-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ff225-114">Remarks</span></span>

<span data-ttu-id="ff225-115">Utilisez cette fonction si votre XLL a besoin effectuer toute tâche lorsqu’elle est supprimée par le Gestionnaire de compléments.</span><span class="sxs-lookup"><span data-stu-id="ff225-115">Use this function if your XLL needs to complete any task when it is removed by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="ff225-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="ff225-116">Example</span></span>

<span data-ttu-id="ff225-117">Consultez les fichiers `\SAMPLES\EXAMPLE\EXAMPLE.C` et `\SAMPLES\GENERIC\GENERIC.C` par exemple les implémentations de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="ff225-117">See the files  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="ff225-118">Le code suivant présente de `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="ff225-118">The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
```cs
int WINAPI xlAutoRemove(void)
{
/* Display a dialog box indicating that the XLL was successfully removed */
   Excel12f(xlcAlert, 0, 2,
      TempStr12(L"Thank you for removing Example.XLL!"),
      TempInt12(2));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="ff225-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff225-119">See also</span></span>



[<span data-ttu-id="ff225-120">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="ff225-120">xlAutoAdd</span></span>](xlautoadd.md)


[<span data-ttu-id="ff225-121">Gestionnaire de compléments et les fonctions de l’Interface XLL</span><span class="sxs-lookup"><span data-stu-id="ff225-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

