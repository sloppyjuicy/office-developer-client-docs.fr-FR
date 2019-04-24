---
title: Ajout d'un gestionnaire d'événements à l'aide du modèle objet InfoPath
manager: soliver
ms.date: 01/20/2015
ms.audience: Developer
keywords:
- onafterimport event [infopath 2007],OnAfterChange event [InfoPath 2007],OnBeforeChange event [InfoPath 2007],OnSubmitRequest event [InfoPath 2007],OnVersionUpgrade event [InfoPath 2007],InfoPath 2003-compatible form templates, event handlers,OnLoad event [InfoPath 2007],event handlers [InfoPath 2007], adding using InfoPath 2003 object model,OnValidate event [InfoPath 2007],OnContextChange event [InfoPath 2007],OnSaveRequest event [InfoPath 2007],OnClick event [InfoPath 2007],OnSwitchView event [InfoPath 2007],OnSign event [InfoPath 2007],OnMergeRequest event [InfoPath 2007]
localization_priority: Normal
ms.assetid: 0520df55-2d91-4cc5-be31-82144a2db4f6
description: Les commandes de menu qui permettent d'ajouter des fonctions de gestionnaire d'événements dans un projet de modèle de formulaire compatible avec le modèle objet InfoPath 2003 sont quasiment les mêmes que pour les autres types de modèle de formulaire.
ms.openlocfilehash: 8533b6bc11dccdad9d0f05de35406ad3cf68eacd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303667"
---
# <a name="add-an-event-handler-using-the-infopath-object-model"></a>Ajout d'un gestionnaire d'événements à l'aide du modèle objet InfoPath

Les commandes de menu qui permettent d'ajouter des fonctions de gestionnaire d'événements dans un projet de modèle de formulaire compatible avec le modèle objet InfoPath 2003 sont quasiment les mêmes que pour les autres types de modèle de formulaire. Par exemple, pour ajouter un gestionnaire d'événements **OnLoad** avec le modèle de formulaire dans le Concepteur InfoPath, sélectionnez la commande **Événement Sur chargement (OnLoad)** sous l'onglet **Développeur**. Le code du formulaire est activé automatiquement pour le gestionnaire d'événements **OnLoad** dans l'éditeur de code Visual Studio 2012. 
  
Dans les projets de modèle avec code managé compatibles avec InfoPath 2003, la classe qui contient les fonctions du gestionnaire d'événements et les gestionnaires d'événements eux-mêmes sont identifiés par des attributs spécifiques à InfoPath dans le module de code.

## <a name="adding-event-handlers"></a>Ajout de gestionnaires d'événements

Toutes les procédures suivantes partent du principe que vous avez ouvert un projet de modèle de formulaire dans Microsoft InfoPath avec Visual Studio 2012.
  
### <a name="add-an-event-handler-for-the-onclick-event-of-a-command-button"></a>Ajout d'un gestionnaire d'événements pour l'événement OnClick d'un bouton de commande

1. Dans le volet **Contrôles**, cliquez sur **Bouton** pour ajouter un bouton au formulaire. 
    
2. Sous l'onglet **Propriétés**, cliquez sur **Code personnalisé**.
    
   L'affichage bascule vers le stub du gestionnaire d'événements de l'événement [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) dans l'éditeur de code. 
    
### <a name="add-an-event-handler-for-the-onbeforechange-onvalidate-or-onafterchange-event-of-a-field-or-group"></a>Ajout d'un gestionnaire d'événements pour l'événement OnBeforeChange, OnValidate ou OnAfterChange d'un champ ou d'un groupe

1. Cliquez avec le bouton droit de la souris sur un contrôle d'entrée de données lié au champ ou au groupe, par exemple un contrôle **Zone de texte**. 
    
2. Pointez sur **Programmation**, puis cliquez sur l'une des commande, comme **Événement Sur validation (OnValidate)**.
    
   Le focus bascule vers le stub du gestionnaire d'événements pour l'un des événements suivants dans l'éditeur de code: [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx), [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx)ou [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx). 
    
### <a name="add-an-event-handler-for-the-onload-onswitchview-oncontextchange-or-onsign-event-of-a-form"></a>Ajout d'un gestionnaire d'événements pour l'événement OnLoad, OnSwitchView, OnContextChange ou OnSign d'un formulaire

