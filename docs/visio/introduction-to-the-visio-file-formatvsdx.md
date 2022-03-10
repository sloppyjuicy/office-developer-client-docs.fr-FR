---
title: Présentation du format de fichier Visio (.vsdx)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.assetid: 69736f40-8f67-46c2-abf6-82dffecb2274
description: Découvrez le nouveau format de fichier Visio 2013, explorez certains concepts généraux relatifs à l’utilisation du format de fichier Visio 2013 par programmation, et créez une application de console simple qui examine un fichier Visio 2013.
ms.localizationpriority: high
ms.openlocfilehash: 07916d83056a6c01336d747b3a361da4cce82c8b
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63426355"
---
# <a name="introduction-to-the-visio-file-format-vsdx"></a>Présentation du format de fichier Visio (.vsdx)

Découvrez le nouveau format de fichier Visio 2013, explorez certains concepts généraux relatifs à l’utilisation du format de fichier Visio 2013 par programmation, et créez une application de console simple qui examine un fichier Visio 2013.
  
||Valeur |
|:-----|:-----|
|**Dans cet article**         [Introduction](#vis15_IntroVSDX_Intro)          [Format de fichier Visio 2013 sous-jacent](#vis15_IntroVSDX_What)          [Scénarios de développeur pour utiliser le format de fichier Visio 2013](#vis15_IntroVSDX_Scenarios)          [Exploration par programmation du format de fichier Visio 2013](#vis15_IntroVSDX_Explore)          [Ressources supplémentaires](#vis15_IntroVSDX_Resources)||

## <a name="introduction"></a>Introduction

<a name="vis15_IntroVSDX_Intro"> </a>

Visio 2013 lance un nouveau format de fichier Visio (.vsdx) qui vient remplacer le format de fichier binaire Visio (.vsd) et le format de fichier de dessin XML Visio (.vdx). Étant donné que le format de fichier Visio 2013 repose sur des conventions Open Packaging et sur XML, les développeurs qui connaissent ces technologies peuvent rapidement apprendre à utiliser les fichiers Visio 2013 par programmation. Les développeurs qui sont habitués au format de fichier de dessin XML Visio (.vdx) des versions précédentes de Visio retrouveront un grand nombre de structures identiques dans le format de fichier .vsdx. L’interopérabilité avec les fichiers Visio a été considérablement augmentée, puisque des logiciels tiers peuvent manipuler les fichiers Visio au niveau du format de fichier. Le format de fichier Visio 2013 est pris en charge par Visio Services dans Microsoft SharePoint Server 2013, sans qu’il ne soit nécessaire d’utiliser un format de fichier « intermédiaire » pour publier sur SharePoint Server.
  
Il existe plusieurs types de fichier qui, par extension, sont compatibles avec le format de fichier Visio 2013.
  
- .vsdx (dessin Visio)
- .vsdm (dessin Visio prenant en charge les macros)
- .vssx (gabarit Visio)
- .vssm (gabarit Visio prenant en charge les macros)
- .vstx (modèle Visio)
- .vstm (modèle Visio prenant en charge les macros)

> [!NOTE]
> Seuls les fichiers prenant en charge les macros (.vsdm, .vssm et .vstm) peuvent contenir des macros VBA. Il est impossible d'enregistrer des macros dans des fichiers dont l'extension est .vsdx, .vssx ou .vstx.
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a>Format de fichier Visio 2013 sous-jacent

<a name="vis15_IntroVSDX_What"> </a>

Le format de fichier Visio 2013 utilise les conventions d'emballage ouvertes (OPC), qui définissent un moyen structuré de stocker des données d'application avec des ressources connexes en utilisant un conteneur quelconque─par exemple, un fichier ZIP. À un niveau de base, un fichier Visio 2013 est en réalité un conteneur ZIP qui contient d'autres types de fichiers. En fait, vous pouvez enregistrer un dessin dans Visio 2013 en tant que fichier .vsdx, renommer l'extension du fichier en «\* .zip » dans l'Explorateur Windows, puis ouvrir le fichier comme un dossier pour voir son contenu.
  
> [!NOTE]
> Cet article ne contient qu’une présentation rapide d’Open Packaging Conventions. Les conventions sont présentées plus en détail dans d’autres articles : > Pour plus d’informations sur les spécifications Open Packaging Conventions, consultez [OPC : une nouvelle norme standard pour les packages de données](https://msdn.microsoft.com/magazine/cc163372.aspx).
> Pour plus d’informations sur les spécifications Open Packaging Conventions et leur utilisation dans des fichiers Microsoft Office, reportez-vous aux rubriques [Éléments fondamentaux des OPC (Open Packaging Conventions)](https://msdn.microsoft.com/library/ee361919.aspx) et [Présentation des formats de fichier Open XML Microsoft Office (2007)](https://msdn.microsoft.com/library/aa338205.aspx).
  
### <a name="packages-and-package-parts"></a>Packages et parties de Package

Comme nous l'avons vu précédemment, les fichiers Visio 2013 sont des conteneurs ZIP ou des « paquets » qui contiennent d'autres fichiers (appelés « parties de paquet »). Une partie de paquet peut être un fichier XML, une image, voire une solution VBA. Les éléments du paquet peuvent être divisés en deux grandes catégories : les "éléments de document" et les « éléments de relation ». Les parties de document contiennent le contenu réel et les métadonnées du fichier Visio, comme le nom du fichier, la première page et toutes les formes qu'elle contient, et même les connexions de données pour les formes. Les images et les fichiers texte contenus dans le paquet sont considérés comme des parties de document. Les parties relationnelles sont décrites plus en détail plus loin dans cet article.
  
> [!NOTE]
> Si vous ouvrez un fichier Visio 2013 à l'aide d'un utilitaire ZIP, vous pouvez probablement voir plusieurs dossiers contenus à l'intérieur du paquet ZIP. Vous pouvez même manipuler ces sous-adresses comme des dossiers à l'aide d'un utilitaire ZIP. Toutefois, ces « dossiers » représentent des sous-adresses au sein du paquet ZIP, et non des dossiers réels. Vous ne pouvez pas utiliser les équivalents programmatiques des dossiers pour travailler avec ces sous-adresses dans votre solution.
  
Les parties de package (documents et relations) ont également des types de contenus associés. Ces types de contenus sont des chaînes qui définissent un type de support MIME. Ces types de contenus spécifient les types de MIME que le fichier peut contenir, et en définissent l'étendue.
  
### <a name="relationships"></a>Relations

Les parties relationnelles (qui se terminent par l'extension « \*.rels » et sont stockées dans un dossier « _rels ») décrivent comment les parties du paquetage sont liées les unes aux autres et fournissent la structure du fichier. Un document XML autonome utilise la relation parent/enfant des éléments pour déterminer la relation des entités entre elles. D'autres fichiers peuvent utiliser d'autres hiérarchies ou une structure de dossiers de fichiers pour décrire l'interaction du contenu du fichier. Pour le format de fichier Visio 2013, le paquet est un fichier Visio valide s'il contient l'ensemble correct de parties et si le paquet contient les relations entre les parties.
  
Les parties relations sont des documents XML qui décrivent les relations entre les différentes parties documents à l'intérieur du package. Elles définissent une association entre deux éléments : une source spécifiée (définie par le nom et l'emplacement du fichier de relation), et une partie document cible spécifiée. Par exemple, les parties relations sont utilisées pour décrire les formes de base associées au fichier, la relation des pages avec le fichier et entre elles, et la relation des images et objets avec une page spécifique.
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a>Similitudes et différences avec le schéma VDX Visio

Comme mentionné, les versions antérieures de Visio contenaient également un format de fichier basé sur XML, le format de dessin XML Visio XML, ou .vdx. (Dans les versions précédentes de Visio, le schéma utilisé pour le format de dessin XML Visio est appelé DatadiagramML). Certaines parties du schéma XML Visio sont restées identiques d’un format à l’autre. Par exemple, l’élément **Windows** et ses enfants n’ont pas changé, hormis le fait que l’élément **Windows** est désormais un élément racine d’un document XML (window.xml).
  
La principale différence entre le format de dessin XML et le format de fichier Visio 2013 est le conditionnement. Un fichier XML Drawing Format peut être manipulé comme un fichier XML autonome normal ; le format de fichier Visio 2013 doit être manipulé comme un paquet. Dans le Visio 2013, le XML a été divisé en plusieurs parties pour une utilisation plus facile. Un autre changement notable est que le format de fichier Visio 2013 stocke toutes les propriétés du document dans des parties de document décrites par la norme OPC (app.xml, core.xml, custom.xml).
  
Cependant, il existe un changement important que tous les développeurs Visio doivent connaître : l'introduction des éléments **Cellule**, **Ligne** et **Section**. Dans le schéma du format de fichier de dessin XML, les rangées et les cellules individuelles de la ShapeSheet sont représentées par des éléments nommés. Par exemple, imaginez que vous avez un document d'une seule page qui contient une forme avec une valeur **PinX** de « 2 » (ce qui signifie que l'axe de rotation de la forme est à 2 pouces du bord gauche du dessin). Le balisage pertinent pour ce paramètre dans le format de fichier de dessin XML est présenté dans le code suivant.
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

Ici, l'élément **PinX** est un enfant de l'élément **XForm**, qui est à son tour un enfant de l'élément **Forme**. Il s'agit d'un modèle de l'interface utilisateur de Visio ShapeSheet, où la cellule **PinX** est incluse dans la section **Transformation de forme** d'une forme.
  
Dans le format de fichier Visio 2013, toutes les cellules de la feuille ShapeSheet (**PinX**, **LinePattern**, la cellule **X** d’une ligne **MoveTo** dans une section **Géométrie**, etc.) sont représentées par un seul type d’élément XML, l’élément **Cellule**. Différents éléments **Cellule** sont individualisés les uns par rapport aux autres par la valeur de leur attribut **N**. Par conséquent, dans l’exemple ci-dessus, les données contenues dans la cellule **PinX** de la feuille ShapeSheet sont stockées dans un fichier VSDX, comme illustré dans le code suivant.
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

L'élément **Cell** pour **PinX** (ainsi que d'autres cellules nommées « singletons » telles que **LinePattern** ou **LockSelect**) est un enfant direct de l'élément **Shape**. Aucun élément unique n'est nécessaire pour représenter la ligne contenant la cellule **PinX**, car chaque forme ne peut avoir qu'un seul **PinX**.
  
Qu'en est-il des sections qui comprennent des données tabulaires, comme les sections de **géométrie**? Pour les cellules de ces sections, le schéma du format de fichier Visio 2013 utilise des éléments **Section** et **Ligne** ─également distingués par leur attribut **N** ou leur attribut **T**, comme indiqué ci-dessous─pour contenir les données. Par exemple, la même forme de l'exemple précédent peut contenir des données dans la section **Géométrie 1** qui ressemblent au code suivant dans le schéma de dessin XML.
  
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

Toutefois, elles ressemblent au code suivant dans le fichier Visio 2013.
  
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

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a>Scénarios développeur d’utilisation du format de fichier Visio 2013

<a name="vis15_IntroVSDX_Scenarios"> </a>

Comme il a été expliqué plus haut, le format de fichier Visio 2013 exploite plusieurs technologies bien comprises telles que les fichiers ZIP et XML pour stocker des données. Pour manipuler un dessin Visio 2013 au niveau fichier, une solution a uniquement besoin d’utiliser les espaces de noms et les classes .NET Framework associés à l’utilisation de fichiers ZIP ou XML, tels que [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) ou [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).
  
Le principal avantage du format de fichier Visio 2013 pour les développeurs est qu’il est possible de lire et d’écrire dans des fichiers Visio 2013 sans automatiser l’application cliente Visio. En tant que développeur vous pouvez envisager l’un des scénarios suivants pour travailler avec le format de fichier Visio 2013 :
  
- Vérification de données spécifiques dans des fichiers Visio 2013 individuels. Vous pouvez lire de manière sélective un élément du conteneur ZIP sans avoir à extraire l'ensemble du fichier.

- Mise à jour des bibliothèques de fichiers Visio 2013 avec un contenu spécifique. Vous pouvez modifier de façon programmatique le logo de toutes les pages d'arrière-plan afin de refléter les nouvelles directives en matière d'image de marque.

- Création d'applications qui consomment des fichiers Visio 2013. Par exemple, vous pouvez créer un outil qui lit un diagramme de flux de travail Visio et exécute ensuite sa propre logique d'entreprise en fonction de ce flux.

Soyez conscient que, du fait que ces solutions utilisent des assemblys .NET Framework standard, la plupart de celles qui peuvent être exécutées sur un ordinateur client peuvent également l'être sur un serveur.
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a>Exploration par programmation du format de fichier Visio 2013

<a name="vis15_IntroVSDX_Explore"> </a>

La tâche la plus élémentaire et la plus fondamentale pour tout développeur travaillant avec le format de fichier Visio 2013 est d'ouvrir le fichier en tant que package et d'accéder ensuite à des parties individuelles au sein du package. Le paquet **System.IO.Packaging.Package** de WindowsBase.dll contient de nombreuses classes qui vous permettent d'ouvrir et de manipuler les paquets et les parties.
  
Dans l'exemple de code suivant, vous pouvez voir comment ouvrir un fichier .vsdx, lire la liste des parties du package, et obtenir des informations sur chacune d'elles.
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a>Pour ouvrir un fichier .vsdx et afficher les parties de document

1. Ouvrez Visio 2013 et créez un document.

2. Créez un document et enregistrez-le sur le bureau.

3. Ouvrez Visual Studio 2012.

4. Dans le menu **Fichier**, sélectionnez **Nouveau**, puis **Projet**.

5. Sous **Visual C#** ou **Visual Basic**, développez **Windows**, puis sélectionnez **Application Console**.

6. Dans la zone **Nom**, entrez « VisioFileExplorer ». Le projet Application console s'ouvre.

7. Dans l’**Explorateur de solutions**, cliquez avec le bouton droit de la souris sur **VisioFileExplorer**, puis cliquez sur **Ajouter une référence**.

8. Dans la boîte de dialogue **Ajouter une référence**, sous **Assemblys**, développez **Framework**, puis sélectionnez **WindowsBase**.

9. Collez le code suivant dans la solution.

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

10. Appuyez sur F5 pour déboguer la solution. Lorsque le programme est terminé, appuyez sur une touche pour quitter.

## <a name="see-also"></a>Voir aussi

<a name="vis15_IntroVSDX_Resources"> </a>

Pour plus d’informations sur le format de fichier Visio 2013, les spécifications Open Packaging Convention ou la manière d’utiliser des fichiers Visio 2013 ou Office OpenXML par programmation, consultez les ressources suivantes :
  
- [Visio pour les développeurs](https://msdn.microsoft.com/office/aa905478.aspx)
- [OPC : une nouvelle norme pour les packages de données](https://msdn.microsoft.com/magazine/cc163372.aspx)
- [Éléments fondamentaux des OPC (Open Packaging Conventions)](https://msdn.microsoft.com/library/ee361919.aspx)
- [Présentation des formats de fichier Office (2007) Open XML](https://msdn.microsoft.com/library/aa338205.aspx)
