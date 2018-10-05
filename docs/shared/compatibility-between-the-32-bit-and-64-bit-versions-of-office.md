---
title: Compatibilité entre les versions 32 bits et 64 bits d’Office
ms.date: 04/27/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: ff49dc9e-daf8-43cf-8802-51c2537ed561
description: Découvrez comment la version 32 bits d’Office est compatible avec la version 64 bits d’Office.
ms.openlocfilehash: eeff11f11d4f2595b7111c0233703d09b1c46651
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390939"
---
# <a name="compatibility-between-the-32-bit-and-64-bit-versions-of-office"></a><span data-ttu-id="3e696-103">Compatibilité entre les versions 32 bits et 64 bits d’Office</span><span class="sxs-lookup"><span data-stu-id="3e696-103">Compatibility between the 32-bit and 64-bit versions of Office</span></span>

<span data-ttu-id="3e696-104">Découvrez comment la version 32 bits d’Office est compatible avec la version 64 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="3e696-104">Find out how the 32-bit version of Office is compatible with the 64-bit version of Office.</span></span>
  
<span data-ttu-id="3e696-105">Applications Office sont disponibles en versions 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3e696-105">Office applications are available in 32-bit and 64-bit versions.</span></span> 
  
<span data-ttu-id="3e696-106">Les versions 64 bits d’Office permettent de déplacer des données pour des capacités, par exemple, lorsque vous travaillez avec un grand nombre de Microsoft Excel 2010.</span><span class="sxs-lookup"><span data-stu-id="3e696-106">The 64-bit versions of Office enable you to move more data around for increased capability, for example when you work with large numbers in Microsoft Excel 2010.</span></span> <span data-ttu-id="3e696-107">Lorsque vous écrivez du code 32 bits, vous pouvez utiliser la version 64 bits d’Office sans aucune modification.</span><span class="sxs-lookup"><span data-stu-id="3e696-107">When writing 32-bit code, you can use the 64-bit version of Office without any changes.</span></span> <span data-ttu-id="3e696-108">Toutefois, lorsque vous écrivez du code 64 bits, vous devez vous assurer que votre code contienne des constantes de compilation conditionnelle pour vous assurer que le code est compatible avec la version antérieure d’Office et les mots clés spécifiques, et que le code est en cours d’exécution si vous combinaison de code 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3e696-108">However, when you write 64-bit code, you should ensure that your code contains specific keywords and conditional compilation constants to ensure that the code is backward compatible with earlier version of Office, and that the correct code is being executed if you mix 32-bit and 64-bit code.</span></span>
  
<span data-ttu-id="3e696-109">Visual Basic pour Applications 7.0 (7 VBA) est publié dans les versions 64 bits d’Office, et elle fonctionne avec les applications 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3e696-109">Visual Basic for Applications 7.0 (VBA 7) is released in the 64-bit versions for Office, and it works with both 32-bit and 64-bit applications.</span></span> <span data-ttu-id="3e696-110">Les modifications décrites dans cet article s’appliquent uniquement aux versions 64 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="3e696-110">The changes described in this article apply only to the 64-bit versions of Office.</span></span> <span data-ttu-id="3e696-111">Utilisant les versions 32 bits d’activation de Microsoft Office vous permet d’utiliser les solutions créées dans les versions précédentes d’Office sans aucune modification.</span><span class="sxs-lookup"><span data-stu-id="3e696-111">Using the 32-bit versions of Microsoft Office enable you to use solutions built in previous versions of Office without further modifications.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3e696-112">Par défaut, lorsque vous installez une version 64 bits d’Office, vous installez également la version 32 bits est installé avec le système 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3e696-112">By default, when you install a 64-bit version of Office, you also install the 32-bit version is installed along with the 64-bit system.</span></span> <span data-ttu-id="3e696-113">Vous devez sélectionner explicitement l’option d’installation de Microsoft Office 64 bits version.</span><span class="sxs-lookup"><span data-stu-id="3e696-113">You must explicitly select the Microsoft Office 64-bit version installation option.</span></span> 
  
<span data-ttu-id="3e696-114">Dans VBA 7, vous devez mettre à jour des instructions d’API Windows existantes (les instructions**Declare** ) pour fonctionner avec la version 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3e696-114">In VBA 7, you must update existing Windows API statements (**Declare** statements) to work with the 64-bit version.</span></span> <span data-ttu-id="3e696-115">En outre, vous devez mettre à jour des pointeurs d’adresse et afficher les poignées de fenêtre dans les types définis par l’utilisateur qui sont utilisés par ces instructions.</span><span class="sxs-lookup"><span data-stu-id="3e696-115">Additionally, you must update address pointers and display window handles in user-defined types that are used by these statements.</span></span> <span data-ttu-id="3e696-116">Cette opération est abordée plus en détail dans cet article, ainsi que les problèmes de compatibilité entre les versions 32 bits et 64 bits et les solutions suggérées.</span><span class="sxs-lookup"><span data-stu-id="3e696-116">This is discussed in more detail in this article as well as compatibility issues between the 32-bit and 64-bit versions and suggested solutions.</span></span> 
  
## <a name="comparing-32-bit-and-64-bit-systems"></a><span data-ttu-id="3e696-117">Comparaison des systèmes 32 bits et 64 bits</span><span class="sxs-lookup"><span data-stu-id="3e696-117">Comparing 32-bit and 64-bit systems</span></span>
<span data-ttu-id="3e696-118"><a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a></span><span class="sxs-lookup"><span data-stu-id="3e696-118"></span></span>

