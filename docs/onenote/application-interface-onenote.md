---
title: Interface d’application (OneNote)
manager: lindalu
ms.date: 02/22/2022
ms.audience: Developer
ms.topic: overview
ms.assetid: 87926f7d-e1dc-41d5-8805-6ba91fc7b154
description: 'L’interface d’application inclut des méthodes qui vous aident à récupérer, à manipuler et à mettre à jour les informations et le contenu de OneNote. Les méthodes se divisent en quatre catégories générales :'
ms.localizationpriority: high
ms.openlocfilehash: 50bec66f7418c1035ec898a6c438ac84c09c51f9
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374760"
---
# <a name="application-interface-onenote"></a>Interface d’application (OneNote)

L’interface d’**application** inclut des méthodes qui vous aident à récupérer, à manipuler et à mettre à jour les informations et le contenu de OneNote. Les méthodes se divisent en quatre catégories générales :
  
- **Structure de bloc-notes** &ndash; Méthodes permettant d’utiliser la structure de bloc-notes, y compris les méthodes de découverte, d’ouverture, de modification, de fermeture et de suppression de blocs-notes, de groupes de sections et de sections.

- **Contenu de page** &ndash; Méthodes permettant d’utiliser les pages et le contenu de page, y compris les méthodes de découverte, de modification, d’enregistrement et de suppression du contenu de page. Le contenu de page inclut les objets binaires, comme les entrées manuscrites et les images, ainsi que les objets texte, tels que les plans.

- **Navigation** &ndash; Méthodes de recherche, de liaison et de navigation dans les pages et les objets.

- **Fonctionnelle** &ndash; Toutes les autres méthodes qui effectuent certaines actions ou définissent des paramètres dans OneNote.

En outre, l’interface d’**application** inclut un certain nombre de *propriétés* et d’*événements*.
  
## <a name="notebook-structure-methods"></a>Méthodes de structure de bloc-notes

<a name="ON14DevRef_Application_NotebookStructure"> </a>

Les méthodes décrites dans cette section vous permettent de découvrir, d’ouvrir, de modifier, de fermer et de supprimer des blocs-notes, des groupes de sections et des sections OneNote.
  
### <a name="gethierarchy-method"></a>Méthode GetHierarchy

|||
|:-----|:-----|
|**Description** <br/> |Obtient la structure de la hiérarchie du nœud de bloc-notes, en commençant par le nœud que vous spécifiez (tous les blocs-notes ou un seul bloc-notes, un groupe de sections ou une section), puis en continuant avec tous les descendants au niveau que vous spécifiez. |
|**Syntaxe** <br/> | `HRESULT GetHierarchy(`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]HierarchyScope hsScope,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(xs2013)]XMLSchema xsSchema);` <br/> |
|**Paramètres** <br/> | *bstrStartNodeID* &ndash; Nœud (bloc-notes, groupe de sections ou section) dont vous souhaitez obtenir les descendants. Si vous indiquez une chaîne null (« »), la méthode obtient tous les nœuds sous le nœud racine (autrement dit, tous les blocs-notes, tous les groupes de sections et toutes les sections). Si vous spécifiez un nœud de type bloc-notes, groupe de sections ou section, la méthode obtient uniquement les descendants de ce nœud.<br/>*hsScope* &ndash; Niveau de nœud descendant souhaité le plus bas. Par exemple, si vous spécifiez les pages, la méthode obtient tous les nœuds jusqu’au niveau page. Si vous spécifiez les sections, la méthode obtient uniquement les nœuds de section sous le bloc-notes. Pour plus d’informations, reportez-vous à l’énumération **HierarchyScope** dans la rubrique [Énumérations](enumerations-onenote-developer-reference.md#odc_HierarchyScope).<br/>*pbstrHierarchyXmlOut* &ndash; (Paramètre de sortie) Pointeur vers la chaîne dans laquelle vous voulez que OneNote écrive la sortie XML.<br/>*xsSchema* &ndash; (Facultatif) Version du schéma XML OneNote, de type **XMLSchema**, que vous voulez obtenir en sortie. Vous pouvez spécifier la version de schéma XML 2013, 2010, 2007 ou la version actuelle.<br/>**Remarque :** pour que votre complément fonctionne avec les versions ultérieures de OneNote, nous vous recommandons de spécifier une version de OneNote (par exemple, **xs2013**) plutôt que d’utiliser **xsCurrent** ou de laisser le champ vide.           |

La méthode GetHierarchy renvoie une chaîne au format XML OneNote 2013 par défaut. Sinon, vous pouvez définir la version de schéma XML par défaut à l’aide du paramètre facultatif *xsSchema*.
  
En fonction des paramètres que vous spécifiez, la méthode **GetHierarchy** peut renvoyer plusieurs listes (par exemple, tous les blocs-notes, toutes les sections dans tous les blocs-notes, toutes les pages dans une section donnée ou toutes les pages dans un bloc-notes donné). Pour chaque nœud, la chaîne XML renvoyée fournit des propriétés (par exemple, le titre de la page ou de la section, l’ID et l’heure de la dernière modification).
  
Toutes les combinaisons de nœud de départ et d’étendue ne sont pas valides. Par exemple, si vous spécifiez un nœud de début de section et une portée de bloc-notes, **GetHierarchy** renvoie un résultat nul car un bloc-notes est plus haut dans la hiérarchie des nœuds qu’une section.
  
L’exemple C# qui suit indique comment utiliser la méthode **GetHierarchy** pour obtenir la hiérarchie OneNote entière, y compris tous les blocs-notes jusqu’au niveau page. GetHierarchy copie la chaîne de sortie dans le Presse-papiers, à partir duquel vous pouvez coller la chaîne dans un éditeur de texte pour révision.
  
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
|**Description**|Modifie ou met à jour la hiérarchie des bloc-notes. Par exemple, vous pouvez ajouter des sections ou des groupes de sections à un bloc-notes, ajouter un nouveau bloc-notes, déplacer des sections au sein d’un bloc-notes, modifier le nom d’une section, ajouter des pages à une section ou modifier l’ordre des pages dans des sections.|
|**Syntaxe**| `HRESULT UpdateHierarchy(`<br/>`[in]BSTR bstrChangesXmlIn,`<br/>`[in,defaultvalue(xsCurrent)] XMLSchema xsSchema);`|
|**Paramètres**| *bstrChangesXmlIn* &ndash; Chaîne contenant le code XML OneNote qui spécifie les modifications de hiérarchie à apporter. Par exemple, si vous voulez insérer une nouvelle section, vous pouvez ajouter un élément **Section** dans la chaîne XML afin d’indiquer l’emplacement où la nouvelle section doit être ajoutée. Par ailleurs, si vous voulez modifier le nom d’une section existante, vous pouvez conserver le même ID de section et modifier son attribut **name** dans le code XML.<br/><br/>*xsSchema* &ndash; (Facultatif) Version de schéma OneNote de la chaîne *bstrChangesXmln*. Cette valeur facultative est utilisée pour spécifier la version du schéma XML OneNote qui contient la chaîne *bstrChangesXmlIn*. Si cette valeur n’est pas spécifiée, OneNote part du principe que la version du schéma XML est *xsCurrent*. <br/><br/>**Remarque :** pour que votre complément fonctionne avec les versions ultérieures de OneNote, nous vous recommandons de spécifier une version de OneNote (par exemple, **xs2013**) plutôt que d’utiliser **xsCurrent** ou de laisser le champ vide.           |

Si vous transmettez uniquement une chaîne partielle XML OneNote pour le paramètre *bstrChangesXmlIn*, OneNote tente de déduire les modifications souhaitées. Par exemple, si vous incluez un élément **Notebook** qui ne contient qu’une section, OneNote ajoute la section après toute section existante. Toutefois, si l’opération que vous spécifiez est ambiguë, le résultat peut être difficile à déterminer. Par exemple, si un bloc-notes existant contient quatre sections et si la chaîne XML que vous spécifiez inclut le bloc-notes, ainsi que la quatrième et la première sections (dans cet ordre) uniquement, OneNote peut placer la deuxième et la troisième sections avant la quatrième section ou après la première section.
  
Vous ne pouvez pas utiliser la méthode **UpdateHierarchy** pour supprimer une partie d’un bloc-notes. Autrement dit, la spécification d’une chaîne XML qui inclut uniquement une partie d’une hiérarchie existante ne supprime pas les sections qui ne sont pas incluses dans la chaîne. Pour supprimer une partie d’une hiérarchie, utilisez la méthode **DeleteHierarchy**.
  
Le code C# qui suit illustre une manière d’utiliser la méthode **UpdateHierarchy** afin de modifier la hiérarchie OneNote, en changeant le nom d’une section existante. Cette opération lit le code XML à partir d’un exemple de fichier nommé ChangeSectionName.xml au niveau de la racine du lecteur C, le charge dans un document XML, puis transmet la structure XML de ce document à la méthode.
  
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

Le code XML suivant est un extrait du fichier ChangeSectionName.xml que le code C# précédent transmet à la méthode. Lorsque le code XML est transmis à la méthode **UpdateHierarchy**, il modifie le nom d’une des sections dans la hiérarchie existante (en remplaçant la valeur de l’attribut **name** par « My Renamed Section »). Ensuite, il supprime toutes les sections à l’exception de celle dont le nom a été modifié. Par ailleurs, le code supprime les attributs inutiles de l’élément **Section** cible, y compris les attributs **lastModifiedTime**, **isCurrentlyViewed** et **color**, en laissant intacts uniquement les attributs **name**, **ID** et **path**.
  
```XML
<?xml version="1.0" ?> 
    <one:Notebooks xmlns:one="http://schemas.microsoft.com/office/onenote/12/2004/onenote"> 
        <one:Notebook name="My Notebook" nickname="My Notebook" ID="{0B8E7305-AC2C-4BCB-8651-1CDA55AAE14C}{1}{B0}"> 
            <one:Section name="My Renamed Section" ID="{5F4E2908-44BA-4C02-91FE-49FC665E9A33}{1}{B0}" path="C:\My Section.one" /> 
        </one:Notebook> 
    </one:Notebooks>
