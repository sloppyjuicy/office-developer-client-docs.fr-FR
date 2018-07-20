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
ms.openlocfilehash: 3cbe1cd879fb5a91d14b38f8a659a7f77d943fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782223"
---
# <a name="xlautoclose"></a><span data-ttu-id="37f52-104">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="37f52-104">xlAutoClose</span></span>

 <span data-ttu-id="37f52-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="37f52-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="37f52-106">Activée par Microsoft Excel chaque fois que la XLL est désactivée.</span><span class="sxs-lookup"><span data-stu-id="37f52-106">Called by Microsoft Excel whenever the XLL is deactivated.</span></span> <span data-ttu-id="37f52-107">Le complément est désactivé lorsqu’une session Excel se termine normalement.</span><span class="sxs-lookup"><span data-stu-id="37f52-107">The add-in is deactivated when an Excel session ends normally.</span></span> <span data-ttu-id="37f52-108">Le complément peut être désactivé par l’utilisateur pendant une session Excel, et dans ce cas, cette fonction est activée.</span><span class="sxs-lookup"><span data-stu-id="37f52-108">The add-in can be deactivated by the user during an Excel session, and this function will be called in that case.</span></span>
  
<span data-ttu-id="37f52-109">Excel ne requiert pas une XLL pour exécuter et exporter cette fonction, bien que cela soit conseillé afin que votre XLL puisse annuler les fonctions et les commandes, libérer des ressources, annuler des personnalisations et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="37f52-109">Excel does not require an XLL to implement and export this function, although it is advisable so that your XLL can unregister functions and commands, release resources, undo customizations, and so on.</span></span> <span data-ttu-id="37f52-110">Si les fonctions et les commandes ne sont pas explicitement désinscrites par la XLL, Excel l’effectue après avoir activé la**fonction**xlAutoClose.</span><span class="sxs-lookup"><span data-stu-id="37f52-110">If functions and commands are not explicitly unregistered by the XLL, Excel does this after calling the **xlAutoClose** function.</span></span> 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a><span data-ttu-id="37f52-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37f52-111">Parameters</span></span>

<span data-ttu-id="37f52-112">Cette fonction ne prend aucun argument.</span><span class="sxs-lookup"><span data-stu-id="37f52-112">This function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="37f52-113">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="37f52-113">Property value/Return value</span></span>

<span data-ttu-id="37f52-114">Votre exécution de cette fonction doit renvoyer 1 (**ent**).</span><span class="sxs-lookup"><span data-stu-id="37f52-114">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="37f52-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="37f52-115">Remarks</span></span>

<span data-ttu-id="37f52-116">Excel active la fonction **xlAutoClose** chaque fois que la XLL est désactivée, autrement dit, déchargée à partir de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="37f52-116">Excel calls the **xlAutoClose** function whenever the XLL is deactivated, that is, unloaded from memory.</span></span> <span data-ttu-id="37f52-117">La XLL est désactivée dans les situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="37f52-117">The XLL is deactivated in the following situations:</span></span> 
  
- <span data-ttu-id="37f52-118">À la fin d’une session normale Excel si celle-ci est active au cours de cette session.</span><span class="sxs-lookup"><span data-stu-id="37f52-118">At the normal end of an Excel session if active during that session.</span></span>
    
- <span data-ttu-id="37f52-119">Si elle est explicitement déchargée pendant une session Excel.</span><span class="sxs-lookup"><span data-stu-id="37f52-119">If explicitly unloaded during an Excel session.</span></span>
    
- <span data-ttu-id="37f52-120">Une XLL peut être déchargée de différentes manières :</span><span class="sxs-lookup"><span data-stu-id="37f52-120">An XLOPERXLOPER12 can be created in several ways:</span></span>
    
- <span data-ttu-id="37f52-121">Utilisation du Gestionnaire de compléments.</span><span class="sxs-lookup"><span data-stu-id="37f52-121">Using the Add-In Manager</span></span>
    
- <span data-ttu-id="37f52-122">À partir d’une autre XLL qui active [xlfUnregister](xlfunregister-form-1.md) avec le nom de cette DLL comme argument unique.</span><span class="sxs-lookup"><span data-stu-id="37f52-122">From another XLL that calls [xlfUnregister](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="37f52-123">À partir d’une autre feuille macro XLL qui active [DÉSINCRIRE](xlfunregister-form-1.md) avec le nom de cette DLL comme argument unique.</span><span class="sxs-lookup"><span data-stu-id="37f52-123">From an XLM macro sheet that calls [UNREGISTER](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
<span data-ttu-id="37f52-124">Cette fonction effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="37f52-124">This function should do the following:</span></span>
  
- <span data-ttu-id="37f52-125">Supprimer les menus ou les éléments du menu qui ont été ajoutés via la XLL.</span><span class="sxs-lookup"><span data-stu-id="37f52-125">Remove any menus or menu items that were added by the XLL.</span></span>
    
- <span data-ttu-id="37f52-126">Effectuer tout nettoyage général nécessaire.</span><span class="sxs-lookup"><span data-stu-id="37f52-126">Perform any necessary global cleanup.</span></span>
    
- <span data-ttu-id="37f52-127">Supprimer les noms qui ont été créés en particulier les noms de fonctions exportées.</span><span class="sxs-lookup"><span data-stu-id="37f52-127">Delete any names that were created, especially names of exported functions.</span></span> <span data-ttu-id="37f52-128">N’oubliez pas qu’inscrire les fonctions peut entraîner la création de certains noms, si le quatrième argument de **INSCRIRE** est présent.</span><span class="sxs-lookup"><span data-stu-id="37f52-128">Remember that registering functions may cause some names to be created, if the fourth argument to **REGISTER** is present.</span></span> 
    
## <a name="example"></a><span data-ttu-id="37f52-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="37f52-129">Example</span></span>

<span data-ttu-id="37f52-130">Afficher les fichiers `SAMPLES\EXAMPLE\EXAMPLE.C` et `SAMPLES\GENERIC\GENERIC.C` par exemple les exécutions de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="37f52-130">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="37f52-131">Ajouter le code suivant à partir de `SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="37f52-131">The following code is from  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="37f52-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37f52-132">See also</span></span>



[<span data-ttu-id="37f52-133">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="37f52-133">xlAutoOpen</span></span>](xlautoopen.md)


[<span data-ttu-id="37f52-134">Gestionnaire de compléments et fonctions d’interface XLL</span><span class="sxs-lookup"><span data-stu-id="37f52-134">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

