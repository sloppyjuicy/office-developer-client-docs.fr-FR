---
title: Développement de DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- DLL [Excel 2007], création, création de DLL [Excel 2007]
ms.assetid: 5d69d06d-a126-4c47-82ad-17112674c8a3
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 89dd7b65ad94ba2fc7e1cf3f99ee163d3003d0fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310919"
---
# <a name="developing-dlls"></a><span data-ttu-id="04b57-104">Développement de DLL</span><span class="sxs-lookup"><span data-stu-id="04b57-104">Developing DLLs</span></span>

<span data-ttu-id="04b57-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="04b57-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="04b57-106">Une bibliothèque est une collection de code compilé qui fournit des fonctionnalités et des données à une application exécutable.</span><span class="sxs-lookup"><span data-stu-id="04b57-106">A library is a body of compiled code that provides some functionality and data to an executable application.</span></span> <span data-ttu-id="04b57-107">Les bibliothèques peuvent être liées statiquement ou dynamiquement et ont conventionnellement les extensions de nom de fichier .lib et .dll, respectivement.</span><span class="sxs-lookup"><span data-stu-id="04b57-107">Libraries can be either statically linked or dynamically linked, and they conventionally have the file name extensions .lib and .dll respectively.</span></span> <span data-ttu-id="04b57-108">Les bibliothèques statiques (par exemple, la bibliothèque en C) sont liées à l’application lors de la compilation et font donc partie intégrante de l’exécutable qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="04b57-108">Static libraries (such as the C run-time library) are linked to the application at compilation and so become part of the resulting executable.</span></span> <span data-ttu-id="04b57-109">L’application charge une DLL lorsque nécessaire, généralement au démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="04b57-109">The application loads a DLL when it is needed, usually when the application starts up.</span></span> <span data-ttu-id="04b57-110">Une DLL peut charger et établir un lien dynamiquement vers une autre DLL.</span><span class="sxs-lookup"><span data-stu-id="04b57-110">One DLL can load and dynamically link to another DLL.</span></span>
  
## <a name="benefits-of-using-dlls"></a><span data-ttu-id="04b57-111">Avantages de l'utilisation des DLL</span><span class="sxs-lookup"><span data-stu-id="04b57-111">Benefits of using DLLs</span></span>

<span data-ttu-id="04b57-112">Les principaux avantages des DLL sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="04b57-112">The main benefits of DLLs are as follows:</span></span>
  
- <span data-ttu-id="04b57-113">Toutes les applications peuvent partager une copie unique sur disque.</span><span class="sxs-lookup"><span data-stu-id="04b57-113">All applications can share a single copy on disk.</span></span>
    
- <span data-ttu-id="04b57-114">Les fichiers exécutables des applications sont plus petits.</span><span class="sxs-lookup"><span data-stu-id="04b57-114">Applications' executable files are kept smaller.</span></span>
    
- <span data-ttu-id="04b57-115">Ils permettent de diviser les projets de développement volumineux.</span><span class="sxs-lookup"><span data-stu-id="04b57-115">They enable large development projects to be broken down.</span></span> <span data-ttu-id="04b57-116">Les développeurs d’application et de DLL doivent uniquement se mettre chacun d’accord sur une interface.</span><span class="sxs-lookup"><span data-stu-id="04b57-116">Application and DLL developers only need agree an interface between their respective parts.</span></span> <span data-ttu-id="04b57-117">Cette interface est exportée par la DLL.</span><span class="sxs-lookup"><span data-stu-id="04b57-117">This interface is exported by the DLL.</span></span>
    
- <span data-ttu-id="04b57-118">Les développeurs de DLL peuvent mettre à jour les DLL (pour augmenter leur efficacité ou corriger un bogue, par exemple) sans avoir à mettre à jour toutes les applications qui l’utilisent, tant que l’interface exportée de la DLL ne change pas.</span><span class="sxs-lookup"><span data-stu-id="04b57-118">DLL developers can update DLLs—perhaps to make them more efficient or to fix a bug—without having to update all the applications that use it, provided that the exported interface of the DLL does not change.</span></span>
    
<span data-ttu-id="04b57-119">Vous pouvez utiliser les DLL pour ajouter des commandes et les fonctions de feuille de calcul dans Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="04b57-119">You can use DLLs to add worksheet functions and commands in Microsoft Excel.</span></span>
  
