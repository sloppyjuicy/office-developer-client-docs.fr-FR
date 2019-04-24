---
title: Utilisation d'ADO avec Microsoft Visual Basic
TOCTitle: Using ADO with Microsoft Visual Basic
ms:assetid: 5e0fb2ec-42aa-e181-386f-099607ac7400
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249338(v=office.15)
ms:contentKeyID: 48545130
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 26eaa93a1abbb3778a2735d50dd5022edb3023d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306222"
---
# <a name="using-ado-with-microsoft-visual-basic"></a><span data-ttu-id="9cc28-102">Utilisation d’ADO avec Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9cc28-102">Using ADO with Microsoft Visual Basic</span></span>

<span data-ttu-id="9cc28-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9cc28-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9cc28-p101">Configurer un projet ADO et écrire du code ADO sont des tâches similaires que vous utilisiez Visual Basic ou Visual Basic pour Applications. Cette rubrique explique comment utiliser ADO avec Visual Basic et Visual Basic pour Applications en relevant les différences qui existent selon le programme utilisé.</span><span class="sxs-lookup"><span data-stu-id="9cc28-p101">Setting up an ADO project and writing ADO code is similar whether you use Visual Basic or Visual Basic for Applications. This topic addresses using ADO with both Visual Basic and Visual Basic for Applications and notes any differences.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="9cc28-106">Référencement de la bibliothèque ADO</span><span class="sxs-lookup"><span data-stu-id="9cc28-106">Referencing the ADO library</span></span>

<span data-ttu-id="9cc28-107">La bibliothèque ADO doit être référencée par votre projet.</span><span class="sxs-lookup"><span data-stu-id="9cc28-107">The ADO library must be referenced by your project.</span></span>

### <a name="to-reference-ado-from-microsoft-visual-basic"></a><span data-ttu-id="9cc28-108">Pour référencer la bibliothèque ADO à partir de Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9cc28-108">To reference ADO from Microsoft Visual Basic</span></span>

1. <span data-ttu-id="9cc28-109">Dans le menu **Projet** de Visual Basic, sélectionnez **Références...**.</span><span class="sxs-lookup"><span data-stu-id="9cc28-109">In Visual Basic, from the **Project** menu, select **References...**.</span></span>

2. <span data-ttu-id="9cc28-p102">Sélectionnez **Bibliothèque Microsoft ActiveX Data Objects x.x** dans la liste. Vérifiez que les bibliothèques suivantes sont au moins sélectionnées :</span><span class="sxs-lookup"><span data-stu-id="9cc28-p102">Select **Microsoft ActiveX Data Objects x.x Library** from the list. Verify that at least the following libraries are also selected:</span></span>
   
   - <span data-ttu-id="9cc28-112">Visual Basic pour Applications</span><span class="sxs-lookup"><span data-stu-id="9cc28-112">Visual Basic for Applications</span></span>
   - <span data-ttu-id="9cc28-113">Objets et procédures d'exécution Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9cc28-113">Visual Basic runtime objects and procedures</span></span>
   - <span data-ttu-id="9cc28-114">Objets et procédures Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9cc28-114">Visual Basic objects and procedures</span></span>
   - <span data-ttu-id="9cc28-115">OLE Automation</span><span class="sxs-lookup"><span data-stu-id="9cc28-115">OLE Automation</span></span>

3. <span data-ttu-id="9cc28-116">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="9cc28-116">Click **OK**.</span></span>

<span data-ttu-id="9cc28-117">ADO s'utilise aussi facilement avec Visual Basic pour Applications, via Microsoft Access par exemple.</span><span class="sxs-lookup"><span data-stu-id="9cc28-117">You can use ADO just as easily with Visual Basic for Applications, using Microsoft Access, for example.</span></span>

### <a name="to-reference-ado-from-microsoft-access"></a><span data-ttu-id="9cc28-118">Pour référencer ADO à partir de Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="9cc28-118">To reference ADO from Microsoft Access</span></span>

1. <span data-ttu-id="9cc28-119">Dans Microsoft Access, sélectionnez ou créez un module dans l'onglet **Modules** de la fenêtre **Base de données**.</span><span class="sxs-lookup"><span data-stu-id="9cc28-119">In Microsoft Access, select or create a module from the **Modules** tab in the **Database** window.</span></span>

