---
title: Présentation du format de fichier Visio (.vsdx)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 69736f40-8f67-46c2-abf6-82dffecb2274
description: Découvrez le nouveau format de fichier dans Visio 2013, explorez certains concepts généraux relatifs à l’utilisation par programme le format de fichier Visio 2013 et créer une application de console simple qui examine un fichier Visio 2013.
ms.openlocfilehash: 4efa90ee513def005653f4f8717b0149de1cdc3d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389364"
---
# <a name="introduction-to-the-visio-file-format-vsdx"></a><span data-ttu-id="3e64b-103">Présentation du format de fichier Visio (.vsdx)</span><span class="sxs-lookup"><span data-stu-id="3e64b-103">Introduction to the Visio file format (.vsdx)</span></span>

<span data-ttu-id="3e64b-104">Découvrez le nouveau format de fichier dans Visio 2013, explorez certains concepts généraux relatifs à l’utilisation par programme le format de fichier Visio 2013 et créer une application de console simple qui examine un fichier Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="3e64b-104">Learn about the new file format in Visio 2013, explore some high-level concepts for working with the Visio 2013 file format programmatically, and create a simple console application that examines a Visio 2013 file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3e64b-105">**Dans cet article** [Présentation](#vis15_IntroVSDX_Intro) [Quel est le format de fichier Visio 2013 « à la Loupe » ?](#vis15_IntroVSDX_What)                   </span><span class="sxs-lookup"><span data-stu-id="3e64b-105">**In this article**         [Introduction](#vis15_IntroVSDX_Intro)          [What is the Visio 2013 file format "under the hood"?](#vis15_IntroVSDX_What)</span></span>          <span data-ttu-id="3e64b-106">[Scénarios de développement pour l’utilisation du format de fichier Visio 2013](#vis15_IntroVSDX_Scenarios) [Exploration du format de fichier Visio 2013 par programme](#vis15_IntroVSDX_Explore) [Ressources supplémentaires](#vis15_IntroVSDX_Resources)                    </span><span class="sxs-lookup"><span data-stu-id="3e64b-106">[Developer scenarios for working with the Visio 2013 file format](#vis15_IntroVSDX_Scenarios)          [Exploring the Visio 2013 file format programmatically](#vis15_IntroVSDX_Explore)          [Additional resources](#vis15_IntroVSDX_Resources)</span></span>||
   
## <a name="introduction"></a><span data-ttu-id="3e64b-107">Introduction</span><span class="sxs-lookup"><span data-stu-id="3e64b-107">Introduction</span></span>
<span data-ttu-id="3e64b-108"><a name="vis15_IntroVSDX_Intro"> </a></span><span class="sxs-lookup"><span data-stu-id="3e64b-108"></span></span>

<span data-ttu-id="3e64b-109">Visio 2013 introduit un nouveau format de fichier (.vsdx) pour Visio qui remplace le format de fichier binaire Visio (.vsd) et le format de fichier de dessin de Visio XML (.vdx).</span><span class="sxs-lookup"><span data-stu-id="3e64b-109">Visio 2013 introduces a new file format (.vsdx) for Visio that replaces the Visio binary file format (.vsd) and Visio XML Drawing file format (.vdx).</span></span> <span data-ttu-id="3e64b-110">Car le format de fichier Visio 2013 repose sur Open Packaging Conventions et XML, les développeurs qui sont familiarisés avec ces technologies peuvent rapidement comment travailler avec des fichiers Visio 2013 par programmation.</span><span class="sxs-lookup"><span data-stu-id="3e64b-110">Because the Visio 2013 file format is based upon Open Packaging Conventions and XML, developers who are familiar with these technologies can quickly learn how to work with Visio 2013 files programmatically.</span></span> <span data-ttu-id="3e64b-111">Les développeurs qui sont familiarisés avec le format de fichier de dessin de Visio XML (.vdx) à partir de versions antérieures de Visio trouverez nombre des mêmes structures XML dans les composants du format de fichier .vsdx.</span><span class="sxs-lookup"><span data-stu-id="3e64b-111">Developers who are familiar with the Visio XML Drawing file format (.vdx) from previous versions of Visio can find many of the same XML structures within the parts of .vsdx file format.</span></span> <span data-ttu-id="3e64b-112">Interopérabilité avec les fichiers Visio est considérablement plue complexe car les logiciels tiers peuvent manipuler les fichiers à un niveau de format de fichier Visio.</span><span class="sxs-lookup"><span data-stu-id="3e64b-112">Interoperability with Visio files is greatly increased since third-party software can manipulate Visio files at a file format level.</span></span> <span data-ttu-id="3e64b-113">Le format de fichier Visio 2013 est pris en charge sur Visio Services dans Microsoft SharePoint Server 2013, sans avoir besoin d’un format de fichier « intermédiaire » pour la publication vers SharePoint Server.</span><span class="sxs-lookup"><span data-stu-id="3e64b-113">The Visio 2013 file format is supported on Visio Services in Microsoft SharePoint Server 2013, without the need of an "intermediary" file format for publishing to SharePoint Server.</span></span>
  
