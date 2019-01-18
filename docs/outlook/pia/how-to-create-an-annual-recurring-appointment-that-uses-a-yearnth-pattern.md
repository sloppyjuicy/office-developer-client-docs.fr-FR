---
title: Création d’un rendez-vous périodique annuel selon une périodicité toutes les n années
TOCTitle: Create an annual recurring appointment that uses a YearNth pattern
ms:assetid: 5fb2ad0b-248c-417d-8868-52e0550d970f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184611(v=office.15)
ms:contentKeyID: 55119811
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc50166674ee7b9699ef8e29c5ff1e54db705ad
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712154"
---
# <a name="create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern"></a>Création d’un rendez-vous périodique annuel selon une périodicité toutes les n années

Cet exemple montre comment créer un rendez-vous dont le modèle de périodicité annuelle est un jour spécifique comme le premier lundi de juin.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Si vous voulez créer un rendez-vous annuel qui se produit un jour spécifique de la semaine d'un mois particulier (par exemple, le premier lundi de juin), vous devez utiliser des périodicités YearNth. Pour définir une périodicité YearNth, vous devez d’abord définir la propriété [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) de l’objet [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) sur olRecursYearNth. Puis, vous définissez la propriété [DayOfWeekMask](https://msdn.microsoft.com/library/bb609163\(v=office.15\)) pour spécifier le jour de la semaine où le rendez-vous doit avoir lieu, et la propriété [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)) pour spécifier le numéro d'occurrence du jour de semaine spécifié (par exemple, le troisième jeudi) du mois spécifié pour la périodicité annuelle.

Lors de l'utilisation d'éléments de rendez-vous périodique, vous devez libérer les références antérieures, le cas échéant, obtenir les nouvelles références à l'élément de rendez-vous périodique avant d'accéder à cet élément ou de le modifier, et libérer ces références dès que vous avez terminé et enregistré les modifications. Cette pratique s’applique à l’objet **AppointmentItem** périodique, ainsi qu’à tous les objets [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) ou [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Pour publier une référence dans Visual Basic, définissez cet objet existant sur Rien. Dans C\#, libérez explicitement la mémoire pour cet objet.

Notez que même après la libération de votre référence et la tentative d'obtention d'une nouvelle référence, s'il y a toujours une référence active (détenue par un autre complément ou Outlook) à l'un des objets ci-dessus, la nouvelle référence pointera toujours vers une copie obsolète de l'objet. Par conséquent, il est important que vous libériez vos références dès que vous avez terminé le rendez-vous périodique.

Dans l’exemple de code suivant, RecurringYearNthAppointment crée un rendez-vous ayant un modèle de périodicité YearNth. RecurringYearNthAppointment crée d’abord un rendez-vous périodique en créant un objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)). Ensuite, il récupère le modèle de périodicité du rendez-vous en utilisant la méthode [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)). Il définit ensuite les propriétés RecurrencePattern suivantes : RecurrenceType, DayOfWeekMask, [MonthOfYear](https://msdn.microsoft.com/library/bb610515\(v=office.15\)), [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)), [Occurrences](https://msdn.microsoft.com/library/bb611303\(v=office.15\)), [Duration](https://msdn.microsoft.com/library/bb644889\(v=office.15\)), [PatternStartDate](https://msdn.microsoft.com/library/bb624492\(v=office.15\)), [StartTime](https://msdn.microsoft.com/library/bb646324\(v=office.15\)) et [EndTime](https://msdn.microsoft.com/library/bb644544\(v=office.15\)). La propriété MonthOfYear peut prendre une valeur numérique de 1 à 12, où chaque numéro représente le mois correspondant. Une fois les propriétés définies, RecurringYearNthAppointment enregistre le rendez-vous, puis l’affiche selon le schéma « A lieu le premier lundi de juin à compter du 01/06/2007 jusqu’au 06/06/2016 de 14:00 à 17:00 ».

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void RecurringYearNthAppointment()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Recurring YearNth Appointment";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    pattern.RecurrenceType = Outlook.OlRecurrenceType.olRecursYearNth;
    pattern.DayOfWeekMask = Outlook.OlDaysOfWeek.olMonday;
    pattern.MonthOfYear = 6;
    pattern.Instance = 1;
    pattern.Occurrences = 10;
    pattern.Duration = 180;
    pattern.PatternStartDate = DateTime.Parse("6/1/2007");
    pattern.StartTime = DateTime.Parse("2:00:00 PM");
    pattern.EndTime = DateTime.Parse("5:00:00 PM");
    appt.Save();
    appt.Display(false);
}
```

## <a name="see-also"></a>Voir aussi

- [Rendez-vous](appointments.md)

