---
title: Données de formulaire Access
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- form data [infopath 2007],forms [InfoPath 2007], accessing properties,form templates [InfoPath 2007], accessing properties,opening forms [InfoPath 2007],printing forms [InfoPath 2007],forms [InfoPath 2007], printing,closing forms [InfoPath 2007],InfoPath 2007, accessing form data,forms [InfoPath 2007], accessing data source,forms [InfoPath 2007], closing,forms [InfoPath 2007], opening,printing [InfoPath 2007], forms,forms [InfoPath 2007], creating
localization_priority: Normal
ms.assetid: fd7374d3-a268-4e30-9872-7579cd681bd0
description: Pour utiliser les fonctionnalités avancées d'un formulaire InfoPath, il est souvent nécessaire d'accéder par programme aux informations sur le document XML sous-jacent du formulaire et aux données qu'il contient, ou d'exécuter certaines actions sur le document XML. Le modèle objet InfoPath prend en charge l'accès et la manipulation d'un document XML sous-jacent d'un formulaire par le biais de l'utilisation de la classe XmlForm en association avec la classe XmlFormCollection .
ms.openlocfilehash: c8251afcd75391f102215811694515c06b9f3e7e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386830"
---
# <a name="access-form-data"></a>Données de formulaire Access

Pour utiliser les fonctionnalités avancées d'un formulaire InfoPath, il est souvent nécessaire d'accéder par programme aux informations sur le document XML sous-jacent du formulaire et aux données qu'il contient, ou d'exécuter certaines actions sur le document XML. Le modèle objet InfoPath prend en charge l'accès et la manipulation d'un document XML sous-jacent d'un formulaire par le biais de l'utilisation de la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) en association avec la classe [XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) . 
  
La classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) est l'une des plus utiles dans le modèle objet InfoPath, car elle fournit un ensemble de propriétés et de méthodes qui non seulement interagissent avec le document XML sous-jacent d'un formulaire, mais exécutent également un grand nombre d'actions disponibles dans l'interface utilisateur d'InfoPath. 
  
## <a name="overview-of-the-xmlformcollection-class"></a>Vue d'ensemble de la classe XmlFormCollection

La classe [XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) fournit les méthodes et les propriétés suivantes que les développeurs de formulaires peuvent utiliser pour gérer les objets [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) que la collection contient. 
  