<span data-ttu-id="3e696-119">Les applications créées avec les versions 64 bits d’Office peuvent référencer des espaces d’adressage plus grandes que les versions 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3e696-119">Applications built with the 64-bit versions of Office can reference larger address spaces than 32-bit versions.</span></span> <span data-ttu-id="3e696-120">Cela signifie que vous pouvez utiliser davantage de mémoire physique pour que les données avant, ce qui peut réduire la surcharge passé le transfert de données dans la mémoire physique</span><span class="sxs-lookup"><span data-stu-id="3e696-120">This means you can use more physical memory for data than before, potentially reducing the overhead spent moving data in and out of physical memory</span></span>
  
<span data-ttu-id="3e696-121">En plus de faire référence à des emplacements spécifiques (appelés pointeurs) dans la mémoire physique, vous pouvez également utiliser des adresses pour référencer des identificateurs de fenêtre d’affichage (appelés poignées).</span><span class="sxs-lookup"><span data-stu-id="3e696-121">In addition to referring specific locations (known as pointers) in physical memory, you can also use addresses to reference display window identifiers (known as handles).</span></span> <span data-ttu-id="3e696-122">La taille (en octets) du pointeur ou handle varie selon que vous utilisez un système 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3e696-122">The size (in bytes) of the pointer or handle depends on whether you're using a 32-bit or 64-bit system.</span></span> 
  
<span data-ttu-id="3e696-123">Si vous souhaitez exécuter vos solutions existantes avec les versions 64 bits d’Office, prenez en compte les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="3e696-123">If you want to run your existing solutions with the 64-bit versions of Office, be aware of the following:</span></span>
  
- <span data-ttu-id="3e696-124">Impossible de charger le processus 64 bits natifs dans Office binaires 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3e696-124">Native 64-bit processes in Office cannot load 32-bit binaries.</span></span> <span data-ttu-id="3e696-125">Ce programme devrait être des problèmes lorsque vous avez des contrôles Microsoft ActiveX existants et compléments existants.</span><span class="sxs-lookup"><span data-stu-id="3e696-125">This is expected to be a common issue when you have existing Microsoft ActiveX controls and existing add-ins.</span></span>
    
- <span data-ttu-id="3e696-126">VBA n’a pas été précédemment ont un type de données pointeur, afin que vous deviez utiliser des variables 32 bits pour stocker des pointeurs et les poignées.</span><span class="sxs-lookup"><span data-stu-id="3e696-126">VBA previously didn't have a pointer data type, so you had to use 32-bit variables to store pointers and handles.</span></span> <span data-ttu-id="3e696-127">Ces variables tronquent 64 bits les valeurs renvoyées par les appels d’API lors de l’utilisation des instructions **Declare** .</span><span class="sxs-lookup"><span data-stu-id="3e696-127">These variables now truncate 64-bit values returned by API calls when using **Declare** statements.</span></span> 
    
## <a name="vba-7-code-base"></a><span data-ttu-id="3e696-128">Base de code VBA 7</span><span class="sxs-lookup"><span data-stu-id="3e696-128">VBA 7 code base</span></span>
<span data-ttu-id="3e696-129"><a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a></span><span class="sxs-lookup"><span data-stu-id="3e696-129"></span></span>

<span data-ttu-id="3e696-130">VBA 7 remplace le code VBA dans Office 2007 et versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="3e696-130">VBA 7 replaces the VBA code base in Office 2007 and earlier versions.</span></span> <span data-ttu-id="3e696-131">VBA 7 est disponible dans les versions 32 bits et 64 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="3e696-131">VBA 7 is available in both the 32-bit and 64-bit versions of Office.</span></span> <span data-ttu-id="3e696-132">Il fournit des deux constantes de compilation conditionnelle :</span><span class="sxs-lookup"><span data-stu-id="3e696-132">It provides two conditional compilation constants:</span></span> 
  
- <span data-ttu-id="3e696-133">**VBA7** - permet d’assurer la compatibilité descendante de votre code en vérifiant si votre application est à l’aide de VBA 7 ou la version précédente de VBA.</span><span class="sxs-lookup"><span data-stu-id="3e696-133">**VBA7** - Helps ensure the backward compatibility of your code by testing whether your application is using VBA 7 or the previous version of VBA.</span></span> 
    
- <span data-ttu-id="3e696-134">**Win64** Teste l’exécution du code 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3e696-134">**Win64** Tests whether code is running as 32-bit or 64-bit.</span></span> 
    
<span data-ttu-id="3e696-135">À quelques exceptions près, les macros dans un document qui fonctionnent dans la version 32 bits de l’application fonctionnent également dans la version 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3e696-135">With certain exceptions, the macros in a document that work in the 32-bit version of the application also work in the 64-bit version.</span></span>
  
## <a name="activex-control-and-com-add-in-compatibility"></a><span data-ttu-id="3e696-136">Contrôle ActiveX et la compatibilité des compléments COM</span><span class="sxs-lookup"><span data-stu-id="3e696-136">ActiveX control and COM add-in compatibility</span></span>
<span data-ttu-id="3e696-137"><a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a></span><span class="sxs-lookup"><span data-stu-id="3e696-137"></span></span>

<span data-ttu-id="3e696-138">Existants les contrôles ActiveX 32 bits, ne sont pas compatibles avec les versions 64 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="3e696-138">Existing 32-bit ActiveX controls, are not compatible with the 64-bit versions of Office.</span></span> <span data-ttu-id="3e696-139">Pour les contrôles ActiveX et les objets COM :</span><span class="sxs-lookup"><span data-stu-id="3e696-139">For ActiveX controls and COM objects:</span></span>
  