<span data-ttu-id="3e64b-114">Il existe plusieurs types de fichier, par extension, qui composent le format de fichier Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="3e64b-114">There are several file types, by extension, that comprise the Visio 2013 file format.</span></span> <span data-ttu-id="3e64b-115">Ces extensions sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3e64b-115">These extensions include:</span></span>
  
- <span data-ttu-id="3e64b-116">.vsdx (dessin Visio)</span><span class="sxs-lookup"><span data-stu-id="3e64b-116">.vsdx (Visio drawing)</span></span>
    
- <span data-ttu-id="3e64b-117">.vsdm (Dessin Visio prenant en charge les macros)</span><span class="sxs-lookup"><span data-stu-id="3e64b-117">.vsdm (Visio macro-enabled drawing)</span></span>
    
- <span data-ttu-id="3e64b-118">.vssx (Gabarit Visio)</span><span class="sxs-lookup"><span data-stu-id="3e64b-118">.vssx (Visio stencil)</span></span>
    
- <span data-ttu-id="3e64b-119">.vssm (Gabarit Visio prenant en charge les macros)</span><span class="sxs-lookup"><span data-stu-id="3e64b-119">.vssm (Visio macro-enabled stencil)</span></span>
    
- <span data-ttu-id="3e64b-120">.vstx (Modèle Visio)</span><span class="sxs-lookup"><span data-stu-id="3e64b-120">.vstx (Visio template)</span></span>
    
- <span data-ttu-id="3e64b-121">.vstm (Modèle Visio prenant en charge les macros)</span><span class="sxs-lookup"><span data-stu-id="3e64b-121">.vstm (Visio macro-enabled template)</span></span>
    
> [!NOTE]
> <span data-ttu-id="3e64b-p104">Seuls les fichiers prenant en charge les macros (.vsdm, .vssm et .vstm) peuvent contenir des macros VBA. Il est impossible d'enregistrer des macros dans des fichiers dont l'extension est .vsdx, .vssx ou .vstx.</span><span class="sxs-lookup"><span data-stu-id="3e64b-p104">Only the macro-enabled files (.vsdm, .vssm, .vstm) can store VBA macros. You cannot store macros in files with a .vsdx, .vssx, or .vstx extension.</span></span> 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a><span data-ttu-id="3e64b-124">Quel est le format de fichier Visio 2013 « à la Loupe » ?</span><span class="sxs-lookup"><span data-stu-id="3e64b-124">What is the Visio 2013 file format "under the hood"?</span></span>
<span data-ttu-id="3e64b-125"><a name="vis15_IntroVSDX_What"> </a></span><span class="sxs-lookup"><span data-stu-id="3e64b-125"></span></span>

<span data-ttu-id="3e64b-126">Le format de fichier Visio 2013 utilise Open livraison Conventions (OPC), qui définit un moyen structuré pour stocker les données d’application avec les ressources associées à l’aide d’un conteneur de certains sort─for exemple, un fichier ZIP.</span><span class="sxs-lookup"><span data-stu-id="3e64b-126">The Visio 2013 file format uses the Open Packing Conventions (OPC), which defines a structured means to store application data together with related resources using a container of some sort─for example, a ZIP file.</span></span> <span data-ttu-id="3e64b-127">Un niveau de base, un fichier Visio 2013 est réellement un conteneur ZIP qui contient d’autres types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3e64b-127">At a basic level, a Visio 2013 file is really a ZIP container that contains other types of files.</span></span> <span data-ttu-id="3e64b-128">En fait, vous pouvez enregistrer un dessin dans Visio 2013 en tant que fichier .vsdx, renommer l’extension de fichier à «\*.zip » dans l’Explorateur Windows et puis ouvrez le fichier comme un dossier pour afficher le contenu à l’intérieur.</span><span class="sxs-lookup"><span data-stu-id="3e64b-128">In fact, you can save a drawing in Visio 2013 as a .vsdx file, rename the file extension to "\*.zip" in Windows Explorer, and then open the file like a folder to see the contents inside.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="3e64b-129">Cet article contient uniquement une vue d’ensemble de l’Open Packaging Conventions.</span><span class="sxs-lookup"><span data-stu-id="3e64b-129">This article contains only a brief overview of the Open Packaging Conventions.</span></span> <span data-ttu-id="3e64b-130">Vous trouverez plus détaillée des conventions dans d’autres articles de la couverture : > Pour plus d’informations sur l’Open Packaging Conventions, consultez la rubrique [OPC : une nouvelle norme pour l’empaquetage de vos données](https://msdn.microsoft.com/magazine/cc163372.aspx).</span><span class="sxs-lookup"><span data-stu-id="3e64b-130">You can find more detailed coverage of the conventions in other articles: >  For more information about the Open Packaging Conventions themselves, see [OPC: A New Standard for Packaging Your Data](https://msdn.microsoft.com/magazine/cc163372.aspx).</span></span> <span data-ttu-id="3e64b-131">> Pour plus d’informations sur l’Open Packaging Conventions et leur utilisation dans les fichiers Microsoft Office, voir [Notions essentielles de l’Open Packaging Conventions](https://msdn.microsoft.com/library/ee361919.aspx) et [Présentation des Formats XML ouverts Office (2007)](https://msdn.microsoft.com/library/aa338205.aspx).</span><span class="sxs-lookup"><span data-stu-id="3e64b-131">>  For more information about the Open Packaging Conventions and their use in Microsoft Office files, see [Essentials of the Open Packaging Conventions](https://msdn.microsoft.com/library/ee361919.aspx) and [Introducing the Office (2007) Open XML File Formats](https://msdn.microsoft.com/library/aa338205.aspx).</span></span> 
  
