---
title: Développement de DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- DLL [excel 2007], création, la création de DLL [Excel 2007]
localization_priority: Normal
ms.assetid: 5d69d06d-a126-4c47-82ad-17112674c8a3
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 030cdd4358d9a71841eca6acfcef6e71839e02a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782038"
---
# <a name="developing-dlls"></a><span data-ttu-id="a9579-104">Développement de DLL</span><span class="sxs-lookup"><span data-stu-id="a9579-104">Developing DLLs</span></span>

<span data-ttu-id="a9579-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a9579-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a9579-106">Une bibliothèque est un corps de code compilé qui fournit des fonctionnalités et des données à une application exécutable.</span><span class="sxs-lookup"><span data-stu-id="a9579-106">A library is a body of compiled code that provides some functionality and data to an executable application.</span></span> <span data-ttu-id="a9579-107">Bibliothèques peuvent être liées statiquement ou liées de manière dynamique, et traditionnellement ont les .lib d’extensions de nom de fichier .dll respectivement.</span><span class="sxs-lookup"><span data-stu-id="a9579-107">Libraries can be either statically linked or dynamically linked, and they conventionally have the file name extensions .lib and .dll respectively.</span></span> <span data-ttu-id="a9579-108">Bibliothèques statiques (par exemple, la bibliothèque Runtime C) sont liés à l’application au niveau de compilation et donc font partie de l’exécutable qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="a9579-108">Static libraries (such as the C run-time library) are linked to the application at compilation and so become part of the resulting executable.</span></span> <span data-ttu-id="a9579-109">L’application charge une DLL lorsqu’il est nécessaire, généralement au démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="a9579-109">The application loads a DLL when it is needed, usually when the application starts up.</span></span> <span data-ttu-id="a9579-110">Une DLL peut charger et lier dynamiquement à une autre DLL.</span><span class="sxs-lookup"><span data-stu-id="a9579-110">One DLL can load and dynamically link to another DLL.</span></span>
  
## <a name="benefits-of-using-dlls"></a><span data-ttu-id="a9579-111">Avantages de l’utilisation des DLL</span><span class="sxs-lookup"><span data-stu-id="a9579-111">Benefits of using DLLs</span></span>

<span data-ttu-id="a9579-112">Les principaux avantages des DLL sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a9579-112">The main benefits of DLLs are as follows:</span></span>
  
- <span data-ttu-id="a9579-113">Toutes les applications peuvent partager une seule copie sur le disque.</span><span class="sxs-lookup"><span data-stu-id="a9579-113">All applications can share a single copy on disk.</span></span>
    
- <span data-ttu-id="a9579-114">Les fichiers exécutables des applications sont conservés plus petits.</span><span class="sxs-lookup"><span data-stu-id="a9579-114">Applications' executable files are kept smaller.</span></span>
    
- <span data-ttu-id="a9579-115">Ils permettent aux projets de développement grande être réparties.</span><span class="sxs-lookup"><span data-stu-id="a9579-115">They enable large development projects to be broken down.</span></span> <span data-ttu-id="a9579-116">Les développeurs d’application et la DLL doivent accepter une interface entre leurs composants respectifs.</span><span class="sxs-lookup"><span data-stu-id="a9579-116">Application and DLL developers only need agree an interface between their respective parts.</span></span> <span data-ttu-id="a9579-117">Cette interface est exportée par la DLL.</span><span class="sxs-lookup"><span data-stu-id="a9579-117">This interface is exported by the DLL.</span></span>
    
- <span data-ttu-id="a9579-118">Les développeurs DLL peuvent mettre à jour les DLL — par exemple, pour les rendre plus efficace ou pour résoudre un bogue, sans avoir à mettre à jour toutes les applications qui l’utilisent, à condition que l’interface de la DLL exportée ne change pas.</span><span class="sxs-lookup"><span data-stu-id="a9579-118">DLL developers can update DLLs—perhaps to make them more efficient or to fix a bug—without having to update all the applications that use it, provided that the exported interface of the DLL does not change.</span></span>
    
<span data-ttu-id="a9579-119">Vous pouvez utiliser la DLL pour ajouter des fonctions de feuille de calcul et les commandes dans Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="a9579-119">You can use DLLs to add worksheet functions and commands in Microsoft Excel.</span></span>
  
