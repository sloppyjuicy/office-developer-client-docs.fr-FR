---
title: Interface application (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 87926f7d-e1dc-41d5-8805-6ba91fc7b154
description: 'L’interface d’Application inclut des méthodes aide récupérer, manipuler et mettre à jour le contenu et les informations de OneNote. Les méthodes sont en quatre catégories générales :'
ms.openlocfilehash: 25bb1aa570f6c36aa04140d9256d277bee65152b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782524"
---
# <a name="application-interface-onenote"></a>Interface application (OneNote)

L’interface **d’Application** inclut des méthodes aide récupérer, manipuler et mettre à jour le contenu et les informations de OneNote. Les méthodes sont en quatre catégories générales : 
  
- **Structure d’un bloc-notes** &ndash; Méthodes pour travailler avec la structure d’un bloc-notes, y compris celles pour la découverte, l’ouverture, modification, fermeture et suppression des ordinateurs portables, les groupes de sections et sections. 
    
- **Contenu de la page** &ndash; Méthodes pour travailler avec des pages et le contenu de la page, y compris celles pour la découverte, la modification, l’enregistrement et la suppression du contenu de page. Contenu de la page inclut des objets binaires, tels que les entrées manuscrites et les images et objets de texte, tels que des plans. 
    
- **Navigation** &ndash; Méthodes de recherche, liaison à et naviguer vers des pages et des objets. 
    
- **Fonctionnel** &ndash; Toutes les autres méthodes que certaines actions ou de définir des paramètres dans OneNote. 
    
En outre, l’interface **d’Application** inclut un nombre de *Propriétés* et *événements* . 
  
## <a name="notebook-structure-methods"></a>Méthodes de Structure de bloc-notes
<a name="ON14DevRef_Application_NotebookStructure"> </a>

Les méthodes décrites dans cette section vous permettent de découvrir, ouvrir, modifier, fermer et supprimer des blocs-notes OneNote, groupes de sections et sections.
  
### <a name="gethierarchy-method"></a>Méthode GetHierarchy

|||
|:-----|:-----|
|**Description** <br/> |Obtient la nœud hiérarchie structure d’un bloc-notes, à partir du nœud que vous spécifiez (tous les ordinateurs portables ou un seul ordinateur portable, section groupe ou section) et l’extension vers le bas à tous les descendants du niveau que vous spécifiez.  <br/> |
|**Syntaxe** <br/> | `HRESULT GetHierarchy(`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]HierarchyScope hsScope,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(xs2013)]XMLSchema xsSchema);` <br/> |
|**Paramètres** <br/> | _bstrStartNodeID_ &ndash; Le nœud (bloc-notes, groupe de sections ou section) dont vous souhaitez que les descendants. Si vous passez une chaîne vide (« »), la méthode obtient tous les nœuds sous le nœud racine (autrement dit, tous les ordinateurs portables, les groupes de sections et sections). Si vous spécifiez un bloc-notes, le groupe de section ou le nœud de section, la méthode obtient uniquement les descendants de ce nœud.  <br/><br/>_hsScope_ &ndash; Le plus bas niveau de nœud descendant. Par exemple, si vous spécifiez des pages, la méthode obtient tous les nœuds dans la mesure où vers le bas comme le niveau de la page. Si vous spécifiez sections, la méthode obtient uniquement les nœuds de section en dessous du bloc-notes. Pour plus d’informations, voir l’énumération **HierarchyScope** dans la rubrique [énumérations](enumerations-onenote-developer-reference.md#odc_HierarchyScope) .  <br/><br/>_pbstrHierarchyXmlOut_ &ndash; Pointeur de A (paramètre de sortie) à la chaîne dans laquelle vous souhaitez que OneNote pour écrire la sortie XML.  <br/><br/>_xsSchema_ &ndash; (Facultatif) la version du schéma XML de OneNote, de type **XMLSchema**, que vous souhaitez en sortie. Vous pouvez spécifier si vous souhaitez que le schéma XML version 2013, 2010, 2007, ou la version actuelle.  <br/><br/>**Remarque**: nous vous recommandons de spécifier une version de OneNote (par exemple, **xs2013**) au lieu de l’aide de **xsCurrent** ou laisser vide, car cela permettra à votre complément travailler avec les futures versions de OneNote.           |
   
La méthode GetHierarchy renvoie qu'une chaîne au format OneNote 2013 XML par défaut, ou vous pouvez définir la version du schéma XML par défaut en utilisant le paramètre facultatif _xsSchema_ . 
  
En fonction des paramètres que vous transmettez, la méthode **GetHierarchy** peut renvoyer différentes listes (par exemple, tous les ordinateurs portables, toutes les sections dans toutes les pages dans un bloc-notes donné, toutes les pages au sein d’une section donnée ou tous les ordinateurs portables). Pour chaque nœud, la chaîne XML renvoyée fournit des propriétés (par exemple, le titre de section ou une page, ID et heure de dernière modification). 
  
Pas toutes les combinaisons de nœud de départ et l’étendue sont valides. Par exemple, si vous spécifiez une section Démarrer nœud et une étendue de bloc-notes, **GetHierarchy** renvoie un résultat null car un bloc-notes est supérieur dans la hiérarchie de nœud une section. 
  
L’exemple c# suivant montre comment utiliser la méthode **GetHierarchy** pour obtenir la hiérarchie OneNote entière, y compris tous les ordinateurs portables, au niveau de la page. Il copie la chaîne de sortie dans le Presse-papiers, à partir de laquelle vous pouvez coller la chaîne dans un éditeur de texte pour la révision. 
  
```cs
static void GetEntireHierarchy()
    {
        String strXML;
        OneNote.Application onApplication = new OneNote.Application();
        onApplication.GetHierarchy(null, 
            OneNote.HierarchyScope.hsPages, out strXML);
        Clipboard.SetText(strXML);
        MessageBox.Show("The XML has been copied to the clipboard");
    }