### <a name="packages-and-package-parts"></a><span data-ttu-id="3e64b-132">Packages et parties de packages</span><span class="sxs-lookup"><span data-stu-id="3e64b-132">Packages and Package Parts</span></span>

<span data-ttu-id="3e64b-133">Comme démarré précédemment, fichiers Visio 2013 sont des conteneurs ZIP ou des « packages » contenant les autres fichiers (appelées « parties de package ») au sein de celles-ci.</span><span class="sxs-lookup"><span data-stu-id="3e64b-133">As started earlier, Visio 2013 files are ZIP containers or "packages" that hold other files (called "package parts") within them.</span></span> <span data-ttu-id="3e64b-134">Un composant de package peut être un fichier XML, une image, même une solution VBA.</span><span class="sxs-lookup"><span data-stu-id="3e64b-134">A package part can be an XML file, an image, even a VBA solution.</span></span> <span data-ttu-id="3e64b-135">Les composants dans le package peuvent être réparties en deux grandes catégories, « parties de document » et « composants de relation ».</span><span class="sxs-lookup"><span data-stu-id="3e64b-135">The parts within the package can be further divided into two broad categories, "document parts" and "relationship parts."</span></span> <span data-ttu-id="3e64b-136">Les parties du document contient le contenu et les métadonnées du fichier Visio, telles que le nom du fichier, la première page et toutes les formes qu’il contient, et même les connexions de données pour les formes.</span><span class="sxs-lookup"><span data-stu-id="3e64b-136">The document parts contain the actual content and metadata of the Visio file, like the name of the file, the first page and all of the shapes that it contains, and even the data connections for the shapes.</span></span> <span data-ttu-id="3e64b-137">Images et des fichiers texte dans le package sont considérés comme des parties de document.</span><span class="sxs-lookup"><span data-stu-id="3e64b-137">Images and text files within the package are considered document parts.</span></span> <span data-ttu-id="3e64b-138">Composants de relation sont décrites plus en détail plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="3e64b-138">Relationship parts are described in more detail later in this article.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3e64b-139">Si vous ouvrez un fichier Visio 2013 à l’aide d’un utilitaire de compression, vous pouvez voir probablement plusieurs dossiers contenus dans le package ZIP.</span><span class="sxs-lookup"><span data-stu-id="3e64b-139">If you open a Visio 2013 file using a ZIP utility, you can probably see several folders contained inside of the ZIP package.</span></span> <span data-ttu-id="3e64b-140">Vous pouvez même manipuler ces adresses sous-sites tels que des dossiers à l’aide d’un utilitaire ZIP.</span><span class="sxs-lookup"><span data-stu-id="3e64b-140">You can even manipulate these sub-addresses like folders using a ZIP utility.</span></span> <span data-ttu-id="3e64b-141">Toutefois, ces « dossiers » représentent des adresses de sous-sites dans le package ZIP, dossiers pas réels.</span><span class="sxs-lookup"><span data-stu-id="3e64b-141">However, these "folders" represent sub-addresses within the ZIP package, not actual folders.</span></span> <span data-ttu-id="3e64b-142">Vous ne pouvez pas utiliser les équivalents par programmation des dossiers pour fonctionner avec ces adresses sous-sites dans votre solution.</span><span class="sxs-lookup"><span data-stu-id="3e64b-142">You cannot use the programmatic equivalents of folders to work with these sub-addresses in your solution.</span></span> 
  
<span data-ttu-id="3e64b-p109">Les parties de package (documents et relations) ont également des types de contenus associés. Ces types de contenus sont des chaînes qui définissent un type de support MIME. Ces types de contenus spécifient les types de MIME que le fichier peut contenir, et en définissent l'étendue.</span><span class="sxs-lookup"><span data-stu-id="3e64b-p109">Package parts─both document parts and relationship parts─also have associated content types. These content types are strings that define a MIME media type. These content types specify and scope the kind of MIME types that can be contained in the file.</span></span>
  
### <a name="relationships"></a><span data-ttu-id="3e64b-146">Relations</span><span class="sxs-lookup"><span data-stu-id="3e64b-146">Relationships</span></span>