## <a name="resources-for-creating-dlls"></a><span data-ttu-id="a9579-120">Ressources pour la création de DLL</span><span class="sxs-lookup"><span data-stu-id="a9579-120">Resources for creating DLLs</span></span>

<span data-ttu-id="a9579-121">Pour créer une DLL, vous devez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="a9579-121">To create a DLL, you need the following:</span></span>
  
- <span data-ttu-id="a9579-122">Un éditeur de code source.</span><span class="sxs-lookup"><span data-stu-id="a9579-122">A source code editor.</span></span>
    
- <span data-ttu-id="a9579-123">Un compilateur pour activer le code source dans le code de l’objet qui est compatible avec votre matériel.</span><span class="sxs-lookup"><span data-stu-id="a9579-123">A compiler to turn source code into object code that is compatible with your hardware.</span></span>
    
- <span data-ttu-id="a9579-124">Un éditeur de liens pour ajouter du code à partir de bibliothèques statiques, où les utilisées et pour créer le fichier exécutable de la DLL.</span><span class="sxs-lookup"><span data-stu-id="a9579-124">A linker to add code from static libraries, where used, and to create the executable DLL file.</span></span>
    
<span data-ttu-id="a9579-125">Fournissent des environnements modernes de développement intégré (IDE), tel que Microsoft Visual Studio, tous ces éléments.</span><span class="sxs-lookup"><span data-stu-id="a9579-125">Modern integrated development environments (IDEs), such as Microsoft Visual Studio, provide all of these things.</span></span> <span data-ttu-id="a9579-126">Elles fournissent également beaucoup plus : actives éditeurs, outils de débogage de votre code, outils permettant de gérer plusieurs projets, de nouveaux Assistants de projet et de nombreux autres outils importants.</span><span class="sxs-lookup"><span data-stu-id="a9579-126">They also provide a great deal more: smart editors, tools to debug your code, tools to manage multiple projects, new project wizards, and many other important tools.</span></span>
  
<span data-ttu-id="a9579-127">Vous pouvez créer des DLL dans plusieurs langues, par exemple, C/C++, Pascal et Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a9579-127">You can create DLLs in several languages, for example, C/C++, Pascal and Visual Basic.</span></span> <span data-ttu-id="a9579-128">Étant donné que l’API de code source fourni avec Excel est C et C++, seuls ces deux langages sont considérés comme dans cette documentation.</span><span class="sxs-lookup"><span data-stu-id="a9579-128">Given that the API source code provided with Excel is C and C++, only these two languages are considered in this documentation.</span></span>
  
## <a name="exporting-functions-and-commands"></a><span data-ttu-id="a9579-129">Exportation des fonctions et les commandes</span><span class="sxs-lookup"><span data-stu-id="a9579-129">Exporting functions and commands</span></span>

<span data-ttu-id="a9579-130">Lors de la compilation d’un projet de DLL, le compilateur et l’éditeur de liens doivent connaître les fonctions qui sont à exporter afin qu’ils peuvent être disponibles à l’application.</span><span class="sxs-lookup"><span data-stu-id="a9579-130">When compiling a DLL project, the compiler and linker need to know what functions are to be exported so that they can make them available to the application.</span></span> <span data-ttu-id="a9579-131">Cette section décrit les moyens de que le faire.</span><span class="sxs-lookup"><span data-stu-id="a9579-131">This section describes the ways this can be done.</span></span>
  
