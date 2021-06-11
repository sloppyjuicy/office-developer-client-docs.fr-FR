---
title: xlAutoClose
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoClose
keywords:
- fonction xlAutoClose [excel 2007]
localization_priority: Normal
ms.assetid: 147e46cd-d4d7-49eb-acdc-5a2ebc2fb6c2
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e27ac922c4ba53a30e8e485d3210acc62b7d4bd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415858"
---
# <a name="xlautoclose"></a><span data-ttu-id="d78a3-104">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="d78a3-104">xlAutoClose</span></span>

 <span data-ttu-id="d78a3-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d78a3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d78a3-106">Activée par Microsoft Excel chaque fois que la XLL est désactivée.</span><span class="sxs-lookup"><span data-stu-id="d78a3-106">Called by Microsoft Excel whenever the XLL is deactivated.</span></span> <span data-ttu-id="d78a3-107">Le complément est désactivé lorsqu’une session Excel se termine normalement.</span><span class="sxs-lookup"><span data-stu-id="d78a3-107">The add-in is deactivated when an Excel session ends normally.</span></span> <span data-ttu-id="d78a3-108">Le complément peut être désactivé par l’utilisateur pendant une session Excel et, dans ce cas, cette fonction est activée.</span><span class="sxs-lookup"><span data-stu-id="d78a3-108">The add-in can be deactivated by the user during an Excel session, and this function will be called in that case.</span></span>
  
<span data-ttu-id="d78a3-109">Excel ne requiert pas de XLL pour exécuter et exporter cette fonction, bien que cela soit conseillé afin que votre XLL puisse désinscrire des fonctions et des commandes, libérer des ressources, annuler des personnalisations et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="d78a3-109">Excel does not require an XLL to implement and export this function, although it is advisable so that your XLL can unregister functions and commands, release resources, undo customizations, and so on.</span></span> <span data-ttu-id="d78a3-110">Si les fonctions et les commandes ne sont pas explicitement désinscrites par la XLL, Excel l’effectue après avoir activé la fonction **xlAutoClose**.</span><span class="sxs-lookup"><span data-stu-id="d78a3-110">If functions and commands are not explicitly unregistered by the XLL, Excel does this after calling the **xlAutoClose** function.</span></span> 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a><span data-ttu-id="d78a3-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d78a3-111">Parameters</span></span>

<span data-ttu-id="d78a3-112">Cette fonction ne prend aucun argument.</span><span class="sxs-lookup"><span data-stu-id="d78a3-112">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d78a3-113">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="d78a3-113">Property value/Return value</span></span>

<span data-ttu-id="d78a3-114">Votre exécution de cette fonction doit renvoyer 1 (**ent**).</span><span class="sxs-lookup"><span data-stu-id="d78a3-114">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d78a3-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="d78a3-115">Remarks</span></span>

<span data-ttu-id="d78a3-116">Excel active la fonction **xlAutoClose** chaque fois que la XLL est désactivée, autrement dit, déchargée à partir de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="d78a3-116">Excel calls the **xlAutoClose** function whenever the XLL is deactivated, that is, unloaded from memory.</span></span> <span data-ttu-id="d78a3-117">La XLL est désactivée dans les situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d78a3-117">The XLL is deactivated in the following situations:</span></span> 
  
- <span data-ttu-id="d78a3-118">À la fin d’une session normale Excel si celle-ci est active au cours de cette session.</span><span class="sxs-lookup"><span data-stu-id="d78a3-118">At the normal end of an Excel session if active during that session.</span></span>
    
- <span data-ttu-id="d78a3-119">Si elle est explicitement déchargée pendant une session Excel.</span><span class="sxs-lookup"><span data-stu-id="d78a3-119">If explicitly unloaded during an Excel session.</span></span>
    
- <span data-ttu-id="d78a3-120">Une XLL peut être déchargée de différentes manières :</span><span class="sxs-lookup"><span data-stu-id="d78a3-120">An XLL can be unloaded in several ways:</span></span>
    
