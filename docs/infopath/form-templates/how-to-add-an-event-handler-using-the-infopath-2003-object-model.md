---
title: Ajouter un handler d’événements à l’aide du modèle objet InfoPath
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
# <a name="add-an-event-handler-using-the-infopath-object-model"></a><span data-ttu-id="e8bce-104">Ajouter un handler d’événements à l’aide du modèle objet InfoPath</span><span class="sxs-lookup"><span data-stu-id="e8bce-104">Add an event handler using the InfoPath object model</span></span>

<span data-ttu-id="e8bce-p101">Les commandes de menu qui permettent d'ajouter des fonctions de gestionnaire d'événements dans un projet de modèle de formulaire compatible avec le modèle objet InfoPath 2003 sont quasiment les mêmes que pour les autres types de modèle de formulaire. Par exemple, pour ajouter un gestionnaire d'événements **OnLoad** avec le modèle de formulaire dans le Concepteur InfoPath, sélectionnez la commande **Événement Sur chargement (OnLoad)** sous l'onglet **Développeur**. Le code du formulaire est activé automatiquement pour le gestionnaire d'événements **OnLoad** dans l'éditeur de code Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="e8bce-p101">The menu commands for adding event handler functions in a form template project that is compatible with the InfoPath 2003 object model are essentially the same as those for other types of form templates. For example, in order to add an **OnLoad** event handler, with the form template open in the InfoPath designer, click the **On Load Event** command on the **Developer** tab. The focus automatically switches to the form code for the **OnLoad** event handler in the Visual Studio 2012 code editor.</span></span> 
  
<span data-ttu-id="e8bce-107">Dans les projets de modèle avec code managé compatibles avec InfoPath 2003, la classe qui contient les fonctions du gestionnaire d'événements et les gestionnaires d'événements eux-mêmes sont identifiés par des attributs spécifiques à InfoPath dans le module de code.</span><span class="sxs-lookup"><span data-stu-id="e8bce-107">In managed-code form template projects compatible with InfoPath 2003, the class that contains event handler functions and the event handlers themselves are identified by attributes specific to InfoPath in the code module.</span></span>

## <a name="adding-event-handlers"></a><span data-ttu-id="e8bce-108">Ajout de handlers d’événements</span><span class="sxs-lookup"><span data-stu-id="e8bce-108">Adding event handlers</span></span>

<span data-ttu-id="e8bce-109">Toutes les procédures suivantes partent du principe que vous avez ouvert un projet de modèle de formulaire dans Microsoft InfoPath avec Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="e8bce-109">All of the following procedures assume that you have a form template project open in Microsoft InfoPath with Visual Studio 2012.</span></span>
  
### <a name="add-an-event-handler-for-the-onclick-event-of-a-command-button"></a><span data-ttu-id="e8bce-110">Ajout d'un gestionnaire d'événements pour l'événement OnClick d'un bouton de commande</span><span class="sxs-lookup"><span data-stu-id="e8bce-110">Add an event handler for the OnClick event of a command button</span></span>

1. <span data-ttu-id="e8bce-111">Dans le volet **Contrôles**, cliquez sur **Bouton** pour ajouter un bouton au formulaire.</span><span class="sxs-lookup"><span data-stu-id="e8bce-111">In the **Controls** pane, click **Button** to add a button to the form.</span></span> 
    