<span data-ttu-id="a9579-132">Lorsque les compilateurs compilent le code source, en général, ils modifient les noms des fonctions à partir de leur affichage dans le code source.</span><span class="sxs-lookup"><span data-stu-id="a9579-132">When compilers compile source code, in general, they change the names of the functions from their appearance in the source code.</span></span> <span data-ttu-id="a9579-133">Ils généralement cela en ajoutant le début et/ou à la fin du nom, dans un processus appelé ornement de nom.</span><span class="sxs-lookup"><span data-stu-id="a9579-133">They usually do this by adding to the beginning and/or end of the name, in a process known as name decoration.</span></span> <span data-ttu-id="a9579-134">Vous devez vous assurer que la fonction est exportée par un nom reconnaissable à l’application de chargement de la DLL.</span><span class="sxs-lookup"><span data-stu-id="a9579-134">You need to make sure that the function is exported with a name that is recognizable to the application loading the DLL.</span></span> <span data-ttu-id="a9579-135">Cela peut signifier pour présenter à l’éditeur de liens pour associer le nom décoré avec un nom plus simple d’exportation.</span><span class="sxs-lookup"><span data-stu-id="a9579-135">This can mean telling the linker to associate the decorated name with a simpler export name.</span></span> <span data-ttu-id="a9579-136">Le nom de l’exportation peut être le nom tel qu’il apparaissait à l’origine dans le code source, ou autre chose.</span><span class="sxs-lookup"><span data-stu-id="a9579-136">The export name can be the name as it originally appeared in the source code, or something else.</span></span>
  
<span data-ttu-id="a9579-137">La façon dont le nom est décoré dépend de la langue et la façon dont le compilateur est invité à mettre à la disposition, la fonction autrement dit, la convention d’appel.</span><span class="sxs-lookup"><span data-stu-id="a9579-137">The way the name is decorated depends on the language and how the compiler is instructed to make the function available, that is, the calling convention.</span></span> <span data-ttu-id="a9579-138">Convention d’appel entre les processus standard de Windows utilisés par les DLL est appelée la convention WinAPI.</span><span class="sxs-lookup"><span data-stu-id="a9579-138">The standard inter-process calling convention for Windows used by DLLs is known as the WinAPI convention.</span></span> <span data-ttu-id="a9579-139">Il est défini dans les fichiers d’en-tête Windows en tant que **WINAPI**, qui est définie à son tour à l’aide de la de déclarateur Win32 **__stdcall**.</span><span class="sxs-lookup"><span data-stu-id="a9579-139">It is defined in Windows header files as **WINAPI**, which is in turn defined using the Win32 declarator **__stdcall**.</span></span>
  
<span data-ttu-id="a9579-140">Une fonction d’exportation de la DLL pour une utilisation avec Excel (si elle est une fonction de feuille de calcul, fonction équivalente feuille macro ou commande définie par l’utilisateur) doit toujours utiliser le **WINAPI** / convention d’appel **__stdcall** .</span><span class="sxs-lookup"><span data-stu-id="a9579-140">A DLL-export function for use with Excel (whether it is a worksheet function, macro-sheet equivalent function, or user-defined command) should always use the **WINAPI** / **__stdcall** calling convention.</span></span> <span data-ttu-id="a9579-141">Il est nécessaire d’inclure le spécificateur **WINAPI** explicitement dans la définition de la fonction que la valeur par défaut dans Win32 compilateurs consiste à utiliser la **__cdecl** convention d’appel, également définie en tant que **WINAPIV**, si aucun n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="a9579-141">It is necessary to include the **WINAPI** specifier explicitly in the function's definition as the default in Win32 compilers is to use the **__cdecl** calling convention, also defined as **WINAPIV**, if none is specified.</span></span>
  
<span data-ttu-id="a9579-142">Vous pouvez indiquer à l’éditeur de liens qui une fonction doit être exporté et le nom qu’il est à l’extérieur de plusieurs façons :</span><span class="sxs-lookup"><span data-stu-id="a9579-142">You can tell the linker that a function is to be exported, and the name it is to be known by externally in one of several ways:</span></span>
  
- <span data-ttu-id="a9579-143">Placez la fonction dans un fichier de définition après le mot clé **EXPORTE** et définir votre projet DLL pour faire référence à ce fichier lors de la liaison.</span><span class="sxs-lookup"><span data-stu-id="a9579-143">Place the function in a DEF file after the **EXPORTS** keyword, and set your DLL project setting to reference this file when linking.</span></span> 
    
- <span data-ttu-id="a9579-144">Utilisez le déclarateur **__declspec (dllexport)** dans la définition de la fonction.</span><span class="sxs-lookup"><span data-stu-id="a9579-144">Use the **__declspec(dllexport)** declarator in the function's definition.</span></span> 
    
