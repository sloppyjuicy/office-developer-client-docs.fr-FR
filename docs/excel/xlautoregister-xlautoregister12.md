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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e6430a54b0c0ed3b6e08d3c9256cae7dcde926ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19782207"
---
# <a name="xlautoregisterxlautoregister12"></a><span data-ttu-id="3e015-104">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="3e015-104">xlAutoRegister/xlAutoRegister12</span></span>

 <span data-ttu-id="3e015-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3e015-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3e015-106">Excel appelle la [fonction xlAutoRegister](xlautoregister-xlautoregister12.md) chaque fois qu’un appel a été effectué pour la fonction XLM **inscrire**ou l' équivalent API C [fonction xlfRegister](xlfregister-form-1.md), avec les types de retour et l’argument de la fonction en cours d’enregistrement manquant.</span><span class="sxs-lookup"><span data-stu-id="3e015-106">Excel calls the [xlAutoRegister function](xlautoregister-xlautoregister12.md) whenever a call has been made to the XLM function **REGISTER**, or the C API equivalent [xlfRegister function](xlfregister-form-1.md), with the return and argument types of the function being registered missing.</span></span> <span data-ttu-id="3e015-107">Il permet la ressource XLL à rechercher ses listes internes de fonctions exportées et commandes pour enregistrer la fonction avec l’argument et retournent des types spécifiés.</span><span class="sxs-lookup"><span data-stu-id="3e015-107">It allows the XLL to search its internal lists of exported functions and commands to register the function with the argument and return types specified.</span></span>
  
<span data-ttu-id="3e015-108">À compter d’Excel 2007, Excel appelle la fonction **xlAutoRegister12** plutôt que la fonction **xlAutoRegister** , si elle est exportée par la ressource XLL.</span><span class="sxs-lookup"><span data-stu-id="3e015-108">Starting in Excel 2007, Excel calls the **xlAutoRegister12** function in preference to the **xlAutoRegister** function if it is exported by the XLL.</span></span> 
  
<span data-ttu-id="3e015-109">Excel ne nécessite pas un ressource XLL à mettre en œuvre et exporter une de ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="3e015-109">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3e015-110">Si **xlAutoRegister**/ **xlAutoRegister12** tente d’inscrire la fonction sans fournir l’argument et types de retour, cet événement produit une boucle appelant récursive finalement de dépassement de la pile des appels et se bloque Excel.</span><span class="sxs-lookup"><span data-stu-id="3e015-110">If **xlAutoRegister**/ **xlAutoRegister12** tries to register the function without supplying the argument and return types, a recursive calling loop occurs which eventually overflows the call stack and crashes Excel.</span></span> 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a><span data-ttu-id="3e015-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e015-111">Parameters</span></span>

 <span data-ttu-id="3e015-112">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="3e015-112">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="3e015-113">Le nom de la fonction XLL qui est enregistré.</span><span class="sxs-lookup"><span data-stu-id="3e015-113">The name of the XLL function that is being registered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="3e015-114">Propriété valeur/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3e015-114">Property value/Return value</span></span>

<span data-ttu-id="3e015-115">La fonction doit renvoyer le résultat de la tentative d’inscrire le de fonction XLL _pxName_ à l’aide de la fonction **xlfRegister** .</span><span class="sxs-lookup"><span data-stu-id="3e015-115">The function should return the result of the attempt to register the XLL function  _pxName_ using the **xlfRegister** function.</span></span> <span data-ttu-id="3e015-116">Si la fonction spécifiée ne fait pas partie des exportations du XLL, elle doit retourner la **#VALUE !**</span><span class="sxs-lookup"><span data-stu-id="3e015-116">If the specified function is not one of the XLL's exports, it should return the **#VALUE!**</span></span> <span data-ttu-id="3e015-117">erreur ou **NULL** qui Excel interprète à **#VALUE !**.</span><span class="sxs-lookup"><span data-stu-id="3e015-117">error, or **NULL** which Excel will interpret at **#VALUE!**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3e015-118">Note</span><span class="sxs-lookup"><span data-stu-id="3e015-118">Remarks</span></span>

<span data-ttu-id="3e015-119">Votre implémentation de **xlAutoRegister** doit effectuer une recherche par le biais de listes internes de votre XLL des fonctions et des commandes qu'exporte vous recherchez une correspondance avec le nom passé pas la casse.</span><span class="sxs-lookup"><span data-stu-id="3e015-119">Your implementation of **xlAutoRegister** should perform a case-insensitive search through your XLL's internal lists of the functions and commands it exports looking for a match with the passed-in name.</span></span> <span data-ttu-id="3e015-120">Si la fonction ou la commande est trouvée, **xlAutoRegister** doit essayer de l’enregistrer à l’aide de la fonction **xlfRegister** , en veillant à fournir la chaîne qui indique les types de retour et l’argument de la fonction, ainsi que les autres requis à Excel informations sur la fonction.</span><span class="sxs-lookup"><span data-stu-id="3e015-120">If the function or command is found, **xlAutoRegister** should attempt to register it, using the **xlfRegister** function, making sure to provide the string that tells Excel the return and argument types of the function, as well as any other required information about the function.</span></span> <span data-ttu-id="3e015-121">Il doit ensuite retourner vers Excel quelle que soit l’appel de **xlfRegister** renvoyé.</span><span class="sxs-lookup"><span data-stu-id="3e015-121">It should then return to Excel whatever the call to **xlfRegister** returned.</span></span> <span data-ttu-id="3e015-122">Si la fonction a été enregistrée avec succès, **xlfRegister** renvoie une valeur de **xltypeNum** contenant l’ID de la fonction Enregistrer.</span><span class="sxs-lookup"><span data-stu-id="3e015-122">If the function was registered successfully, **xlfRegister** returns an **xltypeNum** value containing the Register ID of the function.</span></span> 
  
### <a name="example"></a><span data-ttu-id="3e015-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="3e015-123">Example</span></span>

<span data-ttu-id="3e015-124">Consultez le fichier `SAMPLES\EXAMPLE\EXAMPLE.C` pour un exemple d’implémentation de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="3e015-124">See the file  `SAMPLES\EXAMPLE\EXAMPLE.C` for an example implementation of this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3e015-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e015-125">See also</span></span>



[<span data-ttu-id="3e015-126">INSCRIRE</span><span class="sxs-lookup"><span data-stu-id="3e015-126">REGISTER</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="3e015-127">ANNULER L’INSCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3e015-127">UNREGISTER</span></span>](xlfunregister-form-1.md)

