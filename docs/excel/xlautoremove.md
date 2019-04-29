---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- fonction xlAutoRemove [Excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: af8bd2d44883b1820be42b82d4fe4794fa29caab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425476"
---
# <a name="xlautoremove"></a><span data-ttu-id="c426a-104">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="c426a-104">xlAutoRemove</span></span>

 <span data-ttu-id="c426a-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c426a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c426a-106">Appelé par Microsoft Excel chaque fois que l'utilisateur désactive le XLL au cours d'une session Excel à l'aide du gestionnaire de compléments.</span><span class="sxs-lookup"><span data-stu-id="c426a-106">Called by Microsoft Excel whenever the user deactivates the XLL during an Excel session by using the Add-In Manager.</span></span> <span data-ttu-id="c426a-107">Cette fonction n’est pas appelée lors de la fermeture normale ou anormale d’une session Excel lorsque le complément est installé.</span><span class="sxs-lookup"><span data-stu-id="c426a-107">This function is not called when an Excel session closes, normally or abnormally, with the add-in installed.</span></span>
  
<span data-ttu-id="c426a-108">Cette fonction permet d'afficher une boîte de dialogue personnalisée indiquant à l'utilisateur que le complément a été désactivé ou de lire ou d'écrire dans le registre, par exemple.</span><span class="sxs-lookup"><span data-stu-id="c426a-108">This function can be used to display a custom dialog box telling the user that the add-in has been deactivated, or to read from or write to the registry, for example.</span></span>
  
<span data-ttu-id="c426a-109">Excel ne requiert pas de XLL pour implémenter et exporter cette fonction.</span><span class="sxs-lookup"><span data-stu-id="c426a-109">Excel does not require an XLL to implement and export this function.</span></span> 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a><span data-ttu-id="c426a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c426a-110">Parameters</span></span>

<span data-ttu-id="c426a-111">Cette fonction ne prend aucun argument.</span><span class="sxs-lookup"><span data-stu-id="c426a-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="c426a-112">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="c426a-112">Property value/Return value</span></span>

<span data-ttu-id="c426a-113">Votre exécution de cette fonction doit renvoyer 1 (**ent**).</span><span class="sxs-lookup"><span data-stu-id="c426a-113">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c426a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c426a-114">Remarks</span></span>

<span data-ttu-id="c426a-115">Utilisez cette fonction si votre XLL doit effectuer une tâche lorsqu'elle est supprimée par le gestionnaire de compléments.</span><span class="sxs-lookup"><span data-stu-id="c426a-115">Use this function if your XLL needs to complete any task when it is removed by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="c426a-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="c426a-116">Example</span></span>

<span data-ttu-id="c426a-117">Reportez-vous aux fichiers `\SAMPLES\EXAMPLE\EXAMPLE.C` et `\SAMPLES\GENERIC\GENERIC.C` pour des exemples d’implémentation de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="c426a-117">See the files  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="c426a-118">Le code suivant provient de `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="c426a-118">The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="c426a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c426a-119">See also</span></span>



[<span data-ttu-id="c426a-120">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="c426a-120">xlAutoAdd</span></span>](xlautoadd.md)


[<span data-ttu-id="c426a-121">Fonctions du Gestionnaire de compléments et de l’interface XLL</span><span class="sxs-lookup"><span data-stu-id="c426a-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