- <span data-ttu-id="a9579-145">Utilisez une directive de préprocesseur **#pragma** pour envoyer un message à l’éditeur de liens.</span><span class="sxs-lookup"><span data-stu-id="a9579-145">Use a **#pragma** preprocessor directive to send a message to the linker.</span></span> 
    
<span data-ttu-id="a9579-146">Bien que votre projet peut utiliser ces trois méthodes et votre compilateur et l’éditeur de liens prennent en charge les, vous devriez pas exporter une fonction dans plus d’une des manières suivantes.</span><span class="sxs-lookup"><span data-stu-id="a9579-146">Although your project can use all three methods and your compiler and linker support them, you should not try to export one function in more than one of these ways.</span></span> <span data-ttu-id="a9579-147">Par exemple, supposons qu’une DLL contient les modules de code source deux, C et un langage C++, qui contient deux fonctions à exporter, **Mon\_C\_exporter** et **Mon\_RPC\_exporter** respectivement.</span><span class="sxs-lookup"><span data-stu-id="a9579-147">For example, suppose that a DLL contains two source code modules, one C and one C++, which contain two functions to be exported, **my\_C\_export** and **my\_Cpp\_export** respectively.</span></span> <span data-ttu-id="a9579-148">Par souci de simplicité, supposons que chaque fonction prend un seul argument numérique double précision et renvoie le même type de données.</span><span class="sxs-lookup"><span data-stu-id="a9579-148">For simplicity, suppose that each function takes a single double-precision numerical argument and returns the same data type.</span></span> <span data-ttu-id="a9579-149">Les possibilités d’exportation de chaque fonction à l’aide de chacune de ces méthodes sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="a9579-149">The alternatives for exporting each function by using each of these methods are outlined in the following sections.</span></span> 
  
### <a name="using-a-def-file"></a><span data-ttu-id="a9579-150">À l’aide d’un fichier de définition</span><span class="sxs-lookup"><span data-stu-id="a9579-150">Using a DEF file</span></span>

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

<span data-ttu-id="a9579-151">Le fichier DEF devra puis contient ces lignes.</span><span class="sxs-lookup"><span data-stu-id="a9579-151">The DEF file would then need to contain these lines.</span></span>
  
`EXPORTS my_C_export = _my_C_export@8  my_Cpp_export`

<br/>

<span data-ttu-id="a9579-152">La syntaxe générale d’une ligne qui suit une instruction **exportations** est comme suit.</span><span class="sxs-lookup"><span data-stu-id="a9579-152">The general syntax of a line that follows an **EXPORTS** statement is as follows.</span></span> 
  
`entryname[=internalname] [@ordinal[NONAME]] [DATA] [PRIVATE]`

<span data-ttu-id="a9579-153">Notez que la fonction C a été décorée, mais le fichier DEF force explicitement l’éditeur de liens pour exposer la fonction en utilisant le nom de code source d’origine (dans cet exemple).</span><span class="sxs-lookup"><span data-stu-id="a9579-153">Note that the C function has been decorated, but the DEF file explicitly forces the linker to expose the function using the original source code name (in this example).</span></span> <span data-ttu-id="a9579-154">L’éditeur de liens exporte implicitement la fonction C++ en utilisant le nom de code d’origine, afin qu’il ne soit pas nécessaire d’inclure le nom décoré dans le fichier de définition.</span><span class="sxs-lookup"><span data-stu-id="a9579-154">The linker implicitly exports the C++ function using the original code name, so that it is not necessary to include the decorated name in the DEF file.</span></span>
  
<span data-ttu-id="a9579-155">Pour les appels de fonction API Windows 32 bits, la convention pour l’habillage graphique des fonctions compilé-C est la suivante : **nom de la fonction** devient le **nom de la fonction @** _ _n_ où _n_ est le nombre d’octets exprimée sous la forme d’un nombre décimal pris en charge par tous les arguments, les octets pour chaque arrondi au multiple plus proche de quatre.</span><span class="sxs-lookup"><span data-stu-id="a9579-155">For 32-bit Windows API function calls, the convention for the decoration of C-compiled functions is as follows: **function_name** becomes _ **function_name@** _n_ where  _n_ is the number of bytes expressed as a decimal taken up by all the arguments, with the bytes for each rounded up to the nearest multiple of four.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a9579-156">Tous les pointeurs sont les quatre octets dans Win32.</span><span class="sxs-lookup"><span data-stu-id="a9579-156">All pointers are four bytes wide in Win32.</span></span> <span data-ttu-id="a9579-157">Le type de retour a aucun impact sur ornement de nom.</span><span class="sxs-lookup"><span data-stu-id="a9579-157">The return type has no impact on name decoration.</span></span> 
  