<span data-ttu-id="3e64b-147">Les composants de relation (qui porte l’extension «\*.rels » et sont stockés dans un dossier « _rels ») décrivent comment les composants dans le package par rapport aux autres et fournissent la structure du fichier.</span><span class="sxs-lookup"><span data-stu-id="3e64b-147">The relationship parts (which end with the extension "\*.rels" and are stored in a "_rels" folder) describe how the parts within the package relate to each other and provide the structure of the file.</span></span> <span data-ttu-id="3e64b-148">Document XML autonome utilise la relation parent/enfant des éléments pour déterminer la relation entre les entités avec les autres.</span><span class="sxs-lookup"><span data-stu-id="3e64b-148">A standalone XML document uses the parent/child relationship of elements to determine the relationship of entities to each other.</span></span> <span data-ttu-id="3e64b-149">Autres fichiers peuvent utiliser les autres hiérarchies ou une structure de dossier de fichiers pour décrire les interactions du contenu dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="3e64b-149">Other files may use other hierarchies or file folder structure to describe the interaction of content in the file.</span></span> <span data-ttu-id="3e64b-150">Pour le format de fichier Visio 2013, le package est un fichier Visio valide si elle contient l’ensemble des composants et le package contient les relations entre les composants.</span><span class="sxs-lookup"><span data-stu-id="3e64b-150">For the Visio 2013 file format, the package is a valid Visio file if it contains the correct set of parts and the package contains the relationships between the parts.</span></span> 
  
<span data-ttu-id="3e64b-p111">Les parties relations sont des documents XML qui décrivent les relations entre les différentes parties documents à l'intérieur du package. Elles définissent une association entre deux éléments : une source spécifiée (définie par le nom et l'emplacement du fichier de relation), et une partie document cible spécifiée. Par exemple, les parties relations sont utilisées pour décrire les formes de base associées au fichier, la relation des pages avec le fichier et entre elles, et la relation des images et objets avec une page spécifique.</span><span class="sxs-lookup"><span data-stu-id="3e64b-p111">Relationship parts are XML documents that describe the relationships between different document parts within the package. They define an association between two items: a specified source (defined by the name and location of the relationship file) and a specified target document part. For example, relationship parts are used to describe which shape masters are associated with the file, how pages relate to the file and to each other, or how images and objects relate to a specific page.</span></span> 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a><span data-ttu-id="3e64b-154">Similitudes et différences avec le schéma VDX Visio</span><span class="sxs-lookup"><span data-stu-id="3e64b-154">Similarities and differences with Visio VDX schema</span></span>

<span data-ttu-id="3e64b-155">Comme indiqué, les versions antérieures de Visio également incluaient un fichier XML format, le Format de dessin Visio XML ou .vdx.</span><span class="sxs-lookup"><span data-stu-id="3e64b-155">As mentioned, past versions of Visio also included an XML-based file format, the Visio XML Drawing Format or .vdx.</span></span> <span data-ttu-id="3e64b-156">(Dans les versions précédentes de Visio, le schéma utilisé pour le Format de dessin Visio XML est appelé DatadiagramML). Certains éléments du schéma XML Visio restent identiques entre les deux formats de fichier.</span><span class="sxs-lookup"><span data-stu-id="3e64b-156">(In previous versions of Visio, the schema used for the Visio XML Drawing Format is called DatadiagramML.) Some pieces from the Visio XML schema have stayed the same between the two file formats.</span></span> <span data-ttu-id="3e64b-157">Par exemple, l’élément de **Windows** et ses enfants restent unchanged─with l’élément **Windows** est maintenant un élément racine d’un document XML (window.xml).</span><span class="sxs-lookup"><span data-stu-id="3e64b-157">For example, the **Windows** element and its children remain unchanged─with the exception that the **Windows** element is now a root element of an XML document (window.xml).</span></span> 
  
<span data-ttu-id="3e64b-158">La plus grande différence entre le Format de dessin XML et le format de fichier Visio 2013 est la création d’un package.</span><span class="sxs-lookup"><span data-stu-id="3e64b-158">The largest difference between the XML Drawing Format and the Visio 2013 file format is the packaging.</span></span> <span data-ttu-id="3e64b-159">Un fichier au Format de dessin XML peut être manipulé comme un fichier XML autonome normal ; le format de fichier Visio 2013 doit être manipulé comme un package.</span><span class="sxs-lookup"><span data-stu-id="3e64b-159">An XML Drawing Format file could be manipulated like a normal stand-alone XML; the Visio 2013 file format must be manipulated as a package.</span></span> <span data-ttu-id="3e64b-160">Dans le Visio 2013, le code XML a été divisé en composants pour la consommation plus facile.</span><span class="sxs-lookup"><span data-stu-id="3e64b-160">In the Visio 2013, the XML has been divided up into parts for easier consumption.</span></span> <span data-ttu-id="3e64b-161">Une autre modification notable est que le format de fichier Visio 2013 stocke toutes les propriétés de document dans les parties de document décrits par la norme OPC (App.XML, core.xml, custom.xml).</span><span class="sxs-lookup"><span data-stu-id="3e64b-161">Another noticeable change is that the Visio 2013 file format stores all document properties in document parts described by the OPC standard (app.xml, core.xml, custom.xml).</span></span>
  
