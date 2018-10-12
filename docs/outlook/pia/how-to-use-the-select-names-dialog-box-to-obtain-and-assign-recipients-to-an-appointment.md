---
title: Utiliser la boîte de dialogue Sélectionner des noms pour obtenir et attribuer des destinataires à un rendez-vous
TOCTitle: Use the Select Names dialog box to obtain and assign recipients to an appointment
ms:assetid: b9bcb341-1912-425c-8d75-ed5be233145a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184636(v=office.15)
ms:contentKeyID: 55119878
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 57a7c99efa2bd82e1bc3d3f0855a90b62109719c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407001"
---
# <a name="use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment"></a>Utiliser la boîte de dialogue Sélectionner des noms pour obtenir et attribuer des destinataires à un rendez-vous

Cet exemple montre comment utiliser la boîte de dialogue **Sélectionner des noms** pour obtenir et affecter des destinataires à un élément de rendez-vous.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Pour afficher la boîte de dialogue **Sélectionner des noms**, appelez la méthode [Display()](https://msdn.microsoft.com/library/bb646086\(v=office.15\)) de l'objet [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) . Une fois la boîte de dialogue **Sélectionner des noms** affichée à l'utilisateur, l'exécution du code s'arrête jusqu'à ce que l'utilisateur clique sur **OK** ou ferme la boîte de dialogue. Pour définir les destinataires initiaux à afficher dans la boîte de dialogue, ou pour obtenir les destinataires sélectionnés dans la boîte de dialogue, utilisez la propriété [Recipients](https://msdn.microsoft.com/library/bb652601\(v=office.15\)) de l'objet **SelectNamesDialog**. Une collection [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) associée à l'objet **SelectNamesDialog** est alors retournée. Pour ajouter un objet [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) à la collection **Recipients** de l'objet **SelectNamesDialog**, utilisez la méthode [Add](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) de la collection et spécifiez la propriété [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) de l'objet **Recipient**.

Dans l’exemple de code suivant, DemoSelectNamesDialogRecipients crée un objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) et définit certaines de ses propriétés. Il crée ensuite un objet **SelectNamesDialog** et utilise la méthode [SetDefaultDisplayMode(OlDefaultSelectNamesDisplayMode)](https://msdn.microsoft.com/library/bb623783\(v=office.15\)) pour définir le mode d'affichage des réunions dans la boîte de dialogue **Sélectionner des noms**. L'exemple remplit le sélecteur de destinataires **Resource** avec la chaîne « Conf Room 36/2739 ». Une fois la boîte de dialogue affichée à l'utilisateur, le code énumère la collection **Recipients** qui est associée à cette instance de l'objet **SelectNamesDialog** et ajoute ces destinataires au rendez-vous qui a été créé. Enfin, l’exemple affiche la demande de réunion à l’utilisateur.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.

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

## <a name="see-also"></a>Voir aussi

- [Destinataires](recipients.md)