```

Le code XML précédent a été obtenu en utilisant le code indiqué dans l’exemple pour la méthode **GetHierarchy**, qui a été modifié comme suit pour limiter l’étendue aux sections.
  
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

L’exemple C# suivant montre une application console complète qui recherche une section nommée "`Sample_Section`", invite l’utilisateur à entrer un nouveau nom pour la section, puis utilise la méthode **UpdateHierarchy** pour remplacer le nom de la section par le nom que l’utilisateur a tapé. Avant d’exécuter le code, remplacez "`Sample_Section`" par le nom d’une section qui existe dans votre hiérarchie OneNote.
  
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
|**Description** <br/> |Ouvre le groupe de sections ou la section que vous spécifiez. |
|**Syntaxe** <br/> | `HRESULT OpenHierarchy(`<br/>`[in]BSTR bstrPath,`<br/>`[in]BSTR bstrRelativeToObjectID,`<br/>`[out]BSTR * pbstrObjectID,`<br/>`[in,defaultvalue(cftNone)]CreateFileType cftIfNotExist);` <br/> |
|**Paramètres** <br/> | *bstrPath* &ndash; Chemin d’accès que vous souhaitez ouvrir. Pour un bloc-notes ou pour un groupe de sections dans un bloc-notes, *bstrPath* peut être un chemin de dossier ou le chemin d’accès à un fichier de section .one. Si vous définissez le chemin d’accès vers un fichier de section .one, vous devez inclure l’extension .one dans la chaîne de chemin d’accès au fichier.<br/>*bstrRelativeToObjectID* &ndash; ID OneNote de l’objet parent (bloc-notes ou groupe de sections) sous lequel vous souhaitez que le nouvel objet s’ouvre. Si le paramètre *bstrPath* est un chemin absolu, vous pouvez passer une chaîne vide ("") pour *bstrRelativeToObjectID*. Sinon, vous pouvez transmettre l’ID d’objet du groupe de sections ou du bloc-notes qui doit contenir l’objet (section ou groupe de sections) à créer, puis spécifier le nom du fichier (par exemple, section1.one) de l’objet à créer sous cet objet parent.<br/>*pbstrObjectID* &ndash; (Paramètre de sortie) ID de l’objet renvoyé par OneNote pour le bloc-notes, le groupe de sections ou la section que la méthode **OpenHierarchy** ouvre. Ce paramètre est un pointeur vers la chaîne dans laquelle vous souhaitez que la méthode écrive l’ID.<br/>*cftlfNotExist* &ndash; (Facultatif) Une valeur énumérée de l’énumération [CreateFileType](enumerations-onenote-developer-reference.md#odc_CreateFileType). Si vous transmettez une valeur pour *cftIfNotExist*, la méthode **OpenHierarchy** crée le groupe de sections ou le fichier de section au chemin spécifié uniquement si le fichier n’existe pas déjà. |

Si vous spécifiez un groupe de sections qui ne figure pas dans un bloc-notes ouvert, la méthode **OpenHierarchy** ouvre le groupe de sections sous la forme d’un bloc-notes. Si vous spécifiez une section qui ne se trouve pas dans un bloc-notes ouvert, la méthode **OpenHierarchy** ouvre la section dans le groupe de sections récemment ouvertes. Si vous spécifiez un groupe de sections ou une section qui se trouve déjà dans un bloc-notes ouvert, rien ne se produit, car la section ou le groupe de sections est déjà ouvert. Dans tous les cas, **OpenHierarchy** renvoie l’ID d’objet pour le groupe de sections, le bloc-notes ou la section que vous spécifiez, afin que vous puissiez l’utiliser dans d’autres opérations.
  
Vous pouvez également utiliser la méthode **OpenHierarchy** pour créer de nouvelles sections au lieu d’importer du code XML.
  
Le code suivant indique comment utiliser la méthode **OpenHierarchy** pour ouvrir la section Meetings dans le bloc-notes Work et obtenir l’ID de la section. Si la section n’existe pas déjà, OneNote la crée à l’emplacement que vous spécifiez.
  
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
|**Description** <br/> |Supprime tout objet de la hiérarchie (groupe de sections, section ou page) de la hiérarchie de bloc-notes OneNote. |
|**Syntaxe** <br/> | `HRESULT DeleteHierarchy(`<br/>`[in]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL deletePermanently);` <br/> |
|**Paramètres** <br/> | *bstrObjectID* &ndash; ID OneNote de l’objet que vous voulez supprimer. L’objet peut être un groupe de sections, une section ou une page.<br/>*dateExpectedLastModified* &ndash; (Facultatif) Date et heure auxquelles vous pensez que l’objet à supprimer a été modifié pour la dernière fois. Si vous transmettez une valeur non nulle pour ce paramètre, OneNote procède à la mise à jour uniquement si cette valeur correspond à la date et à l’heure réelles de la dernière modification de l’objet. La spécification d’une valeur pour ce paramètre permet d’éviter d’écraser accidentellement les modifications apportées par les utilisateurs depuis la dernière modification de l’objet.<br/>*deletePermanently* &ndash; (Facultatif) **true** pour supprimer définitivement le contenu ; **false** afin de déplacer le contenu dans la Corbeille OneNote pour le bloc-notes correspondant (par défaut). Si le bloc-notes est au format OneNote 2007, il n’existe pas de corbeille. Le contenu est donc supprimé définitivement. |

### <a name="createnewpage-method"></a>Méthode CreateNewPage

|||
|:-----|:-----|
|**Description** <br/> |Ajoute une nouvelle page à la section que vous spécifiez. Celle-ci est ajoutée comme la dernière page de la section.  <br/> |
|**Syntaxe** <br/> | `HRESULT CreateNewPage(`<br/>`[in]BSTR bstrSectionID,`<br/>`[out]BSTR * pbstrPageID);`<br/>`[in,defaultvalue(npsDefault)]NewPageStyle npsNewPageStyle);` <br/> |
|**Paramètres** <br/> | *bstrSectionID* &ndash; Chaîne contenant l’ID OneNote de la section dans laquelle créer la page.<br/>*pbstrPageID* &ndash; (Paramètre de sortie) Pointeur vers la chaîne dans laquelle la méthode écrit l’ID OneNote pour la page nouvellement créée.<br/>*npsNewPageStyle* &ndash; Valeur provenant de l’énumération **NewPageStyle** qui spécifie le style de la page à créer. |

L’API OneNote inclut la méthode **CreateNewPage** pour plus de commodité. Vous pouvez obtenir le même résultat, avec un meilleur contrôle sur la façon dont la nouvelle page est positionnée dans la hiérarchie en appelant la méthode **UpdateHierarchy**. La méthode **UpdateHierarchy** vous permet également de créer des sous-pages en même temps que vous créez une page.
  
### <a name="closenotebook-method"></a>Méthode CloseNotebook

|||
|:-----|:-----|
|**Description** <br/> |Ferme le bloc-notes spécifié. |
|**Syntaxe** <br/> | `HRESULT CloseNotebook(`<br/>`[in]BSTR bstrNotebookID,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL force);` <br/> |
|**Paramètres** <br/> | *bstrNotebookID* &ndash; ID OneNote du bloc-notes à fermer.<br/>*force* &ndash; (Facultatif) **true** pour fermer le bloc-notes, même si certaines modifications dans le bloc-notes ne peuvent pas être synchronisées par OneNote avant la fermeture ; sinon, **false** (par défaut). |

Utilisez la méthode **CloseNotebook** pour fermer le bloc-notes de votre choix. Lorsque vous appelez cette méthode, OneNote synchronise les fichiers hors connexion avec le contenu du bloc-notes en cours, si nécessaire, et ferme le bloc-notes spécifié. Après le retour de la méthode, le bloc-notes n’apparaît plus dans la liste des blocs-notes ouverts dans l’interface utilisateur OneNote (IU).
  
### <a name="gethierarchyparent-method"></a>Méthode GetHierarchyParent

|||
|:-----|:-----|
|**Description** <br/> |Obtient l’ID OneNote de l’objet parent d’un objet OneNote. |
|**Syntaxe** <br/> | `HRESULT GetHierarchyParent (`<br/>`[in]BSTR bstrObjectID,`<br/>`[out]BSTR * pbstrParentID);` <br/> |
|**Paramètres** <br/> | *bstrObjectID* &ndash; Chaîne contenant l’ID OneNote de l’objet dont vous voulez trouver l’objet parent.<br/>*pbstrParentID* &ndash; (Paramètre de sortie) Pointeur vers la chaîne dans laquelle la méthode écrit l’ID OneNote de l’objet parent. |

Si l’objet OneNote n’a pas d’objet parent (par exemple, lorsqu’un utilisateur souhaite obtenir le parent d’un bloc-notes), une exception est levée.
  
### <a name="getspeciallocation-method"></a>Méthode GetSpecialLocation

|||
|:-----|:-----|
|**Description** <br/> |Recherche le chemin d’accès à l’emplacement où OneNote stocke certains éléments spéciaux, tels que les sauvegardes, les notes non classées et le bloc-notes par défaut. |
|**Syntaxe** <br/> | `HRESULT GetSpecialLocation(`<br/>`[in]SpecialLocation slToGet,`<br/>`[out]BSTR * pbstrSpecialLocationPath);` <br/> |
|**Paramètres** <br/> | *slToGet* &ndash; L’une des valeurs de l’énumération [SpecialLocation](enumerations-onenote-developer-reference.md#odc_SpecialLocation) qui spécifie l’emplacement de dossier spécial à obtenir.<br/>*pbstrSpecialLocationPath* &ndash; (Paramètre de sortie) Pointeur vers la chaîne dans laquelle OneNote doit écrire le chemin d’accès au dossier spécial. |

Vous pouvez utiliser cette méthode pour déterminer l’emplacement sur le disque du dossier Notes non classées. Il s’agit du dossier dans lequel OneNote stocke les notes créées lorsque vous faites glisser un élément dans OneNote, ainsi que les notes provenant directement d’autres applications (telles que celles qui résultent lorsque vous cliquez sur **Envoyer vers OneNote** dans Microsoft Outlook ou Microsoft Internet Explorer) .
  
## <a name="page-content-methods"></a>Méthodes de contenu de page

<a name="ON14DevRef_Application_PageContent"> </a>

Les méthodes décrites dans cette section vous aident à découvrir, mettre à jour et supprimer le contenu des pages dans les blocs-notes OneNote, ainsi qu’à publier du contenu OneNote.
  
### <a name="getpagecontent-method"></a>Méthode GetPageContent

|||
|:-----|:-----|
|**Description**|Obtient l’ensemble du contenu (au format XML OneNote) de la page spécifiée.|
|**Syntaxe**| `HRESULT GetPageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[out]BSTR * pbstrPageXmlOut,`<br/>`[in,defaultvalue(piBasic)]PageInfo pageInfoToExport,`<br/>`[in,defaultvalue(xsCurrent)]XMLSchema xsSchema);`|
|**Paramètres**| *bstrPageId* &ndash; ID OneNote de la page dont vous voulez obtenir le contenu.<br/><br/>*pbstrPageXmlOut* &ndash; (Paramètre de sortie) Pointeur vers la chaîne dans laquelle vous voulez que OneNote écrive la sortie XML.<br/><br/>*pageInfoToExport* &ndash; (Facultatif) Spécifie si la méthode **GetPageContent** renvoie du contenu binaire, incorporé dans le code XML et encodé en base 64. Le contenu binaire peut inclure, par exemple, des images et des données d’entrée manuscrite. Le paramètre *pageInfoToExport* spécifie également s’il faut baliser la sélection dans le code XML renvoyé par la méthode **GetPageContent**. Il prend une valeur énumérée à partir de l’énumération [PageInfo](enumerations-onenote-developer-reference.md#odc_PageInfo).<br/><br/>*xsSchema* &ndash; (Facultatif) Version du schéma XML OneNote, de type **XMLSchema**, que vous voulez obtenir en sortie. Vous pouvez spécifier la version de schéma XML 2013, 2010, 2007 ou la version actuelle. <br/><br/>**Remarque :** pour que votre complément fonctionne avec les versions ultérieures de OneNote, nous vous recommandons de spécifier une version de OneNote (par exemple, **xs2013**) plutôt que d’utiliser **xsCurrent** ou de laisser le champ vide.           |

Par défaut, pour éviter que la chaîne XML renvoyée soit trop longue, OneNote n’incorpore pas de contenu binaire dans le code XML. Pour la même raison, il ne marque pas la sélection en cours avec les attributs de sélection. Les objets binaires incluent un ID OneNote dans leurs balises. Pour obtenir un objet binaire, appelez la méthode **GetBinaryPageContent** et transmettez-lui l’ID OneNote que vous obtenez à partir de la méthode **GetPageContent**. Utilisez la méthode **GetPageContent** lorsque vous n’avez pas besoin des données binaires immédiatement.
  
### <a name="updatepagecontent-method"></a>Méthode UpdatePageContent

|||
|:-----|:-----|
|**Description**|Met à jour ou modifie le contenu de la page.|
|**Syntaxe**| `HRESULT UpdatePageContent(`<br/>`[in]BSTR bstrPageChangesXmlIn,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(xsCurrent)]XMLSchema xsSchema,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL force);`|
|**Paramètres**| *bstrPageChangesXmlIn* &ndash; Chaîne contenant le code XML OneNote qui inclut les modifications à apporter à la page.<br/><br/>*dateExpectedLastModified* &ndash; (Facultatif) Date et heure auxquelles vous pensez que la page à mettre à jour a été modifiée pour la dernière fois. Si vous transmettez une valeur non nulle pour ce paramètre, OneNote procède à la mise à jour uniquement si cette valeur correspond à la date et à l’heure réelles de la dernière modification de la page. La spécification d’une valeur pour ce paramètre permet d’éviter d’écraser accidentellement les modifications apportées par les utilisateurs depuis la dernière modification de la page.<br/><br/>*xsSchema* &ndash; (Facultatif) Version du schéma XML OneNote, de type **XMLSchema**, que vous voulez obtenir en sortie. Vous pouvez spécifier la version de schéma XML 2013, 2010, 2007 ou la version actuelle. <br/><br/>**Remarque :** pour que votre complément fonctionne avec les versions ultérieures de OneNote, nous vous recommandons de spécifier une version de OneNote (par exemple, **xs2013**) plutôt que d’utiliser **xsCurrent** ou de laisser le champ vide.<br/><br/>*force* (Facultatif) **true** pour mettre à jour le contenu de la page, même si certaines données de la page sont inconnues et proviennent d’une version ultérieure de OneNote ; sinon, **false** (par défaut). |

Vous pouvez utiliser cette méthode pour modifier la page de différentes manières. Par exemple, vous pouvez utiliser la méthode **UpdatePageContent** pour ajouter un plan à une page, modifier le contenu d’un plan, ajouter des images, ajouter de l’encre, déplacer du contenu ou modifier du texte dans des plans.
  
En guise d’exemple plus spécifique, vous pouvez utiliser la méthode **GetPageContent** pour exporter une page existante, apporter des modifications au code XML de la page, puis utiliser la méthode **UpdatePageContent** pour importer la page entière à nouveau. Sinon, utilisez cette méthode pour ajouter de nouveaux objets de page, tels que des images, en bas d’une page existante.
  
Les seuls objets que vous devez inclure dans le code XML que vous transmettez à la méthode **UpdatePageContent** sont les objets de niveau page (par exemple, des plans, des images sur la page ou des entrées manuscrites sur la page) qui ont été modifiés. Cette méthode ne modifie ni ne supprime les objets de niveau page que vous ne spécifiez pas dans le paramètre *bstrPageChangesXmlIn*. La méthode remplace entièrement les objets de niveau de page, tels que les plans, dont les ID correspondent à ceux des objets que vous transmettez. Par conséquent, vous devez spécifier entièrement tous les objets de niveau page dans votre code, y compris leur contenu existant et les modifications que vous souhaitez y apporter.
  
Par exemple, si votre page contient un plan et une image de page d’arrière-plan, vous pouvez remplacer le plan et conserver l’image en spécifiant complètement le plan dans le code XML, en utilisant l’ID du plan existant et en excluant l’image du code. Étant donné que le plan révisé que vous incluez dans le code remplace complètement le plan existant, vous devez inclure l’ensemble du contenu du plan.
  
Par ailleurs, la méthode **UpdatePageContent** modifie uniquement les propriétés d’élément que vous spécifiez dans le paramètre *bstrPageChangesXmlIn*. Par exemple, si vous spécifiez certaines propriétés de l’élément **PageSettings** mais pas toutes, les propriétés que vous ne spécifiez pas restent inchangées.
  
L’exemple suivant montre comment utiliser la méthode **UpdatePageContent** pour modifier le titre d’une page et ajouter un échantillon de texte à la page. Avant d’exécuter le code, remplacez un ID de page valide pour l’ID de page affiché dans le code, afin que le code fonctionne sur votre ordinateur. Vous pouvez obtenir l’ID d’une page en utilisant la méthode **GetHierarchy**, puis en examinant la sortie.
  
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
|**Description** <br/> |Renvoie un objet binaire, comme une entrée manuscrite ou une image, sur une page OneNote sous forme de chaîne encodée en base 64. |
|**Syntaxe** <br/> | `HRESULT GetBinaryPageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[in]BSTR bstrCallbackID,`<br/>`[out]BSTR * pbstrBinaryObjectB64Out);` <br/> |
|**Paramètres** <br/> | *bstrPageID* &ndash; ID OneNote de la page contenant l’objet binaire à obtenir.<br/>*bstrCallBackID* &ndash; ID OneNote de l’objet binaire à obtenir. Cet ID, nommé **callbackID**, se trouve dans le code XML OneNote pour une page renvoyée par la méthode **GetPageContent**.<br/>*pbstrBinaryObectB64Out* &ndash; (Paramètre de sortie) Pointeur vers une chaîne dans laquelle OneNote écrit l’objet binaire sous forme de chaîne encodée en base 64. |

### <a name="deletepagecontent-method"></a>Méthode DeletePageContent

|||
|:-----|:-----|
|**Description** <br/> |Supprime un objet &ndash; comme un objet **Outline**, **Ink** ou **Image** d’une page. |
|**Syntaxe** <br/> | `HRESULT DeletePageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[in]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL force);` <br/> |
|**Paramètres** <br/> | *bstrPageID* &ndash; ID OneNote de la page contenant l’objet à supprimer.<br/>*bstrObjectID* &ndash; ID OneNote de l’objet à supprimer.<br/>*dateExpectedLastModified* &ndash; (Facultatif) Date et heure auxquelles vous pensez que la page dont vous voulez supprimer le contenu a été modifiée pour la dernière fois. Si vous transmettez une valeur non nulle pour ce paramètre, OneNote procède à la suppression uniquement si cette valeur correspond à la date et à l’heure réelles de la dernière modification de la page. La spécification d’une valeur pour ce paramètre permet d’éviter d’écraser accidentellement les modifications apportées par les utilisateurs depuis la dernière modification de la page.<br/>*force* &ndash; (Facultatif) **true** pour mettre à jour le contenu de la page, même si certaines données de la page sont inconnues et proviennent d’une version ultérieure de OneNote ; sinon, **false** (par défaut). |

### <a name="publish-method"></a>Méthode Publish

|||
|:-----|:-----|
|**Description** <br/> |Exporte la page que vous spécifiez dans un fichier sous n’importe quel format pris en charge par OneNote. |
|**Syntaxe** <br/> | `HRESULT Publish(`<br/>`[in]BSTR bstrHierarchyID,`<br/>`[in]BSTR bstrTargetFilePath,`<br/>`[in,defaultvalue(pfOneNote)]PublishFormat pfPublishFormat,`<br/>`[in,defaultvalue(0)]BSTR bstrCLSIDofExporter);` <br/> |
|**Paramètres** <br/> | *bstrHierarchyID* &ndash; ID OneNote de la hiérarchie à exporter.<br/>*bstrTargetFilePath* &ndash; Chemin d’accès absolu à l’emplacement auquel enregistrer le fichier de sortie obtenu. Le fichier que vous spécifiez ne doit pas déjà exister à cet emplacement.<br/>*pfPublishFormat* &ndash; L’une des valeurs de l’énumération [PublishFormat](enumerations-onenote-developer-reference.md#odc_PublishFormat) qui spécifie le format souhaité pour la page publiée (par exemple, MHTML, PDF ou autre).<br/>*bstrCLSIDofExporter* &ndash; ID de classe (CLSID) d’une application COM inscrite qui peut exporter des métafichiers améliorés Microsoft Windows (.emf). L’application COM doit implémenter l’interface **IMsoDocExporter**. Ce paramètre permet aux développeurs tiers d’écrire leur propre code afin de publier du contenu OneNote dans un format personnalisé. Pour plus d’informations sur l’interface **IMsoDocExporter**, consultez la rubrique relative à l’[extension de la fonctionnalité d’exportation au format fixe Office 2007](https://msdn.microsoft.com/library/office/aa338206%28v=office.12%29.aspx). |

Pour l’instant, OneNote prend en charge les formats de fichier suivants :
  
- Fichiers MHTML (.mht)
- Fichiers PDF Adobe Acrobat (.pdf)
- Fichiers XPS (XML Paper Specification, .xps).
- Fichiers OneNote 2013, 2010 ou 2007 (.one)
- Fichiers de package OneNote (.onepkg)
- Documents Microsoft Word (.doc ou .docx)
- Métafichiers améliorés Microsoft Windows (.emf)
- Fichiers HTML (.html)

Cette méthode génère exactement les mêmes résultats que vous obtiendriez en cliquant sur **Publier** dans l’interface utilisateur et en spécifiant le format.
  
## <a name="navigation-methods"></a>Méthodes de navigation

<a name="ON14DevRef_Application_Navigation"> </a>

Les méthodes décrites dans cette section vous aident à rechercher, atteindre et créer un lien vers les blocs-notes OneNote, les groupes de sections, les sections, les pages et les objets de page.
  
### <a name="navigateto-method"></a>Méthode NavigateTo

|||
|:-----|:-----|
|**Description** <br/> |Accède à l’objet spécifié (par exemple, sections, pages et éléments **Outline** au sein des pages). |
|**Syntaxe** <br/> | `HRESULT NavigateTo(`<br/>`[in]BSTR bstrHierarchyObjectID,`<br/>`[in,defaultvalue(#)]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fNewWindow);` <br/> |
|**Paramètres** <br/> | *bstrHierarchyObjectID* &ndash; ID OneNote de l’objet auquel vous voulez accéder dans la hiérarchie OneNote.<br/>*bstrObjectID* &ndash; ID OneNote de l’objet auquel vous voulez accéder sur la page OneNote.<br/>*fNewWindow* &ndash; (Facultatif) **true** pour ouvrir l’objet spécifié dans une nouvelle fenêtre OneNote. La valeur **false** n’ouvre pas de nouvelle fenêtre OneNote si une fenêtre est ouverte. |

### <a name="navigatetourl-method"></a>Méthode NavigateToUrl

|||
|:-----|:-----|
|**Description** <br/> |Si un lien OneNote est transmis (onenote://), cette méthode ouvre la fenêtre OneNote à l’emplacement correspondant dans OneNote. Si le lien est externe à OneNote (par exemple, https:// ou file://), une boîte de dialogue de sécurité s’affiche. Après le renvoi, OneNote essaie d’ouvrir le lien et une erreur **HResult.hrObjectDoesNotExist** est renvoyée. |
|**Syntaxe** <br/> | `HRESULT NavigateTo(`<br/>`[in]BSTR bstrUrl,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fNewWindow);` <br/> |
|**Paramètres** <br/> | *bstrUrl* &ndash; Chaîne qui indique l’emplacement à atteindre. Il peut s’agir d’un lien OneNote ou de toute autre URL, par exemple un emplacement réseau ou un lien web.<br/>*fNewWindow* &ndash; (Facultatif) **true** pour ouvrir l’URL spécifiée dans une nouvelle fenêtre OneNote. La valeur **false** n’ouvre pas de nouvelle fenêtre OneNote si une fenêtre est ouverte. |

### <a name="gethyperlinktoobject-method"></a>Méthode GetHyperLinkToObject

|||
|:-----|:-----|
|**Description** <br/> |Obtient un lien hypertexte OneNote vers le bloc-notes, le groupe de sections, la section, la page ou l’objet de page spécifié. |
|**Syntaxe** <br/> | `HRESULT GetHyperlinkToObject(`<br/>`[in] BSTR bstrHierarchyID,`<br/>`[in] BSTR bstrPageContentObjectID,`<br/>`[out] BSTR * pbstrHyperlinkOut);` <br/> |
|**Paramètres** <br/> | *bstrHierarchyID* &ndash; ID OneNote de l’élément (bloc-notes, groupe de sections, section ou page) pour lequel vous souhaitez obtenir un lien hypertexte.<br/>*bstrPageContentObjectID* &ndash; (Facultatif) ID OneNote de l’objet dans la page pour lequel vous souhaitez obtenir un lien hypertexte. Par exemple, l’objet peut être un plan ou un élément **Outline**. Si vous indiquez une chaîne vide (« »), le lien renvoyé pointe vers le bloc-notes, le groupe de sections, la section ou la page que vous avez spécifié dans le paramètre *bstrHierarchyID*. Si vous transmettez une chaîne non vide pour le paramètre *bstrPageContentObjectID*, le paramètre _ *bstrHierarchyID* doit être une référence à la page qui contient l’objet spécifié.<br/>*pbstrHyperlinkOut* &ndash; (Paramètre de sortie) Pointeur vers une chaîne dans laquelle la méthode **GetHyperlinkToObject** écrit le texte du lien hypertexte de sortie. |

Lorsque vous tentez d’accéder au lien obtenu, OneNote ouvre et affiche l’objet spécifié dans le navigateur.
  
### <a name="getwebhyperlinktoobject-method"></a>Méthode GetWebHyperlinktoObject

|||
|:-----|:-----|
|**Description** <br/> |Renvoie un lien hypertexte vers un objet qui s’ouvre dans le client web de OneNote. |
|**Syntaxe** <br/> | `HRESULT GetWebHyperlinkToObject (`<br/>`[in] BSTR bstrHierarchyID,`<br/>`[in] BSTR bstrPageContentObjectID,`<br/>`[out] BSTR * pbstrHyperlinkOut);` <br/> |
|**Paramètres** <br/> | *bstrHierarchyID* &ndash; ID OneNote de l’élément (bloc-notes, groupe de sections, section ou page) pour lequel vous souhaitez obtenir un lien hypertexte web.<br/>*bstrPageContentObjectID* &ndash; (Facultatif) ID OneNote de l’objet dans la page pour lequel vous souhaitez obtenir un lien hypertexte. Par exemple, l’objet peut être un plan ou un élément **Outline**. Si vous indiquez une chaîne vide (« »), le lien renvoyé pointe vers le bloc-notes, le groupe de sections, la section ou la page que vous avez spécifié dans le paramètre *bstrHierarchyID*. Si vous transmettez une chaîne non vide pour le paramètre *bstrPageContentObjectID*, le paramètre _ *bstrHierarchyID* doit être une référence à la page qui contient l’objet spécifié.<br/>*pbstrHyperlinkOut* &ndash; (Paramètre de sortie) Pointeur vers une chaîne dans laquelle la méthode **GetWebHyperlinkToObject** écrit le texte du lien hypertexte de sortie. Si un lien hypertexte web ne peut pas être créé pour le bloc-notes, une valeur null est renvoyée. |

### <a name="findpages-method"></a>Méthode FindPages

|||
|:-----|:-----|
|**Description**|Renvoie la liste des pages correspondant au terme de requête spécifié.|
|**Syntaxe**| `HRESULT FindPages(`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]BSTR bstrSearchBSTR,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL fIncludeUnindexedPages,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fDisplay,`<br/>`[in,defaultvalue(#)]XMLSchema xsSchema);`|
|**Paramètres**| *bstrStartNodeID* &ndash; Nœud (racine, bloc-notes, groupe de sections ou section) en dessous duquel effectuer la recherche de contenu. Ce paramètre définit l’étendue de la recherche.<br/><br/>*bstrSearchString* &ndash; Chaîne de recherche. Indiquez exactement la même chaîne que vous saisiriez dans la zone de recherche de l’interface utilisateur OneNote. Vous pouvez utiliser des opérateurs de comparaison de bits, tel que **AND** et **OR**, qui doivent apparaître entièrement en majuscules.<br/><br/>*pbstrHierarchyXmlOut* &ndash; (Paramètre de sortie) Pointeur vers une chaîne dans laquelle vous voulez que OneNote écrive la chaîne XML de sortie. La chaîne XML obtenue contient la hiérarchie de bloc-notes, de la racine aux pages qui correspondent à la chaîne de recherche incluses. Par exemple, la méthode **FindPages** ne répertorie pas les sections qui n’ont aucune correspondance de page dans la hiérarchie. Par ailleurs, si une seule page dans une même section correspond à la chaîne, la hiérarchie renvoyée inclut le chemin d’accès à cette section et à cette page, mais à aucune autre partie de la hiérarchie de bloc-notes.<br/><br/>*fIncludeUnindexedPages* &ndash; (Facultatif) **true** pour rechercher des pages qui n’ont pas été indexées par Windows Search ; sinon, **false**.<br/><br/>*fDisplay* &ndash; (Facultatif) **true** pour exécuter la recherche également dans l’interface utilisateur, comme si l’utilisateur l’avait saisie lui-même. **false** pour effectuer la requête sans apporter de modification à l’interface utilisateur (par défaut).<br/><br/>*xsSchema* &ndash; (Facultatif) la version du schéma OneNote de la chaîne *pbstrHierarchyXmlOut*. Cette valeur facultative est utilisée pour spécifier la version du schéma XML OneNote qui contient la chaîne _pbstrHierarchyXmlOut_. Si cette valeur n’est pas spécifiée, OneNote part du principe que la version du schéma XML est *xsCurrent*. <br/><br/>**Remarque :** pour que votre complément fonctionne avec les versions ultérieures de OneNote, nous vous recommandons de spécifier une version de OneNote (par exemple, **xs2013**) plutôt que d’utiliser **xsCurrent** ou de laisser le champ vide.           |

 **FindPages** fonctionne uniquement si vous avez installé la recherche Microsoft 3.0 ou 4.0 sur votre ordinateur. Windows Vista et Windows 7 incluent ce composant. Toutefois, si vous exécutez une version antérieure de Windows, vous devez installer [Windows Search](https://www.microsoft.com/windows/products/winfamily/desktopsearch/getitnow.mspx) pour que la méthode **FindPages** fonctionne.
  
### <a name="findmeta-method"></a>Méthode FindMeta

|||
|:-----|:-----|
|**Description**|Renvoie la liste des objets OneNote qui contiennent des métadonnées correspondant au terme de requête spécifié.|
|**Syntaxe**| `HRESULT FindMeta (`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]BSTR bstrSearchBSTRName,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL fIncludeUnindexedPages,`<br/>`[in,defaultvalue(#)]XMLSchema xsSchema);`|
|**Paramètres**| *bstrStartNodeID* &ndash; Nœud (racine, bloc-notes, groupe de sections ou section) en dessous duquel effectuer la recherche de contenu. Ce paramètre définit l’étendue de la recherche.<br/><br/>*bstrSearchStringName* &ndash; Chaîne de recherche. Indiquez une partie du nom de métadonnées. Si vous transmettez une chaîne vide ou une valeur null, tous les objets contenant des métadonnées correspondent à la requête.<br/><br/>*pbstrHierarchyXmlOut* &ndash; (Paramètre de sortie) Pointeur vers une chaîne dans laquelle vous voulez que OneNote écrive la chaîne XML de sortie. La chaîne XML obtenue contient la hiérarchie de bloc-notes, de la racine aux pages qui correspondent à la chaîne de recherche incluses. Par exemple, la méthode **FindPages** ne répertorie pas les sections qui n’ont aucune correspondance de page dans la hiérarchie. Par ailleurs, si une seule page dans une même section correspond à la chaîne, la hiérarchie renvoyée inclut le chemin d’accès à cette section et à cette page, mais à aucune autre partie de la hiérarchie de bloc-notes.<br/>*fIncludeUnindexedPages* &ndash; (Facultatif) **true** pour rechercher des pages qui n’ont pas été indexées par Windows Search ; sinon, **false**.<br/><br/>*xsSchema* &ndash; (Facultatif) la version du schéma OneNote de la chaîne *pbstrHierarchyXmlOut*. Cette valeur facultative est utilisée pour spécifier la version du schéma XML OneNote qui contient la chaîne _pbstrHierarchyXmlOut_. Si cette valeur n’est pas spécifiée, OneNote part du principe que la version du schéma XML est *xsCurrent*. <br/><br/>**Remarque :** pour que votre complément fonctionne avec les versions ultérieures de OneNote, nous vous recommandons de spécifier une version de OneNote (par exemple, **xs2013**) plutôt que d’utiliser **xsCurrent** ou de laisser le champ vide.           |

**FindMeta** fonctionne uniquement si vous avez installé Microsoft Windows Search 3.0 ou 4.0 sur votre ordinateur. Windows Vista et Windows 7 incluent ce composant. Toutefois, si vous exécutez une version antérieure de Windows, vous devez installer [Windows Search](https://www.microsoft.com/windows/products/winfamily/desktopsearch/getitnow.mspx) pour que la méthode **FindMeta** fonctionne.
  
## <a name="functional-methods"></a>Méthodes fonctionnelles

<a name="ON14DevRef_Application_Functional"> </a>

Les méthodes décrites dans cette section vous aident à effectuer certaines actions ou à définir des paramètres dans l’application OneNote.
  
### <a name="mergefiles-method"></a>Méthode MergeFiles

|||
|:-----|:-----|
|**Description** <br/> |Permet aux utilisateurs de fusionner les modifications pour le même fichier dans un seul fichier. Les fichiers considérés comme identiques doivent avoir le même ID OneNote. |
|**Syntaxe** <br/> | `HRESULT MergeFiles (`<br/>`[in]BSTR bstrBaseFile,`<br/>`[in]BSTR bstrClientFile,`<br/>`[in]BSTR bstrServerFile,`<br/>`[in]BSTR bstrTargetFile);` <br/> |
|**Paramètres** <br/> | *bstrBaseFile* &ndash; Chaîne de chemin d’accès à l’emplacement du fichier .one de l’état initial du fichier.<br/>*bstrClientFile* &ndash; Chaîne de chemin d’accès à l’emplacement du fichier .one de la deuxième série de modifications à fusionner avec le fichier de base une fois que les modifications du fichier serveur ont été fusionnées avec la base.<br/>*bstrServerFile* &ndash; Chaîne de chemin d’accès à l’emplacement du fichier .one de la première série de modifications à fusionner avec le fichier de base.<br/>*bstrTargetFile* &ndash; Chaîne de chemin d’accès à l’emplacement du fichier .one avec les modifications fusionnées. |

La méthode **MergeFiles** a été conçue pour les scénarios mobiles dans lesquels plusieurs versions d’un fichier OneNote peuvent exister.
  
### <a name="mergesections-method"></a>Méthode MergeSections

|||
|:-----|:-----|
|**Description** <br/> |Fusionne le contenu d’une section dans une autre section dans OneNote. |
|**Syntaxe** <br/> | `HRESULT MergeSections (`<br/>`[in]BSTR bstrSectionSourceId,`<br/>`[in]BSTR bstrSectionDestinationId);` <br/> |
|**Paramètres** <br/> | *bstrSectionSourceId* &ndash; ID OneNote de la section à fusionner.<br/>*bstrSectionDestinationId* &ndash; ID OneNote de la section dans laquelle effectuer la fusion. La section source est fusionnée dans cette section de destination. |

Cette méthode effectue la même opération que la fonctionnalité **Fusionner dans une autre section** qui est visible lorsque vous cliquez avec le bouton droit de la souris sur une section.
  
### <a name="quickfiling-method"></a>Méthode QuickFiling

|||
|:-----|:-----|
|**Description** <br/> |Renvoie une instance de la boîte de dialogue [IQuickFilingDialog](quick-filing-dialog-box-interfaces-onenote.md#odc_IQuickFilingDialog), qui peut être utilisée pour sélectionner un emplacement dans l’arborescence de la hiérarchie OneNote. |
|**Syntaxe** <br/> | `HRESULT QuickFiling (`<br/>`);` <br/> |

### <a name="synchierarchy-method"></a>Méthode SyncHierarchy

|||
|:-----|:-----|
|**Description** <br/> |Force OneNote à synchroniser l’objet spécifié avec le fichier source sur le disque. |
|**Syntaxe** <br/> | `HRESULT SyncHierarchy (`<br/>`[in]BSTR bstrHierarchyID);` <br/> |
|**Paramètres** <br/> | *bstrHierarchyID* &ndash; ID OneNote de l’objet à synchroniser. |

### <a name="setfilinglocation-method"></a>Méthode SetFilingLocation

|||
|:-----|:-----|
|**Description** <br/> |Permet aux utilisateurs de spécifier où et comment certains types de contenu doivent être classés dans OneNote. |
|**Syntaxe** <br/> | `HRESULT SetFilingLocation (`<br/>`[in]FilingLocation flToSet,`<br/>`[in]FilingLocationType fltToSet,`<br/>`[in]BSTR bstrFilingSectionID);`           <br/> |
|**Paramètres** <br/> | *flToSet* &ndash; Type d’objet de l’emplacement de classement à définir.<br/>*fltToSet* &ndash; Emplacement où classer le type.<br/>*bstrFilingSectionID* &ndash; ID OneNote de la section ou de la page où définir l’emplacement. Si ce n’est pas applicable, l’utilisateur peut transmettre une valeur null ou une chaîne vide. |

Les types de contenu qui peuvent être classés incluent les éléments Outlook et les notes web d’Internet Explorer qui sont importés dans OneNote via la commande **Envoyer à OneNote** dans chaque application. L’emplacement de classement des éléments imprimés dans OneNote peuvent également être définis avec cette méthode.
  
## <a name="properties"></a>Propriétés

<a name="ON14DevRef_Application_Properties"> </a>

Cette section décrit les propriétés de l’interface d’**application**.
  
|**Propriété**|**Description**|
|:-----|:-----|
|**Fenêtres** <br/> |Permet aux utilisateurs d’accéder aux fenêtres OneNote ouvertes. Cette propriété permet aux utilisateurs d’énumérer l’ensemble des fenêtres OneNote et de modifier certaines propriétés de fenêtre. Pour plus d’informations, reportez-vous à l’article relatif aux [interfaces de fenêtre](window-interfaces-onenote.md). |
|**COMAddIns** <br/> |Renvoie la collection **COMAddIns** pour OneNote. Cette collection contient tous les compléments COM disponibles dans OneNote. La propriété **Count** de la collection **COMAddins** renvoie le nombre de compléments COM disponibles. Pour plus d’informations, reportez-vous à l’article relatif à l’objet [COMAddIns](https://msdn.microsoft.com/library/office/ff865489.aspx). |
|**LanguageSettings** <br/> |Permet d’accéder à certaines API pour modifier les paramètres de langue commune de OneNote. |

## <a name="events"></a>Événements

<a name="ON14DevRef_Application_Events"> </a>

Cette section décrit les événements de l’interface d’application.
  
> [!CAUTION]
> Actuellement, les événements ne peuvent pas être ajoutés dans le code géré.
  
### <a name="onnavigate-event"></a>Événement OnNavigate

|||
|:-----|:-----|
|**Description** <br/> |Permet à l’utilisateur d’affecter une fonction à appeler lorsqu’il s’éloigne de l’emplacement OneNote en cours dans l’interface utilisateur OneNote. |
|**Syntaxe** <br/> | `Event OnNavigate (`<br/>`);` <br/> |

### <a name="onhierarchychange-method"></a>Méthode OnHierarchyChange

|||
|:-----|:-----|
|**Description** <br/> |Permet à l’utilisateur d’affecter une fonction à appeler à tout moment en cas de modifications de hiérarchie OneNote (par exemple, ajout ou suppression de pages, ou déplacement de sections). Les modifications de hiérarchie sont regroupées. De cette façon, si plusieurs modifications se produisent en même temps ou presque, OneNote déclenche l’événement une seule fois. |
|**Syntaxe** <br/> | `Event OnHierarchyChange (`<br/>`BSTR bstrActivePageID);` <br/> |
|**Paramètres** <br/> | *bstrActivePageID* &ndash; Indique l’ID OneNote de la page active. |

## <a name="see-also"></a>Voir aussi

- [Référence du développeur OneNote](onenote-developer-reference.md)