<span data-ttu-id="3e64b-162">Toutefois, il existe une modification significative que tous les développeurs Visio à l’esprit : l’introduction des éléments de **cellule**, **ligne**et **Section** .</span><span class="sxs-lookup"><span data-stu-id="3e64b-162">However, there is one significant change that all Visio developers must be aware of: the introduction of the **Cell**, **Row**, and **Section** elements.</span></span> <span data-ttu-id="3e64b-163">Dans le schéma de Format de fichier de dessin XML, des lignes et des cellules dans la feuille ShapeSheet sont représentées par des éléments nommés.</span><span class="sxs-lookup"><span data-stu-id="3e64b-163">In the XML Drawing File Format schema, individual rows and cells in the ShapeSheet are represented by named elements.</span></span> <span data-ttu-id="3e64b-164">Par exemple, imaginez que vous disposez d’un document avec une seule page qui contient une forme avec la valeur « 2 » (ce qui signifie que l’axe de la rotation de la forme 2 pouces du bord gauche du dessin) **PinX** .</span><span class="sxs-lookup"><span data-stu-id="3e64b-164">For example, imagine that you have a document with a single page that contains a shape with a **PinX** value of "2" (meaning that the rotation pin of the shape is 2 inches from the left edge of the drawing).</span></span> <span data-ttu-id="3e64b-165">Le balisage approprié pour que le paramétrage du format de fichier dessin XML est indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="3e64b-165">The relevant markup for that setting in the XML Drawing File Format is shown in the following code.</span></span> 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

<span data-ttu-id="3e64b-166">Ici, l’élément **PinX** est un enfant de l’élément **XForm** , qui est à son tour un enfant de l’élément de la **forme** .</span><span class="sxs-lookup"><span data-stu-id="3e64b-166">Here, the **PinX** element is a child of the **XForm** element, which is in turn a child of the **Shape** element.</span></span> <span data-ttu-id="3e64b-167">Ce modèle de l’interface utilisateur de feuille ShapeSheet Visio, où la cellule **PinX** est incluse dans la section **Shape Transform** d’une forme.</span><span class="sxs-lookup"><span data-stu-id="3e64b-167">This models the Visio ShapeSheet UI, where the **PinX** cell is included in the **Shape Transform** section of a shape.</span></span> 
  
<span data-ttu-id="3e64b-168">Dans le format de fichier Visio 2013, toutes les cellules de la ShapeSheet─ **PinX**, **LinePattern**, une cellule **X** dans une ligne **DéplacerVers** dans une section **Geometry** , etc.─are représenté par un type d’élément XML, l’élément de **cellule** .</span><span class="sxs-lookup"><span data-stu-id="3e64b-168">In the Visio 2013 file format, all cells in the ShapeSheet─ **PinX**, **LinePattern**, an **X** cell in a **MoveTo** row in a **Geometry** section, etc.─are represented by one type of XML element, the **Cell** element.</span></span> <span data-ttu-id="3e64b-169">Différents éléments de **cellule** sont individuated uns des autres par la valeur de leur attribut **N** .</span><span class="sxs-lookup"><span data-stu-id="3e64b-169">Different **Cell** elements are individuated from each other by the value of their **N** attribute.</span></span> <span data-ttu-id="3e64b-170">Par conséquent, dans l’exemple ci-dessus, les données contenues dans la cellule **PinX** dans la feuille ShapeSheet sont stockées dans un fichier VSDX, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="3e64b-170">Thus, in the example from above, the data contained in the **PinX** cell in the ShapeSheet is stored in a VSDX file as shown in the following code.</span></span> 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

<span data-ttu-id="3e64b-171">L’élément **cellule** **PinX** (ainsi que d’autres cellules individuelles, nommées appelées « cellules singleton » comme **LinePattern** ou **LockSelect**) est un enfant direct de l’élément de la **forme** .</span><span class="sxs-lookup"><span data-stu-id="3e64b-171">The **Cell** element for **PinX** (as well as other individual, named cells called "singleton cells" like **LinePattern** or **LockSelect**) is a direct child of the **Shape** element.</span></span> <span data-ttu-id="3e64b-172">Aucun élément unique n’est nécessaire pour représenter la ligne qui contient la cellule **PinX** , chaque forme peut comporter un **PinX**.</span><span class="sxs-lookup"><span data-stu-id="3e64b-172">No unique element is needed to represent the row that contains the **PinX** cell, as each shape can only have one **PinX**.</span></span>
  
<span data-ttu-id="3e64b-173">Qu’advient-il des sections qui incluent des données tabulaires, comme les sections **Geometry** ?</span><span class="sxs-lookup"><span data-stu-id="3e64b-173">What about sections that include tabular data, like **Geometry** sections?</span></span> <span data-ttu-id="3e64b-174">Pour les cellules dans ces sections, le schéma de format de fichier Visio 2013 utilise **Section** et elements─also **ligne** unique par leur attribut **N** ou **T** comme illustré below─to contiennent les données.</span><span class="sxs-lookup"><span data-stu-id="3e64b-174">For the cells in those sections, the Visio 2013 file format schema uses **Section** and **Row** elements─also distinguished by their **N** attribute or **T** attribute as shown below─to contain the data.</span></span> <span data-ttu-id="3e64b-175">Par exemple, la même forme à partir de l’exemple précédent peut contenir des données dans la section **Geometry 1** qui ressemble au code suivant dans le schéma de dessin XML.</span><span class="sxs-lookup"><span data-stu-id="3e64b-175">For example, the same shape from the previous example might contain data in the **Geometry 1** section that looks like the following code in the XML Drawing schema.</span></span> 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <!--- Other cells in the ShapeSheet -->
    <Geom IX="0">
        <!--- Other cells and rows in the Geometry 1 section -->
        <LineTo IX="1">
            <X F="Width*0">0</X>
            <Y F="Height*0">0</Y>
        </LineTo>
    </Geom>
