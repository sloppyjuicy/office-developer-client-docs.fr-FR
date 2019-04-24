---
title: Présentation du format de fichier Visio (.vsdx)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.assetid: 69736f40-8f67-46c2-abf6-82dffecb2274
description: Découvrez le nouveau format de fichier Visio 2013, explorez certains concepts généraux relatifs à l’utilisation du format de fichier Visio 2013 par programmation, et créez une application de console simple qui examine un fichier Visio 2013.
localization_priority: Priority
ms.openlocfilehash: 74c0f05a1db280386f3dc9dfd23da73a9b2daaf5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357273"
---
# <a name="introduction-to-the-visio-file-format-vsdx"></a><span data-ttu-id="30fac-103">Présentation du format de fichier Visio (.vsdx)</span><span class="sxs-lookup"><span data-stu-id="30fac-103">Introduction to the Visio file format (.vsdx)</span></span>

<span data-ttu-id="30fac-104">Découvrez le nouveau format de fichier Visio 2013, explorez certains concepts généraux relatifs à l’utilisation du format de fichier Visio 2013 par programmation, et créez une application de console simple qui examine un fichier Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="30fac-104">Learn about the new file format in Visio 2013, explore some high-level concepts for working with the Visio 2013 file format programmatically, and create a simple console application that examines a Visio 2013 file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="30fac-105">**Dans cet article**         [Introduction](#vis15_IntroVSDX_Intro)          [Format de fichier Visio 2013 sous-jacent](#vis15_IntroVSDX_What)</span><span class="sxs-lookup"><span data-stu-id="30fac-105">**In this article**         [Introduction](#vis15_IntroVSDX_Intro)          [What is the Visio 2013 file format "under the hood"?](#vis15_IntroVSDX_What)</span></span>          <span data-ttu-id="30fac-106">[Scénarios de développeur pour utiliser le format de fichier Visio 2013](#vis15_IntroVSDX_Scenarios)          [Exploration par programmation du format de fichier Visio 2013](#vis15_IntroVSDX_Explore)          [Ressources supplémentaires](#vis15_IntroVSDX_Resources)</span><span class="sxs-lookup"><span data-stu-id="30fac-106">[Developer scenarios for working with the Visio 2013 file format](#vis15_IntroVSDX_Scenarios)          [Exploring the Visio 2013 file format programmatically](#vis15_IntroVSDX_Explore)          [Additional resources](#vis15_IntroVSDX_Resources)</span></span>||
   
## <a name="introduction"></a><span data-ttu-id="30fac-107">Introduction</span><span class="sxs-lookup"><span data-stu-id="30fac-107">Introduction</span></span>
<span data-ttu-id="30fac-108"><a name="vis15_IntroVSDX_Intro"> </a></span><span class="sxs-lookup"><span data-stu-id="30fac-108"></span></span>

<span data-ttu-id="30fac-109">Visio 2013 lance un nouveau format de fichier Visio (.vsdx) qui vient remplacer le format de fichier binaire Visio (.vsd) et le format de fichier de dessin XML Visio (.vdx).</span><span class="sxs-lookup"><span data-stu-id="30fac-109">Visio 2013 introduces a new file format (.vsdx) for Visio that replaces the Visio binary file format (.vsd) and Visio XML Drawing file format (.vdx).</span></span> <span data-ttu-id="30fac-110">Étant donné que le format de fichier Visio 2013 repose sur des conventions Open Packaging et sur XML, les développeurs qui connaissent ces technologies peuvent rapidement apprendre à utiliser les fichiers Visio 2013 par programmation.</span><span class="sxs-lookup"><span data-stu-id="30fac-110">Because the Visio 2013 file format is based upon Open Packaging Conventions and XML, developers who are familiar with these technologies can quickly learn how to work with Visio 2013 files programmatically.</span></span> <span data-ttu-id="30fac-111">Les développeurs qui sont habitués au format de fichier de dessin XML Visio (.vdx) des versions précédentes de Visio retrouveront un grand nombre de structures identiques dans le format de fichier .vsdx.</span><span class="sxs-lookup"><span data-stu-id="30fac-111">Developers who are familiar with the Visio XML Drawing file format (.vdx) from previous versions of Visio can find many of the same XML structures within the parts of .vsdx file format.</span></span> <span data-ttu-id="30fac-112">L’interopérabilité avec les fichiers Visio a été considérablement augmentée, puisque des logiciels tiers peuvent manipuler les fichiers Visio au niveau du format de fichier.</span><span class="sxs-lookup"><span data-stu-id="30fac-112">Interoperability with Visio files is greatly increased since third-party software can manipulate Visio files at a file format level.</span></span> <span data-ttu-id="30fac-113">Le format de fichier Visio 2013 est pris en charge par Visio Services dans Microsoft SharePoint Server 2013, sans qu’il ne soit nécessaire d’utiliser un format de fichier « intermédiaire » pour publier sur SharePoint Server.</span><span class="sxs-lookup"><span data-stu-id="30fac-113">The Visio 2013 file format is supported on Visio Services in Microsoft SharePoint Server 2013, without the need of an "intermediary" file format for publishing to SharePoint Server.</span></span>
  
<span data-ttu-id="30fac-114">Il existe plusieurs types de fichier qui, par extension, sont compatibles avec le format de fichier Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="30fac-114">There are several file types, by extension, that comprise the Visio 2013 file format.</span></span> <span data-ttu-id="30fac-115">Ces extensions sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="30fac-115">These extensions include:</span></span>
  
- <span data-ttu-id="30fac-116">.vsdx (dessin Visio)</span><span class="sxs-lookup"><span data-stu-id="30fac-116">.vsdx (Visio drawing)</span></span>
    
- <span data-ttu-id="30fac-117">.vsdm (dessin Visio prenant en charge les macros)</span><span class="sxs-lookup"><span data-stu-id="30fac-117">.vsdm (Visio macro-enabled drawing)</span></span>
    
- <span data-ttu-id="30fac-118">.vssx (gabarit Visio)</span><span class="sxs-lookup"><span data-stu-id="30fac-118">.vssx (Visio stencil)</span></span>
    
- <span data-ttu-id="30fac-119">.vssm (gabarit Visio prenant en charge les macros)</span><span class="sxs-lookup"><span data-stu-id="30fac-119">.vssm (Visio macro-enabled stencil)</span></span>
    
- <span data-ttu-id="30fac-120">.vstx (modèle Visio)</span><span class="sxs-lookup"><span data-stu-id="30fac-120">.vstx (Visio template)</span></span>
    
- <span data-ttu-id="30fac-121">.vstm (modèle Visio prenant en charge les macros)</span><span class="sxs-lookup"><span data-stu-id="30fac-121">.vstm (Visio macro-enabled template)</span></span>
    
> [!NOTE]
> <span data-ttu-id="30fac-p104">Seuls les fichiers prenant en charge les macros (.vsdm, .vssm et .vstm) peuvent contenir des macros VBA. Il est impossible d'enregistrer des macros dans des fichiers dont l'extension est .vsdx, .vssx ou .vstx.</span><span class="sxs-lookup"><span data-stu-id="30fac-p104">Only the macro-enabled files (.vsdm, .vssm, .vstm) can store VBA macros. You cannot store macros in files with a .vsdx, .vssx, or .vstx extension.</span></span> 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a><span data-ttu-id="30fac-124">Format de fichier Visio 2013 sous-jacent</span><span class="sxs-lookup"><span data-stu-id="30fac-124">What is the Visio 2013 file format "under the hood"?</span></span>
<span data-ttu-id="30fac-125"><a name="vis15_IntroVSDX_What"> </a></span><span class="sxs-lookup"><span data-stu-id="30fac-125"></span></span>

<span data-ttu-id="30fac-126">Le format de fichier Visio 2013 utilise les Open Packing Conventions (OPC), qui définissent un moyen structuré de stocker des données d’application avec des ressources associées à l’aide d’un conteneur quelconque, par exemple un fichier ZIP.</span><span class="sxs-lookup"><span data-stu-id="30fac-126">The Visio 2013 file format uses the Open Packing Conventions (OPC), which defines a structured means to store application data together with related resources using a container of some sort─for example, a ZIP file.</span></span> <span data-ttu-id="30fac-127">Fondamentalement, un fichier Visio 2013 n’est qu’un conteneur ZIP qui contient d’autres types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="30fac-127">At a basic level, a Visio 2013 file is really a ZIP container that contains other types of files.</span></span> <span data-ttu-id="30fac-128">En fait, vous pouvez enregistrer un dessin Visio 2013 dans un fichier .vsdx, renommer l’extension en « \*.zip » dans l’Explorateur Windows, puis ouvrir le fichier comme un dossier pour en voir le contenu.</span><span class="sxs-lookup"><span data-stu-id="30fac-128">In fact, you can save a drawing in Visio 2013 as a .vsdx file, rename the file extension to "\*.zip" in Windows Explorer, and then open the file like a folder to see the contents inside.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="30fac-129">Cet article ne contient qu’une présentation rapide d’Open Packaging Conventions.</span><span class="sxs-lookup"><span data-stu-id="30fac-129">This article contains only a brief overview of the Open Packaging Conventions.</span></span> <span data-ttu-id="30fac-130">Les conventions sont présentées plus en détail dans d’autres articles : > Pour plus d’informations sur les spécifications Open Packaging Conventions, consultez [OPC : une nouvelle norme pour les packages de données](https://msdn.microsoft.com/magazine/cc163372.aspx).</span><span class="sxs-lookup"><span data-stu-id="30fac-130">You can find more detailed coverage of the conventions in other articles: >  For more information about the Open Packaging Conventions themselves, see [OPC: A New Standard for Packaging Your Data](https://msdn.microsoft.com/magazine/cc163372.aspx).</span></span> <span data-ttu-id="30fac-131">> Pour plus d’informations sur les spécifications Open Packaging Conventions et leur utilisation dans des fichiers Microsoft Office, reportez-vous aux rubriques [Éléments fondamentaux des OPC (Open Packaging Conventions)](https://msdn.microsoft.com/library/ee361919.aspx) et [Présentation des formats de fichier Open XML Microsoft Office (2007)](https://msdn.microsoft.com/library/aa338205.aspx).</span><span class="sxs-lookup"><span data-stu-id="30fac-131">>  For more information about the Open Packaging Conventions and their use in Microsoft Office files, see [Essentials of the Open Packaging Conventions](https://msdn.microsoft.com/library/ee361919.aspx) and [Introducing the Office (2007) Open XML File Formats](https://msdn.microsoft.com/library/aa338205.aspx).</span></span> 
  
### <a name="packages-and-package-parts"></a><span data-ttu-id="30fac-132">Packages et parties de Package</span><span class="sxs-lookup"><span data-stu-id="30fac-132">Packages and Package Parts</span></span>

<span data-ttu-id="30fac-133">Comme évoqué plus haut, les fichiers Visio 2013 sont des conteneurs ZIP ou « packages » qui contiennent d’autres fichiers (appelés « parties de package »).</span><span class="sxs-lookup"><span data-stu-id="30fac-133">As started earlier, Visio 2013 files are ZIP containers or "packages" that hold other files (called "package parts") within them.</span></span> <span data-ttu-id="30fac-134">Une partie de package peut être un fichier XML, une image, voire une solution VBA.</span><span class="sxs-lookup"><span data-stu-id="30fac-134">A package part can be an XML file, an image, even a VBA solution.</span></span> <span data-ttu-id="30fac-135">Les parties d’un package peuvent être subdivisées en deux grandes catégories, « parties de documents » et « parties de relations ».</span><span class="sxs-lookup"><span data-stu-id="30fac-135">The parts within the package can be further divided into two broad categories, "document parts" and "relationship parts."</span></span> <span data-ttu-id="30fac-136">Les parties de documents sont le contenu effectif et les métadonnées du fichier Visio, tels que le nom du fichier, la première page et toutes les formes qu’il contient, et même les connexions de données des formes.</span><span class="sxs-lookup"><span data-stu-id="30fac-136">The document parts contain the actual content and metadata of the Visio file, like the name of the file, the first page and all of the shapes that it contains, and even the data connections for the shapes.</span></span> <span data-ttu-id="30fac-137">Les images et les fichiers texte contenus dans le package sont considérés comme des parties de document.</span><span class="sxs-lookup"><span data-stu-id="30fac-137">Images and text files within the package are considered document parts.</span></span> <span data-ttu-id="30fac-138">Les parties de relations sont décrites plus en détail plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="30fac-138">Relationship parts are described in more detail later in this article.</span></span>
  
> [!NOTE]
> <span data-ttu-id="30fac-139">Si vous ouvrez un fichier Visio 2013 à l’aide d’un utilitaire ZIP, vous pourrez probablement voir plusieurs dossiers à l’intérieur du package.</span><span class="sxs-lookup"><span data-stu-id="30fac-139">If you open a Visio 2013 file using a ZIP utility, you can probably see several folders contained inside of the ZIP package.</span></span> <span data-ttu-id="30fac-140">Vous pouvez même manipuler des sous-adresses comme des dossiers à l’aide d’un utilitaire ZIP.</span><span class="sxs-lookup"><span data-stu-id="30fac-140">You can even manipulate these sub-addresses like folders using a ZIP utility.</span></span> <span data-ttu-id="30fac-141">Toutefois, ces « dossiers » représentent des sous-adresses dans le package ZIP, et non des dossiers réels.</span><span class="sxs-lookup"><span data-stu-id="30fac-141">However, these "folders" represent sub-addresses within the ZIP package, not actual folders.</span></span> <span data-ttu-id="30fac-142">Vous ne pouvez pas utiliser les équivalents par programmation des dossiers pour travailler avec ces sous-adresses dans votre solution.</span><span class="sxs-lookup"><span data-stu-id="30fac-142">You cannot use the programmatic equivalents of folders to work with these sub-addresses in your solution.</span></span> 
  
<span data-ttu-id="30fac-p109">Les parties de package (documents et relations) ont également des types de contenus associés. Ces types de contenus sont des chaînes qui définissent un type de support MIME. Ces types de contenus spécifient les types de MIME que le fichier peut contenir, et en définissent l'étendue.</span><span class="sxs-lookup"><span data-stu-id="30fac-p109">Package parts─both document parts and relationship parts─also have associated content types. These content types are strings that define a MIME media type. These content types specify and scope the kind of MIME types that can be contained in the file.</span></span>
  
### <a name="relationships"></a><span data-ttu-id="30fac-146">Relations</span><span class="sxs-lookup"><span data-stu-id="30fac-146">Relationships</span></span>

<span data-ttu-id="30fac-147">Les parties de relations (qui se terminent par l’extension « \*.rels » et sont stockées dans un dossier « _rels ») décrivent la relation mutuelle entre les parties du package et fournissent la structure du fichier.</span><span class="sxs-lookup"><span data-stu-id="30fac-147">The relationship parts (which end with the extension "\*.rels" and are stored in a "_rels" folder) describe how the parts within the package relate to each other and provide the structure of the file.</span></span> <span data-ttu-id="30fac-148">Un document XML autonome utilise la relation parent/enfant d’éléments pour déterminer la relation mutuelle entre des entités.</span><span class="sxs-lookup"><span data-stu-id="30fac-148">A standalone XML document uses the parent/child relationship of elements to determine the relationship of entities to each other.</span></span> <span data-ttu-id="30fac-149">D’autres fichiers peuvent utiliser d’autres hiérarchies ou structures de dossiers pour décrire l’interaction des contenus du fichier.</span><span class="sxs-lookup"><span data-stu-id="30fac-149">Other files may use other hierarchies or file folder structure to describe the interaction of content in the file.</span></span> <span data-ttu-id="30fac-150">Pour le format de fichier Visio 2013, le package est un fichier Visio valide s’il contient d’une part l’ensemble de parties appropriées et d’autre part les relations entre ces parties.</span><span class="sxs-lookup"><span data-stu-id="30fac-150">For the Visio 2013 file format, the package is a valid Visio file if it contains the correct set of parts and the package contains the relationships between the parts.</span></span> 
  
<span data-ttu-id="30fac-p111">Les parties relations sont des documents XML qui décrivent les relations entre les différentes parties documents à l'intérieur du package. Elles définissent une association entre deux éléments : une source spécifiée (définie par le nom et l'emplacement du fichier de relation), et une partie document cible spécifiée. Par exemple, les parties relations sont utilisées pour décrire les formes de base associées au fichier, la relation des pages avec le fichier et entre elles, et la relation des images et objets avec une page spécifique.</span><span class="sxs-lookup"><span data-stu-id="30fac-p111">Relationship parts are XML documents that describe the relationships between different document parts within the package. They define an association between two items: a specified source (defined by the name and location of the relationship file) and a specified target document part. For example, relationship parts are used to describe which shape masters are associated with the file, how pages relate to the file and to each other, or how images and objects relate to a specific page.</span></span> 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a><span data-ttu-id="30fac-154">Similitudes et différences avec le schéma VDX Visio</span><span class="sxs-lookup"><span data-stu-id="30fac-154">Similarities and differences with Visio VDX schema</span></span>

<span data-ttu-id="30fac-155">Comme mentionné, les versions antérieures de Visio contenaient également un format de fichier basé sur XML, le format de dessin XML Visio XML, ou .vdx.</span><span class="sxs-lookup"><span data-stu-id="30fac-155">As mentioned, past versions of Visio also included an XML-based file format, the Visio XML Drawing Format or .vdx.</span></span> <span data-ttu-id="30fac-156">(Dans les versions précédentes de Visio, le schéma utilisé pour le format de dessin XML Visio est appelé DatadiagramML). Certaines parties du schéma XML Visio sont restées identiques d’un format à l’autre.</span><span class="sxs-lookup"><span data-stu-id="30fac-156">(In previous versions of Visio, the schema used for the Visio XML Drawing Format is called DatadiagramML.) Some pieces from the Visio XML schema have stayed the same between the two file formats.</span></span> <span data-ttu-id="30fac-157">Par exemple, l’élément **Windows** et ses enfants n’ont pas changé, hormis le fait que l’élément **Windows** est désormais un élément racine d’un document XML (window.xml).</span><span class="sxs-lookup"><span data-stu-id="30fac-157">For example, the **Windows** element and its children remain unchanged─with the exception that the **Windows** element is now a root element of an XML document (window.xml).</span></span> 
  
<span data-ttu-id="30fac-158">La plus grande différence entre le format de dessin XML et le format de fichier Visio 2013 est constituée par le packaging.</span><span class="sxs-lookup"><span data-stu-id="30fac-158">The largest difference between the XML Drawing Format and the Visio 2013 file format is the packaging.</span></span> <span data-ttu-id="30fac-159">Un fichier au format de dessin XML pouvait être manipulé comme un fichier XML autonome normal ; le format de fichier Visio 2013 doit être manipulé en tant que package.</span><span class="sxs-lookup"><span data-stu-id="30fac-159">An XML Drawing Format file could be manipulated like a normal stand-alone XML; the Visio 2013 file format must be manipulated as a package.</span></span> <span data-ttu-id="30fac-160">Dans Visio 2013, le fichier XML a été divisé en plusieurs parties pour en faciliter l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="30fac-160">In the Visio 2013, the XML has been divided up into parts for easier consumption.</span></span> <span data-ttu-id="30fac-161">Parmi les autres modifications visibles, le format de fichier Visio 2013 stocke désormais toutes les propriétés du document dans les parties de documents décrites par la norme OPC (app.xml, core.xml, custom.xml).</span><span class="sxs-lookup"><span data-stu-id="30fac-161">Another noticeable change is that the Visio 2013 file format stores all document properties in document parts described by the OPC standard (app.xml, core.xml, custom.xml).</span></span>
  
<span data-ttu-id="30fac-162">Une modification significative doit être signalée à tous les développeurs Visio : l’introduction d’éléments **Cellule**, **Ligne** et **Section**.</span><span class="sxs-lookup"><span data-stu-id="30fac-162">However, there is one significant change that all Visio developers must be aware of: the introduction of the **Cell**, **Row**, and **Section** elements.</span></span> <span data-ttu-id="30fac-163">Dans le schéma du format de fichier de dessin XML, les lignes et les cellules individuelles d’une feuille ShapeSheet sont représentées par des éléments nommés.</span><span class="sxs-lookup"><span data-stu-id="30fac-163">In the XML Drawing File Format schema, individual rows and cells in the ShapeSheet are represented by named elements.</span></span> <span data-ttu-id="30fac-164">Par exemple, supposons un document d’une seule page contenant une forme avec une valeur **PinX** de « 2 » (qui indique que l’axe de rotation de la forme est situé à 2 pouces du bord gauche du dessin).</span><span class="sxs-lookup"><span data-stu-id="30fac-164">For example, imagine that you have a document with a single page that contains a shape with a **PinX** value of "2" (meaning that the rotation pin of the shape is 2 inches from the left edge of the drawing).</span></span> <span data-ttu-id="30fac-165">La balise pertinente pour ce paramètre dans le format de fichier de dessin XML s’affiche dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="30fac-165">The relevant markup for that setting in the XML Drawing File Format is shown in the following code.</span></span> 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

<span data-ttu-id="30fac-166">Ici, l’élément **PinX** est un enfant de l’élément **XForm**, qui est à son tour un enfant de l’élément **Forme**.</span><span class="sxs-lookup"><span data-stu-id="30fac-166">Here, the **PinX** element is a child of the **XForm** element, which is in turn a child of the **Shape** element.</span></span> <span data-ttu-id="30fac-167">Cela modélise l’interface utilisateur de la feuille ShapeSheet Visio, où la cellule **PinX** est incluse dans la section **Transformation d’une forme** d’une forme.</span><span class="sxs-lookup"><span data-stu-id="30fac-167">This models the Visio ShapeSheet UI, where the **PinX** cell is included in the **Shape Transform** section of a shape.</span></span> 
  
<span data-ttu-id="30fac-168">Dans le format de fichier Visio 2013, toutes les cellules de la feuille ShapeSheet (**PinX**, **LinePattern**, la cellule **X** d’une ligne **MoveTo** dans une section **Géométrie**, etc.) sont représentées par un seul type d’élément XML, l’élément **Cellule**.</span><span class="sxs-lookup"><span data-stu-id="30fac-168">In the Visio 2013 file format, all cells in the ShapeSheet─ **PinX**, **LinePattern**, an **X** cell in a **MoveTo** row in a **Geometry** section, etc.─are represented by one type of XML element, the **Cell** element.</span></span> <span data-ttu-id="30fac-169">Différents éléments **Cellule** sont individualisés les uns par rapport aux autres par la valeur de leur attribut **N**.</span><span class="sxs-lookup"><span data-stu-id="30fac-169">Different **Cell** elements are individuated from each other by the value of their **N** attribute.</span></span> <span data-ttu-id="30fac-170">Par conséquent, dans l’exemple ci-dessus, les données contenues dans la cellule **PinX** de la feuille ShapeSheet sont stockées dans un fichier VSDX, comme illustré dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="30fac-170">Thus, in the example from above, the data contained in the **PinX** cell in the ShapeSheet is stored in a VSDX file as shown in the following code.</span></span> 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

<span data-ttu-id="30fac-171">L’élément **Cellule** de **PinX** (ainsi que d’autres cellules nommées individuelles, appelées « cellules singleton », telles que **LinePattern** ou **LockSelect**) est un enfant direct de l’élément **Forme**.</span><span class="sxs-lookup"><span data-stu-id="30fac-171">The **Cell** element for **PinX** (as well as other individual, named cells called "singleton cells" like **LinePattern** or **LockSelect**) is a direct child of the **Shape** element.</span></span> <span data-ttu-id="30fac-172">Aucun élément unique n’est nécessaire pour représenter la ligne qui contient la cellule **PinX**, puisque chaque forme ne peut contenir qu’un élément **PinX**.</span><span class="sxs-lookup"><span data-stu-id="30fac-172">No unique element is needed to represent the row that contains the **PinX** cell, as each shape can only have one **PinX**.</span></span>
  
<span data-ttu-id="30fac-173">Traitement des sections qui incluent des données tabulaires, par exemple **Géométrie**</span><span class="sxs-lookup"><span data-stu-id="30fac-173">What about sections that include tabular data, like **Geometry** sections?</span></span> <span data-ttu-id="30fac-174">Pour les cellules de ces sections, le schéma de format de fichier Visio 2013 utilise des éléments **Section** et **Ligne**, également distingués par leur attribut **N** ou leur attribut **T**, comme illustré ci-dessous, pour contenir les données.</span><span class="sxs-lookup"><span data-stu-id="30fac-174">For the cells in those sections, the Visio 2013 file format schema uses **Section** and **Row** elements─also distinguished by their **N** attribute or **T** attribute as shown below─to contain the data.</span></span> <span data-ttu-id="30fac-175">Par exemple, la forme de l’exemple précédent peut contenir des données dans la section **Géométrie 1** qui ressemblent au code suivant dans le schéma Dessin XML.</span><span class="sxs-lookup"><span data-stu-id="30fac-175">For example, the same shape from the previous example might contain data in the **Geometry 1** section that looks like the following code in the XML Drawing schema.</span></span> 
  
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

<span data-ttu-id="30fac-176">Toutefois, elles ressemblent au code suivant dans le fichier Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="30fac-176">However, it looks like the following code in the Visio 2013 file.</span></span>
  
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

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a><span data-ttu-id="30fac-177">Scénarios développeur d’utilisation du format de fichier Visio 2013</span><span class="sxs-lookup"><span data-stu-id="30fac-177">Developer scenarios for working with the Visio 2013 file format</span></span>
<span data-ttu-id="30fac-178"><a name="vis15_IntroVSDX_Scenarios"> </a></span><span class="sxs-lookup"><span data-stu-id="30fac-178"></span></span>

<span data-ttu-id="30fac-179">Comme il a été expliqué plus haut, le format de fichier Visio 2013 exploite plusieurs technologies bien comprises telles que les fichiers ZIP et XML pour stocker des données.</span><span class="sxs-lookup"><span data-stu-id="30fac-179">As explained above, the Visio 2013 file format leverages several well-understood technologies like ZIP files and XML to store data.</span></span> <span data-ttu-id="30fac-180">Pour manipuler un dessin Visio 2013 au niveau fichier, une solution a uniquement besoin d’utiliser les espaces de noms et les classes .NET Framework associés à l’utilisation de fichiers ZIP ou XML, tels que [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) ou [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="30fac-180">To manipulate a Visio 2013 drawing at the file level, a solution need only to use the .NET Framework namespaces and classes associated with working with ZIP files or XML, like [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) or [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).</span></span>
  
<span data-ttu-id="30fac-181">Le principal avantage du format de fichier Visio 2013 pour les développeurs est qu’il est possible de lire et d’écrire dans des fichiers Visio 2013 sans automatiser l’application cliente Visio.</span><span class="sxs-lookup"><span data-stu-id="30fac-181">The key benefit to developers of the Visio 2013 file format is that you can read and write to Visio 2013 files without automating the Visio client application.</span></span> <span data-ttu-id="30fac-182">En tant que développeur vous pouvez envisager l’un des scénarios suivants pour travailler avec le format de fichier Visio 2013 :</span><span class="sxs-lookup"><span data-stu-id="30fac-182">Some scenarios that you might consider as a developer for working with Visio 2013 file format include:</span></span>
  
- <span data-ttu-id="30fac-183">Recherche de données spécifiques dans des fichiers Visio 2013 individuels.</span><span class="sxs-lookup"><span data-stu-id="30fac-183">Checking individual Visio 2013 files for specific data.</span></span> <span data-ttu-id="30fac-184">Vous pouvez lire sélectivement un élément du conteneur ZIP sans avoir à extraire l’intégralité du fichier.</span><span class="sxs-lookup"><span data-stu-id="30fac-184">You can selectively read one item out of the ZIP container without having to extract the whole file.</span></span>
    
- <span data-ttu-id="30fac-185">Mise à jour des bibliothèques de fichiers Visio 2013 avec un contenu spécifique.</span><span class="sxs-lookup"><span data-stu-id="30fac-185">Updating libraries of Visio 2013 files with specific content.</span></span> <span data-ttu-id="30fac-186">Vous pouvez modifier par programmation le logo de toutes les pages d’arrière-plan pour refléter de nouvelles directives liées à la marque.</span><span class="sxs-lookup"><span data-stu-id="30fac-186">You can programmatically change the logo in all of the background pages to reflect new branding guidelines.</span></span>
    
- <span data-ttu-id="30fac-187">Création d’applications qui utilisent des fichiers Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="30fac-187">Creating applications that consume Visio 2013 files.</span></span> <span data-ttu-id="30fac-188">Vous pouvez, par exemple, créer un outil qui lit un diagramme de flux de travail Visio, puis exécute sa propre logique métier à partir de ce flux de travail.</span><span class="sxs-lookup"><span data-stu-id="30fac-188">For example, you can build a tool that reads a Visio workflow diagram and then executes its own business logic based upon that workflow.</span></span>
    
<span data-ttu-id="30fac-189">Soyez conscient que, du fait que ces solutions utilisent des assemblys .NET Framework standard, la plupart de celles qui peuvent être exécutées sur un ordinateur client peuvent également l'être sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="30fac-189">Be aware that because these solutions use standard .NET Framework assemblies, most solutions that can be run on a client machine can also be run on a server!</span></span>
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a><span data-ttu-id="30fac-190">Exploration par programmation du format de fichier Visio 2013</span><span class="sxs-lookup"><span data-stu-id="30fac-190">Exploring the Visio 2013 file format programmatically</span></span>
<span data-ttu-id="30fac-191"><a name="vis15_IntroVSDX_Explore"> </a></span><span class="sxs-lookup"><span data-stu-id="30fac-191"></span></span>

<span data-ttu-id="30fac-192">La tâche la plus simple et la plus fondamentale pour n’importe quel développeur travaillant avec le format de fichier Visio 2013 consiste à ouvrir le fichier en tant que package, puis d’accéder aux parties individuelles du package.</span><span class="sxs-lookup"><span data-stu-id="30fac-192">The most basic and fundamental task for any developer working with the Visio 2013 file format is opening the file as a package and then accessing individual parts within the package.</span></span> <span data-ttu-id="30fac-193">**System.IO.Packaging.Package**, dans WindowsBase.dll, contient de nombreuses classes qui vous permettent d’ouvrir et de manipuler des packages et des parties.</span><span class="sxs-lookup"><span data-stu-id="30fac-193">The **System.IO.Packaging.Package** in the WindowsBase.dll contains many classes that enable you to open and manipulate packages and parts.</span></span> 
  
<span data-ttu-id="30fac-194">Dans l'exemple de code suivant, vous pouvez voir comment ouvrir un fichier .vsdx, lire la liste des parties du package, et obtenir des informations sur chacune d'elles.</span><span class="sxs-lookup"><span data-stu-id="30fac-194">In the following code sample, you can see how to open a .vsdx file, read the list of parts in the package, and get information about each part.</span></span>
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a><span data-ttu-id="30fac-195">Pour ouvrir un fichier .vsdx et afficher les parties de document</span><span class="sxs-lookup"><span data-stu-id="30fac-195">To open a .vsdx file and view the document parts</span></span>

1. <span data-ttu-id="30fac-196">Ouvrez Visio 2013 et créez un document.</span><span class="sxs-lookup"><span data-stu-id="30fac-196">Open Visio 2013 and create a new document.</span></span>
    
2. <span data-ttu-id="30fac-197">Créez un document et enregistrez-le sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="30fac-197">Create a new document and save it to the Desktop.</span></span>
    
3. <span data-ttu-id="30fac-198">Ouvrez Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="30fac-198">Open Visual Studio 2012.</span></span>
    
4. <span data-ttu-id="30fac-199">Dans le menu **Fichier**, pointez sur **Nouveau**, puis cliquez sur **Projet**.</span><span class="sxs-lookup"><span data-stu-id="30fac-199">On the **File** menu, choose **New**, and then choose \*\* Project \*\*.</span></span>
    
5. <span data-ttu-id="30fac-200">Sous **Visual C#** ou **Visual Basic**, développez **Windows**, puis sélectionnez **Application Console**.</span><span class="sxs-lookup"><span data-stu-id="30fac-200">Under **Visual C#** or **Visual Basic**, expand **Windows**, and then select **Console Application**.</span></span>
    
6. <span data-ttu-id="30fac-201">Dans la zone **Nom**, entrez « VisioFileExplorer ».</span><span class="sxs-lookup"><span data-stu-id="30fac-201">In the **Name** box, type 'VisioFileExplorer'.</span></span> <span data-ttu-id="30fac-202">Le projet Application Console s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="30fac-202">The Console Application project opens.</span></span> 
    
7. <span data-ttu-id="30fac-203">Dans l’**Explorateur de solutions**, cliquez avec le bouton droit de la souris sur **VisioFileExplorer**, puis cliquez sur **Ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="30fac-203">In the **Solution Explorer**, right-click **VisioFileExplorer**, and then click **Add Reference**.</span></span> 
    
8. <span data-ttu-id="30fac-204">Dans la boîte de dialogue **Ajouter une référence**, sous **Assemblys**, développez **Framework**, puis sélectionnez **WindowsBase**.</span><span class="sxs-lookup"><span data-stu-id="30fac-204">In the **Add Reference** dialog box, under **Assemblies**, expand **Framework**, and then choose **WindowsBase**.</span></span>
    
9. <span data-ttu-id="30fac-205">Collez le code suivant dans la solution.</span><span class="sxs-lookup"><span data-stu-id="30fac-205">Paste the following code into the solution.</span></span>
    
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

10. <span data-ttu-id="30fac-p126">Appuyez sur F5 pour déboguer la solution. Lorsque le programme est terminé, appuyez sur une touche pour quitter.</span><span class="sxs-lookup"><span data-stu-id="30fac-p126">Press F5 to debug the solution. When the program has completed running, press any key to exit.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="30fac-208">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30fac-208">See also</span></span>
<span data-ttu-id="30fac-209"><a name="vis15_IntroVSDX_Resources"> </a></span><span class="sxs-lookup"><span data-stu-id="30fac-209"></span></span>

<span data-ttu-id="30fac-210">Pour plus d’informations sur le format de fichier Visio 2013, les spécifications Open Packaging Convention ou la manière d’utiliser des fichiers Visio 2013 ou Office OpenXML par programmation, consultez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="30fac-210">For more information about the Visio 2013 file format, the Open Packaging Convention, or how to work with Visio 2013or Office OpenXML files programmatically, see the following resources:</span></span>
  
- [<span data-ttu-id="30fac-211">Visio pour les développeurs</span><span class="sxs-lookup"><span data-stu-id="30fac-211">Visio for developers</span></span>](https://msdn.microsoft.com/office/aa905478.aspx)
    
- <span data-ttu-id="30fac-212">[OPC : une nouvelle norme pour les packages de données](https://msdn.microsoft.com/magazine/cc163372.aspx).</span><span class="sxs-lookup"><span data-stu-id="30fac-212">[OPC: A New Standard for Packaging Your Data](https://msdn.microsoft.com/magazine/cc163372.aspx).</span></span>
    
- [<span data-ttu-id="30fac-213">Éléments fondamentaux des OPC (Open Packaging Conventions)</span><span class="sxs-lookup"><span data-stu-id="30fac-213">Essentials of the Open Packaging Conventions</span></span>](https://msdn.microsoft.com/library/ee361919.aspx)
    
- [<span data-ttu-id="30fac-214">Présentation des formats de fichier Office (2007) Open XML</span><span class="sxs-lookup"><span data-stu-id="30fac-214">Introducing the Office (2007) Open XML File Formats</span></span>](https://msdn.microsoft.com/library/aa338205.aspx)
    

