---
title: Création d’un rendez-vous exceptionnel dans une série de rendez-vous périodiques
TOCTitle: Create an exception appointment in a recurring appointment series
ms:assetid: b7cd0975-4f44-453a-b878-ec55feeedc4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184635(v=office.15)
ms:contentKeyID: 55119813
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ed3936c5acef1d4dc9526588f7322ac759f5db25
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616368"
---
# <a name="create-an-exception-appointment-in-a-recurring-appointment-series"></a>Création d’un rendez-vous exceptionnel dans une série de rendez-vous périodiques

Cet exemple utilise un objet [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) pour créer une exception à la périodicité standard d’un rendez-vous.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Quand vous supprimez ou modifiez une instance d’un rendez-vous périodique, Outlook crée un objet [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)). L’objet Exception vous permet de créer une exception selon une périodicité standard. Les propriétés de l’objet contiennent les modifications apportées à l’instance de rendez-vous. La collection [Exceptions](https://msdn.microsoft.com/library/bb647601\(v=office.15\)) contient tous les objets Exception d’un rendez-vous périodique et est associée avec l’objet [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) du rendez-vous.

Pour obtenir l’objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) représentant l’exception à la périodicité d’origine du rendez-vous périodique, utilisez la propriété [AppointmentItem](https://msdn.microsoft.com/library/bb645648\(v=office.15\)) de l’objet Exception. En utilisant les méthodes et les propriétés de la propriété AppointmentItem renvoyée, vous pouvez définir les propriétés de l’exception de rendez-vous.

Lorsque vous travaillez avec des éléments de rendez-vous périodiques, vous devez libérer les références antérieures, obtenir de nouvelles références à l'élément de rendez-vous périodique avant d'accéder à l'élément ou de le modifier, et libérer ces références dès que vous avez terminé et enregistré les modifications. Cette pratique s’applique à l’objet **AppointmentItem** périodique, ainsi qu’aux objets [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) ou [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Pour publier une référence dans Visual Basic, définissez cet objet existant sur Rien. Dans C\#, libérez explicitement la mémoire pour cet objet.

Notez que même après avoir libéré votre référence et tenté d’obtenir une nouvelle référence, s’il existe encore une référence active détenue par un autre complément ou par Outlook vers un des objets mentionnés ci-dessus, votre nouvelle référence pointera encore vers une copie périmée de l’objet. Il est donc important de libérer vos références dès que vous en avez terminé avec le rendez-vous périodique.

Dans l’exemple de code suivant, CreateExceptionExample change l’objet du rendez-vous périodique créé dans la rubrique [Trouver un rendez-vous spécifique dans une série de rendez-vous périodiques](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md), puis utilise la propriété AppointmentItem de l’objet Exception résultant pour récupérer l’objet AppointmentItem qui correspond à l’exception de rendez-vous. CreateExceptionExample modifie ensuite les heures de début et de fin de l’exception de rendez-vous.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CreateExceptionExample()
{
    Outlook.AppointmentItem appt = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderCalendar).
        Items.Find(
        "[Subject]='Recurring Appointment DaysOfWeekMask Example'")
        as Outlook.AppointmentItem;
    if (appt != null)
    {
        try
        {
            Outlook.RecurrencePattern pattern =
                appt.GetRecurrencePattern();
            Outlook.AppointmentItem myInstance =
                pattern.GetOccurrence(DateTime.Parse(
                "7/21/2006 2:00 PM"))
                as Outlook.AppointmentItem;
            if (myInstance != null)
            {
                myInstance.Subject = "My Exception";
                myInstance.Save();
                Outlook.RecurrencePattern newPattern =
                    appt.GetRecurrencePattern();
                Outlook.Exception myException =
                    newPattern.Exceptions[1];
                if (myException != null)
                {
                    Outlook.AppointmentItem myNewInstance =
                        myException.AppointmentItem;
                    myNewInstance.Start =
                        DateTime.Parse("7/21/2006 1:00 PM");
                    myNewInstance.End =
                        DateTime.Parse("7/21/2006 2:00 PM");
                    myNewInstance.Save();
                }
            }
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Rendez-vous](appointments.md)