</Shape>

```

<span data-ttu-id="3e64b-176">Toutefois, elle ressemble au code suivant dans le fichier Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="3e64b-176">However, it looks like the following code in the Visio 2013 file.</span></span>
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <!--- Other cells in the ShapeSheet -->
    <Section N="Geometry" IX="0"> 
        <!--- Other cells and rows in the Geometry 1 section -->
        <Row IX="1" T="LineTo">
            <Cell V="0" N="X" V="Width*0" />
            <Cell V="0" N="Y" V="Height*0" />
        </Row>
    </Section>
</Shape>

```

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a><span data-ttu-id="3e64b-177">Scénarios de développeur pour l'utilisation du format de fichier Visio 2013</span><span class="sxs-lookup"><span data-stu-id="3e64b-177">Developer scenarios for working with the Visio 2013 file format</span></span>
<span data-ttu-id="3e64b-178"><a name="vis15_IntroVSDX_Scenarios"> </a></span><span class="sxs-lookup"><span data-stu-id="3e64b-178"></span></span>

<span data-ttu-id="3e64b-179">Comme expliqué ci-dessus, le format de fichier Visio 2013 tire parti de plusieurs technologies bien maîtrisés tels que les fichiers ZIP et XML pour stocker les données.</span><span class="sxs-lookup"><span data-stu-id="3e64b-179">As explained above, the Visio 2013 file format leverages several well-understood technologies like ZIP files and XML to store data.</span></span> <span data-ttu-id="3e64b-180">Pour manipuler un Visio 2013 au niveau du fichier de dessin, une solution faut uniquement utiliser les espaces de noms .NET Framework et les classes associées à utilisation des fichiers ZIP ou XML, comme [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) ou [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3e64b-180">To manipulate a Visio 2013 drawing at the file level, a solution need only to use the .NET Framework namespaces and classes associated with working with ZIP files or XML, like [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) or [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).</span></span>
  
<span data-ttu-id="3e64b-181">Le principal avantage pour les développeurs du format de fichier Visio 2013 est que vous pouvez lire et écrire dans fichiers Visio 2013 sans automatiser l’application cliente de Visio.</span><span class="sxs-lookup"><span data-stu-id="3e64b-181">The key benefit to developers of the Visio 2013 file format is that you can read and write to Visio 2013 files without automating the Visio client application.</span></span> <span data-ttu-id="3e64b-182">Certains scénarios peuvent prendre en compte en tant que développeur pour l’utilisation de format de fichier Visio 2013 sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3e64b-182">Some scenarios that you might consider as a developer for working with Visio 2013 file format include:</span></span>
  
- <span data-ttu-id="3e64b-183">Vérification des fichiers Visio 2013 individuels pour des données spécifiques.</span><span class="sxs-lookup"><span data-stu-id="3e64b-183">Checking individual Visio 2013 files for specific data.</span></span> <span data-ttu-id="3e64b-184">Vous pouvez sélectivement lire un élément en dehors du conteneur ZIP sans avoir à extraire l’intégralité du fichier.</span><span class="sxs-lookup"><span data-stu-id="3e64b-184">You can selectively read one item out of the ZIP container without having to extract the whole file.</span></span>
    
- <span data-ttu-id="3e64b-185">Mise à jour des bibliothèques de fichiers Visio 2013 avec un contenu spécifique.</span><span class="sxs-lookup"><span data-stu-id="3e64b-185">Updating libraries of Visio 2013 files with specific content.</span></span> <span data-ttu-id="3e64b-186">Vous pouvez modifier par programme le logo de toutes les pages d’arrière-plan pour refléter les nouvelles instructions de personnalisation.</span><span class="sxs-lookup"><span data-stu-id="3e64b-186">You can programmatically change the logo in all of the background pages to reflect new branding guidelines.</span></span>
    
- <span data-ttu-id="3e64b-187">Création d’applications qui utilisent des fichiers Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="3e64b-187">Creating applications that consume Visio 2013 files.</span></span> <span data-ttu-id="3e64b-188">Par exemple, vous pouvez créer un outil qui lit un diagramme de flux de travail Visio et puis exécute sa propre logique métier en fonction de ce flux de travail.</span><span class="sxs-lookup"><span data-stu-id="3e64b-188">For example, you can build a tool that reads a Visio workflow diagram and then executes its own business logic based upon that workflow.</span></span>
    
<span data-ttu-id="3e64b-189">Soyez conscient que, du fait que ces solutions utilisent des assemblys .NET Framework standard, la plupart de celles qui peuvent être exécutées sur un ordinateur client peuvent également l'être sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="3e64b-189">Be aware that because these solutions use standard .NET Framework assemblies, most solutions that can be run on a client machine can also be run on a server!</span></span>
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a><span data-ttu-id="3e64b-190">Exploration du format de fichier Visio 2013 par programmation</span><span class="sxs-lookup"><span data-stu-id="3e64b-190">Exploring the Visio 2013 file format programmatically</span></span>
<span data-ttu-id="3e64b-191"><a name="vis15_IntroVSDX_Explore"> </a></span><span class="sxs-lookup"><span data-stu-id="3e64b-191"></span></span>

<span data-ttu-id="3e64b-192">La tâche plus simple et fondamentale pour les développeurs de travailler avec le format de fichier Visio 2013 est l’ouverture du fichier en tant que package et accéder à des composants individuels dans le package.</span><span class="sxs-lookup"><span data-stu-id="3e64b-192">The most basic and fundamental task for any developer working with the Visio 2013 file format is opening the file as a package and then accessing individual parts within the package.</span></span> <span data-ttu-id="3e64b-193">Le **System.IO.Packaging.Package** dans le WindowsBase.dll contient de nombreuses classes qui vous permettent d’ouvrir et de manipuler des packages et composants.</span><span class="sxs-lookup"><span data-stu-id="3e64b-193">The **System.IO.Packaging.Package** in the WindowsBase.dll contains many classes that enable you to open and manipulate packages and parts.</span></span> 
  
<span data-ttu-id="3e64b-194">Dans l'exemple de code suivant, vous pouvez voir comment ouvrir un fichier .vsdx, lire la liste des parties du package, et obtenir des informations sur chacune d'elles.</span><span class="sxs-lookup"><span data-stu-id="3e64b-194">In the following code sample, you can see how to open a .vsdx file, read the list of parts in the package, and get information about each part.</span></span>
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a><span data-ttu-id="3e64b-195">Pour ouvrir un fichier .vsdx et afficher les parties documents</span><span class="sxs-lookup"><span data-stu-id="3e64b-195">To open a .vsdx file and view the document parts</span></span>

1. <span data-ttu-id="3e64b-196">Ouvrez Visio 2013 et créez un nouveau document.</span><span class="sxs-lookup"><span data-stu-id="3e64b-196">Open Visio 2013 and create a new document.</span></span>
    
2. <span data-ttu-id="3e64b-197">Créez un document et enregistrez-le sur le Bureau.</span><span class="sxs-lookup"><span data-stu-id="3e64b-197">Create a new document and save it to the Desktop.</span></span>
    
3. <span data-ttu-id="3e64b-198">Ouvrez Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="3e64b-198">Open Visual Studio 2012.</span></span>
    
4. <span data-ttu-id="3e64b-199">Dans le menu **fichier** , choisissez **Nouveau**, puis choisissez \*\* Project \*\*.</span><span class="sxs-lookup"><span data-stu-id="3e64b-199">On the **File** menu, choose **New**, and then choose \*\* Project \*\*.</span></span>
    
5. <span data-ttu-id="3e64b-200">Sous **Visual C#** ou **Visual Basic**, développez **Windows**, puis sélectionnez **Application console**.</span><span class="sxs-lookup"><span data-stu-id="3e64b-200">Under **Visual C#** or **Visual Basic**, expand **Windows**, and then select **Console Application**.</span></span>
    
6. <span data-ttu-id="3e64b-201">Dans la zone **nom** , tapez 'VisioFileExplorer'.</span><span class="sxs-lookup"><span data-stu-id="3e64b-201">In the **Name** box, type 'VisioFileExplorer'.</span></span> <span data-ttu-id="3e64b-202">Le projet d’Application Console s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="3e64b-202">The Console Application project opens.</span></span> 
    
7. <span data-ttu-id="3e64b-203">Dans l'**Explorateur de solutions**, cliquez avec le bouton droit sur **VisioFileExplorer**, puis cliquez sur **Ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="3e64b-203">In the **Solution Explorer**, right-click **VisioFileExplorer**, and then click **Add Reference**.</span></span> 
    
8. <span data-ttu-id="3e64b-204">Dans la boîte de dialogue **Ajouter une référence**, sous **Assemblys**, développez **Framework**, puis sélectionnez **WindowsBase**.</span><span class="sxs-lookup"><span data-stu-id="3e64b-204">In the **Add Reference** dialog box, under **Assemblies**, expand **Framework**, and then choose **WindowsBase**.</span></span>
    
9. <span data-ttu-id="3e64b-205">Collez le code suivant dans la solution.</span><span class="sxs-lookup"><span data-stu-id="3e64b-205">Paste the following code into the solution.</span></span>
    
  ```cs
  using System;
  using System.Collections.Generic;
  using System.Linq;
  using System.Text;
  using System.IO;
  using System.IO.Packaging;
  using System.Diagnostics;
  namespace VisioFileExplorer
  {
      class Program
      {
          static void Main(string[] args)
          {    
              try
              {
                  Console.WriteLine("Opening the VSDX file ...");
                  // Need to get the folder path for the Desktop
                  // where the file is saved.
                  string dirPath = System.Environment.GetFolderPath(
                      System.Environment.SpecialFolder.Desktop);
                  DirectoryInfo myDir = new DirectoryInfo(dirPath);
                  // It is a best practice to get the file name string
                  // using a FileInfo object, but it isn't necessary.
                  FileInfo[] fInfos = myDir.GetFiles("*.vsdx");
                  FileInfo fi = fInfos[0];
                  string fName = fi.FullName;
                  // We're not going to do any more than open
                  // and read the list of parts in the package, although
                  // we can create a package or read/write what's inside.
                  using (Package fPackage = Package.Open(
                      fName, FileMode.Open, FileAccess.Read))
                  {
                      
                      // The way to get a reference to a package part is
                      // by using its URI. Thus, we're reading the URI
                      // for each part in the package.
                      PackagePartCollection fParts = fPackage.GetParts();
                      foreach (PackagePart fPart in fParts)
                      {
                          Console.WriteLine("Package part: {0}", fPart.Uri);
                      }
                  }   
              }
              catch (Exception err)
              {
                  Console.WriteLine("Error: {0}", err.Message);
              }
              finally
              {
                  Console.Write("\nPress any key to continue ...");
                  Console.ReadKey();
              }   
          }
      }
  }
  ```

  ```vb
  Imports System
  Imports System.Collections.Generic
  Imports System.Linq
  Imports System.Text
  Imports System.IO
  Imports System.IO.Packaging
  Imports System.Diagnostics
  Module Module1
      Sub Main()
          Try
              Console.WriteLine("Opening the VSDX file ...")
              ' Need to get the folder path for the Desktop
              ' or where the file is saved.
              Dim dirPath As String = System.Environment.GetFolderPath( _
                  System.Environment.SpecialFolder.Desktop)
              Dim myDir As New DirectoryInfo(dirPath)
              ' It is a best practice to get the file name string
              ' using a FileInfo object, but it isn't necessary.
              Dim fInfos As FileInfo() = myDir.GetFiles("*.vsdx")
              Dim fi As FileInfo = fInfos(0)
              Dim fName As String = fi.FullName
              ' We don't need to do any more than open
              ' and read the list of parts in the package, although
              ' we can create a package or read/write what's inside.
              Using fPackage As Package = Package.Open( _
                  fName, FileMode.Open, FileAccess.Read)
                  ' The way to get a reference to a document part is
                  ' by using its URI. Thus, we're reading the URI
                  ' for each document part in the package.
                  Dim fParts As PackagePartCollection = fPackage.GetParts()
                  For Each fPart As PackagePart In fParts
                      Console.WriteLine("Package part: {0}", fPart.Uri)
                  Next
              End Using
          Catch err As Exception
              Console.WriteLine("Error: {0}", err.Message)
          Finally
              Console.Write(vbLf &amp; "Press any key to continue ...")
              Console.ReadKey()
          End Try
      End Sub
  End Module
  
  ```

10. <span data-ttu-id="3e64b-p126">Appuyez sur F5 pour déboguer la solution. Lorsque l'exécution du programme est terminée, appuyez sur une touche pour quitter.</span><span class="sxs-lookup"><span data-stu-id="3e64b-p126">Press F5 to debug the solution. When the program has completed running, press any key to exit.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3e64b-208">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e64b-208">See also</span></span>
<span data-ttu-id="3e64b-209"><a name="vis15_IntroVSDX_Resources"> </a></span><span class="sxs-lookup"><span data-stu-id="3e64b-209"></span></span>

<span data-ttu-id="3e64b-210">Pour plus d’informations sur l’utilisation des fichiers de Visio 2013or Office OpenXML par programme, la spécification Open Packaging Convention ou le format de fichier Visio 2013, voir les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="3e64b-210">For more information about the Visio 2013 file format, the Open Packaging Convention, or how to work with Visio 2013or Office OpenXML files programmatically, see the following resources:</span></span>
  
- [<span data-ttu-id="3e64b-211">Visio pour les développeurs</span><span class="sxs-lookup"><span data-stu-id="3e64b-211">Visio for developers</span></span>](https://msdn.microsoft.com/office/aa905478.aspx)
    
- <span data-ttu-id="3e64b-212">[OPC : une nouvelle norme pour l’empaquetage de vos données](https://msdn.microsoft.com/magazine/cc163372.aspx).</span><span class="sxs-lookup"><span data-stu-id="3e64b-212">[OPC: A New Standard for Packaging Your Data](https://msdn.microsoft.com/magazine/cc163372.aspx).</span></span>
    
- [<span data-ttu-id="3e64b-213">Notions essentielles de l’Open Packaging Conventions</span><span class="sxs-lookup"><span data-stu-id="3e64b-213">Essentials of the Open Packaging Conventions</span></span>](https://msdn.microsoft.com/library/ee361919.aspx)
    
- [<span data-ttu-id="3e64b-214">Présentation des Formats de fichier Open XML Office (2007)</span><span class="sxs-lookup"><span data-stu-id="3e64b-214">Introducing the Office (2007) Open XML File Formats</span></span>](https://msdn.microsoft.com/library/aa338205.aspx)
    