- Dans le menu **Outils**, pointez sur **Programmation**, puis cliquez sur l'événement de formulaire pour lequel vous souhaitez écrire un gestionnaire d'événements.
    
    Le focus bascule vers le stub du gestionnaire d'événements pour l'un des éléments suivants dans l'éditeur de code: [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx), [OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx), [OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx)ou [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx). 
    
### <a name="add-an-event-handler-for-the-onsubmitrequest-event-of-a-form"></a>Ajout d'un gestionnaire d'événements pour l'événement OnSubmitRequest d'un formulaire

1. Sous l'onglet **Données**, cliquez sur **Options d'envoi**.
    
2. Activez la case à cocher **Autoriser les utilisateurs à envoyer ce formulaire**, puis cliquez sur **Effectuer une action personnalisée à l'aide du code**.
    
3. Cliquez sur **Modifier le code**, puis sur **OK**.
    
   L'affichage bascule vers le stub du gestionnaire d'événements de l'événement [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) dans l'éditeur de code. 
    
### <a name="add-an-event-handler-for-the-onsaverequest-event-of-a-form"></a>Ajout d'un gestionnaire d'événements pour l'événement OnSaveRequest d'un formulaire

1. Cliquez sur l'onglet **Fichier**, puis cliquez sur **Options de formulaire**.
    
2. Dans la catégorie **Enregistrer**, cliquez sur **Enregistrer au moyen d'un code personnalisé**, sur **Modifier**, puis sur **OK**.
    
   L'affichage bascule vers le stub du gestionnaire d'événements de l'événement [OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) dans l'éditeur de code. 
    
### <a name="add-an-event-handler-for-the-onversionupgrade-event-of-a-form"></a>Ajout d'un gestionnaire d'événements pour l'événement OnVersionUpgrade d'un formulaire

1. Cliquez sur l'onglet **Fichiers**, cliquez sur **Options de formulaire**.
    
2. Dans la catégorie **Contrôle de version**, sélectionnez **Utiliser un événement personnalisé** dans la liste **Mettre à jour les formulaires existants**, cliquez sur **Modifier**, puis sur **OK**.
    
    L'affichage bascule vers le stub du gestionnaire d'événements de l'événement [OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) dans l'éditeur de code. 
    
### <a name="add-an-event-handler-for-the-onmergerequest-event-of-a-form"></a>Ajout d'un gestionnaire d'événements pour l'événement OnMergeRequest d'un formulaire

1. Cliquez sur l'onglet **Fichiers**, puis cliquez sur **Options de formulaire**.
    
2. Dans la catégorie **Avancé**, activez les cases à cocher **Activer la fusion de formulaires** et **Fusionner à l'aide d'un code personnalisé**, cliquez sur **Modifier**, puis cliquez sur **OK**.
    
    L'affichage bascule vers le stub du gestionnaire d'événements de l'événement [OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) dans l'éditeur de code. 
    
## <a name="adding-an-event-handler-for-the-onafterimport-event"></a>Ajout d'un gestionnaire d'événements pour l'événement OnAfterImport

Pour ajouter des gestionnaires d'événements pour l'événement [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) , vous devez ouvrir le code de formulaire de votre modèle de formulaire avec code managé et ajouter manuellement la fonction de gestionnaire d'événements. Pour plus d'informations sur la création d'un gestionnaire d'événements pour cet événement, cliquez sur le lien correspondant à l'événement **OnAfterImport**. 
  
## <a name="adding-an-event-handler-for-a-secondary-data-source"></a>Ajout d'un gestionnaire d'événements pour une source de données secondaire

L'exemple qui suit illustre l'ajout d'un gestionnaire d'événements pour une source de données secondaire. Cet exemple part du principe qu'il existe une source de données secondaire basée sur un fichier de ressource, books.xml, qui présente le schéma suivant :
  
