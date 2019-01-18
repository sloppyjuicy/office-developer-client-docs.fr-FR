---
title: Utiliser la boîte de dialogue Sélectionner des noms pour obtenir et attribuer des destinataires à un rendez-vous
TOCTitle: Use the Select Names dialog box to obtain and assign recipients to an appointment
ms:assetid: b9bcb341-1912-425c-8d75-ed5be233145a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184636(v=office.15)
ms:contentKeyID: 55119878
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 408d2fbdc3c89b7f2bad1fe9c2c76c1f47ae05ff
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722766"
---
# <a name="use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment"></a><span data-ttu-id="1ac4f-102">Utiliser la boîte de dialogue Sélectionner des noms pour obtenir et attribuer des destinataires à un rendez-vous</span><span class="sxs-lookup"><span data-stu-id="1ac4f-102">Use the Select Names dialog box to obtain and assign recipients to an appointment</span></span>

<span data-ttu-id="1ac4f-103">Cet exemple montre comment utiliser la boîte de dialogue **Sélectionner des noms** pour obtenir et affecter des destinataires à un élément de rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="1ac4f-103">This example shows how to use the **Select Names** dialog box to obtain and assign recipients to an appointment item.</span></span>

## <a name="example"></a><span data-ttu-id="1ac4f-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="1ac4f-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="1ac4f-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="1ac4f-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="1ac4f-p101">Pour afficher la boîte de dialogue **Sélectionner des noms**, appelez la méthode [Display()](https://msdn.microsoft.com/library/bb646086\(v=office.15\)) de l'objet [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) . Une fois la boîte de dialogue **Sélectionner des noms** affichée à l'utilisateur, l'exécution du code s'arrête jusqu'à ce que l'utilisateur clique sur **OK** ou ferme la boîte de dialogue. Pour définir les destinataires initiaux à afficher dans la boîte de dialogue, ou pour obtenir les destinataires sélectionnés dans la boîte de dialogue, utilisez la propriété [Recipients](https://msdn.microsoft.com/library/bb652601\(v=office.15\)) de l'objet **SelectNamesDialog**. Une collection [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) associée à l'objet **SelectNamesDialog** est alors retournée. Pour ajouter un objet [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) à la collection **Recipients** de l'objet **SelectNamesDialog**, utilisez la méthode [Add](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) de la collection et spécifiez la propriété [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) de l'objet **Recipient**.</span><span class="sxs-lookup"><span data-stu-id="1ac4f-p101">To display the **Select Names** dialog box, call the [Display()](https://msdn.microsoft.com/library/bb646086\(v=office.15\)) method of the [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) object. Once the **Select Names** dialog box is displayed to the user, code execution halts until the user clicks **OK** or closes the dialog box. To set initial recipients to display in the dialog box, or to get the recipients selected in the dialog box, use the [Recipients](https://msdn.microsoft.com/library/bb652601\(v=office.15\)) property of the **SelectNamesDialog** object. This returns a [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection that is associated with the **SelectNamesDialog**. To add a [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object to the **Recipients** collection for the **SelectNamesDialog**, use the [Add](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) method for the collection and specify the [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) property of the **Recipient** object.</span></span>

<span data-ttu-id="1ac4f-111">Dans l’exemple de code suivant, DemoSelectNamesDialogRecipients crée un objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) et définit certaines de ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="1ac4f-111">In the following code example, DemoSelectNamesDialogRecipients creates an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object and sets some of its properties.</span></span> <span data-ttu-id="1ac4f-112">Il crée ensuite un objet **SelectNamesDialog** et utilise la méthode [SetDefaultDisplayMode(OlDefaultSelectNamesDisplayMode)](https://msdn.microsoft.com/library/bb623783\(v=office.15\)) pour définir le mode d'affichage des réunions dans la boîte de dialogue **Sélectionner des noms**.</span><span class="sxs-lookup"><span data-stu-id="1ac4f-112">It then creates a **SelectNamesDialog** and uses the [SetDefaultDisplayMode(OlDefaultSelectNamesDisplayMode)](https://msdn.microsoft.com/library/bb623783\(v=office.15\)) method to set a meeting display mode for the **Select Names** dialog box.</span></span> <span data-ttu-id="1ac4f-113">L'exemple remplit le sélecteur de destinataires **Resource** avec la chaîne « Conf Room 36/2739 ».</span><span class="sxs-lookup"><span data-stu-id="1ac4f-113">The example populates the **Resource** recipient selector with the string "Conf Room 36/2739".</span></span> <span data-ttu-id="1ac4f-114">Une fois la boîte de dialogue affichée à l'utilisateur, le code énumère la collection **Recipients** qui est associée à cette instance de l'objet **SelectNamesDialog** et ajoute ces destinataires au rendez-vous qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="1ac4f-114">Once the dialog box is displayed to the user, the code enumerates the **Recipients** collection that is associated with this instance of **SelectNamesDialog** and adds those recipients to the appointment that was created.</span></span> <span data-ttu-id="1ac4f-115">Enfin, l’exemple affiche la demande de réunion à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1ac4f-115">Finally, the example displays the meeting request to the user.</span></span>

<span data-ttu-id="1ac4f-116">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="1ac4f-116">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="1ac4f-117">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="1ac4f-117">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="1ac4f-118">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="1ac4f-118">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoSelectNamesDialogRecipients()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.MeetingStatus = Outlook.OlMeetingStatus.olMeeting;
    appt.Subject = "Team Morale Event";
    appt.Start = DateTime.Parse("5/17/2007 11:00 AM");
    appt.End = DateTime.Parse("5/17/2007 12:00 PM");
    Outlook.SelectNamesDialog snd =
        Application.Session.GetSelectNamesDialog();
    snd.SetDefaultDisplayMode(
        Outlook.OlDefaultSelectNamesDisplayMode.olDefaultMeeting);
    Outlook.Recipient confRoom =
        snd.Recipients.Add("Conf Room 36/2739");
    // Explicitly specify Recipient.Type.
    confRoom.Type = (int)Outlook.OlMeetingRecipientType.olResource;
    snd.Recipients.ResolveAll();
    snd.Display();
    // Add Recipients to meeting request.
    Outlook.Recipients recips = snd.Recipients;
    if (recips.Count > 0)
    {
        foreach (Outlook.Recipient recip in recips)
        {
            appt.Recipients.Add(recip.Name);
        }
    }
    appt.Recipients.ResolveAll();
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="1ac4f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ac4f-119">See also</span></span>

- [<span data-ttu-id="1ac4f-120">Destinataires</span><span class="sxs-lookup"><span data-stu-id="1ac4f-120">Recipients</span></span>](recipients.md)

