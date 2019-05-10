---
title: Manipuler le format de fichier Visio par programmation
manager: soliver
ms.date: 04/17/2019
ms.audience: Developer
ms.topic: overview
ms.assetid: 5f5e2288-7539-41b8-916d-410be028ed9b
description: Créez une solution dans Visual Studio 2012 pour lire le nouveau package de format de fichier dans Visio 2013, sélectionner des composants du package, modifier les données d’un composant et ajouter de nouveaux composants au package.
localization_priority: Priority
ms.openlocfilehash: 2b031a74fa8d2df9b9baa15e97652b8d8afdaf23
ms.sourcegitcommit: 6f3f42b656afb45a0189a0ad4c81c095e285b3d9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "33655610"
---
# <a name="manipulate-the-visio-file-format-programmatically"></a><span data-ttu-id="b8154-103">Manipuler le format de fichier Visio par programmation</span><span class="sxs-lookup"><span data-stu-id="b8154-103">Manipulate the Visio file format programmatically</span></span>

![Rubrique de procédure](media/mod_icon_howto.png)
  
<span data-ttu-id="b8154-105">Découvrez comment créer une solution dans Visual Studio 2012 pour lire le nouveau package de format de fichier dans Visio 2013, sélectionner des composants du package, modifier les données d’un composant et ajouter de nouveaux composants au package.</span><span class="sxs-lookup"><span data-stu-id="b8154-105">Learn how to create a solution in Visual Studio 2012 to read the new file format package in Visio 2013, select parts in the package, change the data in a part, and add new parts to the package.</span></span>
   
## <a name="visio-file-format-manipulation-essentials"></a><span data-ttu-id="b8154-106">Principes essentiels de manipulation du format de fichier Visio</span><span class="sxs-lookup"><span data-stu-id="b8154-106">Visio file format manipulation essentials</span></span>
<span data-ttu-id="b8154-107"><a name="vis15_ManipulateFF_Essentials"> </a></span><span class="sxs-lookup"><span data-stu-id="b8154-107"><a name="vis15_ManipulateFF_Essentials"> </a></span></span>

<span data-ttu-id="b8154-108">Les versions précédentes de Visio enregistraient les fichiers dans un format de fichier binaire propriétaire (.vsd) ou dans un format de fichier de dessin Visio XML (.vdx) de document unique.</span><span class="sxs-lookup"><span data-stu-id="b8154-108">Previous versions of Visio saved files in a proprietary binary file format (.vsd) or a single-document Visio XML Drawing file format (.vdx).</span></span> <span data-ttu-id="b8154-109">Visio 2013 propose un nouveau format de fichier (.vsdx) qui est basé sur les technologies d’archive XML et ZIP.</span><span class="sxs-lookup"><span data-stu-id="b8154-109">Visio 2013 introduces a new file format (.vsdx), which is based on XML and ZIP archive technologies.</span></span> <span data-ttu-id="b8154-110">Comme dans les versions précédentes de Visio, les fichiers sont enregistrés dans un seul conteneur.</span><span class="sxs-lookup"><span data-stu-id="b8154-110">Just as in previous versions of Visio, files are saved in a single container.</span></span> <span data-ttu-id="b8154-111">Toutefois, contrairement aux fichiers hérités, le nouveau format de fichier peut être ouvert, lu, mis à jour, modifié et créé sans automatiser l’application Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="b8154-111">Unlike legacy files, however, the new file format can be opened, read, updated, changed, and constructed without automating the Visio 2013 application.</span></span> <span data-ttu-id="b8154-112">Les développeurs qui sont habitués à manipuler le code XML ou l’espace de noms [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) peuvent rapidement commencer à utiliser le nouveau format de fichier par programmation.</span><span class="sxs-lookup"><span data-stu-id="b8154-112">Developers who are familiar with manipulating XML or working with the [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) namespace can quickly get started working with the new file format programmatically.</span></span> <span data-ttu-id="b8154-113">Les développeurs ayant travaillé avec le format de dessin Visio XML des versions précédentes s’apercevront que bon nombre des structures de ce format ont été conservées dans le nouveau format de fichier.</span><span class="sxs-lookup"><span data-stu-id="b8154-113">Developers who have worked with the Visio XML Drawing format from previous versions can find that many of the structures from that format have been retained in the new file format.</span></span> 
  
<span data-ttu-id="b8154-114">Dans cet article, nous expliquons comment utiliser le format de fichier Visio 2013 par programmation, à l’aide de Microsoft .NET Framework 4.5, C# ou Visual Basic et Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="b8154-114">In this article, we examine how to work with the Visio 2013 file format programmatically, using the Microsoft .NET Framework 4.5, C# or Visual Basic, and Visual Studio 2012.</span></span> <span data-ttu-id="b8154-115">Vous découvrirez comment ouvrir un fichier Visio 2013, sélectionner des composants de document dans ce fichier, modifier des données dans les composants et créer un composant de document.</span><span class="sxs-lookup"><span data-stu-id="b8154-115">You can see how to open a Visio 2013 file, select document parts within the file, change data in parts, and create a new document part.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b8154-116">Les exemples de code présentés dans cet article supposent que vous disposiez d’une connaissance rudimentaire des classes dans les espaces de noms [System.Xml.Linq](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) et [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx).</span><span class="sxs-lookup"><span data-stu-id="b8154-116">The code samples in this article assume that you have a rudimentary understanding of the classes in the [System.Xml.Linq](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) and [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) namespaces.</span></span> <span data-ttu-id="b8154-117">> Cet article repose également sur l’hypothèse selon laquelle vous comprenez les concepts et la terminologie des OPC (Open Packaging Conventions).</span><span class="sxs-lookup"><span data-stu-id="b8154-117">> This article also assumes that you understand the concepts and terminology of the Open Packaging Conventions.</span></span> <span data-ttu-id="b8154-118">Vous devez être familier avec les concepts de packages, les composants de document ou les composants de package et les relations.</span><span class="sxs-lookup"><span data-stu-id="b8154-118">You should have some familiarity with the concepts of packages, document parts or package parts, and relationships.</span></span> <span data-ttu-id="b8154-119">Pour plus d’informations, voir [OPC : une nouvelle norme pour les packages de données](https://msdn.microsoft.com/magazine/cc163372.aspx).</span><span class="sxs-lookup"><span data-stu-id="b8154-119">For more information, see [OPC: A New Standard for Packaging Your Data](https://msdn.microsoft.com/magazine/cc163372.aspx).</span></span> <span data-ttu-id="b8154-120">> Le code montre comment créer des requêtes LINQ (Language Integrated Query) pour sélectionner XML.</span><span class="sxs-lookup"><span data-stu-id="b8154-120">> The code demonstrates how to create LINQ (Language-Integrated Query) queries to select XML.</span></span> <span data-ttu-id="b8154-121">La plupart des exemples de code utilisent la syntaxe de la requête pour créer des requêtes LINQ.</span><span class="sxs-lookup"><span data-stu-id="b8154-121">Most of the code samples use the query syntax for building LINQ queries.</span></span> <span data-ttu-id="b8154-122">Vous pouvez réécrire n’importe quelle requête LINQ fournie dans le code à l’aide de la syntaxe de la méthode LINQ, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="b8154-122">You can rewrite any of the LINQ queries provided in the code by using the LINQ method syntax, if necessary.</span></span> <span data-ttu-id="b8154-123">Pour plus d’informations sur la syntaxe de la requête LINQ et la syntaxe de la méthode, voir [Comparaisons entre la syntaxe de la requête LINQ et la syntaxe de la méthode (C#)](https://msdn.microsoft.com/library/bb397947.aspx)> Le Tableau 1 indique les rubriques essentielles que vous devez connaître avant de parcourir cet article.</span><span class="sxs-lookup"><span data-stu-id="b8154-123">For more information about LINQ query syntax and method syntax, see [LINQ Query Syntax versus Method Syntax (C#)](https://msdn.microsoft.com/library/bb397947.aspx)> Table 1 shows the essential topics that you should be familiar with before you work through this article.</span></span> 
  
<span data-ttu-id="b8154-124">**Tableau 1. Principes de base pour la manipulation du format de fichier Visio 2013**</span><span class="sxs-lookup"><span data-stu-id="b8154-124">**Table 1. Core concepts for manipulating the Visio 2013 file format**</span></span>