```

### <a name="updatehierarchy-method"></a>Méthode UpdateHierarchy

|||
|:-----|:-----|
|**Description**|Modifie ou met à jour la hiérarchie des ordinateurs portables. Par exemple, vous pouvez ajouter des sections ou des groupes de sections dans un bloc-notes, ajouter un nouvel ordinateur portable, déplacer des sections dans un bloc-notes, modifiez le nom d’une section, ajouter des pages à une section ou modifier l’ordre des pages dans les sections.|
|**Syntaxe**| `HRESULT UpdateHierarchy(`<br/>`[in]BSTR bstrChangesXmlIn,`<br/>`[in,defaultvalue(xsCurrent)] XMLSchema xsSchema);`|
|**Paramètres**| _bstrChangesXmlIn_ &ndash; Une chaîne qui contient le code XML OneNote qui spécifie les modifications de la hiérarchie à effectuer. Par exemple, si vous souhaitez insérer une nouvelle section, vous pouvez ajouter un élément de **Section** dans la chaîne XML pour indiquer où vous souhaitez que la nouvelle section à ajouter. Sinon, si vous souhaitez modifier le nom d’une section existante, vous pouvez conserver le même ID de section et changez son attribut de **nom** dans le code XML.<br/><br/>_xsSchema_ &ndash; (Facultatif) le OneNote version du schéma de la chaîne _bstrChangesXmln_. Cette valeur facultative est utilisée pour spécifier la version du schéma XML de OneNote figurant dans la chaîne _bstrChangesXmlIn_ . Si cette valeur n’est pas spécifiée, OneNote part du principe que le code XML est dans la version de schéma _xsCurrent_. <br/><br/>**Remarque**: nous vous recommandons de spécifier une version de OneNote (par exemple, **xs2013**) au lieu de l’aide de **xsCurrent** ou laisser vide, car cela permettra à votre complément travailler avec les futures versions de OneNote.           |
   
Si vous passez uniquement une chaîne XML OneNote partielle pour le paramètre _bstrChangesXmlIn_ , OneNote essaie de déduire les modifications souhaitées. Par exemple, si vous incluez un élément de **bloc-notes** contenant qu’une seule section, OneNote ajoute la section après toutes les sections existantes. Toutefois, si l’opération que vous spécifiez est ambigüe, le résultat peut être difficile à déterminer. Par exemple, si un bloc-notes existant contient quatre sections, ainsi que la chaîne XML que vous passez le bloc-notes et les sections quatrième et premières (dans cet ordre), OneNote peut-être placer les sections de deuxième et troisième avant la quatrième section ou après la première section . 
  
Vous ne pouvez pas utiliser la méthode **UpdateHierarchy** pour supprimer une partie d’un ordinateur portable. Autrement dit, en passant une chaîne XML qui inclut uniquement une partie d’une hiérarchie existante ne supprime pas les sections qui ne sont pas incluses dans la chaîne. Pour supprimer une partie d’une hiérarchie, utilisez la méthode **DeleteHierarchy** . 
  
Le code c# suivant illustre une manière d’utiliser la méthode **UpdateHierarchy** pour modifier la hiérarchie de OneNote, en modifiant le nom d’une section existante. Elle lit le code XML à partir d’un exemple de fichier nommé ChangeSectionName.xml à la racine du lecteur C, charge dans un document XML, puis passe la structure XML de ce document à la méthode. 
  
```cs
static void UpdateExistingHierarchy()
    {
        OneNote.Application onApplication = new OneNote.Application();
        
        // Get the XML from the file.
        XmlTextReader reader = new XmlTextReader("C:\\ChangeSectionName.xml");
        reader.WhitespaceHandling = WhitespaceHandling.None;
        XmlDocument xmlDocIn = new XmlDocument();
        xmlDocIn.Load(reader);
        
        // Update the hierarchy.
        onApplication.UpdateHierarchy(xmlDocIn.OuterXml,
        OneNote.XMLSchema.xs2007);   
    }

```

Le code XML suivant est un extrait du fichier ChangeSectionName.xml qui passe par le code c# précédent à la méthode. Lorsque le code XML est transmis à la méthode **UpdateHierarchy** , il modifie le nom d’une des sections de la hiérarchie existante (en modifiant la valeur de l’attribut **name** « Mon renommé section »). Ensuite, il supprime toutes les sections sauf celle dont le nom a été modifié. En outre, le code supprime les attributs superflus de l’élément de **Section** target, y compris les attributs de **couleur** , **isCurrentlyViewed**et **heure de dernière modification**, en laissant uniquement le **nom**, **l’ID**et ** chemin d’accès** attributs intactes. 
  
```XML
<?xml version="1.0" ?> 
    <one:Notebooks xmlns:one="http://schemas.microsoft.com/office/onenote/12/2004/onenote"> 
        <one:Notebook name="My Notebook" nickname="My Notebook" ID="{0B8E7305-AC2C-4BCB-8651-1CDA55AAE14C}{1}{B0}"> 
            <one:Section name="My Renamed Section" ID="{5F4E2908-44BA-4C02-91FE-49FC665E9A33}{1}{B0}" path="C:\My Section.one" /> 
        </one:Notebook> 
    </one:Notebooks>
```

Le code XML précédent a été obtenu en utilisant le code indiqué dans l’exemple de la méthode **GetHierarchy** , qui est modifiée, comme suit, pour limiter l’étendue aux sections. 
  
```cs
static void GetAllSections()
    {
        String strXML;
        OneNote.Application onApplication = new OneNote.Application();
        onApplication.GetHierarchy(System.String.Empty, 
            OneNote.HierarchyScope.hsSections, out strXML);
        Clipboard.SetText(strXML.ToString());
        MessageBox.Show("The XML has been copied to the Clipboard");
    }

```

L’exemple c# suivant montre une application de console complète qui recherche une section intitulée « `Sample_Section`», invite l’utilisateur à entrer un nouveau nom pour la section, puis utilise la méthode **UpdateHierarchy** pour modifier le nom de la section sur le nom que l’utilisateur typé. Avant d’exécuter le code, remplacez « `Sample_Section`» sur le nom d’une section qui existe dans votre hiérarchie de OneNote.
  
```cs
    static void Main(string[] args)
    {
        
        // OneNote 2013 Schema namespace.
        string strNamespace = "http://schemas.microsoft.com/office/onenote/2013/onenote";
        string outputXML;
        Application onApplication = new Application();
        onApplication.GetHierarchy(null, HierarchyScope.hsSections, out outputXML);
        // Load a new XmlDocument.
        XmlDocument xmlDoc = new XmlDocument();
        xmlDoc.LoadXml(outputXML);
        XmlNamespaceManager nsmgr = new XmlNamespaceManager(xmlDoc.NameTable);
            nsmgr.AddNamespace("one", strNamespace);
        // Search for the section named "Sample_Section".
        XmlNode xmlNode = xmlDoc.SelectSingleNode("//one:Section[@name='Sample_Section']", nsmgr);
        // Prompt for a new section title.
        System.Console.Write("Please enter a new title for the section: ");
        string input = System.Console.ReadLine();
        xmlNode.Attributes["name"].Value = input; 
        // Update the section with the new title.
        onApp.UpdateHierarchy(xmlNode.OuterXml);
        System.Console.Write("Done!\n");
    }