- <span data-ttu-id="3e696-140">Si vous avez le code source, générer une version 64 bits vous-même.</span><span class="sxs-lookup"><span data-stu-id="3e696-140">If you have the source code, generate a 64-bit version yourself.</span></span>
- <span data-ttu-id="3e696-141">Si vous ne disposez pas du code source, contactez le fournisseur pour obtenir une version mise à jour.</span><span class="sxs-lookup"><span data-stu-id="3e696-141">If you don't have the source code, contact the vendor for an updated version.</span></span>
    
<span data-ttu-id="3e696-142">Impossible de charger le processus 64 bits natifs dans Office binaires 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3e696-142">Native 64-bit processes in Office cannot load 32-bit binaries.</span></span> <span data-ttu-id="3e696-143">Cela inclut les contrôles courants de **MSComCtl** (TabStrip, barre d’outils, StatusBar, ProgressBar, TreeView, ListViews, ImageList, curseur, ImageComboBox) et les contrôles de **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar).</span><span class="sxs-lookup"><span data-stu-id="3e696-143">This includes the common controls of **MSComCtl** (TabStrip, Toolbar, StatusBar, ProgressBar, TreeView, ListViews, ImageList, Slider, ImageComboBox) and the controls of **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar).</span></span> <span data-ttu-id="3e696-144">Ces contrôles ont été installés par les versions 32 bits d’Office antérieure à Office 2010.</span><span class="sxs-lookup"><span data-stu-id="3e696-144">These controls were installed by 32-bit versions of Office earlier than Office 2010.</span></span> <span data-ttu-id="3e696-145">Vous devez trouver une alternative de vos solutions VBA existantes qui utilisent ces contrôles lorsque vous migrez le code pour les versions 64 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="3e696-145">You'll need to find an alternative for your existing VBA solutions that use these controls when you migrate the code to the 64-bit versions of Office.</span></span> 
  
## <a name="api-compatibility"></a><span data-ttu-id="3e696-146">Compatibilité des API</span><span class="sxs-lookup"><span data-stu-id="3e696-146">API compatibility</span></span>
<span data-ttu-id="3e696-147"><a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a></span><span class="sxs-lookup"><span data-stu-id="3e696-147"></span></span>