<span data-ttu-id="a9579-158">Il est possible d’obliger le compilateur C++ pour exposer des noms non décorés des fonctions C++ en mettant la fonction et les prototypes de fonction, au sein d’un « C » {...} externe</span><span class="sxs-lookup"><span data-stu-id="a9579-158">It is possible to force the C++ compiler to expose undecorated names for C++ functions by enclosing the function, and any function prototypes, within an extern "C" {…}</span></span> <span data-ttu-id="a9579-159">bloquer, comme illustré dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="a9579-159">block, as shown in this example.</span></span> <span data-ttu-id="a9579-160">(Les accolades **{}** sont tous deux omis ici car la déclaration fait référence uniquement pour le bloc de code de fonction qui suit immédiatement).</span><span class="sxs-lookup"><span data-stu-id="a9579-160">(The braces **{}** are omitted here because the declaration only refers to the function code block that immediately follows it).</span></span> 
  
```cpp
extern "C"
double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}

```

<span data-ttu-id="a9579-161">Lorsque vous placez prototypes de fonction C dans les fichiers d’en-tête qui peuvent être inclus dans les fichiers source C ou C++, vous devez inclure la directive de préprocesseur suivante.</span><span class="sxs-lookup"><span data-stu-id="a9579-161">When you are placing C function prototypes in header files that could be included in C or C++ source files, you should include the following pre-processor directive.</span></span>
  
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

### <a name="using-the-declspecdllexport-declarator"></a><span data-ttu-id="a9579-162">À l’aide de la déclarateur __declspec (dllexport)</span><span class="sxs-lookup"><span data-stu-id="a9579-162">Using the __declspec(dllexport) declarator</span></span>

<span data-ttu-id="a9579-163">Le mot clé **__declspec (dllexport)** peut être utilisé dans la déclaration de la fonction comme suit.</span><span class="sxs-lookup"><span data-stu-id="a9579-163">The **__declspec(dllexport)** keyword can be used in the declaration of the function as follows.</span></span> 
  
```cpp
__declspec(dllexport) double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

<span data-ttu-id="a9579-164">Le mot clé **__declspec (dllexport)** doit être ajouté à l’extrême gauche de la déclaration.</span><span class="sxs-lookup"><span data-stu-id="a9579-164">The **__declspec(dllexport)** keyword must be added at the extreme left of the declaration.</span></span> <span data-ttu-id="a9579-165">Les avantages de cette approche sont que la fonction ne doit pas figurer dans un fichier de définition, et que l’état de l’exportation est à la définition.</span><span class="sxs-lookup"><span data-stu-id="a9579-165">The advantages of this approach are that the function does not need to be listed in a DEF file, and that the export status is right with the definition.</span></span> 
  
<span data-ttu-id="a9579-166">Si vous souhaitez éviter une fonction C++ seront disponible avec l’ornement de nom C++, vous devez déclarer la fonction comme suit.</span><span class="sxs-lookup"><span data-stu-id="a9579-166">If you want to avoid a C++ function being made available with the C++ name decoration, you must declare the function as follows.</span></span>
  
```cpp
extern "C"
__declspec(dllexport) double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

<span data-ttu-id="a9579-167">L’éditeur de liens rend la fonction disponibles en tant que my_undecorated_Cpp_export, autrement dit, le nom tel qu’il apparaît dans le code source avec aucun ornement.</span><span class="sxs-lookup"><span data-stu-id="a9579-167">The linker will make the function available as my_undecorated_Cpp_export, that is, the name as it appears in the source code with no decoration.</span></span>
  
### <a name="using-a-pragma-preprocessor-linker-directive"></a><span data-ttu-id="a9579-168">À l’aide d’une directive de l’éditeur de liens préprocesseur #pragma</span><span class="sxs-lookup"><span data-stu-id="a9579-168">Using a #pragma preprocessor linker directive</span></span>