```

### <a name="openhierarchy-method"></a>Méthode OpenHierarchy

|||
|:-----|:-----|
|**Description** <br/> |Ouvre un groupe de sections ou une section que vous spécifiez.  <br/> |
|**Syntaxe** <br/> | `HRESULT OpenHierarchy(`<br/>`[in]BSTR bstrPath,`<br/>`[in]BSTR bstrRelativeToObjectID,`<br/>`[out]BSTR * pbstrObjectID,`<br/>`[in,defaultvalue(cftNone)]CreateFileType cftIfNotExist);` <br/> |
|**Paramètres** <br/> | _bstrPath_ &ndash; Le chemin d’accès que vous souhaitez ouvrir. Pour un ordinateur portable ou d’un groupe de section dans un bloc-notes, _bstrPath_ peut être un chemin d’accès du dossier ou le chemin d’accès à un fichier de section .one. Si vous spécifiez le chemin d’accès à un fichier de section .one, vous devez inclure l’extension .one sur la chaîne de chemin du fichier.  <br/><br/>_bstrRelativeToObjectID_ &ndash; OneNote d’identification de l’objet parent (bloc-notes ou la section groupe) sous lequel vous souhaitez le nouvel objet à ouvrir. Si le paramètre _bstrPath_ est le chemin d’accès absolu, vous pouvez passer une chaîne vide (« ») pour _bstrRelativeToObjectID_. Vous pouvez également transmettre l’ID d’objet du groupe bloc-notes ou une section qui doit contenir l’objet (section ou le groupe de section) que vous souhaitez créer, puis spécifiez le nom de fichier (par exemple, section1.one) de l’objet que vous souhaitez créer sous celui objet parent.  <br/><br/>_pbstrObjectID_ &ndash; (Paramètre de sortie) l’ID d’objet renvoyant du bloc-notes, section groupe, ou la méthode **OpenHierarchy** ouvre la section OneNote. Ce paramètre est un pointeur vers la chaîne dans laquelle vous souhaitez que la méthode pour écrire le code.  <br/><br/>_cftlfNotExist_ &ndash; (Facultatif) une valeur énumérée issue de l’énumération [CreateFileType](enumerations-onenote-developer-reference.md#odc_CreateFileType) . Si vous transmettez une valeur pour _cftIfNotExist_, la méthode **OpenHierarchy** crée le groupe de la section ou le fichier de section dans le chemin d’accès spécifié uniquement si le fichier n’existe pas déjà.  <br/> |
   
Si vous spécifiez un groupe de sections qui n’est pas dans un bloc-notes ouvert, la méthode **OpenHierarchy** ouvre le groupe de section en tant que bloc-notes. Si vous spécifiez une section qui n’est pas dans un bloc-notes ouvert, la méthode **OpenHierarchy** ouvre la section dans le groupe de section récents Sections ouvert. Si vous spécifiez un groupe de sections ou une section qui se trouve déjà dans un bloc-notes ouvert, rien ne se produit, car le groupe de section ou la section est déjà ouverte, ainsi que. Dans tous les cas, **OpenHierarchy** renvoie l’ID d’objet pour le groupe de section, un ordinateur portable ou une section que vous spécifiez, de sorte que vous pouvez l’utiliser dans d’autres opérations. 
  
Vous pouvez également utiliser la méthode **OpenHierarchy** pour créer de nouvelles sections, au lieu de cela à l’importation de données XML. 
  
Le code suivant montre comment utiliser la méthode **OpenHierarchy** pour ouvrir la section de réunions dans le bloc-notes de travail et obtenir l’ID de la section. Si la section n’existe pas déjà, OneNote crée à l’emplacement que vous spécifiez. 
  
```cs
static void OpenSection()
    {
        String strID;
        OneNote.Application onApplication = new OneNote.Application();
        onApplication.OpenHierarchy("C:\\Documents and Settings\\user\\My Documents\\OneNote Notebooks\\Work\\Meetings.one", 
        System.String.Empty, out strID, OneNote.CreateFileType.cftSection);
    }

