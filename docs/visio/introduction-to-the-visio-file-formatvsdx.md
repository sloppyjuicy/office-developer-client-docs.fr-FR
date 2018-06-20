---
title: Présentation du format de fichier Visio (.vsdx)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 69736f40-8f67-46c2-abf6-82dffecb2274
description: Découvrez le nouveau format de fichier dans Visio 2013, explorez certains concepts généraux relatifs à l’utilisation par programme le format de fichier Visio 2013 et créer une application de console simple qui examine un fichier Visio 2013.
ms.openlocfilehash: aa3497af7c467c8f51ab80ab82071776568b4978
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788840"
---
# <a name="introduction-to-the-visio-file-format-vsdx"></a>Présentation du format de fichier Visio (.vsdx)

Découvrez le nouveau format de fichier dans Visio 2013, explorez certains concepts généraux relatifs à l’utilisation par programme le format de fichier Visio 2013 et créer une application de console simple qui examine un fichier Visio 2013.
  
|||
|:-----|:-----|
|**Dans cet article** [Présentation](#vis15_IntroVSDX_Intro) [Quel est le format de fichier Visio 2013 « à la Loupe » ?](#vis15_IntroVSDX_What)                             [Scénarios de développement pour l’utilisation du format de fichier Visio 2013](#vis15_IntroVSDX_Scenarios) [Exploration du format de fichier Visio 2013 par programme](#vis15_IntroVSDX_Explore) [Ressources supplémentaires](#vis15_IntroVSDX_Resources)                    ||
   
## <a name="introduction"></a>Introduction
<a name="vis15_IntroVSDX_Intro"> </a>

Visio 2013 introduit un nouveau format de fichier (.vsdx) pour Visio qui remplace le format de fichier binaire Visio (.vsd) et le format de fichier de dessin de Visio XML (.vdx). Car le format de fichier Visio 2013 repose sur Open Packaging Conventions et XML, les développeurs qui sont familiarisés avec ces technologies peuvent rapidement comment travailler avec des fichiers Visio 2013 par programmation. Les développeurs qui sont familiarisés avec le format de fichier de dessin de Visio XML (.vdx) à partir de versions antérieures de Visio trouverez nombre des mêmes structures XML dans les composants du format de fichier .vsdx. Interopérabilité avec les fichiers Visio est considérablement plue complexe car les logiciels tiers peuvent manipuler les fichiers à un niveau de format de fichier Visio. Le format de fichier Visio 2013 est pris en charge sur Visio Services dans Microsoft SharePoint Server 2013, sans avoir besoin d’un format de fichier « intermédiaire » pour la publication vers SharePoint Server.
  
Il existe plusieurs types de fichier, par extension, qui composent le format de fichier Visio 2013. Ces extensions sont les suivantes :
  
- .vsdx (dessin Visio)
    
- .vsdm (dessin prenant en charge des Visio)
    
- .vssx (gabarit Visio)
    
- .vssm (gabarit Visio de prenant en charge)
    
- .vstx (modèle Visio)
    
- .vstm (modèle prenant en charge des Visio)
    
> [!NOTE]
> Seuls les fichiers prenant en charge les macros (.vsdm, .vssm et .vstm) peuvent contenir des macros VBA. Il est impossible d'enregistrer des macros dans des fichiers dont l'extension est .vsdx, .vssx ou .vstx. 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a>Quel est le format de fichier Visio 2013 « à la Loupe » ?
<a name="vis15_IntroVSDX_What"> </a>

Le format de fichier Visio 2013 utilise Open livraison Conventions (OPC), qui définit un moyen structuré pour stocker les données d’application avec les ressources associées à l’aide d’un conteneur de certains sort─for exemple, un fichier ZIP. Un niveau de base, un fichier Visio 2013 est réellement un conteneur ZIP qui contient d’autres types de fichiers. En fait, vous pouvez enregistrer un dessin dans Visio 2013 en tant que fichier .vsdx, renommer l’extension de fichier à «\*.zip » dans l’Explorateur Windows et puis ouvrez le fichier comme un dossier pour afficher le contenu à l’intérieur.
  
> [!NOTE]
>  Cet article contient uniquement une vue d’ensemble de l’Open Packaging Conventions. Vous trouverez plus détaillée des conventions dans d’autres articles de la couverture : > Pour plus d’informations sur l’Open Packaging Conventions, consultez la rubrique [OPC : une nouvelle norme pour l’empaquetage de vos données](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx). > Pour plus d’informations sur l’Open Packaging Conventions et leur utilisation dans les fichiers Microsoft Office, voir [Notions essentielles de l’Open Packaging Conventions](http://msdn.microsoft.com/en-us/library/ee361919.aspx) et [Présentation des Formats XML ouverts Office (2007)](http://msdn.microsoft.com/en-us/library/aa338205.aspx). 
  
### <a name="packages-and-package-parts"></a>Packages et parties de packages

Comme démarré précédemment, fichiers Visio 2013 sont des conteneurs ZIP ou des « packages » contenant les autres fichiers (appelées « parties de package ») au sein de celles-ci. Un composant de package peut être un fichier XML, une image, même une solution VBA. Les composants dans le package peuvent être réparties en deux grandes catégories, « parties de document » et « composants de relation ». Les parties du document contient le contenu et les métadonnées du fichier Visio, telles que le nom du fichier, la première page et toutes les formes qu’il contient, et même les connexions de données pour les formes. Images et des fichiers texte dans le package sont considérés comme des parties de document. Composants de relation sont décrites plus en détail plus loin dans cet article.
  
> [!NOTE]
> Si vous ouvrez un fichier Visio 2013 à l’aide d’un utilitaire de compression, vous pouvez voir probablement plusieurs dossiers contenus dans le package ZIP. Vous pouvez même manipuler ces adresses sous-sites tels que des dossiers à l’aide d’un utilitaire ZIP. Toutefois, ces « dossiers » représentent des adresses de sous-sites dans le package ZIP, dossiers pas réels. Vous ne pouvez pas utiliser les équivalents par programmation des dossiers pour fonctionner avec ces adresses sous-sites dans votre solution. 
  
Les parties de package (documents et relations) ont également des types de contenus associés. Ces types de contenus sont des chaînes qui définissent un type de support MIME. Ces types de contenus spécifient les types de MIME que le fichier peut contenir, et en définissent l'étendue.
  
### <a name="relationships"></a>Relations

Les composants de relation (qui porte l’extension «\*.rels » et sont stockés dans un dossier « _rels ») décrivent comment les composants dans le package par rapport aux autres et fournissent la structure du fichier. Document XML autonome utilise la relation parent/enfant des éléments pour déterminer la relation entre les entités avec les autres. Autres fichiers peuvent utiliser les autres hiérarchies ou une structure de dossier de fichiers pour décrire les interactions du contenu dans le fichier. Pour le format de fichier Visio 2013, le package est un fichier Visio valide si elle contient l’ensemble des composants et le package contient les relations entre les composants. 
  
Les parties relations sont des documents XML qui décrivent les relations entre les différentes parties documents à l'intérieur du package. Elles définissent une association entre deux éléments : une source spécifiée (définie par le nom et l'emplacement du fichier de relation), et une partie document cible spécifiée. Par exemple, les parties relations sont utilisées pour décrire les formes de base associées au fichier, la relation des pages avec le fichier et entre elles, et la relation des images et objets avec une page spécifique. 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a>Similitudes et différences avec le schéma VDX Visio

Comme indiqué, les versions antérieures de Visio également incluaient un fichier XML format, le Format de dessin Visio XML ou .vdx. (Dans les versions précédentes de Visio, le schéma utilisé pour le Format de dessin Visio XML est appelé DatadiagramML). Certains éléments du schéma XML Visio restent identiques entre les deux formats de fichier. Par exemple, l’élément de **Windows** et ses enfants restent unchanged─with l’élément **Windows** est maintenant un élément racine d’un document XML (window.xml). 
  
La plus grande différence entre le Format de dessin XML et le format de fichier Visio 2013 est la création d’un package. Un fichier au Format de dessin XML peut être manipulé comme un fichier XML autonome normal ; le format de fichier Visio 2013 doit être manipulé comme un package. Dans le Visio 2013, le code XML a été divisé en composants pour la consommation plus facile. Une autre modification notable est que le format de fichier Visio 2013 stocke toutes les propriétés de document dans les parties de document décrits par la norme OPC (App.XML, core.xml, custom.xml).
  
Toutefois, il existe une modification significative que tous les développeurs Visio à l’esprit : l’introduction des éléments de **cellule**, **ligne**et **Section** . Dans le schéma de Format de fichier de dessin XML, des lignes et des cellules dans la feuille ShapeSheet sont représentées par des éléments nommés. Par exemple, imaginez que vous disposez d’un document avec une seule page qui contient une forme avec la valeur « 2 » (ce qui signifie que l’axe de la rotation de la forme 2 pouces du bord gauche du dessin) **PinX** . Le balisage approprié pour que le paramétrage du format de fichier dessin XML est indiqué dans le code suivant. 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

Ici, l’élément **PinX** est un enfant de l’élément **XForm** , qui est à son tour un enfant de l’élément de la **forme** . Ce modèle de l’interface utilisateur de feuille ShapeSheet Visio, où la cellule **PinX** est incluse dans la section **Shape Transform** d’une forme. 
  
Dans le format de fichier Visio 2013, toutes les cellules de la ShapeSheet─ **PinX**, **LinePattern**, une cellule **X** dans une ligne **DéplacerVers** dans une section **Geometry** , etc.─are représenté par un type d’élément XML, l’élément de **cellule** . Différents éléments de **cellule** sont individuated uns des autres par la valeur de leur attribut **N** . Par conséquent, dans l’exemple ci-dessus, les données contenues dans la cellule **PinX** dans la feuille ShapeSheet sont stockées dans un fichier VSDX, comme indiqué dans le code suivant. 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

L’élément **cellule** **PinX** (ainsi que d’autres cellules individuelles, nommées appelées « cellules singleton » comme **LinePattern** ou **LockSelect**) est un enfant direct de l’élément de la **forme** . Aucun élément unique n’est nécessaire pour représenter la ligne qui contient la cellule **PinX** , chaque forme peut comporter un **PinX**.
  
Qu’advient-il des sections qui incluent des données tabulaires, comme les sections **Geometry** ? Pour les cellules dans ces sections, le schéma de format de fichier Visio 2013 utilise **Section** et elements─also **ligne** unique par leur attribut **N** ou **T** comme illustré below─to contiennent les données. Par exemple, la même forme à partir de l’exemple précédent peut contenir des données dans la section **Geometry 1** qui ressemble au code suivant dans le schéma de dessin XML. 
  
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

Toutefois, elle ressemble au code suivant dans le fichier Visio 2013.
  
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

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a>Scénarios de développeur pour l'utilisation du format de fichier Visio 2013
<a name="vis15_IntroVSDX_Scenarios"> </a>

Comme expliqué ci-dessus, le format de fichier Visio 2013 tire parti de plusieurs technologies bien maîtrisés tels que les fichiers ZIP et XML pour stocker les données. Pour manipuler un Visio 2013 au niveau du fichier de dessin, une solution faut uniquement utiliser les espaces de noms .NET Framework et les classes associées à utilisation des fichiers ZIP ou XML, comme [System.IO.Packaging](http://msdn.microsoft.com/en-us/library/system.io.packaging%28v=vs.110%29.aspx) ou [System.Xml](http://msdn.microsoft.com/en-us/library/system.xml%28v=vs.110%29.aspx).
  
Le principal avantage pour les développeurs du format de fichier Visio 2013 est que vous pouvez lire et écrire dans fichiers Visio 2013 sans automatiser l’application cliente de Visio. Certains scénarios peuvent prendre en compte en tant que développeur pour l’utilisation de format de fichier Visio 2013 sont les suivantes :
  
- Vérification des fichiers Visio 2013 individuels pour des données spécifiques. Vous pouvez sélectivement lire un élément en dehors du conteneur ZIP sans avoir à extraire l’intégralité du fichier.
    
- Mise à jour des bibliothèques de fichiers Visio 2013 avec un contenu spécifique. Vous pouvez modifier par programme le logo de toutes les pages d’arrière-plan pour refléter les nouvelles instructions de personnalisation.
    
- Création d’applications qui utilisent des fichiers Visio 2013. Par exemple, vous pouvez créer un outil qui lit un diagramme de flux de travail Visio et puis exécute sa propre logique métier en fonction de ce flux de travail.
    
Soyez conscient que, du fait que ces solutions utilisent des assemblys .NET Framework standard, la plupart de celles qui peuvent être exécutées sur un ordinateur client peuvent également l'être sur un serveur.
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a>Exploration du format de fichier Visio 2013 par programmation
<a name="vis15_IntroVSDX_Explore"> </a>

La tâche plus simple et fondamentale pour les développeurs de travailler avec le format de fichier Visio 2013 est l’ouverture du fichier en tant que package et accéder à des composants individuels dans le package. Le **System.IO.Packaging.Package** dans le WindowsBase.dll contient de nombreuses classes qui vous permettent d’ouvrir et de manipuler des packages et composants. 
  
Dans l'exemple de code suivant, vous pouvez voir comment ouvrir un fichier .vsdx, lire la liste des parties du package, et obtenir des informations sur chacune d'elles.
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a>Pour ouvrir un fichier .vsdx et afficher les parties documents

1. Ouvrez Visio 2013 et créez un nouveau document.
    
2. Créez un document et enregistrez-le sur le Bureau.
    
3. Ouvrez Visual Studio 2012.
    
4. Dans le menu **fichier** , choisissez **Nouveau**, puis choisissez ** Project **.
    
5. Sous **Visual c#** ou **Visual Basic**, développez **Windows**, puis sélectionnez **Application Console**.
    
6. Dans la zone **nom** , tapez 'VisioFileExplorer'. Le projet d’Application Console s’ouvre. 
    
7. Dans l' **Explorateur de solutions**, cliquez sur **VisioFileExplorer**, puis cliquez sur **Ajouter une référence**. 
    
8. Dans la boîte de dialogue **Ajouter une référence** , sous **assemblys**, développez **Framework**, puis sélectionnez **WindowsBase**.
    
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

10. Appuyez sur F5 pour déboguer la solution. Lorsque l'exécution du programme est terminée, appuyez sur une touche pour quitter.
    
## <a name="see-also"></a>Voir aussi
<a name="vis15_IntroVSDX_Resources"> </a>

Pour plus d’informations sur l’utilisation des fichiers de Visio 2013or Office OpenXML par programme, la spécification Open Packaging Convention ou le format de fichier Visio 2013, voir les ressources suivantes :
  
- [Visio pour les développeurs](http://msdn.microsoft.com/en-us/office/aa905478.aspx)
    
- [OPC : une nouvelle norme pour l’empaquetage de vos données](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx).
    
- [Notions essentielles de l’Open Packaging Conventions](http://msdn.microsoft.com/en-us/library/ee361919.aspx)
    
- [Présentation des Formats de fichier Open XML Office (2007)](http://msdn.microsoft.com/en-us/library/aa338205.aspx)
    