<span data-ttu-id="a9579-169">Dernières versions de Microsoft Visual Studio prend en charge deux macros prédéfinies qui, lorsqu’elle est utilisée conjointement avec une directive **#pragma** , permettent de demander à l’éditeur de liens pour exporter la fonction directement dans le code de la fonction.</span><span class="sxs-lookup"><span data-stu-id="a9579-169">Recent versions of Microsoft Visual Studio support two predefined macros that, when used in conjunction with a **#pragma** directive, enable you to instruct the linker to export the function directly from within the function code.</span></span> <span data-ttu-id="a9579-170">Les macros sont __fonction__ et __FUNCDNAME__ (Notez la double souligné à chaque fin) qui sont développées pour les noms de fonction non décorée et décorée respectivement.</span><span class="sxs-lookup"><span data-stu-id="a9579-170">The macros are __FUNCTION__ and __FUNCDNAME__ (note the double underline at each end) which are expanded to the undecorated and decorated function names respectively.</span></span> 
  
<span data-ttu-id="a9579-171">Par exemple, lorsque vous utilisez Microsoft Visual Studio, ces lignes peuvent être intégrés comme suit dans un fichier d’en-tête courants.</span><span class="sxs-lookup"><span data-stu-id="a9579-171">For example, when you are using Microsoft Visual Studio, these lines can be incorporated into a common header file as follows.</span></span>
  
```cpp
#if _MSC_VER > 1200 // Later than Visual Studio 6.0
#define EXPORT comment(linker, "/EXPORT:"__FUNCTION__"="__FUNCDNAME__)
#else // Cannot use this way of exporting functions.
#define EXPORT
#endif // else need to use DEF file or __declspec(dllexport)

```

<span data-ttu-id="a9579-172">Si cet en-tête est inclus dans les fichiers source, les fonctions de deux exemples peuvent ensuite être exportées comme suit.</span><span class="sxs-lookup"><span data-stu-id="a9579-172">If this header is included in the source files, the two example functions can then be exported as follows.</span></span>
  
<span data-ttu-id="a9579-173">Code C :</span><span class="sxs-lookup"><span data-stu-id="a9579-173">C code:</span></span>
  
```C
double WINAPI my_C_export(double x)
{
#pragma EXPORT
/* Modify x and return it. */
    return x * 2.0;
}
```

<span data-ttu-id="a9579-174">Code C++ :</span><span class="sxs-lookup"><span data-stu-id="a9579-174">C++ code:</span></span>
  
```cpp
double WINAPI my_Cpp_export(double x)
{
#pragma EXPORT
// Modify x and return it.
    return x * 2.0;
}
```

<span data-ttu-id="a9579-175">Notez que la directive doit être placée dans le corps de la fonction et est développée uniquement lorsque aucune des options du compilateur **/EP** ou **/P** est défini.</span><span class="sxs-lookup"><span data-stu-id="a9579-175">Note that the directive must be placed within the body of the function and is only expanded when neither of the compiler options **/EP** or **/P** is set.</span></span> <span data-ttu-id="a9579-176">Cette technique élimine le besoin d’un fichier de définition ou déclaration **__declspec (dllexport)** et conserve la spécification de son état d’exportation avec le code de la fonction.</span><span class="sxs-lookup"><span data-stu-id="a9579-176">This technique removes the need for a DEF file, or **__declspec(dllexport)** declaration, and keeps the specification of its export status with the function code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a9579-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9579-177">See also</span></span>

- [<span data-ttu-id="a9579-178">Accès aux DLL dans Excel</span><span class="sxs-lookup"><span data-stu-id="a9579-178">Access DLLs in Excel</span></span>](how-to-access-dlls-in-excel.md)
- [<span data-ttu-id="a9579-179">Appel dans Excel � partir du fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="a9579-179">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
- [<span data-ttu-id="a9579-180">Concepts de programmation Excel</span><span class="sxs-lookup"><span data-stu-id="a9579-180">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
- [<span data-ttu-id="a9579-181">D�veloppement de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="a9579-181">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

