---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- fonction debugprintf [excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08bde61573874c137b18856fd24d23b324a35328
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424797"
---
# <a name="debugprintf"></a><span data-ttu-id="6f745-104">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="6f745-104">debugPrintf</span></span>

<span data-ttu-id="6f745-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6f745-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6f745-106">Fonction de bibliothèque d’infrastructure qui écrit une chaîne d’byte terminée par null dans le déboguer actif via la fonction SDK **OutputDebugStringA** Windows.</span><span class="sxs-lookup"><span data-stu-id="6f745-106">Framework library function that writes a null-terminated byte-string to the active debugger via the Windows SDK function **OutputDebugStringA**.</span></span> <span data-ttu-id="6f745-107">Si l’application n’a pas de débompeur, le débogger système affiche la chaîne.</span><span class="sxs-lookup"><span data-stu-id="6f745-107">If the application has no debugger, the system debugger displays the string.</span></span> <span data-ttu-id="6f745-108">Si l’application n’a pas de déboguer et que le déboguer système n’est pas actif, **debugPrintf** ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="6f745-108">If the application has no debugger and the system debugger is not active, **debugPrintf** does nothing.</span></span> 
  
<span data-ttu-id="6f745-109">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6f745-109">This function does not return a value.</span></span>
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a><span data-ttu-id="6f745-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="6f745-110">Parameters</span></span>

 <span data-ttu-id="6f745-111">_lpFormat (LPSTR)_</span><span class="sxs-lookup"><span data-stu-id="6f745-111">_lpFormat (LPSTR)_</span></span>
  
<span data-ttu-id="6f745-112">Chaîne de format, qui suit la syntaxe et les règles de celle utilisée avec la **fonction sprintf.**</span><span class="sxs-lookup"><span data-stu-id="6f745-112">The format string, which follows the syntax and rules for that used with the **sprintf** function.</span></span> 
  
 <span data-ttu-id="6f745-113">_arguments_</span><span class="sxs-lookup"><span data-stu-id="6f745-113">_arguments_</span></span>
  
<span data-ttu-id="6f745-114">Zéro ou plusieurs arguments pour correspondre à la chaîne de format.</span><span class="sxs-lookup"><span data-stu-id="6f745-114">Zero or more arguments to match the format string.</span></span>
  
## <a name="example"></a><span data-ttu-id="6f745-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="6f745-115">Example</span></span>

<span data-ttu-id="6f745-116">Cette fonction imprime une chaîne pour montrer que le contrôle lui a été passé.</span><span class="sxs-lookup"><span data-stu-id="6f745-116">This function prints a string to show that control was passed to it.</span></span> <span data-ttu-id="6f745-117">L_DEBUG de base doit être défini avant la compilation, sinon cette fonction ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="6f745-117">The _DEBUG flag must be defined before compiling or else this function does nothing.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI debugPrintfExample(void)
{
#ifdef _DEBUG
   debugPrintf("Made it!\r");
#endif
   return 1;
}

```

## <a name="see-also"></a><span data-ttu-id="6f745-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f745-118">See also</span></span>



[<span data-ttu-id="6f745-119">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="6f745-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