## <a name="resources-for-creating-dlls"></a><span data-ttu-id="04b57-120">Ressources pour la création de DLL</span><span class="sxs-lookup"><span data-stu-id="04b57-120">Resources for creating DLLs</span></span>

<span data-ttu-id="04b57-121">Pour créer une DLL, vous devez disposer des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="04b57-121">To create a DLL, you need the following:</span></span>
  
- <span data-ttu-id="04b57-122">un éditeur de code source ;</span><span class="sxs-lookup"><span data-stu-id="04b57-122">A source code editor.</span></span>
    
- <span data-ttu-id="04b57-123">un compilateur pour transformer le code source en code objet compatible avec votre matériel ;</span><span class="sxs-lookup"><span data-stu-id="04b57-123">A compiler to turn source code into object code that is compatible with your hardware.</span></span>
    
- <span data-ttu-id="04b57-124">un éditeur de liens pour ajouter du code à partir de bibliothèques statiques, le cas échéant, et pour créer le fichier DLL exécutable.</span><span class="sxs-lookup"><span data-stu-id="04b57-124">A linker to add code from static libraries, where used, and to create the executable DLL file.</span></span>
    
<span data-ttu-id="04b57-125">Les environnements de développement intégré moderne (IDE), tels que Microsoft Visual Studio, fournissent tous ces éléments.</span><span class="sxs-lookup"><span data-stu-id="04b57-125">Modern integrated development environments (IDEs), such as Microsoft Visual Studio, provide all of these things.</span></span> <span data-ttu-id="04b57-126">Ils fournissent également d’autres éléments : éditeurs intelligents, outils pour déboguer votre code, outils pour gérer plusieurs projets, nouveaux assistants de projet et de nombreux autres outils importants.</span><span class="sxs-lookup"><span data-stu-id="04b57-126">They also provide a great deal more: smart editors, tools to debug your code, tools to manage multiple projects, new project wizards, and many other important tools.</span></span>
  
<span data-ttu-id="04b57-127">Vous pouvez créer des DLL en plusieurs langages : C/C++, Pascal et Visual Basic, par exemple.</span><span class="sxs-lookup"><span data-stu-id="04b57-127">You can create DLLs in several languages, for example, C/C++, Pascal and Visual Basic.</span></span> <span data-ttu-id="04b57-128">Étant donné que le code source API fourni avec Excel est C et C++, ces deux langages sont pris en compte dans cette documentation.</span><span class="sxs-lookup"><span data-stu-id="04b57-128">Given that the API source code provided with Excel is C and C++, only these two languages are considered in this documentation.</span></span>
  
## <a name="exporting-functions-and-commands"></a><span data-ttu-id="04b57-129">Exportation de fonctions et de commandes</span><span class="sxs-lookup"><span data-stu-id="04b57-129">Exporting functions and commands</span></span>

<span data-ttu-id="04b57-130">Lors de la compilation d’un projet DLL, le compilateur et l’éditeur de liens doivent savoir quelles fonctions doivent être exportées afin qu’elles soient disponibles pour l’application.</span><span class="sxs-lookup"><span data-stu-id="04b57-130">When compiling a DLL project, the compiler and linker need to know what functions are to be exported so that they can make them available to the application.</span></span> <span data-ttu-id="04b57-131">Cette section décrit la façon de le faire.</span><span class="sxs-lookup"><span data-stu-id="04b57-131">This section describes the ways this can be done.</span></span>
  