2. <span data-ttu-id="9cc28-120">Dans le menu **Outils**, cliquez sur **Références...**.</span><span class="sxs-lookup"><span data-stu-id="9cc28-120">From the **Tools** menu, select **References...**.</span></span>

3. <span data-ttu-id="9cc28-p103">Sélectionnez **Bibliothèque Microsoft ActiveX Data Objects x.x** dans la liste. Vérifiez que les bibliothèques suivantes sont au moins sélectionnées :</span><span class="sxs-lookup"><span data-stu-id="9cc28-p103">Select **Microsoft ActiveX Data Objects x.x Library** from the list. Verify that at least the following libraries are also selected:</span></span>
    
   - <span data-ttu-id="9cc28-123">Visual Basic pour Applications</span><span class="sxs-lookup"><span data-stu-id="9cc28-123">Visual Basic for Applications</span></span>
   - <span data-ttu-id="9cc28-124">Bibliothèque d'objets Microsoft Access 11.0 (ou version ultérieure)</span><span class="sxs-lookup"><span data-stu-id="9cc28-124">Microsoft Access 11.0 Object Library (or later)</span></span>

4. <span data-ttu-id="9cc28-125">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="9cc28-125">Click **OK**.</span></span>

## <a name="creating-ado-objects-in-visual-basic"></a><span data-ttu-id="9cc28-126">Création d'objets ADO dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9cc28-126">Creating ADO objects in Visual Basic</span></span>

<span data-ttu-id="9cc28-127">Pour créer une variable Automation et une instance d'un objet pour cette variable, vous pouvez faire appel aux méthodes **Dim** ou **CreateObject**.</span><span class="sxs-lookup"><span data-stu-id="9cc28-127">To create an automation variable and an instance of an object for that variable, you can use two methods: **Dim** or **CreateObject**.</span></span>

### <a name="dim"></a><span data-ttu-id="9cc28-128">Dim</span><span class="sxs-lookup"><span data-stu-id="9cc28-128">Dim</span></span>

<span data-ttu-id="9cc28-129">Vous pouvez utiliser le mot-clé **New** avec la méthode **Dim** pour déclarer et instancier des objets ADO en une seule étape :</span><span class="sxs-lookup"><span data-stu-id="9cc28-129">You can use the **New** keyword with **Dim** to declare and instantiate ADO objects in one step:</span></span>

```vb 
 
Dim conn As New ADODB.Connection 
```

<span data-ttu-id="9cc28-130">Alternately, the **Dim** statement declaration and object instantiation can also be two steps:</span><span class="sxs-lookup"><span data-stu-id="9cc28-130">Alternately, the **Dim** statement declaration and object instantiation can also be two steps:</span></span>

```vb 
 
Dim conn As ADODB.Connection 
Set conn = New ADODB.Connection 
```

> [!NOTE]
> <span data-ttu-id="9cc28-131">Il n'est pas nécessaire d'utiliser explicitement le ProgID ADODB avec l'instruction **Dim** , en supposant que vous avez correctement référencé la bibliothèque ADO dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="9cc28-131">It is not required to explicitly use the ADODB progid with the **Dim** statement, assuming you have properly referenced the ADO library in your project.</span></span> <span data-ttu-id="9cc28-132">Toutefois, son utilisation garantit l'absence de conflits de noms avec d'autres bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="9cc28-132">However, using it ensures that you won't have naming conflicts with other libraries.</span></span>
> 
> <span data-ttu-id="9cc28-133">Par exemple, si vous référencez à des objets ADO et DAO dans le même projet, vous devez inclure un qualificatif afin de spécifier quel modèle objet utiliser lors de l'instanciation d'objets **Recordset** comme dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="9cc28-133">For example, if you include references to both ADO and DAO in the same project, you should include a qualifier to specify which object model to use when instantiating **Recordset** objects, as in the following code:</span></span>  
> 
> `Dim adoRS As ADODB.Recordset`  
>   
> `Dim daoRS As DAO.Recordset`