```

### <a name="deletehierarchy-method"></a>Méthode DeleteHierarchy

|||
|:-----|:-----|
|**Description** <br/> |Supprime toute hierarchy, objet (groupe de section, section ou page) de la hiérarchie de bloc-notes OneNote.  <br/> |
|**Syntaxe** <br/> | `HRESULT DeleteHierarchy(`<br/>`[in]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL deletePermanently);` <br/> |
|**Paramètres** <br/> | _bstrObjectID_ &ndash; OneNote d’identification de l’objet que vous souhaitez supprimer. L’objet peut être un groupe de sections, une section ou une page.  <br/><br/>_dateExpectedLastModified_ &ndash; (Facultatif) la date et l’heure que vous pensez que l’objet que vous souhaitez supprimer a été modifié. Si vous transmettez une valeur non nulle pour ce paramètre, OneNote se poursuit avec la mise à jour uniquement si la valeur que vous passez correspond à la date réelle et l’heure de que dernière modification de l’objet. Passage d’une valeur pour ce paramètre permet d’éviter le remplacement par inadvertance modifie utilisateurs apportées depuis la dernière modification de l’objet.  <br/><br/>_deletePermanently_ &ndash; (Facultatif) **la valeur true** pour supprimer définitivement le contenu ; **false** pour déplacer le contenu dans OneNote Corbeille du bloc-notes correspondante (par défaut). Si l’ordinateur portable est au format de OneNote 2007, aucune Corbeille n’existe, afin que le contenu est définitivement supprimé.  <br/> |
   
### <a name="createnewpage-method"></a>Méthode CreateNewPage

|||
|:-----|:-----|
|**Description** <br/> |Ajoute une nouvelle page à la section que vous spécifiez. La nouvelle page est ajoutée en tant que la dernière page de la section  <br/> |
|**Syntaxe** <br/> | `HRESULT CreateNewPage(`<br/>`[in]BSTR bstrSectionID,`<br/>`[out]BSTR * pbstrPageID);`<br/>`[in,defaultvalue(npsDefault)]NewPageStyle npsNewPageStyle);` <br/> |
|**Paramètres** <br/> | _bstrSectionID_ &ndash; Une chaîne qui contient l’ID de OneNote de la section dans laquelle vous souhaitez créer la nouvelle page.  <br/><br/>_pbstrPageID_ &ndash; Pointeur de A (paramètre de sortie) à la chaîne dans laquelle la méthode écrit l’ID de OneNote pour la page nouvellement créée.  <br/><br/>_npsNewPageStyle_ &ndash; Une valeur de l’énumération **NewPageStyle** qui spécifie le style de la page à créer.  <br/> |
   
L’API OneNote inclut la méthode **CreateNewPage** commodité. Vous pouvez obtenir le même résultat, avec davantage de contrôle sur la façon dont la nouvelle page se trouve dans la hiérarchie, en appelant la méthode **UpdateHierarchy** . La méthode **UpdateHierarchy** vous permet également de créer des sous-pages en même temps que vous créez une nouvelle page. 
  
### <a name="closenotebook-method"></a>Méthode CloseNotebook

|||
|:-----|:-----|
|**Description** <br/> |Ferme le bloc-notes spécifié.  <br/> |
|**Syntaxe** <br/> | `HRESULT CloseNotebook(`<br/>`[in]BSTR bstrNotebookID,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL force);` <br/> |
|**Paramètres** <br/> | _bstrNotebookID_ &ndash; OneNote d’identification de l’ordinateur portable que vous souhaitez fermer.  <br/><br/>_forcer l’archivage_ &ndash; (Facultatif) **la valeur true** pour fermer le bloc-notes, même s’il existe des modifications dans le bloc-notes OneNote ne peut pas synchroniser avant de se fermer ; Sinon, **false** (valeur par défaut).  <br/> |
   
Vous pouvez utiliser la méthode **CloseNotebook** pour fermer le bloc-notes que vous spécifiez. Lorsque vous appelez cette méthode, OneNote synchronise les fichiers en mode hors connexion avec le contenu du bloc-notes actuel, si nécessaire, puis ferme le bloc-notes spécifié. Une fois que la méthode retourne, le bloc-notes n’apparaît plus dans la liste de bloc-notes dans l’interface utilisateur de OneNote (IU). 
  
### <a name="gethierarchyparent-method"></a>Méthode GetHierarchyParent

|||
|:-----|:-----|
|**Description** <br/> |Obtient l’ID de OneNote pour l’objet parent d’un objet OneNote.  <br/> |
|**Syntaxe** <br/> | `HRESULT GetHierarchyParent (`<br/>`[in]BSTR bstrObjectID,`<br/>`[out]BSTR * pbstrParentID);` <br/> |
|**Paramètres** <br/> | _bstrObjectID_ &ndash; Une chaîne qui contient l’ID de OneNote de l’objet dont vous souhaitez rechercher l’objet parent.  <br/><br/>_pbstrParentID_ &ndash; Pointeur de A (paramètre de sortie) à la chaîne dans laquelle la méthode écrit l’ID OneNote de l’objet parent.  <br/> |
   
Si l’objet OneNote n’a aucun objet parent (par exemple, lorsqu’un utilisateur souhaite obtenir le parent d’un ordinateur portable), une exception est levée.
  
### <a name="getspeciallocation-method"></a>Méthode GetSpecialLocation

|||
|:-----|:-----|
|**Description** <br/> |Recherche le chemin d’accès à l’emplacement où OneNote stocke certains éléments spéciaux, tels que les sauvegardes et notes non classées du bloc-notes par défaut.  <br/> |
|**Syntaxe** <br/> | `HRESULT GetSpecialLocation(`<br/>`[in]SpecialLocation slToGet,`<br/>`[out]BSTR * pbstrSpecialLocationPath);` <br/> |
|**Paramètres** <br/> | _slToGet_ &ndash; Une des valeurs d’énumération [SpecialLocation](enumerations-onenote-developer-reference.md#odc_SpecialLocation) qui spécifie l’emplacement du dossier spécial à récupérer.  <br/><br/>_pbstrSpecialLocationPath_ &ndash; Pointeur de A (paramètre de sortie) à la chaîne dans laquelle vous souhaitez OneNote pour écrire le chemin d’accès du dossier spécial.  <br/> |
   
Vous pouvez utiliser cette méthode pour déterminer l’emplacement sur le disque du dossier Notes non classées. C’est le dossier dans lequel OneNote stocke les notes sont créées lorsque vous faites glisser un élément dans OneNote, ainsi que les notes liées directement à partir d’autres applications (telles que celles qui se produire lorsque vous cliquez sur **Envoyer à OneNote** dans Microsoft Outlook ou Microsoft Internet Explorer). 
  
## <a name="page-content-methods"></a>Méthodes de contenu de page
<a name="ON14DevRef_Application_PageContent"> </a>

Les méthodes décrites dans cette section permettent à découvrir, mettre à jour et supprimer le contenu des pages dans les blocs-notes OneNote, ainsi que pour publier du contenu OneNote.
  
### <a name="getpagecontent-method"></a>Méthode GetPageContent

|||
|:-----|:-----|
|**Description**|Obtient l’ensemble du contenu (au format XML OneNote) de la page spécifiée.|
|**Syntaxe**| `HRESULT GetPageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[out]BSTR * pbstrPageXmlOut,`<br/>`[in,defaultvalue(piBasic)]PageInfo pageInfoToExport,`<br/>`[in,defaultvalue(xsCurrent)]XMLSchema xsSchema);`|
|**Paramètres**| _bstrPageId_ &ndash; OneNote d’identification de la page dont vous souhaitez obtenir le contenu.<br/><br/>_pbstrPageXmlOut_ &ndash; Pointeur de A (paramètre de sortie) à la chaîne dans laquelle vous souhaitez OneNote pour écrire la sortie XML.<br/><br/>_pageInfoToExport_ &ndash; (Facultatif) Spécifie si la méthode **GetPageContent** renvoie le contenu binaire, incorporée dans le code XML et codé en base 64. Contenu binaire peut inclure, par exemple, des images et les données d’entrée manuscrite. Le paramètre _pageInfoToExport_ spécifie également s’il faut marquer la sélection dans le code XML retourné par la méthode **GetPageContent** . Valeur énumérée issue de l’énumération [PageInfo](enumerations-onenote-developer-reference.md#odc_PageInfo) nécessaire.<br/><br/>_xsSchema_ &ndash; (Facultatif) la version du schéma XML de OneNote, de type **XMLSchema**, que vous souhaitez en sortie. Vous pouvez spécifier si vous souhaitez que le schéma XML version 2013, 2010, 2007, ou la version actuelle. <br/><br/>**Remarque**: nous vous recommandons de spécifier une version de OneNote (par exemple, **xs2013**) au lieu de l’aide de **xsCurrent** ou laisser vide, car cela permettra à votre complément travailler avec les futures versions de OneNote.           |
   
Par défaut, pour éviter la longueur excessive dans la chaîne XML qu’il renvoie, OneNote n’incorpore pas contenu binaire dans le code XML. Pour la même raison, il ne marque pas la sélection en cours avec les attributs de sélection. Les objets incluent un ID de OneNote dans leurs balises. Pour obtenir un objet binaire, vous appelez la méthode **GetBinaryPageContent** et passez l’ID de OneNote vous obtenir à partir de la méthode **GetPageContent** . Vous utilisez la méthode **GetPageContent** lorsque vous ne devez pas immédiatement les données binaires. 
  
### <a name="updatepagecontent-method"></a>Méthode UpdatePageContent

|||
|:-----|:-----|
|**Description**|Met à jour ou modifie le contenu dans la page.|
|**Syntaxe**| `HRESULT UpdatePageContent(`<br/>`[in]BSTR bstrPageChangesXmlIn,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(xsCurrent)]XMLSchema xsSchema,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL force);`|
|**Paramètres**| _bstrPageChangesXmlIn_ &ndash; Une chaîne qui contient le code XML OneNote qui inclut les modifications que vous souhaitez apporter à la page.<br/><br/>_dateExpectedLastModified_ &ndash; (Facultatif) la date et l’heure que vous pensez que la page que vous souhaitez mettre à jour a été modifié. Si vous transmettez une valeur non nulle pour ce paramètre, OneNote se poursuit avec la mise à jour uniquement si la valeur que vous passez correspond à la date réelle et l’heure de que dernière modification de la page. Passage d’une valeur pour ce paramètre permet d’éviter le remplacement par inadvertance modifie utilisateurs apportées depuis la dernière modification de la page.<br/><br/>_xsSchema_ &ndash; (Facultatif) la version du schéma XML de OneNote, de type **XMLSchema**, que vous souhaitez en sortie. Vous pouvez spécifier si vous souhaitez que XML version du schéma 2013, 2010, 2007, ou la version actuelle. <br/><br/>**Remarque**: nous vous recommandons de spécifier une version de OneNote (par exemple, **xs2013**) au lieu de l’aide de **xsCurrent** ou laisser vide, car cela permettra à votre complément travailler avec les futures versions de OneNote.<br/><br/>_forcer l’archivage_ (Facultatif) **true** pour mettre à jour le contenu de la page, même s’il existe données inconnu dans la page à partir d’une version ultérieure de OneNote ; Sinon, **false** (valeur par défaut). |
   
Vous pouvez utiliser cette méthode pour modifier la page de différentes manières. Par exemple, vous pouvez utiliser la méthode **UpdatePageContent** pour ajouter un contour à une page, modifiez le contenu d’un plan, ajouter des images, ajouter des entrées manuscrites, déplacer du contenu ou modifier le texte dans les plans. 
  
Un exemple plus spécifique, vous pouvez utiliser la méthode **GetPageContent** pour exporter une page existante, apporter quelques modifications au code XML de la page, puis utiliser la méthode **UpdatePageContent** pour importer la page entière à nouveau. Ou bien, vous pouvez utiliser cette méthode pour ajouter de nouveaux objets de page, tels que des images, vers le bas d’une page existante. 
  
Seuls les objets que vous devez inclure dans le code XML que vous passez à la méthode **UpdatePageContent** sont des objets de niveau page (par exemple, des plans, des images dans la page ou encre dans la page) qui ont été modifiés. Cette méthode ne pas modifier ou supprimer des objets de niveau page que vous ne spécifiez pas dans le paramètre _bstrPageChangesXmlIn_ . La méthode remplace entièrement des objets de niveau page, tels que des plans, dont les ID correspondent à ceux des objets que vous passez. Par conséquent, vous devez spécifier entièrement tous les objets de niveau page dans votre code, notamment leur contenu existant et les modifications que vous souhaitez apporter à leur. 
  
Par exemple, si votre page contient un plan et une image de page d’arrière-plan, vous pouvez remplacer le plan et laissez l’image non modifié par la spécification complètement le plan dans le code XML, à l’aide de l’ID de la structure existante et ne pas inclure l’image dans le code. Étant donné que le plan révisé que sont entièrement dans le code remplace le plan existant, vous devez inclure la totalité du plan.
  
En outre, la méthode **UpdatePageContent** modifie uniquement les propriétés d’élément que vous spécifiez dans le paramètre _bstrPageChangesXmlIn_ . Par exemple, si vous spécifiez certains, mais pas toutes les propriétés de l’élément **PageSettings** , les propriétés que vous ne spécifiez pas restent inchangées. 
  
L’exemple suivant montre comment utiliser la méthode **UpdatePageContent** pour modifier le titre d’une page et ajouter un échantillon de texte à la page. Avant d’exécuter le code, remplacez par un ID de page valide pour l’ID de page indiqué dans le code, afin que le code fonctionne sur votre ordinateur. Vous pouvez obtenir l’ID de page pour une page en utilisant la méthode **GetHierarchy** et en examinant la sortie. 
  
```cs
static void UpdatePageContent()
    {
        OneNote.Application onApplication = new OneNote.Application();
        String strImportXML;
        strImportXML = "<?xml version=\"1.0\"?>" +
            "<one:Page xmlns:one=\"http://schemas.microsoft.com/office/onenote/12/2004/onenote\" 
            ID=\"{3428B7BB-EF39-4B9C-A167-3FAE20630C37}{1}{B0}\">" +
            "    <one:PageSettings RTL=\"false\" color=\"automatic\">" +
            "        <one:PageSize>" +
            "            <one:Automatic/>" +
            "        </one:PageSize>" +
            "        <one:RuleLines visible=\"false\"/>" +
            "    </one:PageSettings>" +
            "    <one:Title style=\"font-family:Calibri;
                 font-size:17.0pt\" lang=\"en-US\">" +
            "        <one:OE alignment=\"left\">" +
            "            <one:T>" +
            "                <![CDATA[My Sample Page]]>" +
            "            </one:T>" +
            "        </one:OE>" +
            "    </one:Title>" +
            "    <one:Outline >" +
            "        <one:Position x=\"120\" y=\"160\"/>" +
            "        <one:Size width=\"120\" height=\"15\"/>" +
            "        <one:OEChildren>" +
            "            <one:OE alignment=\"left\">" +
            "                <one:T>" +
            "                    <![CDATA[Sample Text]]>" +
            "                </one:T>" +
            "            </one:OE>" +
            "        </one:OEChildren>" +
            "    </one:Outline>" +
            "</one:Page>";
        // Update the page content.
        onApplication.UpdatePageContent(strImportXML, System.DateTime.MinValue);
    }