```xml
<?xml version="1.0"?>
<xsd:schema xmlns:xsd="https://www.w3.org/2001/XMLSchema">
    <xsd:element name="catalog">
        <xsd:complexType>
            <xsd:sequence>
                <xsd:element ref="book" minOccurs="0" maxOccurs="unbounded"></xsd:element>
            </xsd:sequence>
        </xsd:complexType>
    </xsd:element>
    <xsd:element name="genre" type="xsd:string"></xsd:element>
    <xsd:element name="author" type="xsd:string"></xsd:element>
    <xsd:element name="book">
        <xsd:complexType>
            <xsd:all>
                <xsd:element ref="author" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="title" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="genre" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="price" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="publish_date" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="description" minOccurs="0" maxOccurs="1"></xsd:element>
            </xsd:all>
            <xsd:attribute ref="id"></xsd:attribute>
        </xsd:complexType>
    </xsd:element>
    <xsd:element name="price" type="xsd:string"></xsd:element>
    <xsd:element name="title" type="xsd:string"></xsd:element>
    <xsd:element name="publish_date" type="xsd:string"></xsd:element>
    <xsd:element name="description" type="xsd:string"></xsd:element>
    <xsd:attribute name="id" type="xsd:string"></xsd:attribute>
</xsd:schema>

```

<br/>

La vue du formulaire est générée à partir de cette source de données. Le code du formulaire crée une table de hachage basée sur les auteurs et le nombre de livres qu'ils ont écrits. Vous pouvez mettre à jour une entrée depuis la table présentée dans la vue, et le gestionnaire d'événements **OnAfterChange** met alors à jour la table de hachage. Notez que la propriété [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.DataObject.aspx) de l'attribut **InfoPathEventHandler** (implémenté par la classe [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) est utilisée pour faire référence à la source de données secondaire. 
  
```cs
namespace AuxDom
{
    // InfoPathNamespace attribute goes here.
    public class AuxDom
    {
        private XDocument thisXDocument;
        private Application thisApplication;
        private Hashtable authors;
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            authors = new Hashtable();
        }
        public void _Shutdown()
        {
            authors.Clear();
        }
        // The following function handler is created by Microsoft
        // Office InfoPath. Do not modify the type or number of
        // arguments. 
        [InfoPathEventHandler(EventType=InfoPathEventType.OnLoad)]
        public void OnLoad(DocReturnEvent e)
        {
            IXMLDOMDocument books = thisXDocument.GetDOM("books");
            DOMNodeList externalAuthors = books.selectNodes("/catalog/book/author");
            foreach (IXMLDOMNode authorNode in externalAuthors)
            {
                AddBookFromAuthor(authorNode.text);
            }
        }
        // The following function handler is created by Microsoft
        // Office InfoPath. Do not modify the type or number of
        // arguments. 
        [InfoPathEventHandler(MatchPath="/catalog/book/author", EventType=InfoPathEventType.OnAfterChange, DataObject="books")]
        public void books__author_OnAfterChange(DataDOMEvent e)
        {
            if (e.IsUndoRedo)
            {
                // An undo or redo operation has occurred and the DOM 
                // is read-only.
                return;
            }
            
            if (e.Source.text != e.NewValue.ToString())
            {
                RemoveBookFromAuthor(e.OldValue.ToString());
                AddBookFromAuthor(e.NewValue.ToString());
            }
        }
        private void AddBookFromAuthor(string authorName)
        {
            if (authors.Contains(authorName))
            {
                authors[authorName] = (int)authors[authorName] + 1;
            }
            else
            {
                authors.Add(authorName, 1);
            }
        }
        private void RemoveBookFromAuthor(string authorName)
        {
            if (authors.Contains(authorName))
            {
                authors[authorName] = (int)authors[authorName] - 1;
            }
            if ((int)authors[authorName] == 0)
            {
                authors.Remove(authorName);
            }
        }
        // The following function handler is created by Microsoft
        // Office InfoPath. Do not modify the type or number of
        // arguments. 
        [InfoPathEventHandler(MatchPath="ShowAuthors", EventType=InfoPathEventType.OnClick)]
        public void ShowAuthors_OnClick(DocActionEvent e)
        {
            // Write your code here.
            StringBuilder report = new StringBuilder();
            foreach (string authorName in authors.Keys)
            {
                report.Append(authorName + ",\t\t\t");
                report.Append(authors[authorName] + "\n");
            }
            thisXDocument.UI.Alert(report.ToString());
        }
    }
}

```