2. <span data-ttu-id="e8bce-112">Sous l'onglet **Propriétés**, cliquez sur **Code personnalisé**.</span><span class="sxs-lookup"><span data-stu-id="e8bce-112">On the **Properties** tab, click **Custom Code**.</span></span>
    
   <span data-ttu-id="e8bce-113">L'affichage bascule vers le stub du gestionnaire d'événements de l'événement [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) dans l'éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="e8bce-113">The focus switches to the stub for the event handler for the [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onbeforechange-onvalidate-or-onafterchange-event-of-a-field-or-group"></a><span data-ttu-id="e8bce-114">Ajout d'un gestionnaire d'événements pour l'événement OnBeforeChange, OnValidate ou OnAfterChange d'un champ ou d'un groupe</span><span class="sxs-lookup"><span data-stu-id="e8bce-114">Add an event handler for the OnBeforeChange, OnValidate, or OnAfterChange event of a field or group</span></span>

1. <span data-ttu-id="e8bce-115">Cliquez avec le bouton droit de la souris sur un contrôle d'entrée de données lié au champ ou au groupe, par exemple un contrôle **Zone de texte**.</span><span class="sxs-lookup"><span data-stu-id="e8bce-115">Right-click a data-entry control bound to the field or group, such as a **Text Box** control.</span></span> 
    
2. <span data-ttu-id="e8bce-116">Pointez sur **Programmation**, puis cliquez sur l'une des commande, comme **Événement Sur validation (OnValidate)**.</span><span class="sxs-lookup"><span data-stu-id="e8bce-116">Point to **Programming**, and then click one of the commands, such as **On Validate Event**.</span></span>
    
   <span data-ttu-id="e8bce-117">Le stub du handler d’événements est alors mis au point pour l’un des événements suivants dans l’éditeur de code : [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx), [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx)ou [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx).</span><span class="sxs-lookup"><span data-stu-id="e8bce-117">The focus switches to the stub for the event handler for one of the following events in the code editor: [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx), [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx), or [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx).</span></span> 
    
### <a name="add-an-event-handler-for-the-onload-onswitchview-oncontextchange-or-onsign-event-of-a-form"></a><span data-ttu-id="e8bce-118">Ajout d'un gestionnaire d'événements pour l'événement OnLoad, OnSwitchView, OnContextChange ou OnSign d'un formulaire</span><span class="sxs-lookup"><span data-stu-id="e8bce-118">Add an event handler for the OnLoad, OnSwitchView, OnContextChange, or OnSign event of a form</span></span>

- <span data-ttu-id="e8bce-119">Dans le menu **Outils**, pointez sur **Programmation**, puis cliquez sur l'événement de formulaire pour lequel vous souhaitez écrire un gestionnaire d'événements.</span><span class="sxs-lookup"><span data-stu-id="e8bce-119">On the **Tools** menu, point to **Programming**, and then click the form event that you want to write an event handler for.</span></span>
    
    <span data-ttu-id="e8bce-120">Le stub du handler d’événements est alors mis au point pour l’un des événements suivants dans l’éditeur de code : [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx), [OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx), [OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx)ou [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx).</span><span class="sxs-lookup"><span data-stu-id="e8bce-120">The focus switches to the stub for the event handler for one of the following in the code editor: [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx), [OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx), [OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx), or [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx).</span></span> 
    
### <a name="add-an-event-handler-for-the-onsubmitrequest-event-of-a-form"></a><span data-ttu-id="e8bce-121">Ajout d'un gestionnaire d'événements pour l'événement OnSubmitRequest d'un formulaire</span><span class="sxs-lookup"><span data-stu-id="e8bce-121">Add an event handler for the OnSubmitRequest event of a form</span></span>

1. <span data-ttu-id="e8bce-122">Sous l'onglet **Données**, cliquez sur **Options d'envoi**.</span><span class="sxs-lookup"><span data-stu-id="e8bce-122">On the **Data** tab, click **Submit Options**.</span></span>
    
2. <span data-ttu-id="e8bce-123">Activez la case à cocher **Autoriser les utilisateurs à envoyer ce formulaire**, puis cliquez sur **Effectuer une action personnalisée à l'aide du code**.</span><span class="sxs-lookup"><span data-stu-id="e8bce-123">Select the **Allow users to submit this form** check box, and then click **Perform custom action using Code**.</span></span>
    
3. <span data-ttu-id="e8bce-124">Cliquez sur **Modifier le code**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8bce-124">Click **Edit Code**, and then click **OK**.</span></span>
    
   <span data-ttu-id="e8bce-125">L'affichage bascule vers le stub du gestionnaire d'événements de l'événement [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) dans l'éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="e8bce-125">The focus switches to the stub for the event handler for the [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onsaverequest-event-of-a-form"></a><span data-ttu-id="e8bce-126">Ajout d'un gestionnaire d'événements pour l'événement OnSaveRequest d'un formulaire</span><span class="sxs-lookup"><span data-stu-id="e8bce-126">Add an event handler for the OnSaveRequest event of a form</span></span>

1. <span data-ttu-id="e8bce-127">Cliquez sur l'onglet **Fichiers**, cliquez sur **Options de formulaire**.</span><span class="sxs-lookup"><span data-stu-id="e8bce-127">Click the **File** tab, and then click **Form Options**.</span></span>
    
2. <span data-ttu-id="e8bce-128">Dans la catégorie **Enregistrer**, cliquez sur **Enregistrer au moyen d'un code personnalisé**, sur **Modifier**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8bce-128">In the **Save** category, click **Save using custom code**, click **Edit**, and then click **OK**.</span></span>
    
   <span data-ttu-id="e8bce-129">L'affichage bascule vers le stub du gestionnaire d'événements de l'événement [OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) dans l'éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="e8bce-129">The focus switches to the stub for the event handler for the [OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onversionupgrade-event-of-a-form"></a><span data-ttu-id="e8bce-130">Ajout d'un gestionnaire d'événements pour l'événement OnVersionUpgrade d'un formulaire</span><span class="sxs-lookup"><span data-stu-id="e8bce-130">Add an event handler for the OnVersionUpgrade event of a form</span></span>

1. <span data-ttu-id="e8bce-131">Cliquez sur l'onglet **Fichiers**, cliquez sur **Options de formulaire**.</span><span class="sxs-lookup"><span data-stu-id="e8bce-131">Click the **File** tab, and then click **Form Options**.</span></span>
    
2. <span data-ttu-id="e8bce-132">Dans la catégorie **Contrôle de version**, sélectionnez **Utiliser un événement personnalisé** dans la liste **Mettre à jour les formulaires existants**, cliquez sur **Modifier**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8bce-132">In the **Versioning** category, select **Use custom event** from the **Update existing forms** list, click **Edit**, and then click **OK**.</span></span>
    
    <span data-ttu-id="e8bce-133">L'affichage bascule vers le stub du gestionnaire d'événements de l'événement [OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) dans l'éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="e8bce-133">The focus switches to the stub for the event handler for the [OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onmergerequest-event-of-a-form"></a><span data-ttu-id="e8bce-134">Ajout d'un gestionnaire d'événements pour l'événement OnMergeRequest d'un formulaire</span><span class="sxs-lookup"><span data-stu-id="e8bce-134">Add an event handler for the OnMergeRequest event of a form</span></span>

1. <span data-ttu-id="e8bce-135">Cliquez sur l'onglet **Fichiers**, puis cliquez sur **Options de formulaire**.</span><span class="sxs-lookup"><span data-stu-id="e8bce-135">Click the **File** tab, and then click **Form Options**.</span></span>
    
2. <span data-ttu-id="e8bce-136">Dans la catégorie **Avancé**, activez les cases à cocher **Activer la fusion de formulaires** et **Fusionner à l'aide d'un code personnalisé**, cliquez sur **Modifier**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8bce-136">In the **Advanced** category, select the **Enable Form merging** and the **Merge using custom code** check boxes, click **Edit**, and then click **OK**.</span></span>
    
    <span data-ttu-id="e8bce-137">L'affichage bascule vers le stub du gestionnaire d'événements de l'événement [OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) dans l'éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="e8bce-137">The focus switches to the stub for the event handler for the [OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) event in the code editor.</span></span> 
    
## <a name="adding-an-event-handler-for-the-onafterimport-event"></a><span data-ttu-id="e8bce-138">Ajout d’un handler d’événements pour l’événement OnAfterImport</span><span class="sxs-lookup"><span data-stu-id="e8bce-138">Adding an event handler for the OnAfterImport event</span></span>

<span data-ttu-id="e8bce-p102">Pour ajouter des gestionnaires d'événements pour l'événement [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) , vous devez ouvrir le code de formulaire de votre modèle de formulaire avec code managé et ajouter manuellement la fonction de gestionnaire d'événements. Pour plus d'informations sur la création d'un gestionnaire d'événements pour cet événement, cliquez sur le lien correspondant à l'événement **OnAfterImport**.</span><span class="sxs-lookup"><span data-stu-id="e8bce-p102">To add event handlers for the [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) event, you must open the form code for your managed-code form template and add the event handler function manually. For information on how to write an event handler for this event, click the link for the **OnAfterImport** event.</span></span> 
  
## <a name="adding-an-event-handler-for-a-secondary-data-source"></a><span data-ttu-id="e8bce-141">Ajout d’un handler d’événements pour une source de données secondaire</span><span class="sxs-lookup"><span data-stu-id="e8bce-141">Adding an event handler for a secondary data source</span></span>

<span data-ttu-id="e8bce-p103">L'exemple qui suit illustre l'ajout d'un gestionnaire d'événements pour une source de données secondaire. Cet exemple part du principe qu'il existe une source de données secondaire basée sur un fichier de ressource, books.xml, qui présente le schéma suivant :</span><span class="sxs-lookup"><span data-stu-id="e8bce-p103">The following example shows how to add an event handler for a secondary data source. The example assumes a secondary data source from a resource file named books.xml, which has the following schema:</span></span>
  
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

<span data-ttu-id="e8bce-p104">La vue du formulaire est générée à partir de cette source de données. Le code du formulaire crée une table de hachage basée sur les auteurs et le nombre de livres qu'ils ont écrits. Vous pouvez mettre à jour une entrée depuis la table présentée dans la vue, et le gestionnaire d'événements **OnAfterChange** met alors à jour la table de hachage. Notez que la propriété [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.DataObject.aspx) de l'attribut **InfoPathEventHandler** (implémenté par la classe [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) est utilisée pour faire référence à la source de données secondaire.</span><span class="sxs-lookup"><span data-stu-id="e8bce-p104">The form's view is built from this data source. The form code creates a hash table based on the authors and the number of books they have written. You can update an entry from the table shown in the view and the **OnAfterChange** event handler updates the hash table. Note that the [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.DataObject.aspx) property of the **InfoPathEventHandler** attribute (which is implemented by the [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) class) is used to reference the secondary data source.</span></span> 
  
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

## <a name="how-the-class-that-contains-event-handlers-is-identified"></a><span data-ttu-id="e8bce-148">Comment la classe qui contient les handlers d’événements est identifiée</span><span class="sxs-lookup"><span data-stu-id="e8bce-148">How the class that contains event handlers is identified</span></span>

<span data-ttu-id="e8bce-149">Lorsque vous créez un nouveau projet de modèle de formulaire InfoPath compatible avec le modèle objet avec code managé InfoPath 2003, un attribut **System.ComponentModel.Description** de niveau assembly est appliqué à la classe au début du module du code du formulaire pour identifier la classe contenant tous les gestionnaires d'événements du modèle de formulaire.</span><span class="sxs-lookup"><span data-stu-id="e8bce-149">When you create a new InfoPath form template project that is compatible with the InfoPath 2003 managed code object model, an assembly-level **System.ComponentModel.Description** attribute is applied to the class at the beginning of the form code module to identify the class that contains all event handlers for the form template.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="e8bce-p105">[!IMPORTANTE] Ne modifiez pas l'attribut **System.ComponentModel.Description** de cette classe. Si vous le modifiez, votre modèle de formulaire ne sera plus en mesure d'identifier l'emplacement des gestionnaires d'événements et ceux-ci ne pourront pas fonctionner.</span><span class="sxs-lookup"><span data-stu-id="e8bce-p105">Do not modify the **System.ComponentModel.Description** attribute in this class. If you do so, your form template will not be able to identify where event handlers are located, and the event handlers will fail to run.</span></span> 
  
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

## <a name="how-event-handlers-are-identified"></a><span data-ttu-id="e8bce-152">Comment les handlers d’événements sont identifiés</span><span class="sxs-lookup"><span data-stu-id="e8bce-152">How event handlers are identified</span></span>

<span data-ttu-id="e8bce-p106">Lorsque vous ajoutez un nouveau gestionnaire d'événements à l'aide des commandes ou boutons de menu de l'interface utilisateur du mode Création d'InfoPath, le stub de la fonction du gestionnaire d'événements est écrit dans le formulaire. L'exemple qui suit présente le stub du gestionnaire d'événements créé pour un événement [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) ajouté à un champ appelé « total ».</span><span class="sxs-lookup"><span data-stu-id="e8bce-p106">When you add a new event handler using menu commands or buttons in the InfoPath design mode user interface, the stub for the event handler function is written into the form. The following example shows the stub event handler created for an [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) added for a field named 'total'.</span></span> 
  
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

<span data-ttu-id="e8bce-155">Vous pouvez ensuite ajouter du code pour appeler les membres du modèle objet InfoPath à l'aide des membres cachés privés des variables  `thisXDocument` ou  `thisApplication`, ou à l'aide des membres accessibles via l'objet  `e` **EventArgs** reçu par le gestionnaire d'événements :</span><span class="sxs-lookup"><span data-stu-id="e8bce-155">You can then add code that invokes members of the InfoPath object model using the private cached members of the  `thisXDocument` or  `thisApplication` variables, or by using the members accessed from the  `e` **EventArgs** object received by the event handler:</span></span> 
  
```cs
thisXDocument.UI.Alert.(e.Site.text);

```

```vb
thisXDocument.UI.Alert.(e.Site.text)

```

<span data-ttu-id="e8bce-156">L'attribut **InfoPathEventHandler** (tel que défini par la classe [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ) est l'attribut personnalisé pour les fonctions qui seront utilisées comme gestionnaires d'événements.</span><span class="sxs-lookup"><span data-stu-id="e8bce-156">The **InfoPathEventHandler** attribute (as defined by the [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) class) is the custom attribute for functions that will be used as event handlers.</span></span> 
  
<span data-ttu-id="e8bce-p107">Lorsqu'il est requis par l'événement, le paramètre **MatchPath** (tel que défini par la propriété [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) de la classe **InfoPathEventHandlerAttribute**) spécifie une expression XPath qui identifie la source de l'événement. Le paramètre **EventType** (tel que défini par la propriété [EventType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.EventType.aspx) de la classe **InfoPathEventHandlerAttribute**) spécifie le type de l'événement. Ne modifiez pas la valeur de ces paramètres. Si leur valeur est modifiée, le gestionnaire d'événements peut ne pas être correctement compilé ou la notification d'événement peut ne pas se produire comme prévu.</span><span class="sxs-lookup"><span data-stu-id="e8bce-p107">When required by the event, the **MatchPath** parameter (as defined by the [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) property of the **InfoPathEventHandlerAttribute** class) specifies an XPath expression that identifies the event source. The **EventType** parameter (as defined by the [EventType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.EventType.aspx) property of the **InfoPathEventHandlerAttribute** class) specifies the type of event. You should not change the values of these parameters. If the values of these parameters are changed, the event handler may not compile correctly, or event notification will not occur as expected.</span></span> 
  
## <a name="obfuscating-code-in-event-handlers"></a><span data-ttu-id="e8bce-161">Obfuscating code in event handlers</span><span class="sxs-lookup"><span data-stu-id="e8bce-161">Obfuscating code in event handlers</span></span>

<span data-ttu-id="e8bce-p108">Si vous lancez un utilitaire d'obscurcissement sur l'assembly généré lors de la compilation d'un modèle de formulaire avec code managé ( *nomprojet*  .dll), InfoPath ne peut pas charger l'assembly lorsque l'utilisateur ouvre le formulaire. Si vous voulez obscurcir le code des gestionnaires d'événements ou tout autre code de formulaire, vous devez le placer dans une assembly distincte, puis référencer cette assembly dans votre projet et appeler les membres de l'assembly référencée depuis FormCode.cs ou FormCode.vb. Il est important de lancer l'utilitaire d'obscurcissement uniquement sur l'assembly référencée.</span><span class="sxs-lookup"><span data-stu-id="e8bce-p108">If you run an obfuscator utility on the assembly that is generated when a managed-code form template is compiled ( *projectname*  .dll), InfoPath will not be able to load the assembly when a user opens the form. If you want to obfuscate the code for your event handlers or other form code, you must put the code that you want to obfuscate in a separate assembly, and reference that assembly in your project, and then call members of the referenced assembly from FormCode.cs or FormCode.vb. It is important that you run the obfuscator utility only on the referenced assembly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e8bce-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8bce-165">See also</span></span>

- [<span data-ttu-id="e8bce-166">Répondre aux événements de formulaire à l’aide du modèle objet InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="e8bce-166">Respond to Form Events Using the InfoPath 2003 Object Model</span></span>](how-to-respond-to-form-events-using-the-infopath-2003-object-model.md)