- <span data-ttu-id="d78a3-121">À l’aide du Gestionnaire de compléments.</span><span class="sxs-lookup"><span data-stu-id="d78a3-121">Using the Add-In Manager.</span></span>
    
- <span data-ttu-id="d78a3-122">À partir d’une autre XLL qui active [xlfUnregister](xlfunregister-form-1.md) avec le nom de cette DLL comme argument unique.</span><span class="sxs-lookup"><span data-stu-id="d78a3-122">From another XLL that calls [xlfUnregister](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="d78a3-123">À partir d’une autre feuille macro XLL qui active [DÉSINCRIRE](xlfunregister-form-1.md) avec le nom de cette DLL comme argument unique.</span><span class="sxs-lookup"><span data-stu-id="d78a3-123">From an XLM macro sheet that calls [UNREGISTER](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
<span data-ttu-id="d78a3-124">Cette fonction effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d78a3-124">This function should do the following:</span></span>
  
- <span data-ttu-id="d78a3-125">Supprimer les menus ou les éléments du menu qui ont été ajoutés via la XLL.</span><span class="sxs-lookup"><span data-stu-id="d78a3-125">Remove any menus or menu items that were added by the XLL.</span></span>
    
- <span data-ttu-id="d78a3-126">Effectuer tout nettoyage général nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d78a3-126">Perform any necessary global cleanup.</span></span>
    
- <span data-ttu-id="d78a3-127">Supprimer les noms qui ont été créés en particulier les noms de fonctions exportées.</span><span class="sxs-lookup"><span data-stu-id="d78a3-127">Delete any names that were created, especially names of exported functions.</span></span> <span data-ttu-id="d78a3-128">N’oubliez pas qu’inscrire les fonctions peut entraîner la création de certains noms, si le quatrième argument de **INSCRIRE** est présent.</span><span class="sxs-lookup"><span data-stu-id="d78a3-128">Remember that registering functions may cause some names to be created, if the fourth argument to **REGISTER** is present.</span></span> 
    
## <a name="example"></a><span data-ttu-id="d78a3-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="d78a3-129">Example</span></span>

<span data-ttu-id="d78a3-130">Reportez-vous aux fichiers `SAMPLES\EXAMPLE\EXAMPLE.C` et `SAMPLES\GENERIC\GENERIC.C` pour des exemples d’implémentation de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="d78a3-130">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="d78a3-131">Le code suivant provient de `SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="d78a3-131">The following code is from  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
```cs
int WINAPI xlAutoClose(void)
{
   int i;
   XLOPER12 xRes;
//
// This block first deletes all names added by xlAutoOpen or
// xlAutoRegister12. Next, it checks if the drop-down menu Generic still
// exists. If it does, it is deleted using xlfDeleteMenu. It then checks
// if the Test toolbar still exists. If it is, xlfDeleteToolbar is
// used to delete it.
//
// The following code to delete the defined names
// does not work in the current version of Excel. 
// You cannot delete these names once they are Registered.
// The code is left here in case the functionality becomes 
// available in a future version.
//
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgWorksheetFuncs[i][2]));
   for (i = 0; i < g_rgCommandFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgCommandFuncs[i][2]));
//
// Everything else works as documented.
//
   Excel12f(xlfGetBar, &amp;xRes, 3, TempInt12(10), TempStr12(L"Generic"), TempInt12(0));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteMenu, 0, 2, TempNum12(10), TempStr12(L"Generic"));
      // Free the XLOPER12 returned by xlfGetBar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   Excel12f(xlfGetToolbar, &amp;xRes, 2, TempInt12(7), TempStr12(L"Test"));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteToolbar, 0, 1, TempStr12(L"Test"));
      // Free the XLOPER12 returned by xlfGetToolbar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="d78a3-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d78a3-132">See also</span></span>



[<span data-ttu-id="d78a3-133">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="d78a3-133">xlAutoOpen</span></span>](xlautoopen.md)


[<span data-ttu-id="d78a3-134">Fonctions du Gestionnaire de compléments et de l’interface XLL</span><span class="sxs-lookup"><span data-stu-id="d78a3-134">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