|**Nom**|**Description**|
|:-----|:-----|
|Méthode [New(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx)  <br/> |Crée un nouveau formulaire basé sur le formulaire spécifié.  <br/> |
|Méthode [New (String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) (surcharge 1)  <br/> |Crée un nouveau formulaire basé sur le formulaire spécifié en utilisant le comportement du mode d'ouverture indiqué.  <br/> |
|Méthode [NewFromFormTemplate(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx)  <br/> |Crée un nouveau formulaire basé sur le modèle de formulaire spécifié.  <br/> |
|Méthode [NewFromFormTemplate (String, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (surcharge 1)  <br/> |Crée un formulaire basé sur le modèle de formulaire spécifié et sur les données XML.  <br/> |
|Méthode [NewFromFormTemplate (String, String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (surcharge 2)  <br/> |Crée un nouveau formulaire basé sur le modèle de formulaire spécifié avec des données spécifiées par un objet [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) .  <br/> |
|Méthode [NewFromFormTemplate (String, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (surcharge 3)  <br/> |Crée un formulaire basé sur le modèle de formulaire spécifié avec des données spécifiées par un objet **XPathNavigator** en utilisant le comportement du mode d'ouverture indiqué.  <br/> |
|Méthode [Open(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx)  <br/> |Ouvre le formulaire spécifié.  <br/> |
|Méthode [Open (String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) (surcharge 1)  <br/> |Ouvre le formulaire spécifié à l'aide du mode d'ouverture spécifié.  <br/> |
|Propriété [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Count.aspx)  <br/> |Récupère le nombre d'objets **XmlForm** contenus dans la collection.  <br/> |
|Propriété [Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Item.aspx)  <br/> |Obtient une référence à l'objet **XmlForm** spécifié dans la collection par la valeur de l'index.  <br/> |
   
## <a name="overview-of-the-xmlform-class"></a>Présentation de la classe XmlForm

La classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) fournit les méthodes et les propriétés suivantes que les développeurs de formulaires peuvent utiliser pour interagir avec le document XML sous-jacent d'un formulaire et exécuter des actions sur celui-ci. 
  
|**Nom**|**Description**|
|:-----|:-----|
|Méthode [Close](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Close.aspx)  <br/> |Ferme le formulaire.  <br/> |
|[GetWorkflowTasks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTasks.aspx) , méthode  <br/> |Obtient une référence à une collection **Microsoft.Office.Core.WorkflowTasks** pour le formulaire actif.  <br/> |
|Méthode [GetWorkflowTemplates](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTemplates.aspx)  <br/> |Obtient une référence à une collection **Microsoft.Office.Core.WorkflowTemplates** pour le formulaire actif.  <br/> |
|Méthode [MergeForm(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx)  <br/> |Fusionne le formulaire actif avec le formulaire spécifié par un chemin d'accès ou une URL.  <br/> |
|Méthode [MergeForm(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) (surcharge 1)  <br/> |Fusionne le formulaire actif avec le formulaire cible spécifié dans le nœud renvoyé par l'objet **XPathNavigator** passé à la méthode.  <br/> |
|Méthode [NotifyHost](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NotifyHost.aspx)  <br/> |Fournit une valeur personnalisée à l'application hôte ou à la page ASPX.  <br/> |
|Méthode [Print()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx)  <br/> |Imprime le contenu d'un formulaire tel qu'il s'affiche dans la vue active du formulaire.  <br/> |
|Méthode [Print(Boolean)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) (surcharge 1)  <br/> |Imprime le contenu du formulaire tel qu'il est rendu dans la vue active du formulaire en affichant la boîte de dialogue **Imprimer**.  <br/> |
|Méthode [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx)  <br/> |Enregistre le formulaire dans l'URL (Uniform Resource Locator) qui lui est actuellement associée.  <br/> |
|Méthode [SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx)  <br/> |Enregistre le formulaire dans l'URL (Uniform Resource Locator) spécifiée.  <br/> |
|Méthode [SetSaveAsDialogFilename](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogFilename.aspx)  <br/> |Définit le nom de fichier par défaut dans la boîte de dialogue **Enregistrer sous**.  <br/> |
|Méthode [SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogLocation.aspx)  <br/> |Définit le chemin d'accès par défaut pour enregistrer le formulaire dans la boîte de dialogue **Enregistrer sous**.  <br/> |
|Méthode [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx)  <br/> |Envoie le formulaire à l'aide de l'opération d'envoi définie dans le modèle de formulaire.  <br/> |
|Propriété [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx)  <br/> |Obtient un objet [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) qui représente la vue active du formulaire.  <br/> |
|Propriété [DataConnections](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx)  <br/> |Obtient un objet [DataConnectionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) associé au formulaire.  <br/> |
|[DataSources,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) propriété  <br/> |Obtient l’objet [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) associé au formulaire.  <br/> |
|Propriété [Dirty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Dirty.aspx)  <br/> |Obtient une valeur qui indique si les données d'un formulaire ont été modifiées depuis leur dernier enregistrement.  <br/> |
|Propriété [Errors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx)  <br/> |Obtient une référence à la [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) associé à un formulaire.  <br/> |
|[Extension](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Extension.aspx) , propriété  <br/> |Obtient un [objet System.Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx) pour accéder aux fonctions et variables globales contenues dans le fichier de code de formulaire principal d’un formulaire à l’aide de [System.Reflection](https://msdn.microsoft.com/library/system.reflection(v=vs.110).aspx).  <br/> |
|Propriété [FormState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.FormState.aspx)  <br/> |Obtient une référence à un conteneur de propriétés de type [System.Collections.IDictionary](https://msdn.microsoft.com/library/system.collections.idictionary%28v=vs.110%29.aspx) que les formulaires avec navigation activée peuvent utiliser pour conserver les informations d’état entre les sessions sur le serveur.  <br/> |
|Propriété [Host](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Host.aspx)  <br/> |Obtient un objet [System.Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx) que du code s'exécutant dans une instance hébergée d'InfoPath peut utiliser pour accéder au modèle objet de l'application hôte.  <br/> |
|Propriété [hébergé](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Hosted.aspx)  <br/> |Indique si InfoPath est hébergé sous forme de contrôle dans une autre application.  <br/> |
|[HostName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.HostName.aspx) , propriété  <br/> |Obtient le nom de l'application qui héberge InfoPath sous forme de contrôle.   <br/> |
|Propriété [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx)  <br/> |Obtient un objet [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) qui représente la source de données principale du formulaire.  <br/> |
|[NamespaceManager,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) propriété  <br/> |Obtient une référence à un objet [XmlNamespaceManager](https://msdn.microsoft.com/library/System.Xml.XmlNamespaceManager.aspx) qui peut servir à résoudre, d’ajouter ou supprimer des espaces de noms utilisés dans le formulaire.  <br/> |
|Propriété [New](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.New.aspx)  <br/> |Obtient une valeur qui indique s'il s'agit d'un nouveau formulaire.  <br/> |
|Propriété [permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx)  <br/> |Obtient une référence à un objet [d’autorisation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) associé au formulaire.  <br/> |
|Propriété [QueryDataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.QueryDataConnection.aspx)  <br/> |Obtient une référence à l’objet [DataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.aspx) qui représente la connexion de données qui est associée au formulaire.  <br/> |
|Propriété [en lecture seule](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ReadOnly.aspx)  <br/> |Obtient une valeur qui indique si un modèle de formulaire est en lecture seule ou verrouillé.  <br/> |
|Propriété [récupéré](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Recovered.aspx)  <br/> |Obtient une valeur qui indique si un formulaire a été enregistré pour la dernière fois par une opération de récupération automatique.  <br/> |
|Propriété [signed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx)  <br/> |Obtient une valeur qui indique si un formulaire a été signé numériquement à l'aide de signatures numériques.  <br/> |
|[SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) , propriété  <br/> |Obtient une référence à la collection [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) qui est associée à un formulaire.  <br/> |
|[TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.TaskPanes.aspx) , propriété  <br/> |Obtient une référence à la [collection TaskPaneCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) associée à un modèle de formulaire.  <br/> |
|Propriété [Template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx)  <br/> |Obtient une référence à l’objet [FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) qui représente le manifeste (.xsf) du modèle de formulaire associé au formulaire.  <br/> |
|Propriété [Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Uri.aspx)  <br/> |Obtient l'URI (Uniform Resource Identifier) d'un formulaire.  <br/> |
|Propriété [UserRole](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.UserRole.aspx)  <br/> |Obtient ou définit l'utilisateur actuel du nom de rôle du formulaire.  <br/> |
|Propriété [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx)  <br/> |Obtient une référence à l’objet [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) associé au modèle de formulaire.  <br/> |
|Propriété [XmlLang](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.XmlLang.aspx)  <br/> |Obtient la valeur de l'attribut **xml:lang** dans le document XML sous-jacent du formulaire.  <br/> |
   
## <a name="using-the-xmlformcollection-class"></a>Utilisation de la classe XmlFormCollection

La classe **XmlFormCollection** est accessible via la propriété [XmlForms](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.XmlForms.aspx) de la classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) . Dans un modèle de formulaire contenant du code managé, créé à l'aide de l'objet de modèle fourni par les membres de l'espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , vous pouvez utiliser le mot clé **this** (C#) ou **Me** (Visual Basic) dans le code du formulaire pour accéder à la classe **Application** et à ses membres. 
  
L'exemple suivant utilise la propriété **XmlForms** de la classe **Application** pour créer une variable objet appelée myForms qui fait référence à l'objet **XDocumentsCollection** de l'instance InfoPath actuellement exécutée. Cette variable est ensuite utilisée pour afficher le nombre total de formulaires ouverts. 
  
```cs
// Create variable for accessing the XmlFormCollection.
XmlFormCollection myForms = this.Application.XmlForms;
// Display the number of forms that are currently open.
MessageBox.Show("Forms open: " + myForms.Count);
```

```vb
// Create variable for accessing the XmlFormCollection.
Dim myForms As XmlFormCollection = Me.Application.XmlForms
' Display the number of forms that are currently open.
MessageBox.Show("Forms open: " + myForms.Count)
```

La variable myForms peut ensuite être utilisée pour créer de nouveaux formulaires (à l'aide de la méthode **New** ou **NewFromTemplate**) ou ouvrir des formulaires existants (à l'aide de l'une des méthodes **Open**). 
  
## <a name="using-the-xmlform-class"></a>Utilisation de la classe XmlForm

Dans un modèle de formulaire avec code managé, créé à l'aide du modèle objet fourni par les membres de l'espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , vous pouvez utiliser le mot clé **this** (C#) ou **Me** (Visual Basic) dans le code du formulaire pour accéder aux membres de la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) directement (sans nécessiter une variable d'objet pour faire référence à la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) ). 
  
### <a name="accessing-a-forms-property-values"></a>Accès aux valeurs des propriétés d'un formulaire

L'exemple suivant utilise le mot clé **this** ou **Me** pour accéder aux propriétés **New**, **ReadOnly**, **Signed** et **Uri** de la classe **XmlForm** et afficher les valeurs retournées pour le formulaire actuel dans une zone de message. 
  
```cs
MessageBox.Show(
   "Is new: " + this.New + System.Environment.NewLine +
   "Is read-only: " + this.ReadOnly + System.Environment.NewLine +
   "Is signed: " + this.Signed + System.Environment.NewLine +
   "Form URI: " + this.Uri);
```

```vb
MessageBox.Show( _
   "Is new: " &amp; Me.New &amp; System.Environment.NewLine &amp; _
   "Is read-only: " &amp; Me.ReadOnly &amp; System.Environment.NewLine + _
   "Is signed: " &amp; Me.Signed &amp; System.Environment.NewLine &amp; _
   "Form URI: " &amp; this.Uri)
```

### <a name="accessing-a-forms-data-source"></a>Accès à la source de données d'un formulaire

Une propriété essentielle de la classe **XmlForm** relative aux données du formulaire est la propriété **MainDataSource**. Elle retourne une référence à un objet [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) qui représente les données XML sous-jacentes du formulaire actuel qui sont également référencées en tant que source de données principale ou primaire du formulaire. La classe **DataSource** fournit la méthode [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) qui crée un objet [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) situé à la racine du document XML sous-jacent du formulaire. Les propriétés et les méthodes de la classe **XPathNavigator** peuvent ensuite être utilisées pour parcourir et modifier les données XML sous-jacentes du formulaire. 
  
L'exemple suivant utilise la propriété **MainDataSource** de la classe **XmlForm** pour créer un objet **XPathNavigator** situé à la racine de la source de données principale du formulaire. La propriété **OuterXml** de la classe **XPathNavigator** est ensuite utilisée pour retourner et afficher tout le contenu du document XML sous-jacent d'un formulaire. 
  
```cs
// Get outer XML of the underlying XML document.
string myDoc = this.MainDataSource.CreateNavigator.OuterXml.ToString();
// Display XML.
MessageBox.Show(myDoc);
```

```vb
' Get outer XML of the underlying XML document.
Dim myDoc As String myDoc = _
   Me.MainDataSource.CreateNavigator.OuterXml.ToString()
' Display XML.
MessageBox.Show(myDoc)
```

> [!NOTE]
> [!REMARQUE] Étant donné qu'InfoPath considère la propriété **MainDataSource** comme une propriété par défaut de l'objet **XmlForm** accédé à l'aide du mot clé **this** ou **Me**, vous pouvez le supprimer de la ligne de code utilisée pour créer l'objet **XPathNavigator**. 
  
Pour en savoir plus sur la classe **XPathNavigator** dans la logique métier d’un modèle formulaire InfoPath, voir [utiliser les Classes XPathNavigator et XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
### <a name="accessing-data-about-a-forms-form-template-file"></a>Accès aux données relatives à un fichier de modèle de formulaire

Les informations sur le modèle de formulaire associé à un formulaire, y compris le fichier de définition du formulaire (.xsf ) et les données XML sources qu'il contient sont également accessibles à l'aide de la classe **XmlForm**. Ces informations sont accessibles à l'aide de la propriété [Template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx) qui retourne une référence à un objet [FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) qui représente le modèle de formulaire associé au formulaire actuel. 
  
Dans l'exemple suivant, la première zone de message affiche certaines des données disponibles dans la classe **Template**, notamment l'emplacement de l'URI (Uniform Resource Identifier) (à l'aide de la propriété [Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Uri.aspx) ), l'identificateur de cache (à l'aide de la propriété [CacheId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.CacheId.aspx) ) et le numéro de version (à l'aide de la propriété [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Version.aspx) ). La zone de message suivante utilise la propriété [Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) de la classe **Template** pour créer un objet **XPathNavigator** utilisé pour afficher le code XML source du fichier de définition du formulaire (.xsf). 
  
```cs
// Display form template properties.
MessageBox.Show(
   "Cache ID: " + this.Template.CacheId + System.Environment.NewLine +
   "URI: " + this.ReadOnly + System.Environment.NewLine +
   "Version: " + this.Signed, "Form Template Properties");
// Display form definition file XML.
MessageBox.Show(this.Template.Manifest.OuterXml, 
   "Form Definition File XML");
```

```vb
' Display form template properties.
MessageBox.Show( _
   "Cache ID: " &amp; Me.Template.CacheId &amp; System.Environment.NewLine &amp;
   "URI: " &amp; Me.ReadOnly &amp; System.Environment.NewLine &amp;
   "Version: " &amp; Me.Signed, "Form Template Properties")
' Display form definition file XML.
MessageBox.Show(Me.Template.Manifest.OuterXml, _
   "Form Definition File XML")
```


