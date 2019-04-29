---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- fonction xlAutoAdd [Excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9a38d5dafd30fda87dda5eadf8fa97ab6e6768a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413758"
---
# <a name="xlautoadd"></a><span data-ttu-id="1cfdd-104">xlAutoAdd</span><span class="sxs-lookup"><span data-stu-id="1cfdd-104">xlAutoAdd</span></span>

 <span data-ttu-id="1cfdd-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1cfdd-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1cfdd-106">Ajouté par Microsoft Excel chaque fois que l'utilisateur active le XLL au cours d'une session Excel à l'aide du gestionnaire de compléments.</span><span class="sxs-lookup"><span data-stu-id="1cfdd-106">Added by Microsoft Excel whenever the user activates the XLL during an Excel session by using the Add-In Manager.</span></span> <span data-ttu-id="1cfdd-107">Cette fonction n'est pas appelée lorsqu'Excel démarre et charge un complément préinstallé.</span><span class="sxs-lookup"><span data-stu-id="1cfdd-107">This function is not called when Excel starts up and loads a pre-installed add-in.</span></span>
  
<span data-ttu-id="1cfdd-108">Cette fonction peut être utilisée pour afficher une boîte de dialogue personnalisée qui indique à l'utilisateur que le complément a été activé, ou pour lire ou écrire dans le registre, ou pour vérifier les informations de licence, par exemple.</span><span class="sxs-lookup"><span data-stu-id="1cfdd-108">This function can be used to display a custom dialog box that tells the user that the add-in has been activated, or to read from or write to the registry, or check licensing information, for example.</span></span>
  
<span data-ttu-id="1cfdd-109">Excel ne requiert pas de XLL pour implémenter et exporter cette fonction.</span><span class="sxs-lookup"><span data-stu-id="1cfdd-109">Excel does not require an XLL to implement and export this function.</span></span>
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a><span data-ttu-id="1cfdd-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cfdd-110">Parameters</span></span>

<span data-ttu-id="1cfdd-111">Cette fonction ne prend aucun argument.</span><span class="sxs-lookup"><span data-stu-id="1cfdd-111">This function takes no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="1cfdd-112">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="1cfdd-112">Property value/Return value</span></span>

<span data-ttu-id="1cfdd-113">Votre implémentation de cette fonction doit renvoyer 1.</span><span class="sxs-lookup"><span data-stu-id="1cfdd-113">Your implementation of this function should return 1.</span></span> <span data-ttu-id="1cfdd-114">(**int**).</span><span class="sxs-lookup"><span data-stu-id="1cfdd-114">(**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1cfdd-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="1cfdd-115">Remarks</span></span>

<span data-ttu-id="1cfdd-116">Utilisez cette fonction si votre XLL doit effectuer une opération lorsqu'elle est ajoutée par le gestionnaire de compléments.</span><span class="sxs-lookup"><span data-stu-id="1cfdd-116">Use this function if there is anything your XLL needs to do when it is added by the Add-In Manager.</span></span>
  
## <a name="example"></a><span data-ttu-id="1cfdd-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="1cfdd-117">Example</span></span>

<span data-ttu-id="1cfdd-118">Voir `\SAMPLES\EXAMPLE\EXAMPLE.C` et `\SAMPLES\GENERIC\GENERIC.C` , par exemple, les implémentations de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="1cfdd-118">See  `\SAMPLES\EXAMPLE\EXAMPLE.C` and  `\SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="1cfdd-119">Le code suivant provient de `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="1cfdd-119">The following code is from  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span>
  
```cs
int WINAPI xlAutoAdd(void)
{
    XCHAR szBuf[255];
    wsprintfW((LPWSTR)szBuf, L"Thank you for adding Example.XLL\n"
            L"build date %hs, time %hs",__DATE__, __TIME__);
/* Display a dialog indicating that the XLL was successfully added */
    Excel12f(xlcAlert, 0, 2, TempStr12(szBuf), TempInt12(2));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="1cfdd-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cfdd-120">See also</span></span>



[<span data-ttu-id="1cfdd-121">xlAutoRemove</span><span class="sxs-lookup"><span data-stu-id="1cfdd-121">xlAutoRemove</span></span>](xlautoremove.md)


[<span data-ttu-id="1cfdd-122">Fonctions du Gestionnaire de compléments et de l’interface XLL</span><span class="sxs-lookup"><span data-stu-id="1cfdd-122">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