<span data-ttu-id="04b57-132">Lorsque les compilateurs compilent le code source, en général, ils modifient les noms des fonctions à partir de leur apparence dans le code source.</span><span class="sxs-lookup"><span data-stu-id="04b57-132">When compilers compile source code, in general, they change the names of the functions from their appearance in the source code.</span></span> <span data-ttu-id="04b57-133">Pour ce faire, ils effectuent un ajout généralement à la fin et/ou au début du nom, lors d’un processus appelé décoration de nom.</span><span class="sxs-lookup"><span data-stu-id="04b57-133">They usually do this by adding to the beginning and/or end of the name, in a process known as name decoration.</span></span> <span data-ttu-id="04b57-134">Vous devez vérifier que la fonction est exportée avec un nom reconnaissable pour l’application qui charge la DLL.</span><span class="sxs-lookup"><span data-stu-id="04b57-134">You need to make sure that the function is exported with a name that is recognizable to the application loading the DLL.</span></span> <span data-ttu-id="04b57-135">Ainsi, il est possible d’indiquer à l’éditeur de liens d’associer le nom décoré à un nom d’exportation plus simple.</span><span class="sxs-lookup"><span data-stu-id="04b57-135">This can mean telling the linker to associate the decorated name with a simpler export name.</span></span> <span data-ttu-id="04b57-136">Le nom d’exportation peut être le nom tel qu’il apparaissait à l’origine dans le code source, ou quelque chose d’autre.</span><span class="sxs-lookup"><span data-stu-id="04b57-136">The export name can be the name as it originally appeared in the source code, or something else.</span></span>
  
<span data-ttu-id="04b57-137">La façon dont le nom est décoré dépend du langage et de la façon dont le compilateur doit rendre la fonction disponible, autrement dit, la convention d’appel.</span><span class="sxs-lookup"><span data-stu-id="04b57-137">The way the name is decorated depends on the language and how the compiler is instructed to make the function available, that is, the calling convention.</span></span> <span data-ttu-id="04b57-138">La convention d’appel standard entre les processus pour Windows utilisée par les DLL est appelée la convention WinAPI.</span><span class="sxs-lookup"><span data-stu-id="04b57-138">The standard inter-process calling convention for Windows used by DLLs is known as the WinAPI convention.</span></span> <span data-ttu-id="04b57-139">Elle est définie dans les fichiers d’en-tête Windows sous la forme **WINAPI**, définie à son tour en utilisant le déclarateur Win32 **__stdcall**.</span><span class="sxs-lookup"><span data-stu-id="04b57-139">It is defined in Windows header files as **WINAPI**, which is in turn defined using the Win32 declarator **__stdcall**.</span></span>
  
<span data-ttu-id="04b57-140">Une fonction d’exportation DLL à utiliser avec Excel (fonction de feuille de calcul, fonction équivalente à une feuille macro ou commande définie par l’utilisateur) doit toujours utiliser la convention d’appel **WINAPI** / **__stdcall**.</span><span class="sxs-lookup"><span data-stu-id="04b57-140">A DLL-export function for use with Excel (whether it is a worksheet function, macro-sheet equivalent function, or user-defined command) should always use the **WINAPI** / **__stdcall** calling convention.</span></span> <span data-ttu-id="04b57-141">Il faut inclure le spécificateur **WINAPI** explicitement dans la définition de la fonction car, par défaut, dans les compilateurs Win32, la convention d’appel **__cdecl** (également définie comme **WINAPIV**) est utilisée, si aucune n’est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="04b57-141">It is necessary to include the **WINAPI** specifier explicitly in the function's definition as the default in Win32 compilers is to use the **__cdecl** calling convention, also defined as **WINAPIV**, if none is specified.</span></span>
  
<span data-ttu-id="04b57-142">Vous pouvez indiquer à l’éditeur de liens qu’une fonction doit être exportée et son nom doit être connu de manière externe de plusieurs manières :</span><span class="sxs-lookup"><span data-stu-id="04b57-142">You can tell the linker that a function is to be exported, and the name it is to be known by externally in one of several ways:</span></span>
  
- <span data-ttu-id="04b57-143">Placez la fonction dans un fichier DEF après le mot clé **EXPORTS** et définissez votre paramètre de projet DLL pour référencer ce fichier lors de la liaison.</span><span class="sxs-lookup"><span data-stu-id="04b57-143">Place the function in a DEF file after the **EXPORTS** keyword, and set your DLL project setting to reference this file when linking.</span></span> 
    
- <span data-ttu-id="04b57-144">Utilisez le déclarateur **__declspec (dllexport)** dans la définition de la fonction.</span><span class="sxs-lookup"><span data-stu-id="04b57-144">Use the **__declspec(dllexport)** declarator in the function's definition.</span></span> 
    
