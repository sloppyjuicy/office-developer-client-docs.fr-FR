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
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 25669cfc705e797b80be0fab590d809e8f1e3b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782015"
---
# <a name="debugprintf"></a><span data-ttu-id="44a3b-104">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="44a3b-104">debugPrintf</span></span>

<span data-ttu-id="44a3b-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="44a3b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="44a3b-106">Fonction de bibliothèque Framework écrit une chaîne octet se terminant par null dans le débogueur actif via la fonction Windows SDK **OutputDebugStringA**.</span><span class="sxs-lookup"><span data-stu-id="44a3b-106">Framework library function that writes a null-terminated byte-string to the active debugger via the Windows SDK function **OutputDebugStringA**.</span></span> <span data-ttu-id="44a3b-107">Si l’application ne possède aucun débogueur, le débogueur système affiche la chaîne.</span><span class="sxs-lookup"><span data-stu-id="44a3b-107">If the application has no debugger, the system debugger displays the string.</span></span> <span data-ttu-id="44a3b-108">Si l’application ne possède aucun débogueur et le débogueur système n’est pas actif, **debugPrintf** est sans effet.</span><span class="sxs-lookup"><span data-stu-id="44a3b-108">If the application has no debugger and the system debugger is not active, **debugPrintf** does nothing.</span></span> 
  
<span data-ttu-id="44a3b-109">Cette fonction ne retourne pas une valeur.</span><span class="sxs-lookup"><span data-stu-id="44a3b-109">This function does not return a value.</span></span>
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a><span data-ttu-id="44a3b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44a3b-110">Parameters</span></span>

 <span data-ttu-id="44a3b-111">_lpFormat (LPSTR)_</span><span class="sxs-lookup"><span data-stu-id="44a3b-111">_lpFormat (LPSTR)_</span></span>
  
<span data-ttu-id="44a3b-112">La chaîne de format qui suit la syntaxe et les règles qui est utilisée avec la fonction **sprintf** .</span><span class="sxs-lookup"><span data-stu-id="44a3b-112">The format string, which follows the syntax and rules for that used with the **sprintf** function.</span></span> 
  
 <span data-ttu-id="44a3b-113">_arguments_</span><span class="sxs-lookup"><span data-stu-id="44a3b-113">_arguments_</span></span>
  
<span data-ttu-id="44a3b-114">Zéro ou plusieurs arguments pour la correspondance de la chaîne de format.</span><span class="sxs-lookup"><span data-stu-id="44a3b-114">Zero or more arguments to match the format string.</span></span>
  
## <a name="example"></a><span data-ttu-id="44a3b-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="44a3b-115">Example</span></span>

<span data-ttu-id="44a3b-116">Cette fonction imprime une chaîne pour indiquer que le contrôle a été passé à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="44a3b-116">This function prints a string to show that control was passed to it.</span></span> <span data-ttu-id="44a3b-117">L’indicateur _DEBUG doit être définie avant la compilation, sinon cette fonction n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="44a3b-117">The _DEBUG flag must be defined before compiling or else this function does nothing.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="44a3b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44a3b-118">See also</span></span>



[<span data-ttu-id="44a3b-119">Fonctions de la bibliothèque Framework</span><span class="sxs-lookup"><span data-stu-id="44a3b-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