|<span data-ttu-id="b8154-125">**Titre d’article**</span><span class="sxs-lookup"><span data-stu-id="b8154-125">**Article title**</span></span>|<span data-ttu-id="b8154-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="b8154-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8154-127">Présentation du format de fichier Visio (.vsdx)</span><span class="sxs-lookup"><span data-stu-id="b8154-127">Introduction to the Visio file format (.vsdx)</span></span>](introduction-to-the-visio-file-formatvsdx.md) <br/> |<span data-ttu-id="b8154-128">Cette vue d’ensemble de haut niveau décrit quelques-unes des principales fonctionnalités du format de fichier Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="b8154-128">This high-level overview describes some of the major features of the Visio 2013 file format.</span></span> <span data-ttu-id="b8154-129">Elle traite des OPC (Open Packaging Conventions) qui ont été appliqués au format de fichier Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="b8154-129">It discusses the Open Packaging Conventions (OPC) as they have been applied to the Visio 2013 file format.</span></span> <span data-ttu-id="b8154-130">Elle répertorie également quelques différences entre le format de fichier Visio 2013 et le format de fichier de dessin Visio XML précédent (.vdx).</span><span class="sxs-lookup"><span data-stu-id="b8154-130">It also lists some differences between the Visio 2013 file format and the previous Visio XML Drawing file format (.vdx).</span></span>  <br/> |
|[<span data-ttu-id="b8154-131">OPC : une nouvelle norme pour les packages de données</span><span class="sxs-lookup"><span data-stu-id="b8154-131">OPC: A New Standard for Packaging Your Data</span></span>](https://msdn.microsoft.com/magazine/cc163372.aspx) <br/> |<span data-ttu-id="b8154-132">Cet article de MSDN Magazine décrit les spécifications des normes Open Packaging Conventions sous forme de concept.</span><span class="sxs-lookup"><span data-stu-id="b8154-132">This MSDN Magazine article describes the Open Packaging Conventions as a concept.</span></span>  <br/> |
|[<span data-ttu-id="b8154-133">Éléments fondamentaux des OPC (Open Packaging Conventions)</span><span class="sxs-lookup"><span data-stu-id="b8154-133">Essentials of the Open Packaging Conventions</span></span>](https://msdn.microsoft.com/library/ee361919.aspx) <br/> [<span data-ttu-id="b8154-134">Présentation des formats de fichier Office (2007) Open XML</span><span class="sxs-lookup"><span data-stu-id="b8154-134">Introducing the Office (2007) Open XML File Formats</span></span>](https://msdn.microsoft.com/library/aa338205.aspx) <br/> |<span data-ttu-id="b8154-135">Ces deux articles traitent de la manière dont les spécifications des normes Open Packaging Conventions ont été appliquées aux fichiers Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="b8154-135">These two articles discuss how the Open Packaging Conventions have been applied to Microsoft Office files.</span></span> <span data-ttu-id="b8154-136">Ils contiennent des descriptions sur le fonctionnement des relations dans un package, et incluent également quelques exemples de code.</span><span class="sxs-lookup"><span data-stu-id="b8154-136">They contain descriptions of how relationships work in a package and also include some code examples.</span></span>  <br/> |
   
## <a name="create-a-vsdx-file-and-a-new-visual-studio-solution"></a><span data-ttu-id="b8154-137">Créer un fichier .vsdx et une nouvelle solution Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b8154-137">Create a .vsdx file and a new Visual Studio solution</span></span>
<span data-ttu-id="b8154-138"><a name="vis15_ManipulateFF_CreateFile"> </a></span><span class="sxs-lookup"><span data-stu-id="b8154-138"><a name="vis15_ManipulateFF_CreateFile"> </a></span></span>

<span data-ttu-id="b8154-139">Avant de commencer à parcourir les procédures décrites dans cet article, vous devez créer un fichier Visio 2013 à ouvrir et manipuler.</span><span class="sxs-lookup"><span data-stu-id="b8154-139">Before you can begin working through the procedures in this article, you need to create a Visio 2013 file to open and manipulate.</span></span> <span data-ttu-id="b8154-140">Le dessin utilisé dans les exemples de code au fil de cet article contient une seule page avec deux formes liées. L’une d’elles est une forme « Début/fin » du modèle « Diagramme de flux simple ».</span><span class="sxs-lookup"><span data-stu-id="b8154-140">The drawing used in the code examples in this article contains a single page with two connected shapes on it, one of the shapes being a "Start/End" shape from the "Basic Flowchart" template.</span></span>
  
<span data-ttu-id="b8154-141">Utilisez la procédure suivante pour créer un fichier Visio 2013 à utiliser dans les autres procédures de cet article.</span><span class="sxs-lookup"><span data-stu-id="b8154-141">Use the following procedure to create a new Visio 2013 file to use in the remaining procedures in this article.</span></span>
  
### <a name="to-create-new-file-in-visio-2013"></a><span data-ttu-id="b8154-142">Pour créer un fichier Visio 2013</span><span class="sxs-lookup"><span data-stu-id="b8154-142">To create new file in Visio 2013</span></span>

1. <span data-ttu-id="b8154-143">Ouvrez Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="b8154-143">Open Visio 2013.</span></span>
    
2. <span data-ttu-id="b8154-144">Créez un document à partir du modèle Diagramme de flux simple en choisissant **CATÉGORIES**, **Diagramme de flux**, **Diagramme de flux simple**, **Créer**.</span><span class="sxs-lookup"><span data-stu-id="b8154-144">Create a new document based on the Basic Flowchart template by choosing **CATEGORIES**, **Flowchart**, **Basic Flowchart**, **Create**.</span></span>
    
3. <span data-ttu-id="b8154-145">À partir de la fenêtre **Formes**, faites glisser une forme **Début/fin** sur la zone de dessin.</span><span class="sxs-lookup"><span data-stu-id="b8154-145">From the **Shapes** window, drag a **Start/End** shape onto the canvas.</span></span> 
    
4. <span data-ttu-id="b8154-146">Sélectionnez la nouvelle forme Début/fin sur la zone de dessin et saisissez « Commencer le processus ».</span><span class="sxs-lookup"><span data-stu-id="b8154-146">Select the new Start/End shape on the drawing canvas and type 'Begin Process'.</span></span>
    
5. <span data-ttu-id="b8154-147">À partir de la fenêtre **Formes**, faites glisser une forme **Processus** sur la zone de dessin.</span><span class="sxs-lookup"><span data-stu-id="b8154-147">From the **Shapes** window, drag a **Process** shape onto the canvas.</span></span> 
    
6. <span data-ttu-id="b8154-148">Sélectionnez la nouvelle forme Processus sur la zone de dessin et saisissez « Effectuer certaines tâches ».</span><span class="sxs-lookup"><span data-stu-id="b8154-148">Select the new Process shape on the drawing canvas and type 'Perform some task'.</span></span>
    
7. <span data-ttu-id="b8154-149">Dans le menu contextuel de la forme Début/fin, sélectionnez **Ajouter un connecteur à la page**, puis tracez un connecteur entre les formes Processus et Début/fin sur la zone de dessin, comme illustré dans la figure 1.</span><span class="sxs-lookup"><span data-stu-id="b8154-149">On the shortcut menu for the Start/End shape, select **Add One Connector to the Page**, and then draw a connector between the Start/End and Process shapes on the canvas, as shown in Figure 1.</span></span>
    
    <span data-ttu-id="b8154-150">**Figure 1. Dessin Visio 2013 simple**</span><span class="sxs-lookup"><span data-stu-id="b8154-150">**Figure 1. Simple Visio 2013 drawing**</span></span>
    
     ![Forme de début/fin liée à une forme de processus](media/vis15_SimpleFlowchart.png)
  
8. <span data-ttu-id="b8154-152">Enregistrez le fichier sur votre bureau au format .vsdx en sélectionnant **Fichier**, **Enregistrer sous**, **Ordinateur**, **Bureau**.</span><span class="sxs-lookup"><span data-stu-id="b8154-152">Save the file to your Desktop as a .vsdx file by choosing **File**, **Save As**, **Computer**, **Desktop**.</span></span>
    
    <span data-ttu-id="b8154-153">Dans la boîte de dialogue **Enregistrer sous**, entrez Package Visio dans la zone **Nom de fichier**, sélectionnez **Dessin Visio (\*.vsdx)** dans la liste **Type de fichier**, puis cliquez sur le bouton **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b8154-153">In the **Save As** dialog box, enter Visio Package in the **File name** box"", select **Visio Drawing (\*.vsdx)** in the **Save as type** list, and then choose the **Save** button.</span></span> 
    
9. <span data-ttu-id="b8154-154">Fermez le fichier, puis fermez Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="b8154-154">Close the file and then close Visio 2013.</span></span>
    
> [!TIP]
> <span data-ttu-id="b8154-155">Parfois Visio ouvre un fichier avec succès même s’il existe des problèmes avec ce fichier.</span><span class="sxs-lookup"><span data-stu-id="b8154-155">Sometimes Visio opens a file successfully even if there are issues with the file.</span></span> <span data-ttu-id="b8154-156">Pour vous assurer que Visio vous avertit de tous les problèmes de fichier, vous devez activer les avertissements à l’ouverture des fichiers lors du test des solutions qui manipulent les fichiers Visio au niveau du package de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b8154-156">To ensure that Visio notifies you of any file issues, you should enable file open warnings when testing solutions that manipulate Visio files at the file package level.</span></span> <span data-ttu-id="b8154-157">> Pour activer les avertissements lors de l’ouverture des fichiers, dans Visio 2013, sélectionnez **Fichier**, **Options**, **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="b8154-157">> To enable file open warnings, in Visio 2013, choose **File**, **Options**, **Advanced**.</span></span> <span data-ttu-id="b8154-158">Sous **Enregistrer/Ouvrir**, sélectionnez **Afficher les avertissements lors de l’ouverture des fichiers**.</span><span class="sxs-lookup"><span data-stu-id="b8154-158">Under **Save/Open**, select **Show file open warnings**.</span></span> 
  
<span data-ttu-id="b8154-159">Les procédures suivantes utilisent une application console Windows pour manipuler le fichier « Visio Package.vsdx ».</span><span class="sxs-lookup"><span data-stu-id="b8154-159">These procedures use a Windows console application to manipulate the "Visio Package.vsdx" file.</span></span> <span data-ttu-id="b8154-160">La procédure suivante permet de créer et de configurer une nouvelle application console Windows dans Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="b8154-160">Use the following procedure to create and set up a new Windows console application in Visual Studio 2012.</span></span>
  
### <a name="to-create-a-new-solution-in-visual-studio-2012"></a><span data-ttu-id="b8154-161">Pour créer une nouvelle solution dans Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="b8154-161">To create a new solution in Visual Studio 2012</span></span>

1. <span data-ttu-id="b8154-162">Dans le menu **Fichier**, choisissez **Nouveau**, **Projet**.</span><span class="sxs-lookup"><span data-stu-id="b8154-162">On the **File** menu, choose **New**, **Project**.</span></span>
    
2. <span data-ttu-id="b8154-163">Dans la boîte de dialogue **Nouveau projet**, développez **Visual C#** ou **Visual Basic**, puis choisissez **Windows**, **Application console**.</span><span class="sxs-lookup"><span data-stu-id="b8154-163">In the **New Project** dialog box, expand either **Visual C#** or **Visual Basic**, and then choose **Windows**, **Console Application**.</span></span>
    
    <span data-ttu-id="b8154-164">Dans la zone **Nom**, entrez « VisioFileAccessor », sélectionnez un emplacement pour le projet, puis sélectionnez le bouton **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8154-164">In the **Name** box, enter ' VisioFileAccessor', select a location for the project, and then choose the **OK** button.</span></span> 
    
3. <span data-ttu-id="b8154-165">Dans le menu **Projet**, choisissez **Ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="b8154-165">On the **Project** menu, choose **Add Reference**.</span></span> 
    
    <span data-ttu-id="b8154-166">Dans la boîte de dialogue **Gestionnaire de références**, sous **Montages**, choisissez **Framework**, puis ajoutez une référence aux composants \*\*System.Xml \*\* et **WindowsBase**.</span><span class="sxs-lookup"><span data-stu-id="b8154-166">In the **Reference Manager** dialog box, under **Assemblies**, choose **Framework**, and then add a reference to the **System.Xml** and **WindowsBase** components.</span></span> 
    
4. <span data-ttu-id="b8154-167">Dans le fichier Program.cs ou Module1.vb du projet, ajoutez les directives **using** suivantes (instructions **imports** dans Visual Basic) :</span><span class="sxs-lookup"><span data-stu-id="b8154-167">In the Program.cs or Module1.vb file for the project, add the following **using** directives (**Imports** statements in Visual Basic):</span></span> 
    
    ```cs
    using System.Xml;
    using System.Xml.Linq;
    using System.IO;
    using System.IO.Packaging;
    using System.Text;
    
    ```

    ```vb
    Imports System.Xml
    Imports System.Xml.Linq
    Imports System.IO
    Imports System.IO.Packaging
    Imports System.Text
    
    ```

5. <span data-ttu-id="b8154-168">De même, dans le fichier Program.cs ou Module1.vb, avant la fin de la méthode **Main** de la classe **Program** (**Module1** dans Visual Basic), ajoutez le code suivant qui arrête l’exécution de l’application console jusqu’à ce que l’utilisateur appuie sur une touche.</span><span class="sxs-lookup"><span data-stu-id="b8154-168">Also in the Program.cs or Module1.vb file, before the end of the **Main** method of the **Program** class (**Module1** in Visual Basic), add the following code that stops execution of the console application until the user presses a key.</span></span> 
    
    ```cs
    // This code stops the execution of the console application
    // so you can read the output.
    Console.WriteLine("Press any key to continue ...");
    Console.ReadKey();
    
    ```

    ```vb
    ' This code stops the execution of the console application
    ' so you can read the output.
    Console.WriteLine("Press any key to continue ...")
    Console.ReadKey()
    ```

## <a name="open-a-visio-2013-file-as-a-package"></a><span data-ttu-id="b8154-169">Ouvrir un fichier Visio 2013 sous forme de package</span><span class="sxs-lookup"><span data-stu-id="b8154-169">Open a Visio 2013 file as a package</span></span>
<span data-ttu-id="b8154-170"><a name="vis15_ManipulateFF_OpenPackage"> </a></span><span class="sxs-lookup"><span data-stu-id="b8154-170"><a name="vis15_ManipulateFF_OpenPackage"> </a></span></span>

<span data-ttu-id="b8154-171">Avant de manipuler les données dans le fichier, vous devez tout d’abord ouvrir le fichier dans un objet [Package](https://msdn.microsoft.com/library/System.IO.Packaging.Package.aspx) qui est contenu dans l’espace de noms [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx).</span><span class="sxs-lookup"><span data-stu-id="b8154-171">Before you can manipulate any of the data within the file, you need to first open the file within a [Package](https://msdn.microsoft.com/library/System.IO.Packaging.Package.aspx) object, which is contained within the [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) namespace.</span></span> <span data-ttu-id="b8154-172">L’objet **Package** représente le fichier Visio dans son ensemble.</span><span class="sxs-lookup"><span data-stu-id="b8154-172">The **Package** object represents the Visio file as a whole.</span></span> <span data-ttu-id="b8154-173">Il présente les membres qui vous permettent de sélectionner des composants de documents individuels dans le package de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b8154-173">It exposes members that allow you to select individual document parts within the file package.</span></span> <span data-ttu-id="b8154-174">En particulier, la classe **Package** présente la méthode [Open(String, FileMode, FileAccess)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Open.aspx) statique que vous utilisez pour ouvrir un fichier sous forme de package.</span><span class="sxs-lookup"><span data-stu-id="b8154-174">In particular, the **Package** class exposes the static [Open(String, FileMode, FileAccess)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Open.aspx) method that you use to open a file as a package.</span></span> <span data-ttu-id="b8154-175">Il présente également une méthode [Close()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Close.aspx) pour fermer le package une fois l’opération terminée.</span><span class="sxs-lookup"><span data-stu-id="b8154-175">It also exposes a [Close()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Close.aspx) method for closing the package once you've finished with it.</span></span> 
  
> [!TIP]
> <span data-ttu-id="b8154-176">Il est recommandé d’utiliser un bloc **using** pour ouvrir le fichier Visio dans l’objet **Package** pour ne pas être obligé de fermer explicitement le package de fichiers une fois l’opération terminée. </span><span class="sxs-lookup"><span data-stu-id="b8154-176">As a best practice, use a **using** block to open the Visio file in the **Package** object so that you don't have to explicitly close the file package when you're done with it.</span></span> <span data-ttu-id="b8154-177">Vous pouvez également appeler explicitement la méthode **Package.Close** dans le bloc **finally** d’une construction **try/catch/finally**.</span><span class="sxs-lookup"><span data-stu-id="b8154-177">You can also explicitly call the **Package.Close** method in the **finally** block of a **try/catch/finally** construction.</span></span> 
  
<span data-ttu-id="b8154-178">Utilisez le code suivant pour obtenir le chemin d’accès complet du fichier « Visio Package.vsdx » à l’aide d’un objet [FileInfo](https://msdn.microsoft.com/library/System.IO.FileInfo.aspx), transmettez le chemin d’accès comme un argument vers la méthode **Package.Open**, puis renvoyez un objet **Package** au code appelant.</span><span class="sxs-lookup"><span data-stu-id="b8154-178">Use the following code to get the full path for the "Visio Package.vsdx" file by using a [FileInfo](https://msdn.microsoft.com/library/System.IO.FileInfo.aspx) object, pass the path as an argument to the **Package.Open** method, and then return a **Package** object to the calling code.</span></span> 
  
### <a name="to-open-a-vsdx-file-as-a-package"></a><span data-ttu-id="b8154-179">Pour ouvrir un fichier .vsdx sous forme de package</span><span class="sxs-lookup"><span data-stu-id="b8154-179">To open a .vsdx file as a package</span></span>

1. <span data-ttu-id="b8154-180">Après la méthode **Main** dans la classe **Program** (ou **Module1** dans Visual Basic), ajoutez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="b8154-180">After the **Main** method in the **Program** class (or **Module1** in Visual Basic), add the following code.</span></span> 
    
    ```cs
    private static Package OpenPackage(string fileName, 
        Environment.SpecialFolder folder)
    {
        Package visioPackage = null;
        // Get a reference to the location 
        // where the Visio file is stored.
        string directoryPath = System.Environment.GetFolderPath(
            folder);
        DirectoryInfo dirInfo = new DirectoryInfo(directoryPath);
        // Get the Visio file from the location.
        FileInfo[] fileInfos = dirInfo.GetFiles(fileName);
        if (fileInfos.Count() > 0)
        {
            FileInfo fileInfo = fileInfos[0];
            string filePathName = fileInfo.FullName;
            // Open the Visio file as a package with
            // read/write file access.
            visioPackage = Package.Open(
                filePathName,
                FileMode.Open,
                FileAccess.ReadWrite);
            }
            // Return the Visio file as a package.
            return visioPackage;
    }
    ```

    ```vb
    Private Function OpenPackage(fileName As String, _
        folder As Environment.SpecialFolder) As Package
        Dim visioPackage As Package = Nothing
        ' Get a reference to the location
        ' where the Visio file is stored.
        Dim directoryPath As String = System.Environment.GetFolderPath( _
            folder)
        Dim dirInfo As DirectoryInfo = New DirectoryInfo(directoryPath)
        ' Get the Visio file from the location.
        Dim fileInfos As FileInfo() = dirInfo.GetFiles(fileName)
        If (fileInfos.Count() > 0) Then
            Dim fileInfo As FileInfo = fileInfos(0)
            Dim filePathName As String = fileInfo.FullName
            ' Open the Visio file as a package 
            ' with read/write access.
            visioPackage = Package.Open( _
                filePathName,
                FileMode.Open,
                FileAccess.ReadWrite)
            End If
        ' Return the Visio file as a package.
        Return visioPackage
    End Function
    
    ```

2. <span data-ttu-id="b8154-181">Dans la méthode **Main** de la classe **Program** (ou **Module1** dans Visual Basic), ajoutez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="b8154-181">In the **Main** method of the **Program** class (or **Module1** in Visual Basic), add the following code.</span></span> 
    
    ```cs
    // Open the Visio file in a Package object.
    using (Package visioPackage = OpenPackage("Visio Package.vsdx", 
        Environment.SpecialFolder.Desktop))
    {
    }
    
    ```

    ```vb
    ' Open the Visio file in a Package object.
    Using visioPackage As Package = OpenPackage("Visio Package.vsdx", _
        Environment.SpecialFolder.Desktop)
    End Using
    
    ```

## <a name="select-and-read-package-parts-from-a-package"></a><span data-ttu-id="b8154-182">Sélectionner et lire des composants d’un package</span><span class="sxs-lookup"><span data-stu-id="b8154-182">Select and read package parts from a package</span></span>
<span data-ttu-id="b8154-183"><a name="vis15_ManipulateFF_SelectPart"> </a></span><span class="sxs-lookup"><span data-stu-id="b8154-183"><a name="vis15_ManipulateFF_SelectPart"> </a></span></span>

<span data-ttu-id="b8154-184">Une fois que le fichier Visio 2013 est ouvert sous forme de package, vous pouvez accéder aux composants de documents qu’il contient à l’aide de la classe [PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx) incluse dans l’espace de noms **System.IO.Packaging**.</span><span class="sxs-lookup"><span data-stu-id="b8154-184">Once you have the Visio 2013 file open as a package, you can access the document parts within it using the [PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx) class included in the **System.IO.Packaging** namespace.</span></span> <span data-ttu-id="b8154-185">Les objets **PackagePart** peuvent être instanciés individuellement ou comme un ensemble.</span><span class="sxs-lookup"><span data-stu-id="b8154-185">**PackagePart** objects can be instantiated individually or as a collection.</span></span> <span data-ttu-id="b8154-186">La classe **Package** présente une méthode [GetParts()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx) et une méthode [GetPart(Uri)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx) pour extraire les objets **PackagePart** du \*\* Package\*\*.</span><span class="sxs-lookup"><span data-stu-id="b8154-186">The **Package** class exposes a [GetParts()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx) method and a [GetPart(Uri)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx) method for getting **PackagePart** objects out of the **Package**.</span></span> <span data-ttu-id="b8154-187">La méthode **Package.GetParts** renvoie une instance de la classe [PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx), avec laquelle vous pouvez interagir comme toute autre collection qui implémente l’interface [IEnumerator \<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.ienumerator-1?redirectedfrom=MSDN&view=netframework-4.7.2).</span><span class="sxs-lookup"><span data-stu-id="b8154-187">The **Package.GetParts** method returns an instance of the [PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx) class, which you can then interact with like any other collection that implements the [IEnumerator\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.ienumerator-1?redirectedfrom=MSDN&view=netframework-4.7.2) interface.</span></span> 
  
<span data-ttu-id="b8154-188">Utilisez le code de la procédure suivante pour obtenir un objet **PackagePartCollection** du **Package** sous forme de collection, effectuez une itération dans les objets **PackagePart** de la collection et écrivez l’URI et le type de contenu de chaque **PackagePart** dans la console.</span><span class="sxs-lookup"><span data-stu-id="b8154-188">Use the code in the following procedure to get a **PackagePartCollection** object from the **Package** as a collection, iterate through the **PackagePart** objects in the collection, and write the URI and content type of each **PackagePart** to the console.</span></span> 
  
### <a name="to-iterate-through-the-package-parts-in-a-package"></a><span data-ttu-id="b8154-189">Pour effectuer une itération dans les composants d’un package</span><span class="sxs-lookup"><span data-stu-id="b8154-189">To iterate through the package parts in a package</span></span>

1. <span data-ttu-id="b8154-190">Après la méthode `OpenPackage` dans la classe **Program** (ou **Module1** dans Visual Basic), ajoutez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="b8154-190">After the  `OpenPackage` method in the **Program** class (or **Module1** in Visual Basic), add the following code.</span></span> 
    
    ```cs
    private static void IteratePackageParts(Package filePackage)
    {
        
        // Get all of the package parts contained in the package
        // and then write the URI and content type of each one to the console.
        PackagePartCollection packageParts = filePackage.GetParts();
        foreach (PackagePart part in packageParts)
        {
            Console.WriteLine("Package part URI: {0}", part.Uri);
            Console.WriteLine("Content type: {0}", part.ContentType.ToString());
        }
    }
    
    ```

    ```vb
    Private Sub IteratePackageParts(filePackage As Package)
        ' Get all of the package parts contained in the package
        ' and then write the URI and content type of each one to the console.
        Dim packageParts As PackagePartCollection = filePackage.GetParts()
        For Each part In packageParts
            Console.WriteLine("Package part: {0}", part.Uri)
            Console.WriteLine("Content type: {0}", part.ContentType.ToString())
        Next
    End Sub 
    
    ```

2. <span data-ttu-id="b8154-191">Ajoutez le code suivant dans le bloc **using** de la méthode **Main** de la classe **Program** (le bloc **Using** de la méthode **Main** dans **Module1** dans Visual Basic) :</span><span class="sxs-lookup"><span data-stu-id="b8154-191">Add the following code inside the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic):</span></span> 
    
    ```cs
    // Write the URI and content type of each package part to the console.
    IteratePackageParts(visioPackage);
    
    ```

    ```vb
    ' Write the URI and content type of each package part to the console.
    IteratePackageParts(visioPackage)
    
    ```

3. <span data-ttu-id="b8154-p112">Appuyez sur la touche F5 pour déboguer la solution. Lorsque le programme est terminé, appuyez sur une touche pour le quitter.</span><span class="sxs-lookup"><span data-stu-id="b8154-p112">Choose the F5 key to debug the solution. When the program has completed running, choose any key to exit.</span></span>
    
<span data-ttu-id="b8154-194">L’application console produit une sortie semblable à la suivante (un composant de la sortie a été omis par souci de concision) :</span><span class="sxs-lookup"><span data-stu-id="b8154-194">The console application produces output similar to the following (some of the output has been omitted for brevity):</span></span>
  
 `Package part URI: /docProps/app.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.extended-properties+xml`
  
 `Package part URI: /docProps/core.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.core-properties+xml`
  
 `Package part URI: /docProps/custom.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.custom-properties+xml`
  
 `Package part URI: /docProps/thumbnail.emv`
  
 `Content type: image/x-emf`
  
 `Package part URI: /visio/document.xml`
  
 `Content type: application/vnd.ms-visio.drawing.main+xml`
  
 `Package part URI: /visio/_rels/document.xml.rels`
  
 `Content type: application/vnd.openxmlformats-package.relationships+xml`
  
 `Package part URI: /_rels/.rels`
  
 `Content type: application/vnd.openxmlformats-package.relationships+xml`
  
 `Press any key to continue …`
  
<span data-ttu-id="b8154-195">Bien souvent, vous devez sélectionner un objet **PackagePart** sans avoir à effectuer d’itération dans tous les composants.</span><span class="sxs-lookup"><span data-stu-id="b8154-195">More often than not, you need to select one **PackagePart** without having to iterate over all of them.</span></span> <span data-ttu-id="b8154-196">Vous pouvez obtenir un objet **PackagePart** à partir d’un **Package** à l’aide de sa relation avec un **Package** ou un autre **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="b8154-196">You can get a **PackagePart** object from a **Package** by using its relationship to the **Package** or another **PackagePart**.</span></span> <span data-ttu-id="b8154-197">Une relation dans le format de fichier Visio 2013 est une entité discrète qui décrit comment un composant de document est lié au package de fichiers ou comment deux composants de document sont liés entre eux.</span><span class="sxs-lookup"><span data-stu-id="b8154-197">A relationship in the Visio 2013 file format is a discrete entity that describes how a document part relates to the file package or how two document parts relate to each other.</span></span> <span data-ttu-id="b8154-198">Par exemple, le package de fichiers Visio 2013 a lui-même une relation avec son composant de document Visio et le composant de document Visio a une relation avec le composant Windows.</span><span class="sxs-lookup"><span data-stu-id="b8154-198">For example, the Visio 2013 file package itself has a relationship to its Visio Document part, and the Visio Document part has a relationship to the Windows part.</span></span> <span data-ttu-id="b8154-199">Ces relations sont représentées par des instances des classes [PackageRelationship](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationship.aspx) ou [PackageRelationshipCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationshipCollection.aspx).</span><span class="sxs-lookup"><span data-stu-id="b8154-199">These relationships are represented as instances of the [PackageRelationship](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationship.aspx) or [PackageRelationshipCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationshipCollection.aspx) classes.</span></span> 
  
<span data-ttu-id="b8154-200">La classe **Package** présente plusieurs méthodes pour obtenir les relations qu’elle contient en tant qu’objet **PackageRelationship** ou **PackageRelationshipCollection**.</span><span class="sxs-lookup"><span data-stu-id="b8154-200">The **Package** class exposes several methods for getting the relationships that it contains as **PackageRelationship** or **PackageRelationshipCollection** objects.</span></span> <span data-ttu-id="b8154-201">Vous pouvez utiliser la méthode [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetRelationshipsByType.aspx) pour instancier un objet **PackageRelationshipCollection** qui contient les objets **PackageRelationship** d’un type spécifique.</span><span class="sxs-lookup"><span data-stu-id="b8154-201">You can use the [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetRelationshipsByType.aspx) method to instantiate a **PackageRelationshipCollection** object that contains **PackageRelationship** objects of a single specific type.</span></span> <span data-ttu-id="b8154-202">Bien entendu, l’utilisation de la méthode **Package.GetRelationshipsByType** nécessite que vous connaissiez déjà le type de relation dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="b8154-202">Of course, using the **Package.GetRelationshipsByType** method requires that you already know the relationship type that you need.</span></span> <span data-ttu-id="b8154-203">Les types de relations sont des chaînes au format d’espace de noms XML.</span><span class="sxs-lookup"><span data-stu-id="b8154-203">Relationship types are strings in XML namespace format.</span></span> <span data-ttu-id="b8154-204">Par exemple, le type de relation du composant de document Visio est http://schemas.microsoft.com/visio/2010/relationships/document.</span><span class="sxs-lookup"><span data-stu-id="b8154-204">For example, the relationship type of the Visio Document part is http://schemas.microsoft.com/visio/2010/relationships/document.</span></span> 
  
<span data-ttu-id="b8154-p115">Une fois que vous connaissez la relation entre un **PackagePart** et un **Package** ou un autre **PackagePart** (autrement dit, lorsque vous avez un objet **PackageRelationship** qui fait référence au **PackagePart** de votre choix), vous pouvez utiliser cette relation pour obtenir l’URI de ce **PackagePart**. Vous devez ensuite transmettre l’URI à la méthode **Package.GetPart** pour renvoyer le **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="b8154-p115">Once you know the relationship of a **PackagePart** to the **Package** or to another **PackagePart** (that is, you have a **PackageRelationship** object that references the **PackagePart** that you want), you can use that relationship to get the URI of that **PackagePart**. You then pass the URI to the **Package.GetPart** method to return the **PackagePart**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b8154-207">Vous pouvez également obtenir une référence à un **PackagePart** spécifique à l’aide de la méthode **Package.GetPart** et de l’URI du **PackagePart**, sans passer par l’étape d’obtention des relations du composant de package.</span><span class="sxs-lookup"><span data-stu-id="b8154-207">You can also get a reference to a specific **PackagePart** by using just the **Package.GetPart** method and the URI of the **PackagePart**, bypassing the step where you get the package part's relationships.</span></span> <span data-ttu-id="b8154-208">Toutefois, certains composants de package dans le package de fichiers Visio peuvent être enregistrés à un emplacement différent de leur emplacement par défaut dans un package.</span><span class="sxs-lookup"><span data-stu-id="b8154-208">However, some package parts in the Visio file package can be saved to locations other than their default locations in a package.</span></span> <span data-ttu-id="b8154-209">Vous ne pouvez pas partir du principe qu’un composant de package se trouve toujours dans le même URI pour chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="b8154-209">You cannot assume that a package part is always located at the same URI for every file.</span></span> <span data-ttu-id="b8154-210">> Il est plutôt recommandé d’utiliser les relations pour accéder à des objets **PackagePart** individuels.</span><span class="sxs-lookup"><span data-stu-id="b8154-210">> Instead, it is a best practice to use relationships to access individual **PackagePart** objects.</span></span> 
  
<span data-ttu-id="b8154-211">Utilisez la procédure suivante pour obtenir un **PackagePart** (le composant de document Visio) à l’aide de l’élément **PackageRelationship** à partir du **Package** qui fait référence au composant.</span><span class="sxs-lookup"><span data-stu-id="b8154-211">Use the following procedure to get a **PackagePart** (the Visio Document part) by using the **PackageRelationship** from the **Package** that references the part.</span></span> 
  
### <a name="to-select-a-specific-package-part-in-the-package-by-relationship"></a><span data-ttu-id="b8154-212">Pour sélectionner un composant du package spécifique dans le package par relation</span><span class="sxs-lookup"><span data-stu-id="b8154-212">To select a specific package part in the package by relationship</span></span>

1. <span data-ttu-id="b8154-213">Après la méthode `IteratePackageParts` dans la classe **Program** (ou **Module1** dans Visual Basic), ajoutez la méthode suivante.</span><span class="sxs-lookup"><span data-stu-id="b8154-213">After the  `IteratePackageParts` method in the **Program** class (or **Module1** in Visual Basic), add the following method.</span></span> 
    
    ```cs
    private static PackagePart GetPackagePart(Package filePackage, 
        string relationship)
    {
        
        // Use the namespace that describes the relationship 
        // to get the relationship.
        PackageRelationship packageRel = 
            filePackage.GetRelationshipsByType(relationship).FirstOrDefault();
        PackagePart part = null;
        // If the Visio file package contains this type of relationship with 
        // one of its parts, return that part.
        if (packageRel != null)
        {
            // Clean up the URI using a helper class and then get the part.
            Uri docUri = PackUriHelper.ResolvePartUri(
                new Uri("/", UriKind.Relative), packageRel.TargetUri);
            part = filePackage.GetPart(docUri);
        }
        return part;
    }
    
    ```

    ```vb
    Private Function GetPackagePart(filePackage As Package, relationship As String) _
        As PackagePart
        ' Use the namespace that describes the relationship 
        ' to get the relationship.
        Dim packageRel As PackageRelationship = 
            filePackage.GetRelationshipsByType(relationship).FirstOrDefault()
        Dim part As PackagePart = Nothing
        ' If the Visio file package contains this type of relationship with 
        ' one of its parts, return that part.
        If Not IsNothing(packageRel) Then
            ' Clean up the URI using a helper class and then get the part.
            Dim docUri = PackUriHelper.ResolvePartUri( _
                New Uri("/", UriKind.Relative), packageRel.TargetUri)
            part = filePackage.GetPart(docUri)
        End If
        Return part
    End Function
    
    ```

2. <span data-ttu-id="b8154-214">Remplacez le code dans le bloc **using** de la méthode **Main** de la classe **Program** (le bloc **Using** de la méthode **Main** dans **Module1** dans Visual Basic) par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="b8154-214">Replace the code in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic) with the following code.</span></span> 
    
    ```cs
    // Get a reference to the Visio Document part contained in the file package.
    PackagePart documentPart = GetPackagePart(visioPackage, 
        "http://schemas.microsoft.com/visio/2010/relationships/document");
    
    ```

    ```vb
    ' Get a reference to the Visio Document part contained in the file package.
    Dim documentPart As PackagePart = GetPackagePart(visioPackage, _
        "http://schemas.microsoft.com/visio/2010/relationships/document")
    
    ```

<span data-ttu-id="b8154-215">Comme mentionné précédemment, vous pouvez également obtenir des objets **PackagePart** à l’aide de leur relation avec les autres objets **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="b8154-215">As mentioned previously, you can also get **PackagePart** objects by using their relationship to other **PackagePart** objects.</span></span> <span data-ttu-id="b8154-216">Cet aspect est très important, car, pour un document Visio de n’importe quelle complexité, la plupart des objets **PackagePart** n’ont pas de relation avec le **Package**.</span><span class="sxs-lookup"><span data-stu-id="b8154-216">This is important because, for a Visio document of any complexity, most of the **PackagePart** objects don't have a relationship to the **Package**.</span></span> <span data-ttu-id="b8154-217">Par exemple, un composant du contenu de la page individuelle dans le package de fichiers (c’est-à-dire, /visio/pages/page1.xml) a une relation avec le composant d’index de la page (c’est-à-dire, /visio/pages/pages.xml) mais pas avec le package de fichiers lui-même.</span><span class="sxs-lookup"><span data-stu-id="b8154-217">For example, an individual Page Content part in the file package (that is, /visio/pages/page1.xml) has a relationship to the Page Index part (that is, /visio/pages/pages.xml) but not to the file package itself.</span></span> <span data-ttu-id="b8154-218">Si vous n’avez pas l’URI exact de la page individuelle dans le package, vous pouvez utiliser sa relation avec le composant d’index de la page pour obtenir une référence à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="b8154-218">If you don't have the exact URI of the individual page in the package, you can use its relationship to the Page Index part to get a reference to it.</span></span>
  
<span data-ttu-id="b8154-219">La classe **PackagePart** présente une méthode [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx) qui vous permet de renvoyer un objet **PackageRelationshipCollection** qui contient un seul type d’objet **PackageRelationship**.</span><span class="sxs-lookup"><span data-stu-id="b8154-219">The **PackagePart** class exposes a [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx) method that you can use to return a **PackageRelationshipCollection** object that contains only one type of **PackageRelationship** object.</span></span> <span data-ttu-id="b8154-220">Une fois l’objet **PackageRelationshipCollection** obtenu, vous pouvez sélectionner l’objet **PackageRelationship** dont vous avez besoin à partir de la collection, puis référencer l’objet **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="b8154-220">Once you have the **PackageRelationshipCollection**, you can select the **PackageRelationship** that you need from the collection and then reference the **PackagePart** object.</span></span> 
  
<span data-ttu-id="b8154-221">Utilisez le code suivant pour obtenir un objet **PackagePart** à partir du **Package** à l’aide de sa relation avec (obtention d’un objet **PackageRelationship** à partir de) un autre objet **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="b8154-221">Use the following code to get a **PackagePart** from the **Package** by using its relationship to (getting a **PackageRelationship** object from) another **PackagePart**.</span></span>
  
### <a name="to-select-a-specific-package-part-through-its-relationship-to-another-package-part"></a><span data-ttu-id="b8154-222">Pour sélectionner un composant du package spécifique via sa relation avec un autre composant du package</span><span class="sxs-lookup"><span data-stu-id="b8154-222">To select a specific package part through its relationship to another package part</span></span>

1. <span data-ttu-id="b8154-223">Après la méthode `GetPackagePart` dans la classe **Program** (ou **Module1** dans Visual Basic), ajoutez la méthode de surcharge suivante.</span><span class="sxs-lookup"><span data-stu-id="b8154-223">After the  `GetPackagePart` method in the **Program** class (or **Module1** in Visual Basic), add the following overload method.</span></span> 
    
    ```cs
    private static PackagePart GetPackagePart(Package filePackage, 
        PackagePart sourcePart, string relationship)
    {
        // This gets only the first PackagePart that shares the relationship
        // with the PackagePart passed in as an argument. You can modify the code
        // here to return a different PackageRelationship from the collection.
        PackageRelationship packageRel = 
            sourcePart.GetRelationshipsByType(relationship).FirstOrDefault();
        PackagePart relatedPart = null;
        if (packageRel != null)
        {
            // Use the PackUriHelper class to determine the URI of PackagePart
            // that has the specified relationship to the PackagePart passed in
            // as an argument.
            Uri partUri = PackUriHelper.ResolvePartUri(
                sourcePart.Uri, packageRel.TargetUri);
            relatedPart = filePackage.GetPart(partUri);
        }
        return relatedPart;
    }
    
    ```

    ```vb
    Private Function GetPackagePart(filePackage As Package, 
        sourcePart As PackagePart, relationship As String) As PackagePart
        ' This gets only the first PackagePart that shares the relationship
        ' with the PackagePart passed in as an argument. You can modify the
        ' code to return a different PackageRelationship from the collection.
        Dim packageRel As PackageRelationship = sourcePart. _
            GetRelationshipsByType(relationship).FirstOrDefault()
        Dim relatedPart As PackagePart = Nothing
        If Not IsNothing(packageRel) Then
            ' Use the PackUriHelper class to determine the URI of the 
            ' PackagePart that has the specified relationship to the 
            ' PackagePart passed in as an argument.
            Dim partUri As Uri = PackUriHelper.ResolvePartUri( _
                sourcePart.Uri, packageRel.TargetUri)
            relatedPart = filePackage.GetPart(partUri)
        End If
        Return relatedPart
    End Function
    ```

2. <span data-ttu-id="b8154-p119">Ajoutez le code suivant au bloc **using** dans la méthode **Main** de la classe **Program** (le bloc **Using** de la méthode **Main** dans **Module1** dans Visual Basic), sous le code de la procédure précédente. (Ne supprimez pas le code ajouté dans la procédure précédente.)</span><span class="sxs-lookup"><span data-stu-id="b8154-p119">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure. (Do not delete the code that you added in the previous procedure.)</span></span> 
    
    ```cs
    // Get a reference to the collection of pages in the document, 
    // and then to the first page in the document.
    PackagePart pagesPart = GetPackagePart(visioPackage, documentPart, 
        "http://schemas.microsoft.com/visio/2010/relationships/pages");
    PackagePart pagePart = GetPackagePart(visioPackage, pagesPart, 
        "http://schemas.microsoft.com/visio/2010/relationships/page");
    
    ```

    ```vb
    ' Get a reference to the collection of pages in the document,
    ' and then to the first page in the document.
    Dim pagesPart As PackagePart = GetPackagePart(visioPackage, documentPart, _
        "http://schemas.microsoft.com/visio/2010/relationships/pages") 
    Dim pagePart As PackagePart = GetPackagePart(visioPackage, pagesPart, _
        "http://schemas.microsoft.com/visio/2010/relationships/page") 
    ```

<span data-ttu-id="b8154-226">Avant de pouvoir apporter des modifications au code XML inclus dans un composant de document, vous devez tout d’abord charger le document XML dans un objet qui permet de lire le code XML à l’aide de la classe [XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx) ou de la classe [XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx).</span><span class="sxs-lookup"><span data-stu-id="b8154-226">Before you can make changes to the XML included in a document part, you need to first load the XML document into an object that allows you to read the XML, using the [XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx) class or [XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx) class.</span></span> <span data-ttu-id="b8154-227">Les deux classes présentent les méthodes relatives aux tâches comme la sélection des éléments XML inclus dans les documents XML, la création, la lecture et l’écriture d’attributs et l’insertion de nouveaux éléments XML dans un document.</span><span class="sxs-lookup"><span data-stu-id="b8154-227">Both classes expose methods for tasks such as selecting XML elements contained within the XML documents; creating, reading, and writing attributes; and inserting new XML elements into a document.</span></span> 
  
<span data-ttu-id="b8154-p121">La classe **XDocument** vous permet d’interroger le code XML à l’aide de LINQ. Avec LINQ, vous pouvez facilement sélectionner des éléments individuels à partir d’un document XML en créant des requêtes, plutôt que via une itération sur tous les éléments d’une collection et plutôt qu’un test effectué sur les éléments nécessaires. Pour cela, les procédures suivantes dans cet article utilisent la classe **XDocument** et les autres classes de l’espace de noms **System.Xml.Linq** pour utiliser le langage XML.</span><span class="sxs-lookup"><span data-stu-id="b8154-p121">Of the two, the **XDocument** class allows you to query the XML using LINQ. With LINQ, you can easily select individual elements from an XML document by creating queries, rather than iterating over all of the elements in a collection and testing for the elements that you need. For these reasons, the following procedures in this article use the **XDocument** class and other classes of the **System.Xml.Linq** namespace for working with XML.</span></span> 
  
<span data-ttu-id="b8154-231">Utilisez la procédure suivante pour ouvrir un **PackagePart** sous forme de document XML dans un objet **XDocument**.</span><span class="sxs-lookup"><span data-stu-id="b8154-231">Use the following procedure to open a **PackagePart** as an XML document in an **XDocument** object.</span></span> 
  
### <a name="to-read-the-xml-in-a-package-part"></a><span data-ttu-id="b8154-232">Pour lire le code XML dans un composant de package</span><span class="sxs-lookup"><span data-stu-id="b8154-232">To read the XML in a package part</span></span>

1. <span data-ttu-id="b8154-233">Après la dernière surcharge pour la méthode `GetPackagePart` dans la classe **Program** (ou **Module1** dans Visual Basic), ajoutez la méthode suivante.</span><span class="sxs-lookup"><span data-stu-id="b8154-233">After the last overload for the  `GetPackagePart` method in the **Program** class (or **Module1** in Visual Basic), add the following method.</span></span> 
    
    ```cs
    private static XDocument GetXMLFromPart(PackagePart packagePart)
    {
        XDocument partXml = null;
        // Open the packagePart as a stream and then 
        // open the stream in an XDocument object.
        Stream partStream = packagePart.GetStream();
        partXml = XDocument.Load(partStream);
        return partXml;
    }
    ```

    ```vb
    Private Function GetXMLFromPart(packagePart As PackagePart) As XDocument
        Dim partXml As XDocument = Nothing
        ' Open the packagePart as a stream and then
        ' open the stream in an an XDocument object.
        Dim partStream As Stream = packagePart.GetStream()
        partXml = XDocument.Load(partStream)
        Return partXml
    End Function
    ```

2. <span data-ttu-id="b8154-234">Ajoutez le code suivant au bloc **using** dans la méthode **Main** de la classe **Program** (le bloc **Using** de la méthode **Main** dans **Module1** dans Visual Basic), sous le code de la procédure précédente.</span><span class="sxs-lookup"><span data-stu-id="b8154-234">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> 
    
    ```cs
    // Open the XML from the Page Contents part.
    XDocument pageXML = GetXMLFromPart(pagePart);
    ```

    ```vb
    ' Open the XML from the Page Contents part.
    Dim pageXML As XDocument = GetXMLFromPart(pagePart)
    ```

## <a name="select-and-change-xml-data-in-a-package-part"></a><span data-ttu-id="b8154-235">Sélectionner et modifier des données XML dans un composant de package</span><span class="sxs-lookup"><span data-stu-id="b8154-235">Select and change XML data in a package part</span></span>
<span data-ttu-id="b8154-236"><a name="vis15_ManipulateFF_ChangeXML"> </a></span><span class="sxs-lookup"><span data-stu-id="b8154-236"><a name="vis15_ManipulateFF_ChangeXML"> </a></span></span>

<span data-ttu-id="b8154-p122">Une fois que vous avez chargé un composant de document dans un objet **XDocument**, vous pouvez utiliser LINQ pour sélectionner des éléments XML et apporter des modifications au document XML. Vous pouvez modifier les données XML, ajouter ou supprimer des données, puis enregistrer le document XML sur le composant du document.</span><span class="sxs-lookup"><span data-stu-id="b8154-p122">Once you have loaded a document part into an **XDocument** object, you can use LINQ to select XML elements and make changes to the XML document. You can change XML data, add or remove data, and then save the XML document back to the document part.</span></span> 
  
<span data-ttu-id="b8154-239">La tâche la plus courante pour manipuler le format de fichier Visio consiste à choisir des éléments XML spécifiques ou des ensembles d’éléments dans le document.</span><span class="sxs-lookup"><span data-stu-id="b8154-239">The most common task for manipulating the Visio file format is selecting specific XML elements or collections of elements in the document.</span></span> <span data-ttu-id="b8154-240">L’espace de noms **System.Xml.Linq** inclut la classe [XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx), qui représente un élément XML.</span><span class="sxs-lookup"><span data-stu-id="b8154-240">The **System.Xml.Linq** namespace includes the [XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx) class, which represents an XML element.</span></span> <span data-ttu-id="b8154-241">La classe **XElement** permet d’accéder aux données figurant dans le fichier Visio à un niveau précis, des éléments **Shape** individuels aux éléments **ValidationRule** (en tant qu’exemples).</span><span class="sxs-lookup"><span data-stu-id="b8154-241">The **XElement** class gives you access to the data contained in the Visio file at a granular level, from individual **Shape** elements to **ValidationRule** elements (as examples).</span></span> 
  
<span data-ttu-id="b8154-242">Utilisez le code suivant pour sélectionner les éléments **Shape** à partir d’un **XDocument** (contenant un composant du contenu de la page), puis pour sélectionner un élément **Shape** spécifique.</span><span class="sxs-lookup"><span data-stu-id="b8154-242">Use the following code to select the **Shape** elements from an **XDocument** (containing a Page Contents part) and to then select a specific **Shape** element.</span></span> 
  
### <a name="to-select-a-specific-element-in-a-package-part"></a><span data-ttu-id="b8154-243">Pour sélectionner un élément spécifique dans un composant de package</span><span class="sxs-lookup"><span data-stu-id="b8154-243">To select a specific element in a package part</span></span>

1. <span data-ttu-id="b8154-244">Après la méthode `GetXMLFromPart` dans la classe **Program** (ou **Module1** dans Visual Basic), ajoutez la méthode suivante.</span><span class="sxs-lookup"><span data-stu-id="b8154-244">After the  `GetXMLFromPart` method in the **Program** class (or **Module1** in Visual Basic), add the following method.</span></span> 
        
    ```cs
    private static IEnumerable<XElement> GetXElementsByName(
        XDocument packagePart, string elementType)
    {
        // Construct a LINQ query that selects elements by their element type.
        IEnumerable<XElement> elements = 
            from element in packagePart.Descendants() 
            where element.Name.LocalName == elementType 
            select element;
        // Return the selected elements to the calling code.
        return elements.DefaultIfEmpty(null);
    }
    
    ```

    ```vb
    Private Function GetXElementsByName(partXML As XDocument, _
        elementType As String) As IEnumerable(Of XElement)
        ' Construct a LINQ query that selects elements by their element type.
        Dim elements As IEnumerable(Of XElement) =
            From element In partXML.Descendants()
            Where element.Name.LocalName = elementType
            Select element
        ' If there aren't any elements of the specified type
        ' in the document, return Nothing to the calling code.
        Return elements.DefaultIfEmpty(Nothing)
    End Function
    ```

2. <span data-ttu-id="b8154-245">Après la méthode `GetXElementsByName` dans la classe **Program** (ou **Module1** dans Visual Basic) de l’étape précédente, ajoutez la méthode suivante.</span><span class="sxs-lookup"><span data-stu-id="b8154-245">After the  `GetXElementsByName` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
    ```cs
    private static XElement GetXElementByAttribute(IEnumerable<XElement> elements,
        string attributeName, string attributeValue) 
    {
        // Construct a LINQ query that selects elements from a group
        // of elements by the value of a specific attribute.
        IEnumerable<XElement> selectedElements = 
            from el in elements
            where el.Attribute(attributeName).Value == attributeValue
            select el;
        // If there aren't any elements of the specified type
        // with the specified attribute value in the document,
        // return null to the calling code.
        return selectedElements.DefaultIfEmpty(null).FirstOrDefault();
    }
    ```

    ```vb
    Private Function GetXElementByAttribute(elements As IEnumerable(Of XElement), _
        attributeName As String, attributeValue As String) As XElement
        ' Construct a LINQ query that selects elements from a group
        ' of elements by the value of a specific attribute.
        Dim selectedElements As IEnumerable(Of XElement) =
            From el In elements
            Where el.Attribute(attributeName).Value = attributeValue
            Select el
        ' If there aren't any elements of the specified type 
        ' with the specified attribute value in the document,
        ' return Nothing to the calling code.
        Return selectedElements.DefaultIfEmpty(Nothing).FirstOrDefault()
    End Function
    
    ```

3. <span data-ttu-id="b8154-246">Ajoutez le code suivant au bloc **using** dans la méthode **Main** de la classe **Program** (le bloc **Using** de la méthode **Main** dans **Module1** dans Visual Basic), sous le code de la procédure précédente.</span><span class="sxs-lookup"><span data-stu-id="b8154-246">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> 
    
    ```cs
    // Get all of the shapes from the page by getting
    // all of the Shape elements from the pageXML document.
    IEnumerable<XElement> shapesXML = GetXElementsByName(pageXML, "Shape");
    // Select a Shape element from the shapes on the page by 
    // its name. You can modify this code to select elements
    // by other attributes and their values.
    XElement startEndShapeXML = 
        GetXElementByAttribute(shapesXML, "NameU", "Start/End");
    
    ```

    ```vb
    ' Get all of the shapes from the page by getting
    ' all of the Shape elements from the pageXML document.
    Dim shapesXML As IEnumerable(Of XElement) = GetXElementsByName( _
        pageXML, "Shape")
    ' Select a Shape element from the shapes on the page by
    ' its name. You can modify this code to select elements
    ' by other attributes and their values.
    Dim startEndShapeXML As XElement = GetXElementByAttribute( _
        shapesXML, "NameU", "Start/End")
    ```

<span data-ttu-id="b8154-247">Une fois que vous avez obtenu une référence à un objet **XElement** inclus dans un objet **XDocument**, vous pouvez la manipuler comme les autres données XML et, par conséquent, modifier les données figurant dans le fichier Visio.</span><span class="sxs-lookup"><span data-stu-id="b8154-247">Once you have gotten a reference to a **XElement** object contained within an **XDocument** object, you can manipulate it like any other XML data and, thereby, change the data contained in the Visio file.</span></span> <span data-ttu-id="b8154-248">Par exemple, si une forme comporte du texte lors de son ouverture dans Visio, l’élément **Shape** correspondant contient au moins un élément **Text**.</span><span class="sxs-lookup"><span data-stu-id="b8154-248">For example, if a shape has text when it is opened in Visio, the corresponding **Shape** element will contain at least one **Text** element.</span></span> <span data-ttu-id="b8154-249">Si vous modifiez la valeur de cet élément **Text**, le texte de la forme est modifié lorsque le fichier est affiché dans Visio.</span><span class="sxs-lookup"><span data-stu-id="b8154-249">If you change the value of that **Text** element, the shape's text is changed when the file is viewed in Visio.</span></span> 
  
<span data-ttu-id="b8154-250">Ajoutez le code suivant au bloc **using** dans la méthode **Main** de la classe **Program** (le bloc **Using** de la méthode **Main** dans **Module1** dans Visual Basic), pour modifier le texte de la forme Début/fin : « Commencer le processus » devient « Démarrer le processus ».</span><span class="sxs-lookup"><span data-stu-id="b8154-250">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic) to change the text in the Start/End shape from "Begin process" to "Start process".</span></span> 
  
```cs
// Query the XML for the shape to get the Text element, and
// return the first Text element node.
IEnumerable<XElement> textElements = from element in startEndShapeXML.Elements()
                               where element.Name.LocalName == "Text"
                               select element;
XElement textElement = textElements.ElementAt(0);
// Change the shape text, leaving the <cp> element alone.
textElement.LastNode.ReplaceWith("Start process");

```

```vb
' Query the XML for the shape to get the Text element, and
' return the first Text element node.
Dim textElements As IEnumerable(Of XElement) =
    From element In startEndShapeXML.Elements()
    Where element.Name.LocalName == "Text"
    Select element
Dim textElement As XElement = textElements.ElementAt(0)
' Change the shape text, leaving the <cp> element alone.
textElement.LastNode.ReplaceWith("Start process")

```

> [!CAUTION]
> <span data-ttu-id="b8154-251">Dans l’exemple de code précédent, le texte de la forme existant et la chaîne utilisée pour le remplacer ont le même nombre de caractères.</span><span class="sxs-lookup"><span data-stu-id="b8154-251">In the previous code example, the existing shape text and the string used to replace it have the same number of characters.</span></span> <span data-ttu-id="b8154-252">Notez également que la requête LINQ modifie la valeur du dernier nœud enfant de l’élément renvoyé (dans ce cas, un nœud de texte).</span><span class="sxs-lookup"><span data-stu-id="b8154-252">Also note that the LINQ query changes the value of the last child node of the returned element (which, in this case, is a text node).</span></span> <span data-ttu-id="b8154-253">Cette opération est effectuée pour éviter de modifier les paramètres de l’élément **cp** qui est un enfant de l’élément **Text**.</span><span class="sxs-lookup"><span data-stu-id="b8154-253">This is done to avoid changing the settings of the **cp** element that is a child of the **Text** element.</span></span> <span data-ttu-id="b8154-254">> Vous risquez d’engendrer l’instabilité du fichier si vous modifiez le texte de la forme par programme en remplaçant tous les enfants de l’élément **Text**.</span><span class="sxs-lookup"><span data-stu-id="b8154-254">> It is possible to cause file instability if you alter shape text programmatically by overwriting all children of the **Text** element.</span></span> <span data-ttu-id="b8154-255">Comme dans l’exemple ci-dessus, la mise en forme du texte est représentée par les éléments **cp** sous l’élément **Text** dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="b8154-255">As in the example above, the text formatting is represented by **cp** elements under the **Text** element in the file.</span></span> <span data-ttu-id="b8154-256">La définition de la mise en forme est stockée dans l’élément **Section** parent.</span><span class="sxs-lookup"><span data-stu-id="b8154-256">The definition of the formatting is stored in the parent **Section** element.</span></span> <span data-ttu-id="b8154-257">Si ces deux informations sont incohérentes, le fichier ne peut pas se comporter comme prévu.</span><span class="sxs-lookup"><span data-stu-id="b8154-257">If these two pieces of information become inconsistent, then the file may not behave as expected.</span></span> <span data-ttu-id="b8154-258">Visio règle un grand nombre d’incohérences, mais il est préférable de vous assurer que toute modification apportée par programme est cohérente afin que vous contrôliez le comportement final du fichier.</span><span class="sxs-lookup"><span data-stu-id="b8154-258">Visio heals many inconsistencies, but it is better to ensure that any programmatic changes are consistent so that you are controlling the ultimate behavior of the file.</span></span> 
  
<span data-ttu-id="b8154-p126">Lorsque vous modifiez le code XML d’un composant de document, ces modifications existent seulement en mémoire. Pour rendre ces modifications persistantes dans le fichier, vous devez enregistrer le fichier XML dans le composant du document.</span><span class="sxs-lookup"><span data-stu-id="b8154-p126">When you make changes to the XML of a document part, those changes exist in memory only. To persist the changes in the file, you must save the XML back to the document part.</span></span>
  
<span data-ttu-id="b8154-261">Le code suivant utilise la classe [XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx) et la classe [XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx) pour réécrire le code XML dans le composant de package.</span><span class="sxs-lookup"><span data-stu-id="b8154-261">The following code uses the [XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx) class and [XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx) class to write the XML back to the package part.</span></span> <span data-ttu-id="b8154-262">Même si vous utilisez la méthode [Save()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx) pour réenregistrer le code XML dans le composant, les classes **XmlWriter** et **XmlWriterSettings** vous permettent de mieux contrôler la sortie, y compris la spécification du type de codage.</span><span class="sxs-lookup"><span data-stu-id="b8154-262">Although you can use the [Save()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx) method to save the XML back to the part, the **XmlWriter** and **XmlWriterSettings** classes allow you finer control over the output, including specifying the type of encoding.</span></span> <span data-ttu-id="b8154-263">La classe **XDocument** présente une méthode [WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx) qui prend un objet **XmlWriter** et réécrit le code XML dans un flux de données.</span><span class="sxs-lookup"><span data-stu-id="b8154-263">The **XDocument** class exposes a [WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx) method that takes an **XmlWriter** object and writes XML back to a stream.</span></span> 
  
<span data-ttu-id="b8154-264">Utilisez la procédure suivante pour enregistrer le code XML à partir de la page Visio sur le composant du contenu de la page.</span><span class="sxs-lookup"><span data-stu-id="b8154-264">Use the following procedure to save the XML from the Visio page back to the Page Contents part.</span></span>
  
### <a name="to-save-the-changed-xml-back-to-the-package"></a><span data-ttu-id="b8154-265">Pour enregistrer à nouveau le code XML modifié dans le package</span><span class="sxs-lookup"><span data-stu-id="b8154-265">To save the changed XML back to the package</span></span>

1. <span data-ttu-id="b8154-266">Après la méthode `GetXElementByAttribute` dans la classe **Program** (ou **Module1** dans Visual Basic) de l’étape précédente, ajoutez la méthode suivante.</span><span class="sxs-lookup"><span data-stu-id="b8154-266">After the  `GetXElementByAttribute` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
    ```cs
    private static void SaveXDocumentToPart(PackagePart packagePart, 
        XDocument partXML)
    {
        
        // Create a new XmlWriterSettings object to 
        // define the characteristics for the XmlWriter
        XmlWriterSettings partWriterSettings = new XmlWriterSettings();
        partWriterSettings.Encoding = Encoding.UTF8;
        // Create a new XmlWriter and then write the XML
        // back to the document part.
        XmlWriter partWriter = XmlWriter.Create(packagePart.GetStream(),
            partWriterSettings);
        partXML.WriteTo(partWriter);
        // Flush and close the XmlWriter.
        partWriter.Flush();
        partWriter.Close();
    }
    ```

    ```vb
    Private Sub SaveXDocumentToPart(packagePart As PackagePart, _
        partXML As XDocument)
        ' Create a new XmlWriterSettings object to 
        ' define the characteristics for the XmlWriter.
        Dim partWriterSettings As XmlWriterSettings = New XmlWriterSettings()
        partWriterSettings.Encoding = Encoding.UTF8
        ' Create a new XmlWriter and then write the XML
        ' back to the document part.
        Dim partWriter As XmlWriter = XmlWriter.Create(packagePart.GetStream())
        partXML.WriteTo(partWriter)
        ' Flush and close the XmlWriter.
        partWriter.Flush()
        partWriter.Close()
    End Sub
    ```

2. <span data-ttu-id="b8154-267">Ajoutez le code suivant au bloc **using** dans la méthode **Main** de la classe **Program** (le bloc **Using** de la méthode **Main** dans **Module1** dans Visual Basic), sous le code de la procédure précédente.</span><span class="sxs-lookup"><span data-stu-id="b8154-267">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> 
    
    ```cs
    // Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML);
    
    ```

    ```vb
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

3. <span data-ttu-id="b8154-p128">Appuyez sur la touche F5 pour déboguer la solution. Lorsque le programme est terminé, appuyez sur une touche pour le quitter.</span><span class="sxs-lookup"><span data-stu-id="b8154-p128">Choose the F5 key to debug the solution. When the program has completed running, choose any key to exit.</span></span>
    
4. <span data-ttu-id="b8154-270">Ouvrez le fichier Visio Package.vsdx dans Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="b8154-270">Open the Visio Package.vsdx file in Visio 2013.</span></span> 
    
<span data-ttu-id="b8154-271">La forme Début/fin doit contenir le texte « Démarrer le processus ».</span><span class="sxs-lookup"><span data-stu-id="b8154-271">The Start/End shape should now contain the text "Start process".</span></span>
  
## <a name="recalculate-data-in-the-file"></a><span data-ttu-id="b8154-272">Recalculer des données dans le fichier</span><span class="sxs-lookup"><span data-stu-id="b8154-272">Recalculate data in the file</span></span>
<span data-ttu-id="b8154-273"><a name="vis15_ManipulateFF_Recalculate"> </a></span><span class="sxs-lookup"><span data-stu-id="b8154-273"><a name="vis15_ManipulateFF_Recalculate"> </a></span></span>

<span data-ttu-id="b8154-274">Certaines modifications apportées aux données dans un fichier peuvent exiger de Visio qu’il recalcule le document lors de l’ouverture du fichier.</span><span class="sxs-lookup"><span data-stu-id="b8154-274">Some changes to the data in a file may require Visio to recalculate the document when it opens the file.</span></span> <span data-ttu-id="b8154-275">Visio propose un grand nombre de logiques pour un diagramme, en particulier pour les relations de la forme (c’est-à-dire, lorsqu’une forme dépend d’une autre) et la connexion des formes.</span><span class="sxs-lookup"><span data-stu-id="b8154-275">Visio provides a lot of logic for a diagram, particularly for shape relationships (that is, when one shape depends on another) and connecting shapes.</span></span> <span data-ttu-id="b8154-276">Si des données sur lesquelles repose la logique personnalisée sont modifiées, Visio doit propager les modifications à toutes les données calculées concernées dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="b8154-276">If any of the data that the custom logic relies upon is changed, Visio needs to propagate the changes to all of the affected calculated data in the file.</span></span> 
  
<span data-ttu-id="b8154-277">Le format de fichier Visio 2013 inclut quelques techniques que vous pouvez utiliser pour recalculer des données dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="b8154-277">The Visio 2013 file format includes a couple of techniques that you can use to recalculate data in the file.</span></span> <span data-ttu-id="b8154-278">Vous devez prendre en compte 3 types de scénarios lorsque vous décidez si vous souhaitez recalculer le fichier Visio et décidez de la façon de procéder :</span><span class="sxs-lookup"><span data-stu-id="b8154-278">There are three types of scenarios that you must consider when you decide whether you need to recalculate the Visio file and how to do it:</span></span>
  
- <span data-ttu-id="b8154-279">Les modifications apportées aux données n’affectent pas les autres valeurs dans le format de fichier.</span><span class="sxs-lookup"><span data-stu-id="b8154-279">The changes to the data do not affect any other values in the file format.</span></span> <span data-ttu-id="b8154-280">Vous n’avez pas besoin d’ajouter des instructions supplémentaires à Visio pour recalculer le document.</span><span class="sxs-lookup"><span data-stu-id="b8154-280">You don't need to add any additional instructions to Visio to recalculate the document.</span></span> <span data-ttu-id="b8154-281">Comme indiqué précédemment, vous pouvez très souvent modifier le texte d’une forme sans avoir à recalculer le document.</span><span class="sxs-lookup"><span data-stu-id="b8154-281">As demonstrated previously, you can often change a shape's text without needing to recalculate the document.</span></span>
    
- <span data-ttu-id="b8154-282">Les modifications apportées aux données sont limitées à la modification des valeurs des cellules ShapeSheet dans le fichier XML, et d’autres valeurs ShapeSheet dépendent de ces données.</span><span class="sxs-lookup"><span data-stu-id="b8154-282">The changes to the data are limited to changing the values of ShapeSheet cells in the XML, and there are other ShapeSheet values that depend on this data.</span></span> <span data-ttu-id="b8154-283">Dans ce cas, vous devez ajouter une instruction de traitement XML (à l’aide de la classe [XProcessingInstruction](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx)) à l’élément **Cell** qui a été modifié.</span><span class="sxs-lookup"><span data-stu-id="b8154-283">In this case, you must add an XML processing instruction (using the [XProcessingInstruction](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx) class) to the **Cell** element that has been changed.</span></span> <span data-ttu-id="b8154-284">Par exemple, la cellule **ThemeIndex** pour une forme affecte les valeurs de plusieurs autres cellules ShapeSheet contenues dans la forme.</span><span class="sxs-lookup"><span data-stu-id="b8154-284">For example, the **ThemeIndex** cell for a shape affects the values of several other ShapeSheet cells contained in the shape.</span></span> <span data-ttu-id="b8154-285">Si vous modifiez la cellule **ThemeIndex** dans le fichier lui-même (par exemple, l’élément **Cell** avec une valeur **N** « ThemeIndex »), vous devez ajouter une instruction de traitement à l’élément **Cell** afin que les valeurs dépendantes soient mises à jour.</span><span class="sxs-lookup"><span data-stu-id="b8154-285">If you change the **ThemeIndex** cell within the file itself (for example, the **Cell** element with an **N** value of "ThemeIndex"), you will need to add a processing instruction to the **Cell** element so that the dependent values are updated.</span></span> 
    
- <span data-ttu-id="b8154-286">Les modifications apportées aux données affectent l’emplacement d’un connecteur ou des points de connexion.</span><span class="sxs-lookup"><span data-stu-id="b8154-286">The changes to the data affect the location of a connector or connection points.</span></span> <span data-ttu-id="b8154-287">Vous pouvez également rencontrer le cas où de nombreuses modifications sont apportées aux données ShapeSheet et vous voulez recalculer l’ensemble du document avec une instruction (au lieu d’ajouter des instructions de traitement individuelles pour chaque modification).</span><span class="sxs-lookup"><span data-stu-id="b8154-287">Another situation is when there are many changes to the ShapeSheet data and you want to recalculate the whole document with one instruction (rather than adding individual processing instructions for each change).</span></span> <span data-ttu-id="b8154-288">Dans ce cas, vous pouvez demander à Visio de recalculer la totalité du document lorsqu’il sera ouvert.</span><span class="sxs-lookup"><span data-stu-id="b8154-288">In this case you can instruct Visio to recalculate the entire document when it is opened.</span></span> <span data-ttu-id="b8154-289">Pour ce faire, ajoutez une propriété **RecalcDocument** au composant Propriétés de fichier personnalisées (/docProps/custom.xml) du package Visio.</span><span class="sxs-lookup"><span data-stu-id="b8154-289">You do this by adding a **RecalcDocument** property to the Custom File Properties part (/docProps/custom.xml) of the Visio package.</span></span> <span data-ttu-id="b8154-290">L’ajustement de la position ou de la taille des formes dans un diagramme lié est un exemple de ce type de scénario.</span><span class="sxs-lookup"><span data-stu-id="b8154-290">Adjusting the position or size of shapes in a connected diagram is an example of this type of scenario.</span></span> 
    
    <span data-ttu-id="b8154-291">N’oubliez pas qu’il s’agit de l’option la plus coûteuse en matière de performances.</span><span class="sxs-lookup"><span data-stu-id="b8154-291">Keep in mind that this is the most costly option from a performance standpoint.</span></span>
    
<span data-ttu-id="b8154-292">Utilisez la procédure suivante pour insérer un élément **Cell** dans un élément **Shape**, où d’autres éléments **Cell** dans le même élément **Shape** doivent être recalculés en raison de la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="b8154-292">Use the following procedure to insert a **Cell** element into a **Shape** element, where other **Cell** elements in the same **Shape** need to be recalculated because of the new value.</span></span> <span data-ttu-id="b8154-293">Le nouvel élément **Cell** inclut une instruction de traitement en tant qu’élément enfant pour informer Visio qu’il doit effectuer un recalcul local.</span><span class="sxs-lookup"><span data-stu-id="b8154-293">The new **Cell** element includes a processing instruction as a child element, to inform Visio that it needs to perform some local recalculation.</span></span> 
  
### <a name="to-recalculate-values-for-a-single-shape"></a><span data-ttu-id="b8154-294">Pour recalculer les valeurs d’une forme unique</span><span class="sxs-lookup"><span data-stu-id="b8154-294">To recalculate values for a single shape</span></span>

1. <span data-ttu-id="b8154-295">Remplacez le code dans les deux exemples précédents (modification du texte de la forme et de l’appel par `SaveXDocumentToPart`) dans le bloc **using** de la méthode **Main** de la classe **Program** (le bloc **Using** de la méthode **Main** dans **Module1** Visual Basic) par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="b8154-295">Replace the code from the previous two examples (changing the shape's text and the call to  `SaveXDocumentToPart`) in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic) with the following code.</span></span> 
    
    ```cs
    // Insert a new Cell element in the Start/End shape that adds an arbitrary
    // local ThemeIndex value. This code assumes that the shape does not 
    // already have a local ThemeIndex cell.
    startEndShapeXML.Add(new XElement("Cell",
        new XAttribute("N", "ThemeIndex"),
        new XAttribute("V", "25"),
        new XProcessingInstruction("NewValue", "V")));
    // Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML);
    
    ```

    ```vb
    ' Insert a new Cell element in the shape that adds an arbitrary local
    ' ThemeIndex value. This code assumes that the shape does not
    ' already have a local ThemeIndex cell.
    startEndShapeXML.Add(New XElement("Cell", _
        New XAttribute("N", "ThemeIndex"),
        New XAttribute("V", "25"),
        New XProcessingInstruction("NewValue", "V")))
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

2. <span data-ttu-id="b8154-p135">Appuyez sur la touche F5 pour déboguer la solution. Lorsque le programme est terminé, appuyez sur une touche pour le quitter.</span><span class="sxs-lookup"><span data-stu-id="b8154-p135">Choose the F5 key to debug the solution. When the program has completed running, choose any key to exit.</span></span>
    
3. <span data-ttu-id="b8154-298">Ouvrez le fichier Visio Package.vsdx dans Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="b8154-298">Open the Visio Package.vsdx file in Visio 2013.</span></span> <span data-ttu-id="b8154-299">La forme Début/fin doit maintenant avoir une couleur de remplissage différente.</span><span class="sxs-lookup"><span data-stu-id="b8154-299">The Start/End shape should now have a different fill color.</span></span>
    
<span data-ttu-id="b8154-300">La couleur de la forme s’appuie sur la valeur de la cellule **ThemeIndex**. Elle détermine les thèmes actifs dont hérite la forme.</span><span class="sxs-lookup"><span data-stu-id="b8154-300">The shape's color relies on the value of the **ThemeIndex** cell—it determines which of the active themes the shape inherits from.</span></span> <span data-ttu-id="b8154-301">Dans l’exemple précédent, la forme est définie pour hériter d’un thème différent (la cellule **ThemeIndex** est définie sur une valeur de « 25 »).</span><span class="sxs-lookup"><span data-stu-id="b8154-301">In the previous example, the shape is set to inherit from a different theme (the **ThemeIndex** cell is set to a value of "25").</span></span> <span data-ttu-id="b8154-302">Si vous n’utilisez pas d’instruction de traitement, la couleur du texte de la forme, qui est également affectée par la cellule **ThemeIndex**, n’est pas recalculée.</span><span class="sxs-lookup"><span data-stu-id="b8154-302">If you don't use a processing instruction, the shape's text color—which is also affected by the **ThemeIndex** cell—isn't recalculated.</span></span> <span data-ttu-id="b8154-303">La couleur de remplissage de la forme devient blanc, mais étant donné que son texte reste blanc, le texte est illisible.</span><span class="sxs-lookup"><span data-stu-id="b8154-303">The shape's fill color would change to white, but its text would remain white—leaving the text unreadable.</span></span> <span data-ttu-id="b8154-304">En outre, sans l’instruction de traitement, Visio risque de mettre à jour la forme ultérieurement, ce qui place le fichier dans un état instable, dans lequel les valeurs de mise en forme de la forme peuvent être mises à jour de manière imprévisible.</span><span class="sxs-lookup"><span data-stu-id="b8154-304">Also, without the processing instruction, it is possible that Visio may update the shape at a later date, leaving the file in an unstable state where the formatting values of the shape could be updated unpredictably.</span></span> 
  
<span data-ttu-id="b8154-305">Si vous modifiez des données dans le fichier et que cette action nécessite que Visio recalcule le document (par exemple, la modification de la position d’une forme liée, entraînant par conséquent une obligation de reroutage des connecteurs), vous devez ajouter une instruction de recalcul au fichier Visio.</span><span class="sxs-lookup"><span data-stu-id="b8154-305">If you change data in the file that requires Visio to recalculate the document (for example, changing a connected shape's position and, therefore, forcing the connectors to reroute), you must add a recalculation instruction to the Visio file.</span></span> <span data-ttu-id="b8154-306">L’instruction est créée en ajoutant un élément **property** avec une valeur d’attribut **name** de « RecalcDocument » au fichier XML du composant Propriétés de fichier personnalisées du package de fichiers Visio.</span><span class="sxs-lookup"><span data-stu-id="b8154-306">The instruction is created by adding a **property** element with a **name** attribute value of "RecalcDocument" to the XML of the Custom File Properties part of the Visio file package.</span></span> <span data-ttu-id="b8154-307">Pour obtenir les meilleurs résultats, vous devez vérifier le composant Propriétés de fichier personnalisées pour vous assurer qu’une instruction « RecalcDocument » n’a pas déjà été enregistrée dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="b8154-307">As a best practice, you should check the Custom File Properties part to be sure that a "RecalcDocument" instruction hasn't already been registered in the file.</span></span> 
  
<span data-ttu-id="b8154-308">Utilisez le code suivant pour modifier la valeur de la cellule **PinY** de la forme de début/fin des exemples précédents.</span><span class="sxs-lookup"><span data-stu-id="b8154-308">Use the following code to change the value of the **PinY** cell of the Start/End shape from the previous examples.</span></span> <span data-ttu-id="b8154-309">Le code sélectionne l’élément **Cell** qui contient les données de la cellule **PinY** en tant qu’objet **XElement** à l’aide de la valeur de son attribut **N**.</span><span class="sxs-lookup"><span data-stu-id="b8154-309">The code selects the **Cell** element that contains the **PinY** cell data as an **XElement** object by using the value of its **N** attribute.</span></span> <span data-ttu-id="b8154-310">Le code ajoute ensuite une instruction de recalcul au composant Propriétés de fichier personnalisées du fichier Visio.</span><span class="sxs-lookup"><span data-stu-id="b8154-310">The code then adds a recalculation instruction to the Custom File Properties part of the Visio file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b8154-311">Ce code repose sur les méthodes `GetPackagePart` et `SaveXDocumentToPart` créées précédemment.</span><span class="sxs-lookup"><span data-stu-id="b8154-311">This code relies on the  `GetPackagePart` and  `SaveXDocumentToPart` methods created previously.</span></span> 
  
### <a name="to-recalculate-the-entire-document-when-it-is-opened"></a><span data-ttu-id="b8154-312">Pour recalculer l’intégralité du document lorsque celui-ci est ouvert</span><span class="sxs-lookup"><span data-stu-id="b8154-312">To recalculate the entire document when it is opened</span></span>

1. <span data-ttu-id="b8154-313">Après la méthode `SaveXDocumentToPart` dans la classe **Program** (ou **Module1** dans Visual Basic) de l’étape précédente, ajoutez la méthode suivante.</span><span class="sxs-lookup"><span data-stu-id="b8154-313">After the  `SaveXDocumentToPart` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
    ```cs
    private static void RecalcDocument(Package filePackage)
    {
        // Get the Custom File Properties part from the package and
        // and then extract the XML from it.
        PackagePart customPart = GetPackagePart(filePackage, 
            "https://schemas.openxmlformats.org/officeDocument/2006/relationships/" + 
            "custom-properties");
        XDocument customPartXML = GetXMLFromPart(customPart);
        // Check to see whether document recalculation has already been 
        // set for this document. If it hasn't, use the integer
        // value returned by CheckForRecalc as the property ID.
        int pidValue = CheckForRecalc(customPartXML);
        if (pidValue > -1)
        {
            XElement customPartRoot = customPartXML.Elements().ElementAt(0);
            // Two XML namespaces are needed to add XML data to this 
            // document. Here, we're using the GetNamespaceOfPrefix and 
            // GetDefaultNamespace methods to get the namespaces that 
            // we need. You can specify the exact strings for the 
            // namespaces, but that is not recommended.
            XNamespace customVTypesNS = customPartRoot.GetNamespaceOfPrefix("vt");
            XNamespace customPropsSchemaNS = customPartRoot.GetDefaultNamespace();
            // Construct the XML for the new property in the XDocument.Add method.
            // This ensures that the XNamespace objects will resolve properly, 
            // apply the correct prefix, and will not default to an empty namespace.
            customPartRoot.Add(
                new XElement(customPropsSchemaNS + "property",
                    new XAttribute("pid", pidValue.ToString()),
                    new XAttribute("name", "RecalcDocument"),
                    new XAttribute("fmtid", 
                        "{D5CDD505-2E9C-101B-9397-08002B2CF9AE}"),
                    new XElement(customVTypesNS + "bool", "true")
                ));
        }
        // Save the Custom Properties package part back to the package.
        SaveXDocumentToPart(customPart, customPartXML);
    }
    ```

    ```vb
    Private Sub RecalcDocument(filePackage As Package)
            ' Get the Custom File Properties part from the package and
            ' then extract the XML from it.
            Dim customPart As PackagePart = GetPackagePart(filePackage, _
                "https://schemas.openxmlformats.org/officeDocument/2006/" + _
                "relationships/custom-properties")
            Dim customPartXML As XDocument = GetXMLFromPart(customPart)
            ' Check to see whether document recalculation has already been
            ' set for this document. If it hasn't, use the integer
            ' value returned by CheckForRecalc as the property ID.
            Dim pidValue As Integer = CheckForRecalc(customPartXML)
            If (pidValue > 1) Then
                Dim customPartRoot As XElement = _
                    customPartXML.Elements().ElementAt(0)
                ' Two XML namespaces are needed to add XML data to this 
                ' document. Here, we're using the GetNamespaceOfPrefix and
                ' GetDefaultNamespace methods to get the namespaces that
                ' we need. You can specify the exact strings for the 
                ' namespaces, but that is not recommended.
                Dim customVTypesNS As XNamespace = _
                    customPartRoot.GetNamespaceOfPrefix("vt")
                Dim customPropsSchemaNS As XNamespace = _
                    customPartRoot.GetDefaultNamespace()
                ' Contruct the XML for the new property in the XDocument.Add
                ' method. This ensures that the XML namespaces resolve 
                ' properly, apply the correct prefix, and do not default to 
                ' an empty namespace.
                customPartRoot.Add( _
                    New XElement(customPropsSchemaNS + "property", _
                        New XAttribute("pid", pidValue.ToString()), _
                        New XAttribute("name", "RecalcDocument"), _
                        New XAttribute("fmtid", _
                            "{D5CDD505-2E9C-101B-9397-08002B2CF9AE}"), _
                        New XElement(customVTypesNS + "bool", "true") _
                ))
            ' Save the Custom Properties package part back to the package.
            SaveXDocumentToPart(customPart, customPartXML)
            End If
        End Sub
    ```

2. <span data-ttu-id="b8154-314">Après la méthode `RecalcDocument` dans la classe **Program** (ou **Module1** dans Visual Basic) de l’étape précédente, ajoutez la méthode suivante.</span><span class="sxs-lookup"><span data-stu-id="b8154-314">After the  `RecalcDocument` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
    ```cs
    private static int CheckForRecalc(XDocument customPropsXDoc) 
    {
        
        // Set the inital pidValue to -1, which is not an allowed value.
        // The calling code tests to see whether the pidValue is 
        // greater than -1.
        int pidValue = -1;
        // Get all of the property elements from the document. 
        IEnumerable<XElement> props = GetXElementsByName(
            customPropsXDoc, "property");
        // Get the RecalcDocument property from the document if it exists already.
        XElement recalcProp = GetXElementByAttribute(props, 
            "name", "RecalcDocument");
        // If there is already a RecalcDocument instruction in the 
        // Custom File Properties part, then we don't need to add another one. 
        // Otherwise, we need to create a unique pid value.
        if (recalcProp != null)
        {
            return pidValue;
        }
        else
        {
            // Get all of the pid values of the property elements and then
            // convert the IEnumerable object into an array.
            IEnumerable<string> propIDs = 
                from prop in props
                where prop.Name.LocalName == "property"
                select prop.Attribute("pid").Value;
            string[] propIDArray = propIDs.ToArray();
            // Increment this id value until a unique value is found.
            // This starts at 2, because 0 and 1 are not valid pid values.
            int id = 2;
            while (pidValue == -1)
            {
                if (propIDArray.Contains(id.ToString()))
                {
                    id++;
                }
                else
                {
                    pidValue = id;
                }
            }
        }
        return pidValue;
    }
    
    ```

    ```vb
    Private Function CheckForRecalc(customPropsXDoc As XDocument) As Integer
        ' Set the initial pidValue to -1, which is not an allowed value. 
        ' The calling code test to see whether the pidValue is
        ' greater than -1.
        Dim pidValue As Integer = -1
        ' Get all of the property elements from the document.
        Dim props As IEnumerable(Of XElement) = GetXElementsByName( _
            customPropsXDoc, "property")
        ' Get the RecalcDocument property from the document if 
        ' it exists already.
        Dim recalcProp As XElement = GetXElementByAttribute(props, _
            "name", "RecalcDocument")
        ' If there is already a RecalcDocument instruction in the 
        ' Custom File Properties part, then we don't need another one.
        ' Otherwise, we need to create a unique pid value.
        If Not IsNothing(recalcProp) Then
            Return pidValue
        Else
            ' Get all of the pid values of the proeprty elements and then
            ' convert the IEnumerable object into an array.
            Dim propIDs As IEnumerable(Of String) = _
            From prop In props
            Where prop.Name.LocalName = "property"
            Select prop.Attribute("pid").Value
            Dim propIDArray As String() = propIDs.ToArray()
            ' Increment this id value until a unique value is found.
            ' This starts at 2, because 0 and 1 are not valid pid values.
            Dim id As Integer = 2
            While (pidValue = -1)
                If (propIDArray.Contains(id.ToString())) Then
                    id = id + 1
                Else
                    pidValue = id
                End If
            End While
        End If
        Return pidValue
    End Function
    ```

3. <span data-ttu-id="b8154-315">Remplacez le code de l’exemple précédent dans le bloc **using** de la méthode **Main** de la classe **Program** (le bloc **Using** de la méthode **Main** dans **Module1** dans Visual Basic) par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="b8154-315">Replace the code from the previous example in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), with the following code.</span></span> 
    
    ```cs
    // Change the shape's horizontal position on the page 
    // by getting a reference to the Cell element for the PinY 
    // ShapeSheet cell and changing the value of its V attribute.
    XElement pinYCellXML = GetXElementByAttribute(
        startEndShapeXML.Elements(), "N", "PinY");
    pinYCellXML.SetAttributeValue("V", "2");
    // Add instructions to Visio to recalculate the entire document
    // when it is next opened.
    RecalcDocument(visioPackage);
    // Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML);
    
    ```

    ```vb
    ' Change the shape's horizontal position on the page
    ' by getting a reference to the Cell element for the PinY
    ' ShapeSheet cell and changing the value of its V attribute.
    Dim pinYCellXML As XElement = GetXElementByAttribute(
        startEndShapeXML.Elements(), "N", "PinY")
    pinYCellXML.SetAttributeValue("V", "2")
    ' Add instructions to Visio to recalculate the entire document
    ' when it is next opened.
    RecalcDocument(visioPackage)
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

4. <span data-ttu-id="b8154-p140">Appuyez sur la touche F5 pour déboguer la solution. Lorsque le programme est terminé, appuyez sur une touche pour le quitter.</span><span class="sxs-lookup"><span data-stu-id="b8154-p140">Choose the F5 key to debug the solution. When the program has completed running, choose any key to exit.</span></span>
    
5. <span data-ttu-id="b8154-318">Ouvrez le fichier Visio Package.vsdx dans Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="b8154-318">Open the Visio Package.vsdx file in Visio 2013.</span></span> 
    
<span data-ttu-id="b8154-p141">La forme Début/fin doit maintenant être à 2 pouces du bord inférieur du dessin. Le connecteur entre la forme Début/fin et la forme Processus doit avoir été redirigé pour prendre en charge la modification de la mise en page. Si la propriété **RecalcDocument** n’avait pas été ajoutée au fichier, la position de la forme aurait été modifiée, mais le connecteur n’aurait pas été redirigé vers le nouvel emplacement de la forme.</span><span class="sxs-lookup"><span data-stu-id="b8154-p141">The Start/End shape should now be 2 inches from the bottom edge of the drawing. The connector between the Start/End shape and the Process shape should have rerouted to accommodate the change in layout. If the **RecalcDocument** property had not been added to the file, the shape position would have been changed, but the connector would not have rerouted to the new location of the shape.</span></span> 
  
## <a name="add-a-new-package-part-to-a-package"></a><span data-ttu-id="b8154-322">Ajouter un nouveau composant à un package</span><span class="sxs-lookup"><span data-stu-id="b8154-322">Add a new package part to a package</span></span>
<span data-ttu-id="b8154-323"><a name="vis15_ManipulateFF_AddNewPart"> </a></span><span class="sxs-lookup"><span data-stu-id="b8154-323"><a name="vis15_ManipulateFF_AddNewPart"> </a></span></span>

<span data-ttu-id="b8154-324">L’un des scénarios les plus courants pour modifier un package de fichiers est d’ajouter un nouveau composant de document au package.</span><span class="sxs-lookup"><span data-stu-id="b8154-324">One of the most common scenarios for modifying a file package is adding a new document part to the package.</span></span> <span data-ttu-id="b8154-325">Par exemple, si vous voulez ajouter une page au dessin Visio en ajoutant du contenu au package, vous devez ajouter un composant du contenu de la page au package.</span><span class="sxs-lookup"><span data-stu-id="b8154-325">For example, if you want to add a page to the Visio drawing by adding content to the package, you need to add a Page Contents part to the package.</span></span> 
  
<span data-ttu-id="b8154-326">Le processus d’ajout d’un nouveau composant au package est simple :</span><span class="sxs-lookup"><span data-stu-id="b8154-326">The process for adding a new part to the package is straightforward:</span></span> 
  
1. <span data-ttu-id="b8154-p143">Vous créez le document XML avec les données de **PackagePart**. Vous devez prêter une attention particulière aux espaces de noms XML qui régissent le schéma pour le type spécifique de document XML que vous créez.</span><span class="sxs-lookup"><span data-stu-id="b8154-p143">You create the XML document with the data for the **PackagePart**. You need to pay special attention to the XML namespaces that govern the schema for the specific type of XML document that you create.</span></span>
    
2. <span data-ttu-id="b8154-329">Vous créez un fichier pour contenir le code XML et enregistrez le fichier sur un emplacement dans le **Package**.</span><span class="sxs-lookup"><span data-stu-id="b8154-329">You create a new file to contain the XML and save the file to a location in the **Package**.</span></span>
    
3. <span data-ttu-id="b8154-330">Vous créez les relations nécessaires entre le nouveau **PackagePart** et le **Package** ou d’autres objets **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="b8154-330">You create the necessary relationships between the new **PackagePart** and the **Package** or other **PackagePart** objects.</span></span> 
    
4. <span data-ttu-id="b8154-p144">Vous mettez à jour des composants existants qui doivent faire référence au nouveau composant. Par exemple, si vous ajoutez un nouveau composant de contenu de la page (une nouvelle page) dans le fichier, vous devez également mettre à jour le composant d’index de la page (fichier /visio/pages/pages.xml) pour inclure les informations correctes à propos de la nouvelle page.</span><span class="sxs-lookup"><span data-stu-id="b8154-p144">You update any existing parts that need to reference the new part. For example, if you add a new Page Contents part (a new page) to the file, you also need to update the Page Index part (/visio/pages/pages.xml file) to include the correct information about the new page.</span></span>
    
<span data-ttu-id="b8154-333">La procédure suivante permet de créer un composant d’extensibilité du ruban dans le fichier Visio.</span><span class="sxs-lookup"><span data-stu-id="b8154-333">Use the following procedure to create a new Ribbon Extensibility part in the Visio file.</span></span> <span data-ttu-id="b8154-334">Le nouveau composant d’extensibilité du ruban ajoute au ruban un nouvel onglet avec un seul groupe contenant un seul bouton.</span><span class="sxs-lookup"><span data-stu-id="b8154-334">The new Ribbon Extensibility part adds to the ribbon a new tab with a single group that contains a single button.</span></span>
  
### <a name="to-create-a-new-package-part"></a><span data-ttu-id="b8154-335">Pour créer un composant de package</span><span class="sxs-lookup"><span data-stu-id="b8154-335">To create a new package part</span></span>

1. <span data-ttu-id="b8154-336">Après la méthode `CheckForRecalc` dans la classe **Program** (ou **Module1** dans Visual Basic) de la procédure précédente, ajoutez la méthode suivante.</span><span class="sxs-lookup"><span data-stu-id="b8154-336">After the  `CheckForRecalc` method in the **Program** class (or **Module1** in Visual Basic) from the previous procedure, add the following method.</span></span> 
    
    ```cs
    private static XDocument CreateCustomUI()
    {
        // Add a new Custom User Interface document part to the package.
        // This code adds a new CUSTOM tab to the ribbon for this
        // document. The tab has one group that contains one button.
        XNamespace customUINS = 
            "http://schemas.microsoft.com/office/2006/01/customui";
        XDocument customUIXDoc = new XDocument(
            new XDeclaration("1.0", "utf-8", "true"),
            new XElement(customUINS + "customUI",
                new XElement(customUINS + "ribbon",
                    new XElement(customUINS + "tabs",
                        new XElement(customUINS + "tab",
                            new XAttribute("id", "customTab"),
                            new XAttribute("label", "CUSTOM"),
                            new XElement(customUINS + "group",
                                new XAttribute("id", "customGroup"),
                                new XAttribute("label", "Custom Group"),
                                new XElement(customUINS + "button",
                                    new XAttribute("id", "customButton"),
                                    new XAttribute("label", "Custom Button"),
                                    new XAttribute("size", "large"),
                                    new XAttribute("imageMso", "HappyFace")
                                )
                            )
                        )
                    )
                )
            )
        );
        return customUIXDoc;
    }
    ```

    ```vb
    Private Function CreateCustomUI() As XDocument
        ' Add a new Custom User Interface document part to the package.
        ' This code adds a new CUSTOM tab to the ribbon for this
        ' document. The tab has one group that contains one button.
        Dim customUINS As XNamespace = _
            "http://schemas.microsoft.com/office/2006/01/customui"
        Dim customUIXML = New XDocument( _
            New XDeclaration("1.0", "utf-8", "true"), _
            New XElement(customUINS + "customUI", _
                New XElement(customUINS + "ribbon",
                    New XElement(customUINS + "tabs",
                        New XElement(customUINS + "tab",
                            New XAttribute("id", "customTab"),
                            New XAttribute("label", "CUSTOM"),
                            New XElement(customUINS + "group",
                                New XAttribute("id", "customGroup"),
                                New XAttribute("label", "Custom Group"),
                                New XElement(customUINS + "button",
                                    New XAttribute("id", "customButton"),
                                    New XAttribute("label", "Custom Button"),
                                    New XAttribute("size", "large"),
                                    New XAttribute("imageMso", "HappyFace")
                                )
                            )
                        )
                    )
                )
            )
        )
        Return customUIXML
    End Function
    ```

2. <span data-ttu-id="b8154-337">Après la méthode `CreateCustomUI` dans la classe **Program** (ou **Module1** dans Visual Basic) de l’étape précédente, ajoutez la méthode suivante.</span><span class="sxs-lookup"><span data-stu-id="b8154-337">After the  `CreateCustomUI` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
    ```cs
    private static void CreateNewPackagePart(Package filePackage, 
        XDocument partXML, Uri packageLocation, string contentType, 
        string relationship)
    {
        // Need to check first to see whether the part exists already.
        if (!filePackage.PartExists(packageLocation))
        {
            // Create a new blank package part at the specified URI 
            // of the specified content type.
            PackagePart newPackagePart = filePackage.CreatePart(packageLocation,
                contentType);
            // Create a stream from the package part and save the 
            // XML document to the package part.
            using (Stream partStream = newPackagePart.GetStream(FileMode.Create,
                FileAccess.ReadWrite))
            {
                partXML.Save(partStream);
            }
        }
        // Add a relationship from the file package to this
        // package part. You can also create relationships
        // between an existing package part and a new part.
        filePackage.CreateRelationship(packageLocation,
            TargetMode.Internal,
            relationship);
    }
    ```

    ```vb
    Private Sub CreateNewPackagePart(filePackage As Package, _
        partXML As XDocument, packageLocation As Uri, contentType As String, _
        relationship As String)
        ' Need to check first to see whether the part exists already.
        If Not (filePackage.PartExists(packageLocation)) Then
            ' Create a new blank package part at the specified URI
            ' of the specified content type.
            Dim newPart As PackagePart = filePackage.CreatePart(packageLocation, _
                contentType)
            ' Create a stream from the package part and save the
            ' XML document to the package part.
            Using partStream As Stream = newPart.GetStream(FileMode.Create, _
                FileAccess.ReadWrite)
                partXML.Save(partStream)
            End Using
            ' Add a relationship from the file package to this
            ' package part. You can also create relationships
            ' between an existing package part and a new part.
            filePackage.CreateRelationship(packageLocation, _
                TargetMode.Internal, relationship)
        End If
    End Sub
    ```

3. <span data-ttu-id="b8154-338">Remplacez tout le code dans le bloc **using** de la méthode **Main** de la classe **Program** (le bloc **Using** de la méthode **Main** dans **Module1** dans Visual Basic) par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="b8154-338">Replace all the code in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), with the following code.</span></span> 
    
    ```cs
    // Create a new Ribbon Extensibility part and add it to the file.
    XDocument customUIXML = CreateCustomUI();
    CreateNewPackagePart(visioPackage, customUIXML, 
        new Uri("/customUI/customUI1.xml", UriKind.Relative),
        "application/xml",
        "http://schemas.microsoft.com/office/2006/relationships/ui/extensibility");
    ```

    ```vb
    ' Create a new Ribbon Extensibility part and add it to the file.
    Dim customUIXML As XDocument = CreateCustomUI()
    CreateNewPackagePart(visioPackage, customUIXML, _
        New Uri("/customUI/customUI1.xml", UriKind.Relative), _
        "application/xml", _
        "http://schemas.microsoft.com/office/2006/relationships/ui/extensibility")
    ```

4. <span data-ttu-id="b8154-p146">Appuyez sur la touche F5 pour déboguer la solution. Lorsque le programme est terminé, appuyez sur une touche pour le quitter.</span><span class="sxs-lookup"><span data-stu-id="b8154-p146">Choose the F5 key to debug the solution. When the program has completed running, choose any key to exit.</span></span>
    
5. <span data-ttu-id="b8154-341">Ouvrez le fichier Visio Package.vsdx dans Visio 2013, puis choisissez l’onglet **PERSONNALISÉ**.</span><span class="sxs-lookup"><span data-stu-id="b8154-341">Open the Visio Package.vsdx file in Visio 2013, and then choose the **CUSTOM** tab.</span></span> 
    
<span data-ttu-id="b8154-342">Le ruban personnalisé ressemble à la figure 2 lorsque le fichier est ouvert dans Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="b8154-342">The custom ribbon looks like Figure 2 when the file is opened in Visio 2013.</span></span>
  
 <span data-ttu-id="b8154-343">**Figure 2. Onglet Personnalisé dans le ruban de Visio 2013**</span><span class="sxs-lookup"><span data-stu-id="b8154-343">**Figure 2. Custom tab in the Visio 2013 ribbon**</span></span>
  
![Onglet Personnalisé dans le ruban](media/vis15_CustomRibbonTab.PNG)
  
<span data-ttu-id="b8154-345">Le fichier XML créé par la méthode `CreateCustomUI` se présente comme suit.</span><span class="sxs-lookup"><span data-stu-id="b8154-345">The XML created by the  `CreateCustomUI` method looks like the following.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<customUI xmlns="http://schemas.microsoft.com/office/2006/01/customui">
  <ribbon>
    <tabs>
      <tab id="customTab" label="CUSTOM">
        <group id="customGroup" label="Custom Group">
          <button id="customButton" label="Custom Button" size="large"
              imageMso="HappyFace" />
        </group>
      </tab>
    </tabs>
  </ribbon>
</customUI>
```

## <a name="acknowledgements"></a><span data-ttu-id="b8154-346">Remerciements</span><span class="sxs-lookup"><span data-stu-id="b8154-346">Acknowledgements</span></span>
<span data-ttu-id="b8154-347"><a name="vis15_ManipulateFF_Ackn"> </a></span><span class="sxs-lookup"><span data-stu-id="b8154-347"><a name="vis15_ManipulateFF_Ackn"> </a></span></span>

<span data-ttu-id="b8154-348">Nous aimerions saluer la contribution et les apports de Visio MVP **Al Edlund** pour la création d’exemples de code contenus dans cet article technique.</span><span class="sxs-lookup"><span data-stu-id="b8154-348">We would like to recognize the contribution and input of Visio MVP **Al Edlund** in creating the code examples contained in this technical article.</span></span> <span data-ttu-id="b8154-349">Al est un expert reconnu dans la manipulation du format de fichier Visio, y compris le format de dessin Visio XML (.vdx) et le nouveau format de fichier Visio (.vsdx).</span><span class="sxs-lookup"><span data-stu-id="b8154-349">Al is a recognized expert in manipulating the Visio file format, including both the Visio XML Drawing format (.vdx) and the new Visio file format (.vsdx).</span></span> <span data-ttu-id="b8154-350">Al a créé des projets qui permettent d’explorer les formats de fichier Visio par programme et présente les structures à l’intérieur.</span><span class="sxs-lookup"><span data-stu-id="b8154-350">Al has created projects that explore the Visio file formats programmatically and exposes the structures inside.</span></span> 
  
<span data-ttu-id="b8154-351">Pour plus d’informations sur son travail avec le format de fichier Visio, consultez les liens dans la section Ressources supplémentaires ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b8154-351">For more information about Al's work with the Visio file format, see the links in the Additional Resources section that follows.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b8154-352">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8154-352">See also</span></span>
<span data-ttu-id="b8154-353"><a name="vis15_ManipulateFF_Additional"> </a></span><span class="sxs-lookup"><span data-stu-id="b8154-353"><a name="vis15_ManipulateFF_Additional"> </a></span></span>

- <span data-ttu-id="b8154-354">Par Al Edlund :</span><span class="sxs-lookup"><span data-stu-id="b8154-354">By Al Edlund:</span></span>
    
  - <span data-ttu-id="b8154-355">[pkgVisio - Manipulation du code XML dans Visio 2013](https://pkgvisio.codeplex.com/documentation) projet sur CodePlex.</span><span class="sxs-lookup"><span data-stu-id="b8154-355">[pkgVisio - Visio 2013 XML manipulation](https://pkgvisio.codeplex.com/documentation) project on CodePlex.</span></span> 
    
  - <span data-ttu-id="b8154-356">[pkgVisio_pt1 ](https://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be) vidéo sur YouTube.</span><span class="sxs-lookup"><span data-stu-id="b8154-356">[pkgVisio_pt1 ](https://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be) video on YouTube.</span></span> 
    
  - <span data-ttu-id="b8154-357">[pkgVisio_pt2 ](https://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be) vidéo sur YouTube.</span><span class="sxs-lookup"><span data-stu-id="b8154-357">[pkgVisio_pt2 ](https://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be) video on YouTube.</span></span> 
    
- [<span data-ttu-id="b8154-358">Centre de développement Visio</span><span class="sxs-lookup"><span data-stu-id="b8154-358">Visio Developer Center</span></span>](https://msdn.microsoft.com/office/aa905478.aspx)
    
- [<span data-ttu-id="b8154-359">Manipuler des documents au format Open Office XML</span><span class="sxs-lookup"><span data-stu-id="b8154-359">Manipulate Office Open XML Formats Documents</span></span>](https://msdn.microsoft.com/library/aa982683%28v=office.12%29.aspx)
    
- [<span data-ttu-id="b8154-360">Créer un document avec des espaces de noms (C#) (LINQ vers XML)</span><span class="sxs-lookup"><span data-stu-id="b8154-360">Create a Document with Namespaces (C#) (LINQ to XML)</span></span>](https://msdn.microsoft.com/library/bb387075.aspx)
    
- [<span data-ttu-id="b8154-361">Ajouter des composants XML personnalisés à des documents sans démarrer Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="b8154-361">Add Custom XML Parts to Documents Without Starting Microsoft Office</span></span>](https://msdn.microsoft.com/library/bb608597%28VS.90%29.aspx)
    