- <span data-ttu-id="04b57-145">Utilisez une directive de préprocesseur **#pragma** pour envoyer un message à l’éditeur de liens.</span><span class="sxs-lookup"><span data-stu-id="04b57-145">Use a **#pragma** preprocessor directive to send a message to the linker.</span></span> 
    
<span data-ttu-id="04b57-146">Même si votre projet peut utiliser les trois méthodes, qui sont prises en charge par votre compilateur et l’éditeur de liens, mais vous ne devez pas essayer d’exporter une fonction de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="04b57-146">Although your project can use all three methods and your compiler and linker support them, you should not try to export one function in more than one of these ways.</span></span> <span data-ttu-id="04b57-147">Par exemple, supposons qu’une DLL contient deux modules de code source (un C et un C++) qui contiennent deux fonctions à exporter, **my\_C\_export** et **my\_Cpp\_export**, respectivement.</span><span class="sxs-lookup"><span data-stu-id="04b57-147">For example, suppose that a DLL contains two source code modules, one C and one C++, which contain two functions to be exported, **my\_C\_export** and **my\_Cpp\_export** respectively.</span></span> <span data-ttu-id="04b57-148">Pour simplifier, supposons que chaque fonction prend un argument numérique double précision unique et renvoie le même type de données.</span><span class="sxs-lookup"><span data-stu-id="04b57-148">For simplicity, suppose that each function takes a single double-precision numerical argument and returns the same data type.</span></span> <span data-ttu-id="04b57-149">Les autres façons d’exporter chaque fonction à l’aide de chacune de ces méthodes sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="04b57-149">The alternatives for exporting each function by using each of these methods are outlined in the following sections.</span></span> 
  
### <a name="using-a-def-file"></a><span data-ttu-id="04b57-150">Utilisation d’un fichier DEF</span><span class="sxs-lookup"><span data-stu-id="04b57-150">Using a DEF file</span></span>

```C
double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

```cpp
double WINAPI my_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

<br/>

<span data-ttu-id="04b57-151">Le fichier DEF doit alors contenir ces lignes :</span><span class="sxs-lookup"><span data-stu-id="04b57-151">The DEF file would then need to contain these lines.</span></span>
  
`EXPORTS my_C_export = _my_C_export@8  my_Cpp_export`

<br/>

<span data-ttu-id="04b57-152">La syntaxe générale d’une ligne qui suit une instruction **EXPORTS** est :</span><span class="sxs-lookup"><span data-stu-id="04b57-152">The general syntax of a line that follows an **EXPORTS** statement is as follows.</span></span> 
  
`entryname[=internalname] [@ordinal[NONAME]] [DATA] [PRIVATE]`

<span data-ttu-id="04b57-153">Notez que la fonction C a été décorée, mais le fichier DEF force explicitement l’éditeur de liens à exposer la fonction en utilisant le nom de code source d’origine (dans cet exemple).</span><span class="sxs-lookup"><span data-stu-id="04b57-153">Note that the C function has been decorated, but the DEF file explicitly forces the linker to expose the function using the original source code name (in this example).</span></span> <span data-ttu-id="04b57-154">L’éditeur de liens exporte implicitement la fonction C++ en utilisant le nom de code d’origine, pour éviter d’inclure le nom décoré dans le fichier DEF.</span><span class="sxs-lookup"><span data-stu-id="04b57-154">The linker implicitly exports the C++ function using the original code name, so that it is not necessary to include the decorated name in the DEF file.</span></span>
  
<span data-ttu-id="04b57-155">Pour les appels de fonction API Windows 32 bits, la convention pour la décoration des fonctions compilées en C est la suivante : **function_name** devient _ **function_name@** _n_ où _n_ correspond au nombre d’octets exprimé sous la forme d’un nombre décimal pris par tous les arguments, avec les octets pour chacun arrondi au multiple de quatre le plus proche.</span><span class="sxs-lookup"><span data-stu-id="04b57-155">For 32-bit Windows API function calls, the convention for the decoration of C-compiled functions is as follows: **function_name** becomes _ **function_name@** _n_ where  _n_ is the number of bytes expressed as a decimal taken up by all the arguments, with the bytes for each rounded up to the nearest multiple of four.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="04b57-156">La taille de tous les pointeurs dans Win32 est de quatre octets.</span><span class="sxs-lookup"><span data-stu-id="04b57-156">All pointers are four bytes wide in Win32.</span></span> <span data-ttu-id="04b57-157">Le type de renvoi n’a aucun impact sur la décoration de nom.</span><span class="sxs-lookup"><span data-stu-id="04b57-157">The return type has no impact on name decoration.</span></span> 
  