## <a name="how-the-class-that-contains-event-handlers-is-identified"></a>Identification de la classe qui contient les gestionnaires d'événements

Lorsque vous créez un nouveau projet de modèle de formulaire InfoPath compatible avec le modèle objet avec code managé InfoPath 2003, un attribut **System.ComponentModel.Description** de niveau assembly est appliqué à la classe au début du module du code du formulaire pour identifier la classe contenant tous les gestionnaires d'événements du modèle de formulaire. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Ne modifiez pas l'attribut **System.ComponentModel.Description** de cette classe. Si vous le modifiez, votre modèle de formulaire ne sera plus en mesure d'identifier l'emplacement des gestionnaires d'événements et ceux-ci ne pourront pas fonctionner. 
  
```cs
using System;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
// Office integration attribute. Identifies the startup class for the // form. Do not modify.
[assembly: System.ComponentModel.DescriptionAttribute(    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")]
```

```vb
Imports System
Imports Microsoft.Office.Interop.InfoPath.SemiTrust
' Office integration attribute. Identifies the startup class for the form. Do not modify.
<Assembly: System.ComponentModel.DescriptionAttribute( _    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")>
```

## <a name="how-event-handlers-are-identified"></a>Identification des gestionnaires d'événements

Lorsque vous ajoutez un nouveau gestionnaire d'événements à l'aide des commandes ou boutons de menu de l'interface utilisateur du mode Création d'InfoPath, le stub de la fonction du gestionnaire d'événements est écrit dans le formulaire. L'exemple qui suit présente le stub du gestionnaire d'événements créé pour un événement [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) ajouté à un champ appelé « total ». 
  
```cs
[InfoPathEventHandler(MatchPath="/invoice/total", EventType=InfoPathEventType.OnValidate)]
public void total_OnValidate(DataDOMEvent e)
{
    // Write your code here.
}

```

```vb
<InfoPathEventHandler(MatchPath:="/invoice/total",EventType:= OnValidate)> Public Sub total_OnValidate(ByVal e As EventArgs)
    ' Write your code here.
End Sub

```

Vous pouvez ensuite ajouter du code pour appeler les membres du modèle objet InfoPath à l'aide des membres cachés privés des variables  `thisXDocument` ou  `thisApplication`, ou à l'aide des membres accessibles via l'objet  `e` **EventArgs** reçu par le gestionnaire d'événements : 
  
```cs
thisXDocument.UI.Alert.(e.Site.text);

```

```vb
thisXDocument.UI.Alert.(e.Site.text)

```

L'attribut **InfoPathEventHandler** (tel que défini par la classe [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) est l'attribut personnalisé pour les fonctions qui seront utilisées comme gestionnaires d'événements. 
  
Lorsqu'il est requis par l'événement, le paramètre **MatchPath** (tel que défini par la propriété [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) de la classe **InfoPathEventHandlerAttribute**) spécifie une expression XPath qui identifie la source de l'événement. Le paramètre **EventType** (tel que défini par la propriété [EventType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.EventType.aspx) de la classe **InfoPathEventHandlerAttribute**) spécifie le type de l'événement. Ne modifiez pas la valeur de ces paramètres. Si leur valeur est modifiée, le gestionnaire d'événements peut ne pas être correctement compilé ou la notification d'événement peut ne pas se produire comme prévu. 
  
## <a name="obfuscating-code-in-event-handlers"></a>Masquage du code dans les gestionnaires d'événements

Si vous lancez un utilitaire d'obscurcissement sur l'assembly généré lors de la compilation d'un modèle de formulaire avec code managé ( *nomprojet*  .dll), InfoPath ne peut pas charger l'assembly lorsque l'utilisateur ouvre le formulaire. Si vous voulez obscurcir le code des gestionnaires d'événements ou tout autre code de formulaire, vous devez le placer dans une assembly distincte, puis référencer cette assembly dans votre projet et appeler les membres de l'assembly référencée depuis FormCode.cs ou FormCode.vb. Il est important de lancer l'utilitaire d'obscurcissement uniquement sur l'assembly référencée. 
  
## <a name="see-also"></a>Voir aussi

- [Répondre aux événements de formulaire à l'aide du modèle objet InfoPath 2003](how-to-respond-to-form-events-using-the-infopath-2003-object-model.md)

