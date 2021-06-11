---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- fonction xlautoregister [excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f043558f3f642001e9ba11ee5b18a2721c3dddfb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421164"
---
# <a name="xlautoregisterxlautoregister12"></a><span data-ttu-id="9f660-104">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="9f660-104">xlAutoRegister/xlAutoRegister12</span></span>

 <span data-ttu-id="9f660-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9f660-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9f660-106">Excel appelle la fonction [xlAutoRegister](xlautoregister-xlautoregister12.md) chaque fois qu’un appel a été effectué à la fonction XLM **REGISTER** ou à la fonction [xlfRegister](xlfregister-form-1.md)équivalente à l’API C, les types de retour et d’argument de la fonction étant manquants.</span><span class="sxs-lookup"><span data-stu-id="9f660-106">Excel calls the [xlAutoRegister function](xlautoregister-xlautoregister12.md) whenever a call has been made to the XLM function **REGISTER**, or the C API equivalent [xlfRegister function](xlfregister-form-1.md), with the return and argument types of the function being registered missing.</span></span> <span data-ttu-id="9f660-107">Il permet au XLL de rechercher ses listes internes de fonctions et de commandes exportées pour enregistrer la fonction avec l’argument et les types de retour spécifiés.</span><span class="sxs-lookup"><span data-stu-id="9f660-107">It allows the XLL to search its internal lists of exported functions and commands to register the function with the argument and return types specified.</span></span>
  
<span data-ttu-id="9f660-108">À partir Excel 2007, Excel appelle la fonction **xlAutoRegister12** de préférence à la fonction **xlAutoRegister** si elle est exportée par le XLL.</span><span class="sxs-lookup"><span data-stu-id="9f660-108">Starting in Excel 2007, Excel calls the **xlAutoRegister12** function in preference to the **xlAutoRegister** function if it is exported by the XLL.</span></span> 
  
<span data-ttu-id="9f660-109">Excel ne nécessite pas de XLL pour implémenter et exporter l’une de ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="9f660-109">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9f660-110">Si **xlAutoRegister** /  **xlAutoRegister12** tente d’inscrire la fonction sans fournir les types d’argument et de retour, une boucle d’appel récursive se produit, ce qui finit par déborder la pile d’appels et se Excel.</span><span class="sxs-lookup"><span data-stu-id="9f660-110">If **xlAutoRegister**/ **xlAutoRegister12** tries to register the function without supplying the argument and return types, a recursive calling loop occurs which eventually overflows the call stack and crashes Excel.</span></span> 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a><span data-ttu-id="9f660-111">Parameters</span><span class="sxs-lookup"><span data-stu-id="9f660-111">Parameters</span></span>

 <span data-ttu-id="9f660-112">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="9f660-112">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="9f660-113">Nom de la fonction XLL en cours d’inscription.</span><span class="sxs-lookup"><span data-stu-id="9f660-113">The name of the XLL function that is being registered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="9f660-114">Valeur de propriété/valeur de renvoi</span><span class="sxs-lookup"><span data-stu-id="9f660-114">Property value/Return value</span></span>

<span data-ttu-id="9f660-115">La fonction doit renvoyer le résultat de la tentative d’inscription de la fonction _XLL pxName_ à l’aide de la **fonction xlfRegister.**</span><span class="sxs-lookup"><span data-stu-id="9f660-115">The function should return the result of the attempt to register the XLL function  _pxName_ using the **xlfRegister** function.</span></span> <span data-ttu-id="9f660-116">Si la fonction spécifiée n’est pas l’une des exportations du XLL, elle doit renvoyer le **#VALUE!**</span><span class="sxs-lookup"><span data-stu-id="9f660-116">If the specified function is not one of the XLL's exports, it should return the **#VALUE!**</span></span> <span data-ttu-id="9f660-117">error, or **NULL** which Excel will interpret at **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="9f660-117">error, or **NULL** which Excel will interpret at **#VALUE!**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9f660-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="9f660-118">Remarks</span></span>

<span data-ttu-id="9f660-119">Votre implémentation de **xlAutoRegister** doit effectuer une recherche sans prendre en compte la cas dans les listes internes de votre XLL des fonctions et commandes qu’il exporte à la recherche d’une correspondance avec le nom transmis.</span><span class="sxs-lookup"><span data-stu-id="9f660-119">Your implementation of **xlAutoRegister** should perform a case-insensitive search through your XLL's internal lists of the functions and commands it exports looking for a match with the passed-in name.</span></span> <span data-ttu-id="9f660-120">Si la fonction ou la commande est trouvée, **xlAutoRegister** doit tenter de l’enregistrer à l’aide de la fonction **xlfRegister,** en vous assurez de fournir la chaîne qui indique à Excel les types de retour et d’argument de la fonction, ainsi que toute autre information requise sur la fonction.</span><span class="sxs-lookup"><span data-stu-id="9f660-120">If the function or command is found, **xlAutoRegister** should attempt to register it, using the **xlfRegister** function, making sure to provide the string that tells Excel the return and argument types of the function, as well as any other required information about the function.</span></span> <span data-ttu-id="9f660-121">Il doit ensuite revenir à Excel quel que soit l’appel **à xlfRegister** renvoyé.</span><span class="sxs-lookup"><span data-stu-id="9f660-121">It should then return to Excel whatever the call to **xlfRegister** returned.</span></span> <span data-ttu-id="9f660-122">Si la fonction a été enregistrée avec succès, **xlfRegister** renvoie une valeur **xltypeNum** contenant l’ID d’inscription de la fonction.</span><span class="sxs-lookup"><span data-stu-id="9f660-122">If the function was registered successfully, **xlfRegister** returns an **xltypeNum** value containing the Register ID of the function.</span></span> 
  
### <a name="example"></a><span data-ttu-id="9f660-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="9f660-123">Example</span></span>

<span data-ttu-id="9f660-124">Consultez le fichier  `SAMPLES\EXAMPLE\EXAMPLE.C` pour obtenir un exemple d’implémentation de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="9f660-124">See the file  `SAMPLES\EXAMPLE\EXAMPLE.C` for an example implementation of this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9f660-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f660-125">See also</span></span>



[<span data-ttu-id="9f660-126">REGISTER</span><span class="sxs-lookup"><span data-stu-id="9f660-126">REGISTER</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="9f660-127">UNREGISTER</span><span class="sxs-lookup"><span data-stu-id="9f660-127">UNREGISTER</span></span>](xlfunregister-form-1.md)