<span data-ttu-id="04b57-158">Il est possible de forcer le compilateur C++ à exposer des noms non décorés pour les fonctions C++ en encadrant la fonction et les prototypes de fonction, dans un bloc externe "C" {…},</span><span class="sxs-lookup"><span data-stu-id="04b57-158">It is possible to force the C++ compiler to expose undecorated names for C++ functions by enclosing the function, and any function prototypes, within an extern "C" {…}</span></span> <span data-ttu-id="04b57-159">comme illustré dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="04b57-159">block, as shown in this example.</span></span> <span data-ttu-id="04b57-160">(Les accolades **{}** sont omises ici, car la déclaration fait référence uniquement au bloc de code de fonction qui la suit immédiatement).</span><span class="sxs-lookup"><span data-stu-id="04b57-160">(The braces **{}** are omitted here because the declaration only refers to the function code block that immediately follows it).</span></span> 
  
```cpp
extern "C"
double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}

```

<span data-ttu-id="04b57-161">Lorsque vous placez des prototypes de fonction C dans des fichiers d’en-tête qui pourraient être inclus dans des fichiers source C ou C++, vous devez inclure la directive de préprocesseur suivante.</span><span class="sxs-lookup"><span data-stu-id="04b57-161">When you are placing C function prototypes in header files that could be included in C or C++ source files, you should include the following pre-processor directive.</span></span>
  
```cpp
#ifdef __cplusplus
extern "C" {
#endif
double WINAPI my_C_export(double x);
double WINAPI my_Cdecorated_Cpp_export(double x);
#ifdef __cplusplus
}
#endif
```

### <a name="using-the-declspecdllexport-declarator"></a><span data-ttu-id="04b57-162">Utilisation du déclarateur __declspec (dllexport)</span><span class="sxs-lookup"><span data-stu-id="04b57-162">Using the __declspec(dllexport) declarator</span></span>

<span data-ttu-id="04b57-163">Le mot clé **__declspec (dllexport)** peut être utilisé dans la déclaration de la fonction comme suit.</span><span class="sxs-lookup"><span data-stu-id="04b57-163">The **__declspec(dllexport)** keyword can be used in the declaration of the function as follows.</span></span> 
  
```cpp
__declspec(dllexport) double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

<span data-ttu-id="04b57-164">Le mot clé **__declspec (dllexport)** doit être ajouté tout à fait à gauche de la déclaration.</span><span class="sxs-lookup"><span data-stu-id="04b57-164">The **__declspec(dllexport)** keyword must be added at the extreme left of the declaration.</span></span> <span data-ttu-id="04b57-165">Les avantages de cette approche sont les suivants : la fonction ne doit pas être répertoriée dans un fichier DEF et le statut d’exportation est avec la définition.</span><span class="sxs-lookup"><span data-stu-id="04b57-165">The advantages of this approach are that the function does not need to be listed in a DEF file, and that the export status is right with the definition.</span></span> 
  
<span data-ttu-id="04b57-166">Si vous souhaitez éviter une fonction C++ rendue disponible avec la décoration de nom C++, vous devez déclarer la fonction comme suit.</span><span class="sxs-lookup"><span data-stu-id="04b57-166">If you want to avoid a C++ function being made available with the C++ name decoration, you must declare the function as follows.</span></span>
  
```cpp
extern "C"
__declspec(dllexport) double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

<span data-ttu-id="04b57-167">L’éditeur de liens rend la fonction disponible sous la forme my_undecorated_Cpp_export, autrement dit, le nom tel qu’il apparaît dans le code source sans aucune décoration.</span><span class="sxs-lookup"><span data-stu-id="04b57-167">The linker will make the function available as my_undecorated_Cpp_export, that is, the name as it appears in the source code with no decoration.</span></span>
  
### <a name="using-a-pragma-preprocessor-linker-directive"></a><span data-ttu-id="04b57-168">Utilisation d’une directive de l’éditeur de liens du préprocesseur #pragma</span><span class="sxs-lookup"><span data-stu-id="04b57-168">Using a #pragma preprocessor linker directive</span></span>

