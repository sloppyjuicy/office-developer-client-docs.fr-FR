---
title: Mettre en œuvre un wrapper pour les inspecteurs et suivre les événements au niveau des éléments dans chaque inspecteur
TOCTitle: Implement a wrapper for inspectors and track item-level events in each inspector
ms:assetid: 8021dd2b-c36c-492b-b281-783e85140ad8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184620(v=office.15)
ms:contentKeyID: 55119854
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a70aedf9a8803a2c990f07a77d4fc730f7263aae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320124"
---
# <a name="implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector"></a>Mettre en œuvre un wrapper pour les inspecteurs et suivre les événements au niveau des éléments dans chaque inspecteur

Cette rubrique contient deux exemples de code qui montrent comment implémenter un wrapper pour une collection [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) et comment utiliser ce wrapper pour suivre les événements au niveau des éléments dans chaque objet [Inspector](https://msdn.microsoft.com/library/bb647744\(v=office.15\)) de la collection.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Les exemples de deux codes suivants implémentent les classes Connect et OutlookInspector. Le premier met en œuvre des méthodes et des gestionnaires d'événements que vous incluez dans la classe Connect afin d'implémenter un wrapper pour une collection **Inspecteurs**. Le second met en œuvre une implémentation simple de la classe **OutlookInspector**.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d'abord ajouter une référence au composant Bibliothèque d'objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l'espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l'importation et la tâche dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

Dans l’exemple de code suivant, un événement [NewInspector(Inspector)](https://msdn.microsoft.com/library/bb610594\(v=office.15\)) se produit après qu’une nouvelle fenêtre Inspecteur a été créée et avant qu’elle ne s’affiche. Une action d’un utilisateur peut également créer une nouvelle fenêtre Inspecteur. Une variable instance niveau classe nommée inspecteurs dans la classe **Connect** est déclarée et un événement**NewInspector** est connecté. 

Dans la méthode inspecteur\_NewInspector, la méthode**FindOutlookInspector**vérifie si la nouvelle fenêtre Inspecteur se trouve déjà dans la liste inspectorWindows. Si FindOutlookInspector ne trouve pas l’objet **inspecteur** dans inspectorWindows, la méthode **AddInspector** ajoute une instance de la classe**OutlookInspector** à inspectorWindows. Vous pouvez utiliser la classe **OutlookInspector** afin de déclencher des événements pour cette fenêtre d'inspecteur particulière. L'implémentation de la classe **OutlookInspector** est illustrée dans le second exemple de code.

```csharp
class Connect
{
    // Connect class-level Instance Variables
    // Outlook inspectors collection
    private Outlook.Inspectors inspectors;

    // Collection of tracked inspector windows              
    private List<OutlookInspector> inspectorWindows;    

    // Hook up NewInspector event
    inspectors.NewInspector += new 
        Outlook.InspectorsEvents_NewInspectorEventHandler(
        inspectors_NewInspector);

    // NewInspector event creates new instance of OutlookInspector
    void inspectors_NewInspector(Outlook.Inspector Inspector)
    {
        // Check to see if this is a new window you don't
        // already track
        OutlookInspector existingWindow = 
            FindOutlookInspector(Inspector);
        if (existingWindow == null)
        {
            AddInspector(Inspector);
        }
    }

    // Adds an instance of **OutlookInspector** class
    private void AddInspector(Outlook.Inspector inspector)
    {
        OutlookInspector window = new OutlookInspector(inspector);
        window.Close +=
            new EventHandler(WrappedInspectorWindow_Close);
    }

    // Looks up the window wrapper for a given Inspector 
    // window object
    private OutlookInspector FindOutlookInspector(object window)
    {
        foreach (OutlookInspector inspector in inspectorWindows)
        {
            if (inspector.Window == window)
            {
                return inspector;
            }
        }
        return null;
    }
}
```

L'exemple de code suivant est une implémentation de la classe**OutlookInspector**. Ce cours est utilisé pour déclencher des événements pour la fenêtre Inspecteur à partir de l’exemple de code précédent. Plusieurs fenêtres Inspecteur peuvent être ouvertes simultanément. Les événements au niveau des éléments, comme [Open](https://msdn.microsoft.com/library/bb644296\(v=office.15\)), [PropertyChange](https://msdn.microsoft.com/library/bb647794\(v=office.15\)) et [CustomPropertyChange](https://msdn.microsoft.com/library/bb645015\(v=office.15\)) sont suivis en les raccordant dans ce constructeur de classe. Un événement [fermé](https://msdn.microsoft.com/library/bb645009\(v=office.15\)) pour un objet[ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) est également connecté dans ce constructeur de classe. Vous pouvez définir d’autres variables d’instance pour la classe niveau élément selon vos besoins. Tous les événements qui étaient raccordés dans le constructeur OutlookInspector ne le sont plus dans le gestionnaire d'événement fermé OutlookInspectorWindow\_.

Notez que, au niveau du modèle d’objet, un objet**inspecteur Outlook** n’est pas spécifique à n’importe quel type d’élément Outlook. Cet exemple de code permet d’utiliser la classe d’assistance OutlookItem, définie dans [créer une classe d’assistance pour permettre d’accéder aux membres éléments Outlook courants](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), pour appeler facilement la propriété OutlookItem.Class et vérifier la classe de message de l’élément actuel dans l’inspecteur avant d’assumer que l’élément est un élément de contact.

```csharp
// This class tracks the state of an Outlook Inspector window 
// and ensures that what happens in this window is handled correctly.
class OutlookInspector
{
    // OutlookInspector class-level instance variables 
    // wrapped window object
    private Outlook.Inspector m_Window;             

    // Use these instance variables to handle item-level events
    // wrapped MailItem
    private Outlook.MailItem m_Mail;    
    // wrapped AppointmentItem        
    private Outlook.AppointmentItem m_Appointment;  
    // wrapped ContactItem
    private Outlook.ContactItem m_Contact;
    // wrapped TaskItem      
    private Outlook.TaskItem m_Task;             

    // OutlookInspector constructor
    public OutlookInspector(Outlook.Inspector inspector)
    {
        m_Window = inspector;

        // Hook up the close event
        ((Outlook.InspectorEvents_Event)inspector).Close +=
            new Outlook.InspectorEvents_CloseEventHandler(
            OutlookInspectorWindow_Close);

        // Hook up item-level events as needed
        OutlookItem olItem = new OutlookItem(inspector.CurrentItem);
        if(olItem.Class==Outlook.OlObjectClass.olContact)
        {
            m_Contact = olItem.InnerObject as Outlook.ContactItem;
            m_Contact.Open +=
                new Outlook.ItemEvents_10_OpenEventHandler(
                m_Contact_Open);
            m_Contact.PropertyChange +=
                new Outlook.ItemEvents_10_PropertyChangeEventHandler(
                m_Contact_PropertyChange);
            m_Contact.CustomPropertyChange +=
                new Outlook.ItemEvents_10_CustomPropertyChangeEventHandler(
                m_Contact_CustomPropertyChange);
        }
    }

    // Event Handler for the inspector close event.
    private void OutlookInspectorWindow_Close()
    {
        // Unhook events from any item-level instance variables
        m_Contact.Open -= 
            Outlook.ItemEvents_10_OpenEventHandler(
            m_Contact_Open);
        m_Contact.PropertyChange -= 
            Outlook.ItemEvents_10_PropertyChangeEventHandler(
            m_Contact_PropertyChange);
        m_Contact.CustomPropertyChange -= 
            Outlook.ItemEvents_10_CustomPropertyChangeEventHandler(
            m_Contact_CustomPropertyChange);
        ((Outlook.ItemEvents_Event)m_Contact).Close -= 
            Outlook.ItemEvents_CloseEventHandler(
            m_Contact_Close);

        // Unhook events from the window
        ((Outlook.InspectorEvents_Event)m_Window).Close -=
            new Outlook.InspectorEvents_CloseEventHandler(
            OutlookInspectorWindow_Close);

        // Raise the OutlookInspector close event
        if (Close != null)
        {
            Close(this, EventArgs.Empty);
        }
        // Release item-level instance variables
        m_Mail = null;
        m_Appointment = null;
        m_Contact = null;
        m_Task = null;
        m_Window = null;
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Exemples de tâches utilisant des événements Outlook](sample-tasks-using-outlook-events.md)

