---
title: Créer un affichage
TOCTitle: Create a view
ms:assetid: 2f8ad187-1030-420a-bc74-c327e3521550
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424468(v=office.15)
ms:contentKeyID: 55119902
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c91f43001d6c56ad3b4c316aede9845a5e0a0064
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721870"
---
# <a name="create-a-view"></a>Créer un affichage

Cet exemple montre comment utiliser la méthode [Add(String, OlViewType, OlViewSaveOption)](https://msdn.microsoft.com/library/bb643986\(v=office.15\)) de la collection de [Views](https://msdn.microsoft.com/library/bb644226\(v=office.15\)) pour créer un affichage pour un objet [Dossier](https://msdn.microsoft.com/library/bb645774\(v=office.15\)).

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [Programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Vous pouvez créer des vues personnalisables qui vous permettent de trier, de regrouper et d’afficher des données de types différents dans le volet Affichage de la fenêtre de l’explorateur Outlook. Vous pouvez également personnaliser des affichages intégrés par programmation. Le tableau suivant répertorie des objets qui représentent des affichages Outlook. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom d’objet</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/bb646315(v=office.15)">BusinessCardView</a></p></td>
<td><p>Les données sont affichées comme une série d’images de cartes de visite électroniques.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/bb622874(v=office.15)">CalendarView</a></p></td>
<td><p>Les données sont affichées sous la forme d’un calendrier.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/bb609216(v=office.15)">CardView</a></p></td>
<td><p>Les données sont affichées dans une série de cartes.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/bb612031(v=office.15)">IconView</a></p></td>
<td><p>Les données sont affichées sous la forme d’icônes de dossier Windows ou d’icônes d’explorateur.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/bb608854(v=office.15)">TableView</a></p></td>
<td><p>Les données sont affichées dans un tableau simple contenant des champs.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/bb609455(v=office.15)">TimelineView</a></p></td>
<td><p>Les données sont affichées selon une chronologie linéaire personnalisable.</p></td>
</tr>
</tbody>
</table>


Vous pouvez accéder aux propriétés et aux méthodes communes à tous les affichages en utilisant l’objet [View](https://msdn.microsoft.com/library/bb647396\(v=office.15\)). Cependant, pour accéder à certaines propriétés qui ne sont pas communes à tous les affichages, vous devez caster l'objet **View** à un objet **View** dérivé ayant la propriété à laquelle vous voulez accéder. Par exemple, pour accéder à la propriété [HeadingsFont](https://msdn.microsoft.com/library/bb612522\(v=office.15\)) de l'objet **Cardview**, castez l'objet **View** en l'objet **CardView**. Si vous voulez déterminer quel type d’affichage est représenté par un objet **View** spécifique, utilisez la propriété [ViewType](https://msdn.microsoft.com/library/bb623693\(v=office.15\)).

Pour créer un nouvel affichage, utilisez la méthode **Add** de la collection **Views** pour un objet **Folder**. Définissez ensuite la visibilité de l’affichage, soit au moment de la création ou à tout moment après la création de l’affichage. Pour définir la visibilité de l'affichage au moment de la création, spécifiez une constante [OlViewSaveOption](https://msdn.microsoft.com/library/bb647502\(v=office.15\)) dans le paramètre *SaveOption* de la méthode **Add**. Pour définir la visibilité après la création de l'affichage, spécifiez une constante **OlViewSaveOption** pour la propriété [SaveOption](https://msdn.microsoft.com/library/bb646426\(v=office.15\)) de l'objet **View**. 

L'ajout d'un nouvel affichage déclenche l'événement [ViewAdd](https://msdn.microsoft.com/library/bb647550\(v=office.15\)) de la collection **Views**. Une fois l'affichage créé, personnalisez-le par programmation en castant l'objet **View** à l'un des objets dérivés, puis en effectuant les modifications nécessaires. Utilisez la méthode **Save** de l'objet **View** dérivé ou de l'objet **View** pour enregistrer les éventuelles modifications apportées à l'affichage. Enfin, utilisez la méthode **Apply** de l'objet **View** dérivé ou de l'objet **View** pour appliquer l'affichage à l'objet [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) actuel. Cela déclenche l’événement [ViewSwitch](https://msdn.microsoft.com/library/bb644066\(v=office.15\)) de l’objet **Explorer**.

Dans l'exemple de code suivant, CreateMeetingRequestsView ajoute un nouvel affichage nommé « Meeting Requests » à la Boîte de réception de l'utilisateur en castant l'objet **View** en un objet **TableView**. CreateMeetingRequestsView appelle ensuite la méthode **Add** de l'objet **Views** avec le paramètre *Name* défini comme « Meeting Requests » et le paramètre *ViewType* défini comme **olTableView**. La propriété [Filter](https://msdn.microsoft.com/library/bb610296\(v=office.15\)) de l'objet **TableView** est définie comme une chaîne DASL qui provoque l'affichage de la vue uniquement lorsque figurent des éléments qui contiennent « IPM.Schedule » dans la classe message de l'élément. Le nouvel affichage est ensuite enregistré et appliqué.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d'abord ajouter une référence au composant Bibliothèque d'objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l'espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l'importation et la tâche dans C\#.

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

## <a name="see-also"></a>Voir aussi

- [Affichages](views.md)