<span data-ttu-id="04b57-169">Les versions récentes de Microsoft Visual Studio prennent en charge deux macros prédéfinies qui, lorsqu’elles sont utilisées conjointement avec une directive **#pragma**, vous permettent de demander à l’éditeur de liens d’exporter la fonction directement à partir du code de fonction.</span><span class="sxs-lookup"><span data-stu-id="04b57-169">Recent versions of Microsoft Visual Studio support two predefined macros that, when used in conjunction with a **#pragma** directive, enable you to instruct the linker to export the function directly from within the function code.</span></span> <span data-ttu-id="04b57-170">Les macros sont __FUNCTION__ et __FUNCDNAME__ (notez le double trait de soulignement à chaque extrémité) qui sont développées pour les noms de fonction non décorés et décorés, respectivement.</span><span class="sxs-lookup"><span data-stu-id="04b57-170">The macros are __FUNCTION__ and __FUNCDNAME__ (note the double underline at each end) which are expanded to the undecorated and decorated function names respectively.</span></span> 
  
<span data-ttu-id="04b57-171">Par exemple, lorsque vous utilisez Microsoft Visual Studio, ces lignes peuvent être incorporées dans un fichier d’en-tête courant comme suit.</span><span class="sxs-lookup"><span data-stu-id="04b57-171">For example, when you are using Microsoft Visual Studio, these lines can be incorporated into a common header file as follows.</span></span>
  
```cpp
#if _MSC_VER > 1200 // Later than Visual Studio 6.0
#define EXPORT comment(linker, "/EXPORT:"__FUNCTION__"="__FUNCDNAME__)
#else // Cannot use this way of exporting functions.
#define EXPORT
#endif // else need to use DEF file or __declspec(dllexport)

```

<span data-ttu-id="04b57-172">Si cet en-tête est inclus dans les fichiers source, les deux exemples de fonctions peuvent ensuite être exportés comme suit.</span><span class="sxs-lookup"><span data-stu-id="04b57-172">If this header is included in the source files, the two example functions can then be exported as follows.</span></span>
  
<span data-ttu-id="04b57-173">Code C :</span><span class="sxs-lookup"><span data-stu-id="04b57-173">C code:</span></span>
  
```C
double WINAPI my_C_export(double x)
{
#pragma EXPORT
/* Modify x and return it. */
    return x * 2.0;
}
```

<span data-ttu-id="04b57-174">Code C++ :</span><span class="sxs-lookup"><span data-stu-id="04b57-174">C++ code:</span></span>
  
```cpp
double WINAPI my_Cpp_export(double x)
{
#pragma EXPORT
// Modify x and return it.
    return x * 2.0;
}
```

<span data-ttu-id="04b57-175">Notez que la directive doit être placée dans le corps de la fonction et est développée uniquement lorsque aucune des options du compilateur **/EP** ni **/P** n’est définie.</span><span class="sxs-lookup"><span data-stu-id="04b57-175">Note that the directive must be placed within the body of the function and is only expanded when neither of the compiler options **/EP** or **/P** is set.</span></span> <span data-ttu-id="04b57-176">Grâce à cette technique, aucun fichier DEF ni déclaration **__declspec(dllexport)** n’est nécessaire, et la spécification de son état d’exportation reste avec le code de fonction.</span><span class="sxs-lookup"><span data-stu-id="04b57-176">This technique removes the need for a DEF file, or **__declspec(dllexport)** declaration, and keeps the specification of its export status with the function code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="04b57-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04b57-177">See also</span></span>

- [<span data-ttu-id="04b57-178">Accès aux DLL dans Excel</span><span class="sxs-lookup"><span data-stu-id="04b57-178">Access DLLs in Excel</span></span>](how-to-access-dlls-in-excel.md)
- [<span data-ttu-id="04b57-179">Appel dans Excel à partir du fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="04b57-179">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
- [<span data-ttu-id="04b57-180">Concepts de programmation Excel</span><span class="sxs-lookup"><span data-stu-id="04b57-180">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
- [<span data-ttu-id="04b57-181">Développement de XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="04b57-181">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

