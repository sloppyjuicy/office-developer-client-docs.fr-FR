---
title: Mettre en œuvre un wrapper pour les inspecteurs et suivre les événements au niveau des éléments dans chaque inspecteur
TOCTitle: Implement a wrapper for inspectors and track item-level events in each inspector
ms:assetid: 8021dd2b-c36c-492b-b281-783e85140ad8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184620(v=office.15)
ms:contentKeyID: 55119854
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: d5fee97e27b616232f2f45eb42faf659eee52cda
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405769"
---
# <a name="implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector"></a><span data-ttu-id="678f9-102">Mettre en œuvre un wrapper pour les inspecteurs et suivre les événements au niveau des éléments dans chaque inspecteur</span><span class="sxs-lookup"><span data-stu-id="678f9-102">Implement a Wrapper for Inspectors and Track Item-Level Events in Each Inspector</span></span>

<span data-ttu-id="678f9-103">Cette rubrique contient deux exemples de code qui montrent comment implémenter un wrapper pour une collection [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) et comment utiliser ce wrapper pour suivre les événements au niveau des éléments dans chaque objet [Inspector](https://msdn.microsoft.com/library/bb647744\(v=office.15\)) de la collection.</span><span class="sxs-lookup"><span data-stu-id="678f9-103">This topic contains two code examples that show how to implement a wrapper for an [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) collection and to use that wrapper to track item-level events in each [Inspector](https://msdn.microsoft.com/library/bb647744\(v=office.15\)) object in the collection.</span></span>

## <a name="example"></a><span data-ttu-id="678f9-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="678f9-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="678f9-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="678f9-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="678f9-106">Les exemples de deux codes suivants implémentent les classes Connect et OutlookInspector.</span><span class="sxs-lookup"><span data-stu-id="678f9-106">The following two code examples implement the   and   classes.</span></span> <span data-ttu-id="678f9-107">Le premier met en œuvre des méthodes et des gestionnaires d'événements que vous incluez dans la classe Connect afin d'implémenter un wrapper pour une collection **Inspecteurs**.</span><span class="sxs-lookup"><span data-stu-id="678f9-107">The first code example involves methods and event handlers you include in the   class to implement a wrapper for an Inspectors collection.</span></span> <span data-ttu-id="678f9-108">Le second met en œuvre une implémentation simple de la classe **OutlookInspector**.</span><span class="sxs-lookup"><span data-stu-id="678f9-108">The second code example involves a simple implementation of the  \*\*\*\* class.</span></span>

<span data-ttu-id="678f9-109">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d'abord ajouter une référence au composant Bibliothèque d'objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l'espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="678f9-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="678f9-110">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="678f9-110">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="678f9-111">La ligne de code suivante montre comment effectuer l'importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="678f9-111">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

<span data-ttu-id="678f9-112">Dans l’exemple de code suivant, un événement [NewInspector(Inspector)](https://msdn.microsoft.com/library/bb610594\(v=office.15\)) se produit après qu’une nouvelle fenêtre Inspecteur a été créée et avant qu’elle ne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="678f9-112">In the following code example, a [NewInspector(Inspector)](https://msdn.microsoft.com/library/bb610594\(v=office.15\)) event occurs after a new inspector window has been created and before it is displayed.</span></span> <span data-ttu-id="678f9-113">Une action d’un utilisateur peut également créer une nouvelle fenêtre Inspecteur.</span><span class="sxs-lookup"><span data-stu-id="678f9-113">A user action may also create a new inspector window.</span></span> <span data-ttu-id="678f9-114">Une variable instance niveau classe nommée inspecteurs dans la classe **Connect** est déclarée et un événement**NewInspector** est connecté.</span><span class="sxs-lookup"><span data-stu-id="678f9-114">A class-level instance variable named   in the Connect class is declared, and a NewInspector event is hooked up.</span></span> 

<span data-ttu-id="678f9-115">Dans la méthode inspecteur\_NewInspector, la méthode**FindOutlookInspector**vérifie si la nouvelle fenêtre Inspecteur se trouve déjà dans la liste inspectorWindows.</span><span class="sxs-lookup"><span data-stu-id="678f9-115">In the   method, the   method checks whether the new inspector window is already in the   list.</span></span> <span data-ttu-id="678f9-116">Si FindOutlookInspector ne trouve pas l’objet **inspecteur** dans inspectorWindows, la méthode **AddInspector** ajoute une instance de la classe**OutlookInspector** à inspectorWindows.</span><span class="sxs-lookup"><span data-stu-id="678f9-116">If   does not find the Inspector object in  , the   method adds an instance of the   class to  .</span></span> <span data-ttu-id="678f9-117">Vous pouvez utiliser la classe **OutlookInspector** afin de déclencher des événements pour cette fenêtre d'inspecteur particulière.</span><span class="sxs-lookup"><span data-stu-id="678f9-117">You can use the  \*\*\*\* class to raise events for this particular inspector window.</span></span> <span data-ttu-id="678f9-118">L'implémentation de la classe **OutlookInspector** est illustrée dans le second exemple de code.</span><span class="sxs-lookup"><span data-stu-id="678f9-118">The implementation of the  \*\*\*\* class is shown in the second code example.</span></span>

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

<span data-ttu-id="678f9-119">L'exemple de code suivant est une implémentation de la classe**OutlookInspector**.</span><span class="sxs-lookup"><span data-stu-id="678f9-119">The following code example is an implementation of the  \*\*\*\* class.</span></span> <span data-ttu-id="678f9-120">Ce cours est utilisé pour déclencher des événements pour la fenêtre Inspecteur à partir de l’exemple de code précédent.</span><span class="sxs-lookup"><span data-stu-id="678f9-120">This class is used to raise events for the inspector window from the preceding code example.</span></span> <span data-ttu-id="678f9-121">Plusieurs fenêtres Inspecteur peuvent être ouvertes simultanément.</span><span class="sxs-lookup"><span data-stu-id="678f9-121">Multiple inspector windows can be open simultaneously.</span></span> <span data-ttu-id="678f9-122">Les événements au niveau des éléments, comme [Open](https://msdn.microsoft.com/library/bb644296\(v=office.15\)), [PropertyChange](https://msdn.microsoft.com/library/bb647794\(v=office.15\)) et [CustomPropertyChange](https://msdn.microsoft.com/library/bb645015\(v=office.15\)) sont suivis en les raccordant dans ce constructeur de classe.</span><span class="sxs-lookup"><span data-stu-id="678f9-122">Item-level events such as [Open](https://msdn.microsoft.com/library/bb644296\(v=office.15\)) , [PropertyChange](https://msdn.microsoft.com/library/bb647794\(v=office.15\)) , and [CustomPropertyChange](https://msdn.microsoft.com/library/bb645015\(v=office.15\)) are tracked by hooking them up in this class constructor.</span></span> <span data-ttu-id="678f9-123">Un événement [fermé](https://msdn.microsoft.com/library/bb645009\(v=office.15\)) pour un objet[ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) est également connecté dans ce constructeur de classe.</span><span class="sxs-lookup"><span data-stu-id="678f9-123">A [Close](https://msdn.microsoft.com/library/bb645009\(v=office.15\)) event for a [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) object is also hooked up in this class constructor.</span></span> <span data-ttu-id="678f9-124">Vous pouvez définir d’autres variables d’instance pour la classe niveau élément selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="678f9-124">You can define other class-level item instance variables as needed.</span></span> <span data-ttu-id="678f9-125">Tous les événements qui étaient raccordés dans le constructeur OutlookInspector ne le sont plus dans le gestionnaire d'événement fermé OutlookInspectorWindow\_.</span><span class="sxs-lookup"><span data-stu-id="678f9-125">All the events that were hooked up in the   constructor are unhooked in the   event handler.</span></span>

<span data-ttu-id="678f9-126">Notez que, au niveau du modèle d’objet, un objet**inspecteur Outlook** n’est pas spécifique à n’importe quel type d’élément Outlook.</span><span class="sxs-lookup"><span data-stu-id="678f9-126">Note that at the object model level, an **Outlook inspector** object is not specific to any Outlook item type.</span></span> <span data-ttu-id="678f9-127">Cet exemple de code permet d’utiliser la classe d’assistance OutlookItem, définie dans [créer une classe d’assistance pour permettre d’accéder aux membres éléments Outlook courants](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), pour appeler facilement la propriété OutlookItem.Class et vérifier la classe de message de l’élément actuel dans l’inspecteur avant d’assumer que l’élément est un élément de contact.</span><span class="sxs-lookup"><span data-stu-id="678f9-127">This code sample makes use of the OutlookItem helper class, defined in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), to conveniently call the OutlookItem.Class property to verify the message class of the current item in the inspector, before assuming the item is a contact item.</span></span>

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
    private Outlook.ContactItem m_Task;             

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

## <a name="see-also"></a><span data-ttu-id="678f9-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="678f9-128">See also</span></span>

- [<span data-ttu-id="678f9-129">Exemples de tâches utilisant des événements Outlook</span><span class="sxs-lookup"><span data-stu-id="678f9-129">Sample Tasks Using Outlook Events</span></span>](sample-tasks-using-outlook-events.md)

