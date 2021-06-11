---
title: Ajout de champs à un affichage
TOCTitle: Add fields to a view
ms:assetid: ea371f27-ea65-47ef-ae44-ef843a78ab6f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424481(v=office.15)
ms:contentKeyID: 55119934
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4b850bf87be4024152ee808624ad93836b904897
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359695"
---
# <a name="add-fields-to-a-view"></a><span data-ttu-id="70de5-102">Ajout de champs à un affichage</span><span class="sxs-lookup"><span data-stu-id="70de5-102">Add fields to a view</span></span>

<span data-ttu-id="70de5-103">Cet exemple montre comment personnaliser une vue à l’aide de la méthode [Add(String)](https://msdn.microsoft.com/library/bb646040\(v=office.15\)) de la collection [ViewFields](https://msdn.microsoft.com/library/bb645950\(v=office.15\)) pour ajouter des champs à une vue.</span><span class="sxs-lookup"><span data-stu-id="70de5-103">This example shows how to customize a view by using the [Add(String)](https://msdn.microsoft.com/library/bb646040\(v=office.15\)) method of the [ViewFields](https://msdn.microsoft.com/library/bb645950\(v=office.15\)) collection to add fields to a view.</span></span>

## <a name="example"></a><span data-ttu-id="70de5-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="70de5-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="70de5-105">L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="70de5-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="70de5-106">Vous pouvez spécifier quelles propriétés des éléments d'Outlook sont affichées dans un affichage en ajoutant une ou plusieurs propriétés à la collection **ViewFields** seulement pour les objets [CardView](https://msdn.microsoft.com/library/bb609216\(v=office.15\)) et [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="70de5-106">You can specify which Outlook item properties are displayed in a view by adding one or more properties to the **ViewFields** collection for only the [CardView](https://msdn.microsoft.com/library/bb609216\(v=office.15\)) and [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) objects.</span></span> <span data-ttu-id="70de5-107">Pour d’autres objets **View** dérivés tels que les objets [BusinessCardView](https://msdn.microsoft.com/library/bb646315\(v=office.15\)), [CalendarView](https://msdn.microsoft.com/library/bb622874\(v=office.15\)), [IconView](https://msdn.microsoft.com/library/bb612031\(v=office.15\)) et [TimelineView](https://msdn.microsoft.com/library/bb609455\(v=office.15\)), utilisez d’autres méthodes pour déterminer les propriétés d’élément d’Outlook qui sont affichées dans la vue.</span><span class="sxs-lookup"><span data-stu-id="70de5-107">For other derived **View** objects such as [BusinessCardView](https://msdn.microsoft.com/library/bb646315\(v=office.15\)), [CalendarView](https://msdn.microsoft.com/library/bb622874\(v=office.15\)), [IconView](https://msdn.microsoft.com/library/bb612031\(v=office.15\)), and [TimelineView](https://msdn.microsoft.com/library/bb609455\(v=office.15\)) objects, use other methods of determining which Outlook item properties are displayed within the view.</span></span> <span data-ttu-id="70de5-108">Par exemple, les champs affichés pour l’objet **BusinessCardView** sont déterminés par la disposition de la carte de visite électronique associée à chaque élément d’Outlook affiché.</span><span class="sxs-lookup"><span data-stu-id="70de5-108">For example, the fields displayed for the **BusinessCardView** object are determined by the electronic business card (EBC) layout associated with each displayed Outlook item.</span></span>

<span data-ttu-id="70de5-p102">Pour obtenir la collection **ViewFields** pour un affichage, utilisez la propriété **ViewFields** de l'objet **View** associé (par exemple les objets **CardView** ou **TableView**). La méthode **Add** de la collection **ViewFields** est utilisée pour créer un objet [ViewField](https://msdn.microsoft.com/library/bb610583\(v=office.15\)) qui représente la propriété d'élément Outlook à afficher dans l'affichage. Un objet **ViewField** non seulement identifie une propriété d'élément Outlook à afficher dans l'affichage, mais il décrit aussi comment les valeurs de cette propriété doivent être affichées. Vous pouvez changer la façon dont les propriétés des colonnes individuelles sont affichées dans un affichage en modifiant la propriété [ColumnFormat](https://msdn.microsoft.com/library/bb646462\(v=office.15\)) de l'objet **ViewField**.</span><span class="sxs-lookup"><span data-stu-id="70de5-p102">To get the **ViewFields** collection for a view, use the **ViewFields** property of the associated **View** object (for example, the **CardView** or **TableView** objects). The **Add** method of the **ViewFields** collection is used to create a [ViewField](https://msdn.microsoft.com/library/bb610583\(v=office.15\)) object that represents the Outlook item property to be displayed in the view. A **ViewField** object not only identifies an Outlook item property to display within the view, but it also describes how the values for that property should be displayed. You can change how individual column properties are displayed in a view by modifying the [ColumnFormat](https://msdn.microsoft.com/library/bb646462\(v=office.15\)) property of the **ViewField** object.</span></span>

<span data-ttu-id="70de5-p103">Dans l’exemple de code suivant, ModifyMeetingRequestsView obtient l’objet **TableView** qui représente tous les affichages de la Boîte de réception (Inbox) de l’utilisateur qui sont des affichages « Meeting Requests » (Demandes de réunion). L’exemple utilise ensuite la méthode **Add** pour ajouter les champs « Start » (Début) et « End » (Fin) à l’objet **ViewFields** qui correspond à l’objet **TableView**. Il change aussi le libellé du champ « From » (De) en « Organized By » (Organisé par). ModifyMeetingRequestsView enregistre ensuite l’objet **TableView** modifié.</span><span class="sxs-lookup"><span data-stu-id="70de5-p103">In the following code example, ModifyMeetingRequestsView gets the **TableView** object that represents all the views from the user’s Inbox that are “Meeting Requests” views. The example then uses the **Add** method to add the “Start” and “End” fields to the **ViewFields** object that corresponds to the **TableView** object. It also changes the label for the “From” field to “Organized By”. ModifyMeetingRequestsView then saves the modified **TableView** object.</span></span>

<span data-ttu-id="70de5-117">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="70de5-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="70de5-118">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="70de5-118">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="70de5-119">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="70de5-119">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ModifyMeetingRequestsView()
{
    Outlook.TableView tableView = null;
    Outlook.ViewField startField = null;
    Outlook.ViewField endField = null;
    Outlook.ViewField fromField = null;
    try
    {
        tableView =
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox)
            .Views["Meeting Requests"] as Outlook.TableView;
    }
    catch { }
    if (tableView != null)
    {
        try
        {
            startField = tableView.ViewFields["Start"];
        }
        catch{}
        if (startField == null)
        {
            startField = tableView.ViewFields.Add("Start");
        }
        try
        {
            endField = tableView.ViewFields["End"];
        }
        catch{}
        if (endField == null)
        {
            endField = tableView.ViewFields.Add("End");
        }
        try
        {
            fromField = tableView.ViewFields["From"];
        }
        catch{}
        if (fromField != null)
        {
            fromField.ColumnFormat.Label = "Organized By";
        }
        try
        {
            tableView.Save();
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="70de5-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70de5-120">See also</span></span>

- [<span data-ttu-id="70de5-121">Affichages</span><span class="sxs-lookup"><span data-stu-id="70de5-121">Views</span></span>](views.md)