### <a name="createobject"></a><span data-ttu-id="9cc28-134">CreateObject</span><span class="sxs-lookup"><span data-stu-id="9cc28-134">CreateObject</span></span>

<span data-ttu-id="9cc28-135">Avec la méthode **CreateObject**, la déclaration et l'instanciation d'objet doit se faire en deux étapes discrètes :</span><span class="sxs-lookup"><span data-stu-id="9cc28-135">With the **CreateObject** method, the declaration and object instantiation must be two discrete steps:</span></span>

```vb 
 
Dim conn1 
Set conn1 = CreateObject("ADODB.Connection") As Object 
```

<span data-ttu-id="9cc28-p105">Les objets instanciés avec la méthode **CreateObject** sont à liaison tardive, ce qui signifie qu'ils ne sont pas fortement typés et leur exécution à partir de la ligne de commande est désactivée. Toutefois, cette méthode vous permet de ne pas référencer la bibliothèque ADO à partir de votre projet mais bien d'instancier des versions spécifiques des objets. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="9cc28-p105">Objects instantiated with **CreateObject** are late-bound, which means that they are not strongly typed and command-line completion is disabled. However, it does allow you to skip referencing the ADO library from your project, and enables you to instantiate specific versions of objects. For example:</span></span>

```vb 
 
Set conn1 = CreateObject("ADODB.Connection.2.0") As Object 
```

<span data-ttu-id="9cc28-139">Vous pouvez également exécuter cette opération en définissant une référence spécifique à la bibliothèque de types ADO version 2.0 et en créant l'objet.</span><span class="sxs-lookup"><span data-stu-id="9cc28-139">You could also accomplish this by specifically creating a reference to the ADO version 2.0 type library and creating the object.</span></span>

<span data-ttu-id="9cc28-140">L'instanciation d'objets à l'aide de la méthode **CreateObject** est généralement plus lente qu'avec la déclaration **Dim**.</span><span class="sxs-lookup"><span data-stu-id="9cc28-140">Instantiating objects with the **CreateObject** method is typically slower than using the **Dim** statement.</span></span>

## <a name="handling-events"></a><span data-ttu-id="9cc28-141">Gestion des événements</span><span class="sxs-lookup"><span data-stu-id="9cc28-141">Handling events</span></span>

<span data-ttu-id="9cc28-142">Pour gérer les événements ADO en Microsoft Visual Basic, vous devez déclarer une variable de niveau module à l'aide du mot clé **WithEvents** .</span><span class="sxs-lookup"><span data-stu-id="9cc28-142">To handle ADO events in Microsoft Visual Basic, you must declare a module-level variable using the **WithEvents** keyword.</span></span> <span data-ttu-id="9cc28-143">La variable ne peut être déclarée qu'au sein d'un module de classe et doit être déclarée au niveau du module.</span><span class="sxs-lookup"><span data-stu-id="9cc28-143">The variable can be declared only as part of a class module and must be declared at the module level.</span></span> <span data-ttu-id="9cc28-144">Pour plus d'informations sur la gestion des événements ADO, consultez le [chapitre 7: gestion des événements ADO](chapter-7-handling-ado-events.md).</span><span class="sxs-lookup"><span data-stu-id="9cc28-144">For a more complete discussion of handling ADO events, see [Chapter 7: Handling ADO events](chapter-7-handling-ado-events.md).</span></span>

## <a name="visual-basic-examples"></a><span data-ttu-id="9cc28-145">Exemples Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9cc28-145">Visual Basic examples</span></span>

<span data-ttu-id="9cc28-146">De nombreux exemples Visual Basic sont inclus dans la documentation ADO.</span><span class="sxs-lookup"><span data-stu-id="9cc28-146">Many Visual Basic examples are included with the ADO documentation.</span></span> <span data-ttu-id="9cc28-147">Pour plus d'informations, consultez la rubrique [exemples de code ADO en Microsoft Visual Basic](ado-code-examples-in-microsoft-visual-basic.md).</span><span class="sxs-lookup"><span data-stu-id="9cc28-147">For more information, see [ADO code examples in Microsoft Visual Basic](ado-code-examples-in-microsoft-visual-basic.md).</span></span>

