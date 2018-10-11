---
title: Créer un affichage
TOCTitle: Create a view
ms:assetid: 2f8ad187-1030-420a-bc74-c327e3521550
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424468(v=office.15)
ms:contentKeyID: 55119902
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: e9a68fc6220e1439e517b3d4e7e2ecb30b919ee0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406028"
---
# <a name="create-a-view"></a><span data-ttu-id="9e5be-102">Créer un affichage</span><span class="sxs-lookup"><span data-stu-id="9e5be-102">Create a map view programmatically</span></span>

<span data-ttu-id="9e5be-103">Cet exemple montre comment utiliser la méthode [Add(String, OlViewType, OlViewSaveOption)](https://msdn.microsoft.com/library/bb643986\(v=office.15\)) de la collection de [Views](https://msdn.microsoft.com/library/bb644226\(v=office.15\)) pour créer un affichage pour un objet [Dossier](https://msdn.microsoft.com/library/bb645774\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="9e5be-103">This example shows how to use the [Add(String, OlViewType, OlViewSaveOption)](https://msdn.microsoft.com/library/bb643986\(v=office.15\)) method of the [Views](https://msdn.microsoft.com/library/bb644226\(v=office.15\)) collection to create a view for a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object.</span></span>

## <a name="example"></a><span data-ttu-id="9e5be-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="9e5be-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="9e5be-105">L’exemple de code suivant est un extrait de [Programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="9e5be-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="9e5be-p101">Vous pouvez créer des vues personnalisables qui vous permettent de trier, de regrouper et d’afficher des données de types différents dans le volet Affichage de la fenêtre de l’explorateur Outlook. Vous pouvez également personnaliser des affichages intégrés par programmation. Le tableau suivant répertorie des objets qui représentent des affichages Outlook. </span><span class="sxs-lookup"><span data-stu-id="9e5be-p101">You can create customizable views that allow you to sort, group, and view data of all different types within the View Pane of the Outlook explorer window. You can also customize built-in views programmatically. The following table lists objects that represent Outlook views.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e5be-109">Nom d’objet</span><span class="sxs-lookup"><span data-stu-id="9e5be-109">Object Name</span></span></p></th>
<th><p><span data-ttu-id="9e5be-110">Description</span><span class="sxs-lookup"><span data-stu-id="9e5be-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e5be-111"><a href="https://msdn.microsoft.com/library/bb646315(v=office.15)">BusinessCardView</a></span><span class="sxs-lookup"><span data-stu-id="9e5be-111"><a href="https://msdn.microsoft.com/library/bb646315(v=office.15)">BusinessCardView Object</a></span></span></p></td>
<td><p><span data-ttu-id="9e5be-112">Les données sont affichées comme une série d’images de cartes de visite électroniques.</span><span class="sxs-lookup"><span data-stu-id="9e5be-112">Data is viewed as a series of Electronic Business Card images.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e5be-113"><a href="https://msdn.microsoft.com/library/bb622874(v=office.15)">CalendarView</a></span><span class="sxs-lookup"><span data-stu-id="9e5be-113"><a href="https://msdn.microsoft.com/library/bb622874(v=office.15)">CalendarView</a></span></span></p></td>
<td><p><span data-ttu-id="9e5be-114">Les données sont affichées sous la forme d’un calendrier.</span><span class="sxs-lookup"><span data-stu-id="9e5be-114">Data is viewed in a calendar format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e5be-115"><a href="https://msdn.microsoft.com/library/bb609216(v=office.15)">CardView</a></span><span class="sxs-lookup"><span data-stu-id="9e5be-115"><a href="https://msdn.microsoft.com/library/bb609216(v=office.15)">CardView Object</a></span></span></p></td>
<td><p><span data-ttu-id="9e5be-116">Les données sont affichées dans une série de cartes.</span><span class="sxs-lookup"><span data-stu-id="9e5be-116">Data is viewed in a series of cards.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e5be-117"><a href="https://msdn.microsoft.com/library/bb612031(v=office.15)">IconView</a></span><span class="sxs-lookup"><span data-stu-id="9e5be-117"><a href="https://msdn.microsoft.com/library/bb612031(v=office.15)">IconView Object</a></span></span></p></td>
<td><p><span data-ttu-id="9e5be-118">Les données sont affichées sous la forme d’icônes de dossier Windows ou d’icônes d’explorateur.</span><span class="sxs-lookup"><span data-stu-id="9e5be-118">Data is viewed as Windows folder icons or explorer icons.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e5be-119"><a href="https://msdn.microsoft.com/library/bb608854(v=office.15)">TableView</a></span><span class="sxs-lookup"><span data-stu-id="9e5be-119"><a href="https://msdn.microsoft.com/library/bb608854(v=office.15)">TableView Object</a></span></span></p></td>
<td><p><span data-ttu-id="9e5be-120">Les données sont affichées dans un tableau simple contenant des champs.</span><span class="sxs-lookup"><span data-stu-id="9e5be-120">Data is viewed in a simple field-based table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e5be-121"><a href="https://msdn.microsoft.com/library/bb609455(v=office.15)">TimelineView</a></span><span class="sxs-lookup"><span data-stu-id="9e5be-121"><a href="https://msdn.microsoft.com/library/bb609455(v=office.15)">TimelineView Object</a></span></span></p></td>
<td><p><span data-ttu-id="9e5be-122">Les données sont affichées selon une chronologie linéaire personnalisable.</span><span class="sxs-lookup"><span data-stu-id="9e5be-122">Data is viewed in a customizable linear time line.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9e5be-123">Vous pouvez accéder aux propriétés et aux méthodes communes à tous les affichages en utilisant l’objet [View](https://msdn.microsoft.com/library/bb647396\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="9e5be-123">You can access properties and methods that are common to all views by using the [View](https://msdn.microsoft.com/library/bb647396\(v=office.15\)) object.</span></span> <span data-ttu-id="9e5be-124">Cependant, pour accéder à certaines propriétés qui ne sont pas communes à tous les affichages, vous devez caster l'objet **View** à un objet **View** dérivé ayant la propriété à laquelle vous voulez accéder.</span><span class="sxs-lookup"><span data-stu-id="9e5be-124">However, to access certain properties that are not common to all views, you must cast the View object to a derived view object that the property you want to access belongs to.</span></span> <span data-ttu-id="9e5be-125">Par exemple, pour accéder à la propriété [HeadingsFont](https://msdn.microsoft.com/library/bb612522\(v=office.15\)) de l'objet **Cardview**, castez l'objet **View** en l'objet **CardView**.</span><span class="sxs-lookup"><span data-stu-id="9e5be-125">For example, to access the [HeadingsFont](https://msdn.microsoft.com/library/bb612522\(v=office.15\)) property of the **Cardview** object, cast the **View** object to the **CardView** object.</span></span> <span data-ttu-id="9e5be-126">Si vous voulez déterminer quel type d’affichage est représenté par un objet **View** spécifique, utilisez la propriété [ViewType](https://msdn.microsoft.com/library/bb623693\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="9e5be-126">If you want to determine which type of view is represented by a particular **View** object, use the [ViewType](https://msdn.microsoft.com/library/bb623693\(v=office.15\)) property.</span></span>

<span data-ttu-id="9e5be-127">Pour créer un nouvel affichage, utilisez la méthode **Add** de la collection **Views** pour un objet **Folder**.</span><span class="sxs-lookup"><span data-stu-id="9e5be-127">To create a new view, use the **Add** method of the **Views** collection for a **Folder** object.</span></span> <span data-ttu-id="9e5be-128">Définissez ensuite la visibilité de l’affichage, soit au moment de la création ou à tout moment après la création de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="9e5be-128">Then set the visibility for the view either at the time of creation, or at any time after the view is created.</span></span> <span data-ttu-id="9e5be-129">Pour définir la visibilité de l'affichage au moment de la création, spécifiez une constante [OlViewSaveOption](https://msdn.microsoft.com/library/bb647502\(v=office.15\)) dans le paramètre *SaveOption* de la méthode **Add**.</span><span class="sxs-lookup"><span data-stu-id="9e5be-129">To set the visibility for the view at the time of creation, specify an [OlViewSaveOption](https://msdn.microsoft.com/library/bb647502\(v=office.15\)) constant in the  *SaveOption* parameter of the **Add** method.</span></span> <span data-ttu-id="9e5be-130">Pour définir la visibilité après la création de l'affichage, spécifiez une constante **OlViewSaveOption** pour la propriété [SaveOption](https://msdn.microsoft.com/library/bb646426\(v=office.15\)) de l'objet **View**.</span><span class="sxs-lookup"><span data-stu-id="9e5be-130">To set the visibility at any time after the view is created, specify an **OlViewSaveOption** constant for the [SaveOption](https://msdn.microsoft.com/library/bb646426\(v=office.15\)) property of the **View** object.</span></span> 

<span data-ttu-id="9e5be-131">L'ajout d'un nouvel affichage déclenche l'événement [ViewAdd](https://msdn.microsoft.com/library/bb647550\(v=office.15\)) de la collection **Views**.</span><span class="sxs-lookup"><span data-stu-id="9e5be-131">Adding a new view raises the [ViewAdd](https://msdn.microsoft.com/library/bb647550\(v=office.15\)) event of the **Views** collection.</span></span> <span data-ttu-id="9e5be-132">Une fois l'affichage créé, personnalisez-le par programmation en castant l'objet **View** à l'un des objets dérivés, puis en effectuant les modifications nécessaires.</span><span class="sxs-lookup"><span data-stu-id="9e5be-132">Once the view is created, customize the view programmatically by casting the **View** object to one of the derived objects and then making necessary changes.</span></span> <span data-ttu-id="9e5be-133">Utilisez la méthode **Save** de l'objet **View** dérivé ou de l'objet **View** pour enregistrer les éventuelles modifications apportées à l'affichage.</span><span class="sxs-lookup"><span data-stu-id="9e5be-133">Use the Save method of the derived view object or the View object to save any changes to the view.</span></span> <span data-ttu-id="9e5be-134">Enfin, utilisez la méthode **Apply** de l'objet **View** dérivé ou de l'objet **View** pour appliquer l'affichage à l'objet [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) actuel.</span><span class="sxs-lookup"><span data-stu-id="9e5be-134">Finally, use the Apply method of the derived view object or the View object to apply the view to the current Explorer object.</span></span> <span data-ttu-id="9e5be-135">Cela déclenche l’événement [ViewSwitch](https://msdn.microsoft.com/library/bb644066\(v=office.15\)) de l’objet **Explorer**.</span><span class="sxs-lookup"><span data-stu-id="9e5be-135">This raises the [ViewSwitch](https://msdn.microsoft.com/library/bb644066\(v=office.15\)) event of the **Explorer** object.</span></span>

<span data-ttu-id="9e5be-136">Dans l'exemple de code suivant, CreateMeetingRequestsView ajoute un nouvel affichage nommé « Meeting Requests » à la Boîte de réception de l'utilisateur en castant l'objet **View** en un objet **TableView**.</span><span class="sxs-lookup"><span data-stu-id="9e5be-136">In the following code example,   adds a new view named "Meeting Requests" to the user's Inbox by casting the View object to a TableView object.</span></span> <span data-ttu-id="9e5be-137">CreateMeetingRequestsView appelle ensuite la méthode **Add** de l'objet **Views** avec le paramètre *Name* défini comme « Meeting Requests » et le paramètre *ViewType* défini comme **olTableView**.</span><span class="sxs-lookup"><span data-stu-id="9e5be-137"> then calls the Add method of the Views object with the  Name parameter set to "Meeting Requests" and the  ViewType parameter set to olTableView.</span></span> <span data-ttu-id="9e5be-138">La propriété [Filter](https://msdn.microsoft.com/library/bb610296\(v=office.15\)) de l'objet **TableView** est définie comme une chaîne DASL qui provoque l'affichage de la vue uniquement lorsque figurent des éléments qui contiennent « IPM.Schedule » dans la classe message de l'élément.</span><span class="sxs-lookup"><span data-stu-id="9e5be-138">The [Filter](https://msdn.microsoft.com/library/bb610296\(v=office.15\)) property of the **TableView** object is set to a DAV Searching and Locating (DASL) string that causes the view to display only when there are items that contain "IPM.Schedule" in the message class for the item.</span></span> <span data-ttu-id="9e5be-139">Le nouvel affichage est ensuite enregistré et appliqué.</span><span class="sxs-lookup"><span data-stu-id="9e5be-139">The new view is then saved and applied.</span></span>

<span data-ttu-id="9e5be-140">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d'abord ajouter une référence au composant Bibliothèque d'objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l'espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="9e5be-140">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="9e5be-141">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="9e5be-141">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="9e5be-142">La ligne de code suivante montre comment effectuer l'importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="9e5be-142">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateMeetingRequestsView()
{
    const string PR_MESSAGE_CLASS =
        "https://schemas.microsoft.com/mapi/proptag/0x001A001E";
    Outlook.Views views =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).Views;
    Outlook.TableView tableView = (Outlook.TableView)
        views.Add("Meeting Requests",
        Outlook.OlViewType.olTableView,
        Outlook.OlViewSaveOption.olViewSaveOptionThisFolderEveryone);
    tableView.Filter = "\"" + PR_MESSAGE_CLASS + "\"" +
        " like 'IPM.Schedule%'";
    tableView.Save();
    tableView.Apply();
}
```

## <a name="see-also"></a><span data-ttu-id="9e5be-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e5be-143">See also</span></span>

- [<span data-ttu-id="9e5be-144">Affichages</span><span class="sxs-lookup"><span data-stu-id="9e5be-144">Views</span></span>](views.md)