<span data-ttu-id="3e696-148">La combinaison de bibliothèques VBA et de type vous offre de nombreuses fonctionnalités pour créer des applications Office.</span><span class="sxs-lookup"><span data-stu-id="3e696-148">The combination of VBA and type libraries gives you lots of functionality to create Office applications.</span></span> <span data-ttu-id="3e696-149">Toutefois, vous devez parfois communiquent directement avec le système d’exploitation et d’autres composants, tels que lorsque vous gérez mémoire ou les processus, lorsque vous travaillez avec des contrôles et des fenêtres de linke des éléments de l’interface utilisateur, ou lorsque vous modifiez le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="3e696-149">However, sometimes you must communicate directly with the computer's operating system and other components, such as when you manage memory or processes, when working with UI elements linke windows and controls, or when modifying the Windows registry.</span></span> <span data-ttu-id="3e696-150">Dans ces scénarios, la meilleure solution consiste à utiliser l’une des fonctions externes incorporés dans des fichiers DLL.</span><span class="sxs-lookup"><span data-stu-id="3e696-150">In these scenarios, your best option is to use one of the external functions that are embedded in DLL files.</span></span> <span data-ttu-id="3e696-151">Cela dans VBA en effectuant des appels d’API à l’aide des instructions **Declare** .</span><span class="sxs-lookup"><span data-stu-id="3e696-151">You do this in VBA by making API calls using **Declare** statements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3e696-152">Microsoft propose un fichier Win32API.txt qui contient les instructions Declare 1500 et un outil pour copier l’instruction **Declare** que vous souhaitez dans votre code.</span><span class="sxs-lookup"><span data-stu-id="3e696-152">Microsoft provides a Win32API.txt file that contains 1,500 Declare statements and a tool to copy the **Declare** statement that you want into your code.</span></span> <span data-ttu-id="3e696-153">Toutefois, ces instructions sont pour les systèmes 32 bits et doit être converties en 64 bits en utilisant les informations décrites plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="3e696-153">However, these statements are for 32-bit systems and must be converted to 64-bit by using the information discussed later in this article.</span></span> <span data-ttu-id="3e696-154">Les instructions **Declare** existantes ne seront pas compilées dans VBA 64 bits jusqu'à ce qu’ils ont été marquées comme sûrs pour 64 bits à l’aide de l’attribut **PtrSafe** .</span><span class="sxs-lookup"><span data-stu-id="3e696-154">Existing **Declare** statements won't compile in 64-bit VBA until they've been marked as safe for 64-bit by using the **PtrSafe** attribute.</span></span> <span data-ttu-id="3e696-155">Vous trouverez des exemples de ce type de conversion sur le site Web de Pieterse Excel MVP Jan Karel à [https://www.jkp-ads.com/articles/apideclarations.asp](https://www.jkp-ads.com/articles/apideclarations.asp).</span><span class="sxs-lookup"><span data-stu-id="3e696-155">You can find examples of this type of conversion at Excel MVP Jan Karel Pieterse's website at [https://www.jkp-ads.com/articles/apideclarations.asp](https://www.jkp-ads.com/articles/apideclarations.asp).</span></span> <span data-ttu-id="3e696-156">Le [guide de l’utilisateur Office Code Compatibility Inspector](https://technet.microsoft.com/en-us/library/ee833946%28office.14%29.aspx) est un outil utile pour inspecter la syntaxe des instructions d’API **Declare** pour l’attribut **PtrSafe** , le cas échéant, et le type de retour.</span><span class="sxs-lookup"><span data-stu-id="3e696-156">The [Office Code Compatibility Inspector user's guide](https://technet.microsoft.com/en-us/library/ee833946%28office.14%29.aspx) is a useful tool to inspect the syntax of API **Declare** statements for the **PtrSafe** attribute, if needed, and the appropriate return type.</span></span> 
  
<span data-ttu-id="3e696-157">Les instructions **Declare** ressembler à un des éléments suivants, selon que vous l’appelez une sous-routine (qui ne renvoie aucune valeur) ou une fonction (qui a une valeur de retour).</span><span class="sxs-lookup"><span data-stu-id="3e696-157">**Declare** statements resemble one of the following, depending on whether you are calling a subroutine (which has no return value) or a function (which does have a return value).</span></span> 
  
```vb
Public/Private Declare Sub SubName Lib "LibName" Alias "AliasName" (argument list)
Public/Private Declare Function FunctionName Lib "Libname" alias "aliasname" (argument list) As Type

```

<span data-ttu-id="3e696-158">La fonction **nomsub** ou **suivantes** est remplacée par le nom réel de la procédure dans le fichier DLL et représente le nom qui est utilisé lorsque la procédure est appelée à partir du code VBA.</span><span class="sxs-lookup"><span data-stu-id="3e696-158">The **SubName** function or **FunctionName** function is replaced by the actual name of the procedure in the DLL file and represents the name that is used when the procedure is called from VBA code.</span></span> <span data-ttu-id="3e696-159">Vous pouvez également spécifier un argument **AliasName** pour le nom de la procédure.</span><span class="sxs-lookup"><span data-stu-id="3e696-159">You can also specify an **AliasName** argument for the name of the procedure.</span></span> <span data-ttu-id="3e696-160">Le nom du fichier DLL qui contient la procédure appelée suit le mot clé **Lib** .</span><span class="sxs-lookup"><span data-stu-id="3e696-160">The name of the DLL file that contains the procedure being called follows the **Lib** keyword.</span></span> <span data-ttu-id="3e696-161">Et enfin, la liste d’arguments contient les paramètres et les types de données qui doivent être transmis à la procédure.</span><span class="sxs-lookup"><span data-stu-id="3e696-161">And finally, the argument list contains the parameters and the data types that must be passed to the procedure.</span></span> 
  
<span data-ttu-id="3e696-162">L’instruction **Declare** suivante ouvre une *sous-clé* dans le Registre Windows et remplace sa valeur.</span><span class="sxs-lookup"><span data-stu-id="3e696-162">The following **Declare** statement opens a  *subkey*  in the Windows registry and replaces its value.</span></span> 
  
```vb
Declare Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As Long, ByVal SubKey As String, NewKey As Long) As Long
```

<span data-ttu-id="3e696-163">L’entrée Windows.h (handle de fenêtre) pour la fonction **RegOpenKeyA** est la suivante :</span><span class="sxs-lookup"><span data-stu-id="3e696-163">The Windows.h (window handle) entry for the **RegOpenKeyA** function is as follows:</span></span> 
  
```vb
LONG RegOpenKeyA ( HKEY hKey, LPCSTR lpSubKey, HKEY *phkResult );
```

<span data-ttu-id="3e696-164">Dans Visual C# et Microsoft Visual C++, l’exemple précédent se compile correctement pour 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3e696-164">In Visual C and Microsoft Visual C++, the previous example compiles correctly for both 32-bit and 64-bit.</span></span> <span data-ttu-id="3e696-165">Il s’agit comme HKEY est définie comme un pointeur dont la taille reflète la taille de la mémoire de la plateforme de compilation dans le code.</span><span class="sxs-lookup"><span data-stu-id="3e696-165">This is because HKEY is defined as a pointer, whose size reflects the memory size of the platform that the code is compiled in.</span></span>
  
<span data-ttu-id="3e696-166">Dans les versions précédentes de VBA, il a été aucun type de données pointeur spécifique afin que le type de données **Long** a été utilisé.</span><span class="sxs-lookup"><span data-stu-id="3e696-166">In previous versions of VBA, there was no specific pointer data type so the **Long** data type was used.</span></span> <span data-ttu-id="3e696-167">Et parce que le type de données **Long** est toujours 32 bits, cette sauts lorsqu’elle est utilisée sur un système 64 bits, car les supérieures 32 bits risquent d’être tronqués ou peuvent remplacer les autres adresses de mémoire.</span><span class="sxs-lookup"><span data-stu-id="3e696-167">And because the **Long** data type is always 32-bits, this breaks when used on a system with 64-bit memory because the upper 32-bits might be truncated or might overwrite other memory addresses.</span></span> <span data-ttu-id="3e696-168">Une de ces situations peut entraîner des incidents système ou de comportement imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="3e696-168">Either of these situations can result in unpredictable behavior or system crashes.</span></span> 
  
<span data-ttu-id="3e696-169">Pour résoudre ce problème, VBA inclut un type de données de la valeur true *pointeur* : **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="3e696-169">To resolve this, VBA includes a true  *pointer*  data type: **LongPtr**.</span></span> <span data-ttu-id="3e696-170">Ce nouveau type de données vous permet d’écrire l’instruction **Declare** d’origine correctement en tant que :</span><span class="sxs-lookup"><span data-stu-id="3e696-170">This new data type enables you to write the original **Declare** statement correctly as:</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapire32.dll" (ByVal hKey as LongPtr, ByVal lpSubKey As String, phkResult As LongPtr) As Long
```

<span data-ttu-id="3e696-171">Ce type de données et le nouvel attribut **PtrSafe** permettent d’utiliser cette instruction **Declare** sur les systèmes 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3e696-171">This data type and the new **PtrSafe** attribute enable you to use this **Declare** statement on either 32-bit or 64-bit systems.</span></span> <span data-ttu-id="3e696-172">L’attribut **PtrSafe** indique au compilateur VBA que l’instruction **Declare** est ciblée pour la version 64 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="3e696-172">The **PtrSafe** attribute indicates to the VBA compiler that the **Declare** statement is targeted for the 64-bit version of Office.</span></span> <span data-ttu-id="3e696-173">Sans cet attribut, à l’aide de l’instruction **Declare** dans un système 64 bits provoquera une erreur de compilation.</span><span class="sxs-lookup"><span data-stu-id="3e696-173">Without this attribute, using the **Declare** statement in a 64-bit system will result in a compile-time error.</span></span> <span data-ttu-id="3e696-174">L’attribut **PtrSafe** est facultatif pour la version 32 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="3e696-174">The **PtrSafe** attribute is optional on the 32-bit version of Office.</span></span> <span data-ttu-id="3e696-175">Ainsi, les instructions **Declare** existantes à fonctionner comme ils ont toujours.</span><span class="sxs-lookup"><span data-stu-id="3e696-175">This enables existing **Declare** statements to work as they always have.</span></span> 
  
<span data-ttu-id="3e696-176">Le tableau suivant fournit plus d’informations sur le nouveau qualificateur et typeas de données ainsi que d’un autre type de données, deux opérateurs de conversion et trois fonctions.</span><span class="sxs-lookup"><span data-stu-id="3e696-176">The following table provides more information about the new qualifier and data typeas well as another data type, two conversion operators, and three functions.</span></span>
  
|<span data-ttu-id="3e696-177">Type</span><span class="sxs-lookup"><span data-stu-id="3e696-177">Type</span></span>|<span data-ttu-id="3e696-178">Élément</span><span class="sxs-lookup"><span data-stu-id="3e696-178">Item</span></span>|<span data-ttu-id="3e696-179">Description</span><span class="sxs-lookup"><span data-stu-id="3e696-179">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3e696-180">Qualificateur</span><span class="sxs-lookup"><span data-stu-id="3e696-180">Qualifier</span></span>  <br/> |<span data-ttu-id="3e696-181">**PtrSafe**</span><span class="sxs-lookup"><span data-stu-id="3e696-181">**PtrSafe**</span></span> <br/> |<span data-ttu-id="3e696-p119">Indique que l’instruction **Declare** est compatible 64 bits. Cet attribut est obligatoire sur les systèmes 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3e696-p119">Indicates that the **Declare** statement is compatible with 64-bits. This attribute is mandatory on 64-bit systems.  </span></span><br/> |
|<span data-ttu-id="3e696-184">Type de données</span><span class="sxs-lookup"><span data-stu-id="3e696-184">Data Type</span></span>  <br/> |<span data-ttu-id="3e696-185">**LongPtr**</span><span class="sxs-lookup"><span data-stu-id="3e696-185">**LongPtr**</span></span> <br/> |<span data-ttu-id="3e696-186">Un type de données de la variable qui est un type de données de 4 octets sur les versions 32 bits et un type de données de 8 octets sur les versions 64 bits de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="3e696-186">A variable data type which is a 4-bytes data type on 32-bit versions and an 8-byte data type on 64-bit versions of Microsoft Office.</span></span> <span data-ttu-id="3e696-187">Il est recommandé de déclarer un pointeur ou un handle pour le nouveau code mais aussi pour code hérité si elle doit s’exécuter dans la version 64 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="3e696-187">This is the recommended way of declaring a pointer or a handle for new code but also for legacy code if it has to run in the 64-bit version of Office.</span></span> <span data-ttu-id="3e696-188">Il est uniquement pris en charge dans le runtime VBA 7 sur 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3e696-188">It is only supported in the VBA 7 runtime on 32-bit and 64-bit.</span></span> <span data-ttu-id="3e696-189">Notez que vous pouvez affecter des valeurs numériques à il mais types numériques pas.</span><span class="sxs-lookup"><span data-stu-id="3e696-189">Note that you can assign numeric values to it but not numeric types.</span></span>  <br/> |
|<span data-ttu-id="3e696-190">Type de données</span><span class="sxs-lookup"><span data-stu-id="3e696-190">Data Type</span></span>  <br/> |<span data-ttu-id="3e696-191">**LongLong**</span><span class="sxs-lookup"><span data-stu-id="3e696-191">**LongLong**</span></span> <br/> |<span data-ttu-id="3e696-192">Il s’agit d’un type de données de 8 octets qui est disponible uniquement dans les versions 64 bits de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="3e696-192">This is an 8-byte data type which is available only in 64-bit versions of Microsoft Office.</span></span> <span data-ttu-id="3e696-193">Vous pouvez affecter des valeurs numériques, mais des types non numériques (pour éviter la troncation).</span><span class="sxs-lookup"><span data-stu-id="3e696-193">You can assign numeric values but not numeric types (to avoid truncation).</span></span>  <br/> |
|<span data-ttu-id="3e696-194">Opérateur de conversion</span><span class="sxs-lookup"><span data-stu-id="3e696-194">Conversion Operator</span></span>  <br/> |<span data-ttu-id="3e696-195">**CLngPtr**</span><span class="sxs-lookup"><span data-stu-id="3e696-195">**CLngPtr**</span></span> <br/> |<span data-ttu-id="3e696-196">Convertit une expression simple en un type de données **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="3e696-196">Converts a simple expression to a **LongPtr** data type.</span></span>  <br/> |
|<span data-ttu-id="3e696-197">Opérateur de conversion</span><span class="sxs-lookup"><span data-stu-id="3e696-197">Conversion Operator</span></span>  <br/> |<span data-ttu-id="3e696-198">**CLngLng**</span><span class="sxs-lookup"><span data-stu-id="3e696-198">**CLngLng**</span></span> <br/> |<span data-ttu-id="3e696-199">Convertit une expression simple en un type de données **LongLong**.</span><span class="sxs-lookup"><span data-stu-id="3e696-199">Converts a simple expression to a **LongLong** data type.</span></span>  <br/> |
|<span data-ttu-id="3e696-200">Fonction</span><span class="sxs-lookup"><span data-stu-id="3e696-200">Function</span></span>  <br/> |<span data-ttu-id="3e696-201">**VarPtr**</span><span class="sxs-lookup"><span data-stu-id="3e696-201">**VarPtr**</span></span> <br/> |<span data-ttu-id="3e696-p122">Convertisseur de variant. Retourne un **LongPtr** sur les versions 64 bits et un **Long** sur les versions 32 bits (4 octets).</span><span class="sxs-lookup"><span data-stu-id="3e696-p122">Variant converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
|<span data-ttu-id="3e696-204">Fonction</span><span class="sxs-lookup"><span data-stu-id="3e696-204">Function</span></span>  <br/> |<span data-ttu-id="3e696-205">**ObjPtr**</span><span class="sxs-lookup"><span data-stu-id="3e696-205">**ObjPtr**</span></span> <br/> |<span data-ttu-id="3e696-p123">Convertisseur d’objet. Retourne un **LongPtr** sur les versions 64 bits et un **Long** sur les versions 32 bits (4 octets).</span><span class="sxs-lookup"><span data-stu-id="3e696-p123">Object converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
|<span data-ttu-id="3e696-208">Fonction</span><span class="sxs-lookup"><span data-stu-id="3e696-208">Function</span></span>  <br/> |<span data-ttu-id="3e696-209">**StrPtr**</span><span class="sxs-lookup"><span data-stu-id="3e696-209">**StrPtr**</span></span> <br/> |<span data-ttu-id="3e696-p124">Convertisseur de chaîne. Retourne un **LongPtr** sur les versions 64 bits et un **Long** sur les versions 32 bits (4 octets).</span><span class="sxs-lookup"><span data-stu-id="3e696-p124">String converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
   
<span data-ttu-id="3e696-212">L’exemple suivant montre comment utiliser certains de ces éléments dans une instruction **Declare**.</span><span class="sxs-lookup"><span data-stu-id="3e696-212">The follow example shows how to use some of these items in a **Declare** statement.</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As LongPtr, ByVal SubKey As String, NewKey As LongPtr) As Long
```

<span data-ttu-id="3e696-213">Notez que les instructions **Declare** sans attribut **PtrSafe** sont considérées comme non compatibles avec la version 64 bits d’Office.</span><span class="sxs-lookup"><span data-stu-id="3e696-213">Note that **Declare** statements without the **PtrSafe** attribute are assumed not to be compatible with the 64-bit version of Office.</span></span> 
  
<span data-ttu-id="3e696-214">Il existe deux constantes de compilation conditionnelle : **VBA7** et **Win64**.</span><span class="sxs-lookup"><span data-stu-id="3e696-214">There are two conditional compilation constants: **VBA7** and **Win64**.</span></span> <span data-ttu-id="3e696-215">Pour garantir la compatibilité descendante avec les versions précédentes de Microsoft Office, vous utilisez la constante **VBA7** (c’est le cas plus courant) pour empêcher l’utilisation de la version antérieure d’Office 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3e696-215">To ensure backward compatibility with previous versions of Microsoft Office, you use the **VBA7** constant (this is the more typical case) to prevent 64-bit code from being used in the earlier version of Office.</span></span> <span data-ttu-id="3e696-216">Pour le code qui est différente de la version 32 bits et la version 64 bits, telles que l’appel mathématique **Long** et les API qui utilise **LongLong** pour la version 64 bits pour la version 32 bits, vous utilisez la constante **Win64** .</span><span class="sxs-lookup"><span data-stu-id="3e696-216">For code that is different between the 32-bit version and the 64-bit version, such as calling a math API that uses **LongLong** for its 64-bit version and **Long** for its 32-bit version, you use the **Win64** constant.</span></span> <span data-ttu-id="3e696-217">Le code suivant illustre l’utilisation de ces deux constantes.</span><span class="sxs-lookup"><span data-stu-id="3e696-217">The following code shows the use of these two constants.</span></span> 
  
```vb
#if Win64 then
   Declare PtrSafe Function MyMathFunc Lib "User32" (ByVal N As LongLong) As LongLong
#else
   Declare Function MyMathFunc Lib "User32" (ByVal N As Long) As Long
#end if
#if VBA7 then
   Declare PtrSafe Sub MessageBeep Lib "User32" (ByVal N AS Long)
#else
   Declare Sub MessageBeep Lib "User32" (ByVal N AS Long)
#end if
```

<span data-ttu-id="3e696-218">Pour résumer, si vous écrivez du code 64 bits et envisagez d’utiliser dans les versions précédentes d’Office, vous devez utiliser la constante de compilation conditionnelle **VBA7** .</span><span class="sxs-lookup"><span data-stu-id="3e696-218">To summarize, if you write 64-bit code and intend to use it in previous versions of Office, you will want to use the **VBA7** conditional compilation constant.</span></span> <span data-ttu-id="3e696-219">Toutefois, si vous écrivez du code 32 bits dans Office, que ce code fonctionne comme dans les versions antérieures d’Office sans devoir pour la constante de compilation.</span><span class="sxs-lookup"><span data-stu-id="3e696-219">However, if you write 32-bit code in Office, that code works as is in previous versions of Office without the need for the compilation constant.</span></span> <span data-ttu-id="3e696-220">Si vous voulez vous assurer que vous utilisez les instructions 32 bits pour les versions 32 bits et 64 bits les instructions pour les versions 64 bits, la meilleure solution consiste à utiliser la constante de compilation conditionnelle **Win64** .</span><span class="sxs-lookup"><span data-stu-id="3e696-220">If you want to ensure that you are using 32-bit statements for 32-bit versions and 64-bit statements for 64-bit versions, your best option is to use the **Win64** conditional compilation constant.</span></span> 
  
## <a name="using-conditional-compilation-attributes"></a><span data-ttu-id="3e696-221">Utilisation d’attributs de compilation conditionnelle</span><span class="sxs-lookup"><span data-stu-id="3e696-221">Using conditional compilation attributes</span></span>
<span data-ttu-id="3e696-222"><a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a></span><span class="sxs-lookup"><span data-stu-id="3e696-222"></span></span>

<span data-ttu-id="3e696-223">L’exemple suivant montre le code VBA écrit pour 32 bits qui doit être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="3e696-223">The following example shows VBA code written for 32-bit that needs to be updated.</span></span> <span data-ttu-id="3e696-224">Notez les types de données dans le code hérité qui sont mis à jour pour utiliser **LongPtr** , car elles référencent handles ou pointeurs.</span><span class="sxs-lookup"><span data-stu-id="3e696-224">Notice the data types in the legacy code that are updated to use **LongPtr** because they refer to handles or pointers.</span></span> 
  
### <a name="vba-code-written-for-32-bit-versions"></a><span data-ttu-id="3e696-225">Code VBA écrit pour les versions 32 bits</span><span class="sxs-lookup"><span data-stu-id="3e696-225">VBA code written for 32-bit versions</span></span>
  
```vb
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
  
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
```

### <a name="vba-code-rewritten-for-64-bit-versions"></a><span data-ttu-id="3e696-226">Réécrit pour les versions 64 bits du code VBA</span><span class="sxs-lookup"><span data-stu-id="3e696-226">VBA code rewritten for 64-bit versions</span></span>
  
```vb
#if VBA7 then    ' VBA7 
Declare PtrSafe Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As LongPtr
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As LongPtr
  lParam As LongPtr
  iImage As Long
End Type
 
#else    ' Downlevel when using previous version of VBA7
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
 
#end if
Sub TestSHBrowseForFolder ()
    Dim bInfo As BROWSEINFO
    Dim pidList As Long
    bInfo.pidlRoot = 0&amp;
    bInfo.ulFlags = &amp;H1
    pidList = SHBrowseForFolder(bInfo)
End Sub
```

<span data-ttu-id="3e696-227"><a name="odc_office_Compatibility32bit64bit_FrequentlyAskedQuestions"> </a></span><span class="sxs-lookup"><span data-stu-id="3e696-227"></span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="3e696-228">Questions fréquemment posées</span><span class="sxs-lookup"><span data-stu-id="3e696-228">Frequently asked questions</span></span>

#### <a name="when-should-i-use-the-64-bit-version-of-office"></a><span data-ttu-id="3e696-229">Quand dois-je utiliser la version 64 bits d’Office ?</span><span class="sxs-lookup"><span data-stu-id="3e696-229">When should I use the 64-bit version of Office?</span></span>
  
<span data-ttu-id="3e696-230">Il s’agit plus une question de l’application hôte (Excel, Word, etc.) que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="3e696-230">This is more a matter of which host application (Excel, Word, and so forth) you are using.</span></span> <span data-ttu-id="3e696-231">Par exemple, Excel est en mesure de gérer la plus grande quantité feuilles de calcul avec la version 64 bits de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="3e696-231">For example, Excel is able to handle much larger worksheets with the 64-bit version of Microsoft Office.</span></span>
  
#### <a name="can-i-install-64-bit-and-32-bit-versions-of-office-side-by-side"></a><span data-ttu-id="3e696-232">Puis-je installer les versions 32 bits et 64 bits d’Office côte à côte ?</span><span class="sxs-lookup"><span data-stu-id="3e696-232">Can I install 64-bit and 32-bit versions of Office side-by-side?</span></span>
  
<span data-ttu-id="3e696-233">Non.</span><span class="sxs-lookup"><span data-stu-id="3e696-233">No.</span></span>
  
#### <a name="when-should-i-convert-long-parameters-to-longptr"></a><span data-ttu-id="3e696-234">Quand dois-je convertir paramètres longs à LongPtr ?</span><span class="sxs-lookup"><span data-stu-id="3e696-234">When should I convert Long parameters to LongPtr?</span></span>
  
<span data-ttu-id="3e696-235">Vous devez consulter la documentation de l’API Windows sur le réseau de développeurs Microsoft pour la fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="3e696-235">You need to check the Windows API documentation on the Microsoft Developers Network for the function you want to call.</span></span> <span data-ttu-id="3e696-236">Les poignées et pointeurs doivent être convertie en **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="3e696-236">Handles and pointers need to be converted to **LongPtr**.</span></span> <span data-ttu-id="3e696-237">Par exemple, la documentation pour [RegOpenKeyA](https://msdn.microsoft.com/library/c8a590f2-3249-437f-a320-c7443d42b792.aspx) fournit la signature suivante :</span><span class="sxs-lookup"><span data-stu-id="3e696-237">As an example, the documentation for [RegOpenKeyA](https://msdn.microsoft.com/library/c8a590f2-3249-437f-a320-c7443d42b792.aspx) provides the following signature:</span></span> 
  
```cs
LONG WINAPI RegOpenKeyEx(
  __in        HKEY hKey,
  __in_opt    LPCTSTR lpSubKey,
  __reserved  DWORD ulOptions,
  __in        REGSAM samDesired,
  __out       PHKEY phkResult
);
```

<span data-ttu-id="3e696-238">Les paramètres sont définis en tant que :</span><span class="sxs-lookup"><span data-stu-id="3e696-238">The parameters are defined as:</span></span>
  
|<span data-ttu-id="3e696-239">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3e696-239">Parameter</span></span>|<span data-ttu-id="3e696-240">Description</span><span class="sxs-lookup"><span data-stu-id="3e696-240">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="3e696-241">hKey [in]</span><span class="sxs-lookup"><span data-stu-id="3e696-241">hKey [in]</span></span>  <br/> |<span data-ttu-id="3e696-242">Un *Gérer* une clé de Registre ouverte.</span><span class="sxs-lookup"><span data-stu-id="3e696-242">A  *handle*  to an open registry key.</span></span>  <br/> |
|<span data-ttu-id="3e696-243">lpSubKey [in, facultatif]</span><span class="sxs-lookup"><span data-stu-id="3e696-243">lpSubKey [in, optional]</span></span>  <br/> |<span data-ttu-id="3e696-244">Nom de la sous-clé de Registre à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="3e696-244">The name of the registry subkey to be opened.</span></span>  <br/> |
|<span data-ttu-id="3e696-245">ulOptions</span><span class="sxs-lookup"><span data-stu-id="3e696-245">ulOptions</span></span>  <br/> |<span data-ttu-id="3e696-246">Ce paramètre est réservé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="3e696-246">This parameter is reserved and must be zero.</span></span>  <br/> |
|<span data-ttu-id="3e696-247">samDesired [in]</span><span class="sxs-lookup"><span data-stu-id="3e696-247">samDesired [in]</span></span>  <br/> |<span data-ttu-id="3e696-248">Masque qui spécifie les droits d’accès souhaité pour la clé.</span><span class="sxs-lookup"><span data-stu-id="3e696-248">A mask that specifies the desired access rights to the key.</span></span>  <br/> |
|<span data-ttu-id="3e696-249">phkResult [out]</span><span class="sxs-lookup"><span data-stu-id="3e696-249">phkResult [out]</span></span>  <br/> |<span data-ttu-id="3e696-250">*Pointeur* vers une variable qui reçoit un handle vers la clé ouvert.</span><span class="sxs-lookup"><span data-stu-id="3e696-250">A  *pointer*  to a variable that receives a handle to the opened key.</span></span>  <br/> |
   
<span data-ttu-id="3e696-251">Dans [Win32API_PtrSafe.txt](https://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=035b72a5-eef9-4baf-8dbc-63fbd2dd982b), l’instruction **Declare** est définie en tant que :</span><span class="sxs-lookup"><span data-stu-id="3e696-251">In [Win32API_PtrSafe.txt](https://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=035b72a5-eef9-4baf-8dbc-63fbd2dd982b), the **Declare** statement is defined as:</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyEx Lib "advapi32.dll" Alias "RegOpenKeyExA" (ByVal hKey As LongPtr , ByVal lpSubKey As String, ByVal ulOptions As Long, ByVal samDesired As Long, phkResult As LongPtr ) As Long
```

#### <a name="should-i-convert-pointers-and-handles-in-structures"></a><span data-ttu-id="3e696-252">Dois-je convertir des pointeurs et poignées de structures ?</span><span class="sxs-lookup"><span data-stu-id="3e696-252">Should I convert pointers and handles in structures?</span></span>
  
<span data-ttu-id="3e696-253">Oui.</span><span class="sxs-lookup"><span data-stu-id="3e696-253">Yes.</span></span> <span data-ttu-id="3e696-254">Consultez le type de **message** dans Win32API_PtrSafe.txt :</span><span class="sxs-lookup"><span data-stu-id="3e696-254">See the **MSG** type in Win32API_PtrSafe.txt:</span></span> 
  
```vb
Type MSG
    hwnd As LongPtr 
    message As Long
    wParam As LongPtr 
    lParam As LongPtr 
    time As Long
    pt As POINTAPI
End TypeF
```

#### <a name="when-should-i-use-strptr-varpt-and-objptr"></a><span data-ttu-id="3e696-255">Quand dois-je utiliser strptr et objptr varpt ?</span><span class="sxs-lookup"><span data-stu-id="3e696-255">When should I use strptr, varpt, and objptr?</span></span>
  
<span data-ttu-id="3e696-256">Vous devez utiliser ces fonctions pour récupérer des pointeurs vers des chaînes, des variables et des objets, respectivement.</span><span class="sxs-lookup"><span data-stu-id="3e696-256">You should use these functions to retrieve pointers to strings, variables and objects, respectively.</span></span> <span data-ttu-id="3e696-257">Sur la version 64 bits d’Office, ces fonctions renvoient 64-bit **LongPtr**, qui peut être passé aux instructions **Declare** .</span><span class="sxs-lookup"><span data-stu-id="3e696-257">On the 64-bit version of Office, these functions will return a 64-bit **LongPtr**, which can be passed to **Declare** statements.</span></span> <span data-ttu-id="3e696-258">L’utilisation de ces fonctions n’a pas été modifié à partir de versions antérieures de VBA.</span><span class="sxs-lookup"><span data-stu-id="3e696-258">The use of these functions has not changed from previous versions of VBA.</span></span> <span data-ttu-id="3e696-259">La seule différence est qu’elles retournent maintenant **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="3e696-259">The only difference is that they now return a **LongPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3e696-260">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e696-260">See also</span></span>
<span data-ttu-id="3e696-261"><a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a></span><span class="sxs-lookup"><span data-stu-id="3e696-261"></span></span>

- [<span data-ttu-id="3e696-262">Anatomie d’une instruction Declare</span><span class="sxs-lookup"><span data-stu-id="3e696-262">Anatomy of a Declare Statement</span></span>](https://msdn.microsoft.com/library/office/aa671659.aspx)
    