```

### <a name="getbinarypagecontent-method"></a>Méthode GetBinaryPageContent

|||
|:-----|:-----|
|**Description** <br/> |Renvoie un objet binaire, telles que les entrées manuscrites ou des images, dans une page OneNote sous forme de chaîne codée en base 64.  <br/> |
|**Syntaxe** <br/> | `HRESULT GetBinaryPageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[in]BSTR bstrCallbackID,`<br/>`[out]BSTR * pbstrBinaryObjectB64Out);` <br/> |
|**Paramètres** <br/> | _bstrPageID_ &ndash; OneNote d’identification de la page qui contient l’objet binaire à obtenir.  <br/><br/>_bstrCallBackID_ &ndash; ID de l’objet binaire que vous souhaitez obtenir OneNote. Ce code, appelé un **callbackID**, est dans le code XML OneNote pour une page renvoyé par la méthode **GetPageContent** .  <br/><br/>_pbstrBinaryObectB64Out_ &ndash; Pointeur de A (paramètre de sortie) à une chaîne dans laquelle OneNote écrit l’objet binaire sous forme de chaîne codée en base 64.  <br/> |
   
### <a name="deletepagecontent-method"></a>Méthode DeletePageContent

|||
|:-----|:-----|
|**Description** <br/> |Supprime un objet &ndash; comme un objet **hiérarchique**, **encre**ou **Image** à partir d’une page.  <br/> |
|**Syntaxe** <br/> | `HRESULT DeletePageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[in]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL force);` <br/> |
|**Paramètres** <br/> | _bstrPageID_ &ndash; OneNote d’identification de la page qui contient l’objet à supprimer.  <br/><br/>_bstrObjectID_ &ndash; OneNote d’identification de l’objet que vous souhaitez supprimer.  <br/><br/>_dateExpectedLastModified_ &ndash; (Facultatif) la date et l’heure que vous pensez que la page qui contient le contenu que vous souhaitez supprimer a été modifié. Si vous transmettez une valeur non nulle pour ce paramètre, OneNote se poursuit avec la suppression uniquement si la valeur que vous passez correspond à la date réelle et l’heure de que dernière modification de la page. Passage d’une valeur pour ce paramètre permet d’empêcher remplacement par inadvertance les modifications apportées par les utilisateurs depuis la dernière que modification de la page.  <br/><br/>_forcer l’archivage_ &ndash; (Facultatif) **la valeur true** pour mettre à jour le contenu de la page, même s’il existe données inconnu dans la page à partir d’une version ultérieure de OneNote ; Sinon, **false** (valeur par défaut).  <br/> |
   
### <a name="publish-method"></a>Méthode Publish

|||
|:-----|:-----|
|**Description** <br/> |Exporte la page que vous spécifiez dans un fichier dans n’importe quel format OneNote prend en charge.  <br/> |
|**Syntaxe** <br/> | `HRESULT Publish(`<br/>`[in]BSTR bstrHierarchyID,`<br/>`[in]BSTR bstrTargetFilePath,`<br/>`[in,defaultvalue(pfOneNote)]PublishFormat pfPublishFormat,`<br/>`[in,defaultvalue(0)]BSTR bstrCLSIDofExporter);` <br/> |
|**Paramètres** <br/> | _bstrHierarchyID_ &ndash; OneNote d’identification de la hiérarchie à exporter.  <br/><br/>_bstrTargetFilePath_ &ndash; Le chemin absolu vers l’emplacement où vous souhaitez enregistrer le fichier de sortie. Le fichier que vous spécifiez doit être un objet qui n’existe pas déjà à cet emplacement.  <br/><br/>_pfPublishFormat_ &ndash; Une des valeurs d’énumération [PublishFormat](enumerations-onenote-developer-reference.md#odc_PublishFormat) qui spécifie le format dans lequel vous souhaitez la page publiée (par exemple, en MHTML, PDF, etc.).  <br/><br/>_bstrCLSIDofExporter_ &ndash; L’ID de classe (CLSID) d’une application COM inscrit peut exporter Microsoft Windows enhanced métafichiers (.emf). L’application COM doit implémenter l’interface **IMsoDocExporter** . Ce paramètre est fourni pour permettre aux développeurs tiers d’écrire leur propre code pour publier du contenu OneNote dans un format personnalisé. Pour plus d’informations sur l’interface **IMsoDocExporter** , voir [extension de la fonctionnalité d’exportation Office 2007 au Format fixe](http://msdn.microsoft.com/en-us/library/office/aa338206%28v=office.12%29.aspx).  <br/> |
   
Actuellement, OneNote prend en charge les formats de fichier suivants :
  
- Fichiers MHTML (.mht)
- Adobe Acrobat au format PDF (.pdf)
- Fichiers XML Paper Specification (XPS) (.xps)
- Fichiers de OneNote 2013, 2010 ou 2007 (.one)
- Fichiers de OneNote Package (.onepkg)
- Documents Microsoft Word (.doc ou .docx)
- Microsoft Windows Enhanced métafichiers (.emf)
- Fichiers HTML (.html)
    
Cette méthode produit exactement les mêmes résultats que vous obtenez en cliquant sur **Publier** dans l’interface utilisateur et qui spécifie le format. 
  
## <a name="navigation-methods"></a>Méthodes de navigation
<a name="ON14DevRef_Application_Navigation"> </a>

Les méthodes décrites dans cette section permettent de rechercher, accédez à et lien vers les blocs-notes OneNote, groupes de sections, sections, pages et les objets page.
  
### <a name="navigateto-method"></a>NavigateTo, méthode

|||
|:-----|:-----|
|**Description** <br/> |Accède à l’objet spécifié (par exemple, sections, pages et éléments du **plan** dans les pages).  <br/> |
|**Syntaxe** <br/> | `HRESULT NavigateTo(`<br/>`[in]BSTR bstrHierarchyObjectID,`<br/>`[in,defaultvalue(#)]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fNewWindow);` <br/> |
|**Paramètres** <br/> | _bstrHierarchyObjectID_ &ndash; OneNote d’identification de l’objet que vous souhaitez atteindre dans la hiérarchie de OneNote.  <br/><br/>_bstrObjectID_ &ndash; OneNote d’identification de l’objet que vous souhaitez atteindre dans la page OneNote.  <br/><br/>_fNewWindow_ &ndash; (Facultatif) **la valeur true** pour ouvrir l’objet spécifié dans une nouvelle fenêtre OneNote. **false** n’ouvre pas une nouvelle fenêtre OneNote si une est ouverte.  <br/> |
   
### <a name="navigatetourl-method"></a>Méthode NavigateToUrl

|||
|:-----|:-----|
|**Description** <br/> |Si passé un lien OneNote (onenote: / /), ouvre la fenêtre OneNote à l'emplacement correspondant dans OneNote. Si le lien est externe à OneNote (par exemple http:// ou file://), une boîte de dialogue sécurité s’affiche. Renvoi, OneNote essaie d’ouvrir le lien et une erreur **HResult.hrObjectDoesNotExist** est renvoyée.  <br/> |
|**Syntaxe** <br/> | `HRESULT NavigateTo(`<br/>`[in]BSTR bstrUrl,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fNewWindow);` <br/> |
|**Paramètres** <br/> | _bstrUrl_ &ndash; Une chaîne qui indique l’emplacement à atteindre. Cela peut être un lien OneNote ou autre URL, par exemple un web lien ou l’emplacement réseau.  <br/><br/>_fNewWindow_ &ndash; (Facultatif) **la valeur true** pour ouvrir l’URL spécifiée dans une nouvelle fenêtre OneNote. **false** n’ouvre pas une nouvelle fenêtre OneNote si une est ouverte.  <br/> |
   
### <a name="gethyperlinktoobject-method"></a>Méthode GetHyperLinkToObject

|||
|:-----|:-----|
|**Description** <br/> |Obtient un lien hypertexte OneNote pour le bloc-notes spécifié, le groupe de section, section, page ou objet page.  <br/> |
|**Syntaxe** <br/> | `HRESULT GetHyperlinkToObject(`<br/>`[in] BSTR bstrHierarchyID,`<br/>`[in] BSTR bstrPageContentObjectID,`<br/>`[out] BSTR * pbstrHyperlinkOut);` <br/> |
|**Paramètres** <br/> | _bstrHierarchyID_ &ndash; L’ID de OneNote pour le bloc-notes, le groupe de section, section ou page pour laquelle vous souhaitez un lien hypertexte.  <br/><br/>_bstrPageContentObjectID_ &ndash; L’ID de OneNote (facultatif) pour l’objet au sein de la page pour laquelle vous souhaitez un lien hypertexte. Par exemple, l’objet peut être un plan ou un élément de **plan** . Si vous passez une chaîne vide (« »), le lien retourné pointe vers le bloc-notes, le groupe de section, section ou page que vous avez spécifié dans le paramètre _bstrHierarchyID_ . Si vous passez une chaîne vide pour le paramètre _bstrPageContentObjectID_ , le paramètre _bstrHierarchyID_ doit être une référence à la page qui contient l’objet spécifié.  <br/><br/>_pbstrHyperlinkOut_ &ndash; Pointeur de A (paramètre de sortie) à une chaîne dans laquelle la méthode **GetHyperlinkToObject** écrit le texte de lien hypertexte de sortie.  <br/> |
   
Lorsque vous essayez d’accéder au lien qui en résulte, OneNote s’ouvre et affiche l’objet spécifié dans le navigateur.
  
### <a name="getwebhyperlinktoobject-method"></a>Méthode GetWebHyperlinktoObject

|||
|:-----|:-----|
|**Description** <br/> |Renvoie un lien hypertexte à un objet qui s’ouvre dans le Client Web de OneNote.  <br/> |
|**Syntaxe** <br/> | `HRESULT GetWebHyperlinkToObject (`<br/>`[in] BSTR bstrHierarchyID,`<br/>`[in] BSTR bstrPageContentObjectID,`<br/>`[out] BSTR * pbstrHyperlinkOut);` <br/> |
|**Paramètres** <br/> | _bstrHierarchyID_ &ndash; L’ID de OneNote du bloc-notes, section groupe, section ou une page pour laquelle vous souhaitez un lien hypertexte web.  <br/><br/>_bstrPageContentObjectID_ &ndash; L’ID de OneNote (facultatif) pour l’objet au sein de la page pour laquelle vous souhaitez un lien hypertexte. Par exemple, l’objet peut être un plan ou un élément de **plan** . Si vous passez une chaîne vide (« »), le lien retourné pointe vers le bloc-notes, le groupe de section, section ou page que vous avez spécifié dans le paramètre _bstrHierarchyID_ . Si vous passez une chaîne vide pour le paramètre _bstrPageContentObjectID_ , le paramètre _bstrHierarchyID_ doit être une référence à la page qui contient l’objet spécifié.  <br/><br/>_pbstrHyperlinkOut_ &ndash; Pointeur de A (paramètre de sortie) à une chaîne dans laquelle la méthode **GetWebHyperlinkToObject** écrit le texte de lien hypertexte de sortie. Si un lien hypertexte web ne peut pas être créé pour l’ordinateur portable, une valeur nulle est renvoyée.  <br/> |
   
### <a name="findpages-method"></a>Méthode FindPages

|||
|:-----|:-----|
|**Description**|Renvoie une liste des pages qui correspondent au terme de la requête spécifiée.|
|**Syntaxe**| `HRESULT FindPages(`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]BSTR bstrSearchBSTR,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL fIncludeUnindexedPages,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fDisplay,`<br/>`[in,defaultvalue(#)]XMLSchema xsSchema);`|
|**Paramètres**| _bstrStartNodeID_ &ndash; Le nœud (racine, ordinateur portable, le groupe de section ou section) sous lequel rechercher du contenu. Ce paramètre définit l’étendue de la recherche.<br/><br/>_bstrSearchString_ &ndash; La chaîne de recherche. Passez exactement la même chaîne que vous tapez dans la zone de recherche dans l’UI OneNote. Vous pouvez utiliser les opérateurs de bits, telles que **et** et **ou**, qui doit être en majuscule.<br/><br/>_pbstrHierarchyXmlOut_ &ndash; Pointeur de A (paramètre de sortie) à une chaîne dans laquelle vous souhaitez OneNote pour écrire la chaîne XML de sortie. La chaîne XML qui en résulte contient la hiérarchie de bloc-notes à partir de la racine vers le bas, y compris, toutes les pages qui correspondent à la chaîne de recherche. Par exemple, la méthode **FindPages** ne répertorie pas les sections qui ne possèdent aucune correspondance de page dans la hiérarchie. En outre, si seulement une page dans une seule section correspond à la chaîne, la hiérarchie renvoyée inclut le chemin d’accès à cette section et de page, mais à aucune des autres parties de la hiérarchie de bloc-notes.<br/><br/>_fIncludeUnindexedPages_ &ndash; (Facultatif) **la valeur true** pour rechercher des pages qui n’ont pas été indexés par la recherche de Windows ; Sinon, **false**.<br/><br/>_fDisplay_ &ndash; (Facultatif) **true** également exécuter la recherche dans l’interface utilisateur de l’utilisateur, comme si l’utilisateur a tapé eux-mêmes. **false** pour effectuer la requête sans modifier l’interface utilisateur (par défaut).<br/><br/>_xsSchema_ &ndash; (Facultatif) le OneNote version du schéma de la chaîne _pbstrHierarchyXmlOut_. Cette valeur facultative est utilisée pour spécifier la version du schéma XML de OneNote qui contient la chaîne _pbstrHierarchyXmlOut_ . Si cette valeur n’est pas spécifiée, OneNote part du principe que le code XML est dans la version de schéma _xsCurrent_. <br/><br/>**Remarque**: nous vous recommandons de spécifier une version de OneNote (par exemple, **xs2013**) au lieu de l’aide de **xsCurrent** ou laisser vide, car cela permettra à votre complément travailler avec les futures versions de OneNote.           |
   
 **FindPages** fonctionne uniquement si vous avez Microsoft Search 3.0 ou 4.0 est installé sur votre ordinateur. Windows Vista et Windows 7 incluent ce composant. Toutefois, si vous exécutez une version antérieure de Windows, vous devez installer [Windows Search](http://www.microsoft.com/windows/products/winfamily/desktopsearch/getitnow.mspx) **FindPages** travailler. 
  
### <a name="findmeta-method"></a>Méthode FindMeta

|||
|:-----|:-----|
|**Description**|Renvoie une liste d’objets OneNote qui contiennent des métadonnées qui correspond au terme de la requête spécifiée.|
|**Syntaxe**| `HRESULT FindMeta (`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]BSTR bstrSearchBSTRName,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL fIncludeUnindexedPages,`<br/>`[in,defaultvalue(#)]XMLSchema xsSchema);`|
|**Paramètres**| _bstrStartNodeID_ &ndash; Le nœud (racine, ordinateur portable, le groupe de section ou section) sous lequel rechercher du contenu. Ce paramètre définit l’étendue de la recherche.<br/><br/>_bstrSearchStringName_ &ndash; La chaîne de recherche. Passez dans n’importe quelle partie du nom de métadonnées. Si vous passez une chaîne vide ou une valeur null, tous les objets qui ont des métadonnées seront correspondent à la requête.<br/><br/>_pbstrHierarchyXmlOut_ &ndash; Pointeur de A (paramètre de sortie) à une chaîne dans laquelle vous souhaitez OneNote pour écrire la chaîne XML de sortie. La chaîne XML qui en résulte contient la hiérarchie de bloc-notes à partir de la racine vers le bas, y compris, toutes les pages qui correspondent à la chaîne de recherche. Par exemple, la méthode **FindPages** ne répertorie pas les sections qui ne possèdent aucune correspondance de page dans la hiérarchie. En outre, si seulement une page dans une seule section correspond à la chaîne, la hiérarchie renvoyée inclut le chemin d’accès à cette section et de page, mais à aucune des autres parties de la hiérarchie de bloc-notes.  <br/><br/>_fIncludeUnindexedPages_ &ndash; (Facultatif) **la valeur true** pour rechercher des pages qui n’ont pas été indexés par la recherche de Windows ; Sinon, **false**.<br/><br/>_xsSchema_ &ndash; (Facultatif) le OneNote version du schéma de la chaîne _pbstrHierarchyXmlOut_. Cette valeur facultative est utilisée pour spécifier la version du schéma XML de OneNote qui contient la chaîne _pbstrHierarchyXmlOut_ . Si cette valeur n’est pas spécifiée, OneNote part du principe que le code XML est dans la version de schéma _xsCurrent_. <br/><br/>**Remarque**: nous vous recommandons de spécifier une version de OneNote (par exemple, **xs2013**) au lieu de l’aide de **xsCurrent** ou laisser vide, car cela permettra à votre complément travailler avec les futures versions de OneNote.           |
   
**FindMeta** fonctionne uniquement si vous avez Microsoft Windows Search 3.0 ou 4.0 est installé sur votre ordinateur. Windows Vista et Windows 7 incluent ce composant. Toutefois, si vous exécutez une version antérieure de Windows, vous devez installer [Windows Search](http://www.microsoft.com/windows/products/winfamily/desktopsearch/getitnow.mspx) **FindMeta** travailler. 
  
## <a name="functional-methods"></a>Méthodes fonctionnels
<a name="ON14DevRef_Application_Functional"> </a>

Les méthodes décrites dans cette section permettent d’effectuer certaines actions ou définir des paramètres de l’application OneNote.
  
### <a name="mergefiles-method"></a>Méthode MergeFiles

|||
|:-----|:-----|
|**Description** <br/> |Permet aux utilisateurs de fusionner les modifications pour le même fichier en une seule. Pour les fichiers à prendre en compte les mêmes, ils doivent avoir le même ID de OneNote.  <br/> |
|**Syntaxe** <br/> | `HRESULT MergeFiles (`<br/>`[in]BSTR bstrBaseFile,`<br/>`[in]BSTR bstrClientFile,`<br/>`[in]BSTR bstrServerFile,`<br/>`[in]BSTR bstrTargetFile);` <br/> |
|**Paramètres** <br/> | _bstrBaseFile_ &ndash; La chaîne de chemin d’accès à l’emplacement du fichier de l’état initial du fichier .one.  <br/><br/>_bstrClientFile_ &ndash; La chaîne de chemin d’accès à l’emplacement du fichier .one de la deuxième ensemble de modifications à fusionner avec le fichier de base après la modification du fichier de serveur est fusionnées avec la base.  <br/><br/>_bstrServerFile_ &ndash; La chaîne de chemin d’accès à l’emplacement du fichier .one de la première série de modifications à fusionner avec le fichier de base.  <br/><br/>_bstrTargetFile_ &ndash; La chaîne de chemin d’accès à l’emplacement du fichier .one du fichier avec les modifications fusionnées.  <br/> |
   
La méthode **MergeFiles** a été conçue pour les scénarios dans lesquels plusieurs versions d’un fichier OneNote peuvent exister. 
  
### <a name="mergesections-method"></a>Méthode MergeSections

|||
|:-----|:-----|
|**Description** <br/> |Fusionne le contenu d’une section dans un autre dans OneNote.  <br/> |
|**Syntaxe** <br/> | `HRESULT MergeSections (`<br/>`[in]BSTR bstrSectionSourceId,`<br/>`[in]BSTR bstrSectionDestinationId);` <br/> |
|**Paramètres** <br/> | _bstrSectionSourceId_ &ndash; OneNote d’identification de la section à fusionner.  <br/><br/>_bstrSectionDestinationId_ &ndash; ID de la section à fusionner dans OneNote. La section source est fusionnée dans cette section de destination.  <br/> |
   
Cette méthode effectue la même opération que la fonctionnalité **Fusionner dans une autre Section** qui est affichée lorsque vous cliquez sur une section. 
  
### <a name="quickfiling-method"></a>Méthode QuickFiling

|||
|:-----|:-----|
|**Description** <br/> |Retourne une instance de la boîte de dialogue [IQuickFilingDialog](quick-filing-dialog-box-interfaces-onenote.md#odc_IQuickFilingDialog) , qui peut être utilisée pour sélectionner un emplacement dans l’arborescence de la hiérarchie OneNote.  <br/> |
|**Syntaxe** <br/> | `HRESULT QuickFiling (`<br/>` );` <br/> |
   
### <a name="synchierarchy-method"></a>Méthode SyncHierarchy

|||
|:-----|:-----|
|**Description** <br/> |Force OneNote pour la synchronisation de l’objet spécifié avec le fichier source sur le disque.  <br/> |
|**Syntaxe** <br/> | `HRESULT SyncHierarchy (`<br/>`[in]BSTR bstrHierarchyID);` <br/> |
|**Paramètres** <br/> | _bstrHierarchyID_ &ndash; OneNote ID de l’objet d’être synchronisées.  <br/> |
   
### <a name="setfilinglocation-method"></a>Méthode SetFilingLocation

|||
|:-----|:-----|
|**Description** <br/> |Permet aux utilisateurs de spécifier où et comment certains types de contenu doivent être déposés dans OneNote.  <br/> |
|**Syntaxe** <br/> | `HRESULT SetFilingLocation (`<br/>`[in]FilingLocation flToSet,`<br/>`[in]FilingLocationType fltToSet,`<br/>`[in]BSTR bstrFilingSectionID);`           <br/> |
|**Paramètres** <br/> | _flToSet_ &ndash; De l’emplacement de dépôt pour définir le type d’objet.  <br/><br/>_fltToSet_ &ndash; L’emplacement dans lequel le type de fichier.  <br/><br/>_bstrFilingSectionID_ &ndash; OneNote d’identification de la section ou une page à l’endroit où vous souhaitez définir. Si ce n’est pas le cas échéant, l’utilisateur peut passer dans la valeur null ou une chaîne vide.  <br/> |
   
Les types de contenu qui peuvent être classés incluent les éléments Outlook et Notes Web à partir d’Internet Explorer qui sont importées dans OneNote par le biais de la commande **Envoyer à OneNote** dans chaque application. L’emplacement de classement d’éléments qui sont imprimées dans OneNote peut également être définie avec cette méthode. 
  
## <a name="properties"></a>Propriétés
<a name="ON14DevRef_Application_Properties"> </a>

Cette section décrit les propriétés de l’interface de **l’Application** . 
  
|**Propriété**|**Description**|
|:-----|:-----|
|**Windows** <br/> |Donne aux utilisateurs l’accès ouvert OneNote windows. Cette propriété permet aux utilisateurs d’énumérer l’ensemble des fenêtres OneNote et modifier certaines propriétés de la fenêtre. Pour plus d’informations, voir [Interfaces Windows](window-interfaces-onenote.md).  <br/> |
|**COMAddIns** <br/> |Renvoie la collection **COMAddIns** pour OneNote. Cette collection contient tous les compléments COM qui sont disponibles à OneNote. La propriété **Count** de la collection **COMAddins** renvoie le nombre de compléments COM disponibles. Pour plus d’informations, voir l’objet [COMAddIns](http://msdn.microsoft.com/en-us/library/office/ff865489.aspx) .  <br/> |
|**LanguageSettings** <br/> |Permet d’accéder à certaines API pour modifier les paramètres de langue courantes de OneNote.  <br/> |
   
## <a name="events"></a>Événements
<a name="ON14DevRef_Application_Events"> </a>

Cette section décrit les événements de l’interface de l’Application.
  
> [!CAUTION]
> Événements actuellement ne peut pas être ajoutés dans le code managé. 
  
### <a name="onnavigate-event"></a>Événement OnNavigate

|||
|:-----|:-----|
|**Description** <br/> |Autorise un utilisateur à affecter une fonction à appeler lorsque l’UI OneNote est quitté l’emplacement actuel de OneNote.  <br/> |
|**Syntaxe** <br/> | `Event OnNavigate (`<br/>` );` <br/> |
   
### <a name="onhierarchychange-method"></a>Méthode OnHierarchyChange

|||
|:-----|:-----|
|**Description** <br/> |Autorise un utilisateur à affecter une fonction à appeler chaque fois que les modifications de la hiérarchie OneNote (par exemple, ajout ou suppression de pages ou déplacement des sections). Modifications de la hiérarchie sont regroupées, afin que si plusieurs modifications sont apportées au niveau ou en même temps, OneNote déclenche l’événement qu’une seule fois.  <br/> |
|**Syntaxe** <br/> | `Event OnHierarchyChange (`<br/>` BSTR bstrActivePageID);` <br/> |
|**Paramètres** <br/> | _bstrActivePageID_ &ndash; Transmet l’ID de OneNote de la page active.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Référence du développeur OneNote](onenote-developer-reference.md)

