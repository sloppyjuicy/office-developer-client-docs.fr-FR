---
title: Création d’un rendez-vous périodique selon une périodicité hebdomadaire
TOCTitle: Create a recurring appointment that has a weekly pattern
ms:assetid: 20b46b26-e278-451b-9e35-36683205d164
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184595(v=office.15)
ms:contentKeyID: 55119810
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c233a9641ff47409e885caa4387f6e632345678a
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63631777"
---
# <a name="create-a-recurring-appointment-that-has-a-weekly-pattern"></a>Création d’un rendez-vous périodique selon une périodicité hebdomadaire

Cet exemple explique comment créer un rendez-vous périodique ayant un modèle hebdomadaire (par exemple, il se produit tous les lundis, mercredis et vendredis.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Lorsque vous créez un rendez-vous périodique, la périodicité est basée sur l’heure que vous spécifiez lorsque vous créez le rendez-vous. Par exemple, si vous créez à 13h00 un rendez-vous qui se répète tous les jours, il se produit seulement à 13h00 quotidiennement. Pour changer la périodicité d’un rendez-vous, définissez les propriétés de l’objet [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) du rendez-vous. Définissez la propriété [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) de l’objet RecurrencePattern avant de définir d’autres propriétés RecurrencePattern. Le tableau suivant indique les propriétés RecurrencePattern valides pour un RecurrenceType donné (spécifié par l’énumération [OlRecurrenceType](https://msdn.microsoft.com/library/bb647129\(v=office.15\))).

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Valeur OlRecurrenceType</p></th>
<th><p>Propriétés RecurrencePattern valides</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>olRecursDaily</p></td>
<td><p><a href="https://msdn.microsoft.com/library/bb644889(v=office.15)">Duration</a>, <a href="https://msdn.microsoft.com/library/bb644544(v=office.15)">EndTime</a>, <a href="https://msdn.microsoft.com/library/bb624287(v=office.15)">Interval</a>, <a href="https://msdn.microsoft.com/library/bb646849(v=office.15)">NoEndDate</a>, <a href="https://msdn.microsoft.com/library/bb611303(v=office.15)">Occurrences</a>, <a href="https://msdn.microsoft.com/library/bb624492(v=office.15)">PatternStartDate</a>, <a href="https://msdn.microsoft.com/library/bb609279(v=office.15)">PatternEndDate</a>, <a href="https://msdn.microsoft.com/library/bb646324(v=office.15)">StartTime</a></p></td>
</tr>
<tr class="even">
<td><p>olRecursWeekly</p></td>
<td><p><a href="https://msdn.microsoft.com/library/bb609163(v=office.15)">DayOfWeekMask</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</p></td>
</tr>
<tr class="odd">
<td><p>olRecursMonthly</p></td>
<td><p><a href="https://msdn.microsoft.com/library/bb622604(v=office.15)">DayOfMonth</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</p></td>
</tr>
<tr class="even">
<td><p>olRecursMonthNth</p></td>
<td><p>DayOfWeekMask, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb645269(v=office.15)">Instance</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</p></td>
</tr>
<tr class="odd">
<td><p>olRecursYearly</p></td>
<td><p>DayOfMonth, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb610515(v=office.15)">MonthOfYear</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</p></td>
</tr>
<tr class="even">
<td><p>olRecursYearNth</p></td>
<td><p>DayOfWeekMask, Duration, EndTime, Interval, Instance, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</p></td>
</tr>
</tbody>
</table>


Lorsque vous travaillez avec des éléments de rendez-vous périodiques, vous devez libérer les références antérieures, obtenir de nouvelles références à l'élément de rendez-vous périodique avant d'accéder à l'élément ou de le modifier, et libérer ces références dès que vous avez terminé et enregistré les modifications. Cette pratique s’applique à l’objet **AppointmentItem** périodique, ainsi qu’aux objets [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) ou [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Pour publier une référence dans Visual Basic, définissez cet objet existant sur Rien. Dans C\#, libérez explicitement la mémoire pour cet objet.

Notez que même après la libération de votre référence et la tentative d'obtention d'une nouvelle référence, s'il y a toujours une référence active (détenue par un autre complément ou Outlook) à l'un des objets ci-dessus, la nouvelle référence pointera toujours vers une copie obsolète de l'objet. Par conséquent, il est important que vous libériez vos références dès que vous avez terminé le rendez-vous périodique.

Dans l’exemple de code suivant, RecurringAppointmentEveryMondayWednesdayFriday crée un objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), puis appelle [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) pour obtenir l’objet RecurrencePattern du rendez-vous nouvellement créé. RecurringAppointmentEveryMondayWednesdayFriday définit ensuite les propriétés RecurrenceType, DayOfWeekMask, PatternStartDate, PatternEndDate, Duration, StartTime, EndTime et Subject, enregistre le rendez-vous, puis l’affiche selon le schéma « A lieu tous les lundis, mercredis et vendredis à compter du 10/07/2006 jusqu’au 25/08/2006 de 14:00 à 15:00 ».

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d'objets Microsoft Outlook 15.0 et spécifier la variable Outlook lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration Class publique. La ligne de code suivante montre comment effectuer l’importation et l’affectation dans C \#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void RecurringAppointmentEveryMondayWednesdayFriday()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Recurring Appointment DaysOfWeekMask Example";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    pattern.RecurrenceType = Outlook.OlRecurrenceType.olRecursWeekly;
    // Logical OR for DayOfWeekMask creates pattern
    pattern.DayOfWeekMask = Outlook.OlDaysOfWeek.olMonday |
        Outlook.OlDaysOfWeek.olWednesday |
        Outlook.OlDaysOfWeek.olFriday;
    pattern.PatternStartDate = DateTime.Parse("7/10/2006");
    pattern.PatternEndDate = DateTime.Parse("8/25/2006");
    pattern.Duration = 60;
    pattern.StartTime = DateTime.Parse("2:00:00 PM");
    pattern.EndTime = DateTime.Parse("3:00:00 PM");
    appt.Save();
    appt.Display(false);
}
```

## <a name="see-also"></a>Voir aussi

- [Rendez-vous](appointments.md)

