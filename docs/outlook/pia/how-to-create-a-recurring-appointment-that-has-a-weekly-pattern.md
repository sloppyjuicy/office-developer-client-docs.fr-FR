---
title: Création d’un rendez-vous périodique selon une périodicité hebdomadaire
TOCTitle: Create a recurring appointment that has a weekly pattern
ms:assetid: 20b46b26-e278-451b-9e35-36683205d164
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184595(v=office.15)
ms:contentKeyID: 55119810
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b326ad23f8cbe47e5141775eacdd2bc9302db3cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359170"
---
# <a name="create-a-recurring-appointment-that-has-a-weekly-pattern"></a><span data-ttu-id="241da-102">Création d’un rendez-vous périodique selon une périodicité hebdomadaire</span><span class="sxs-lookup"><span data-stu-id="241da-102">Create a recurring appointment that has a weekly pattern</span></span>

<span data-ttu-id="241da-103">Cet exemple explique comment créer un rendez-vous périodique ayant un modèle hebdomadaire (par exemple, il se produit tous les lundis, mercredis et vendredis.</span><span class="sxs-lookup"><span data-stu-id="241da-103">This example shows how to create a recurring appointment that has a weekly pattern (for example, an appointment that occurs every Monday, Wednesday, and Friday).</span></span>

## <a name="example"></a><span data-ttu-id="241da-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="241da-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="241da-105">L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="241da-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="241da-106">Lorsque vous créez un rendez-vous périodique, la périodicité est basée sur l’heure que vous spécifiez lorsque vous créez le rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="241da-106">When you create a new recurring appointment, the recurrence pattern is based on the time you specify when you create the appointment.</span></span> <span data-ttu-id="241da-107">Par exemple, si vous créez à 13h00 un rendez-vous qui se répète tous les jours, il se produit seulement à 13h00 quotidiennement.</span><span class="sxs-lookup"><span data-stu-id="241da-107">For example, if you create an appointment that recurs daily at 1:00 PM, the appointment will recur only at 1:00 PM on a daily basis.</span></span> <span data-ttu-id="241da-108">Pour changer la périodicité d’un rendez-vous, définissez les propriétés de l’objet [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) du rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="241da-108">To change the recurrence pattern of an appointment, set the properties of the appointment’s [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="241da-109">Définissez la propriété [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) de l’objet RecurrencePattern avant de définir d’autres propriétés RecurrencePattern.</span><span class="sxs-lookup"><span data-stu-id="241da-109">Set the [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) property of the RecurrencePattern object before setting other RecurrencePattern properties.</span></span> <span data-ttu-id="241da-110">Le tableau suivant indique les propriétés RecurrencePattern valides pour un RecurrenceType donné (spécifié par l’énumération [OlRecurrenceType](https://msdn.microsoft.com/library/bb647129\(v=office.15\))).</span><span class="sxs-lookup"><span data-stu-id="241da-110">The following table shows valid RecurrencePattern properties for a given RecurrenceType (specified by the [OlRecurrenceType](https://msdn.microsoft.com/library/bb647129\(v=office.15\)) enumeration).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="241da-111">Valeur OlRecurrenceType</span><span class="sxs-lookup"><span data-stu-id="241da-111">OlRecurrenceType value</span></span></p></th>
<th><p><span data-ttu-id="241da-112">Propriétés RecurrencePattern valides</span><span class="sxs-lookup"><span data-stu-id="241da-112">Valid RecurrencePattern properties</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="241da-113">olRecursDaily</span><span class="sxs-lookup"><span data-stu-id="241da-113">olRecursDaily</span></span></p></td>
<td><p><span data-ttu-id="241da-114"><a href="https://msdn.microsoft.com/library/bb644889(v=office.15)">Duration</a>, <a href="https://msdn.microsoft.com/library/bb644544(v=office.15)">EndTime</a>, <a href="https://msdn.microsoft.com/library/bb624287(v=office.15)">Interval</a>, <a href="https://msdn.microsoft.com/library/bb646849(v=office.15)">NoEndDate</a>, <a href="https://msdn.microsoft.com/library/bb611303(v=office.15)">Occurrences</a>, <a href="https://msdn.microsoft.com/library/bb624492(v=office.15)">PatternStartDate</a>, <a href="https://msdn.microsoft.com/library/bb609279(v=office.15)">PatternEndDate</a>, <a href="https://msdn.microsoft.com/library/bb646324(v=office.15)">StartTime</a></span><span class="sxs-lookup"><span data-stu-id="241da-114"><a href="https://msdn.microsoft.com/library/bb644889(v=office.15)">Duration</a>, <a href="https://msdn.microsoft.com/library/bb644544(v=office.15)">EndTime</a>, <a href="https://msdn.microsoft.com/library/bb624287(v=office.15)">Interval</a>, <a href="https://msdn.microsoft.com/library/bb646849(v=office.15)">NoEndDate</a>, <a href="https://msdn.microsoft.com/library/bb611303(v=office.15)">Occurrences</a>, <a href="https://msdn.microsoft.com/library/bb624492(v=office.15)">PatternStartDate</a>, <a href="https://msdn.microsoft.com/library/bb609279(v=office.15)">PatternEndDate</a>, <a href="https://msdn.microsoft.com/library/bb646324(v=office.15)">StartTime</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241da-115">olRecursWeekly</span><span class="sxs-lookup"><span data-stu-id="241da-115">olRecursWeekly</span></span></p></td>
<td><p><span data-ttu-id="241da-116"><a href="https://msdn.microsoft.com/library/bb609163(v=office.15)">DayOfWeekMask</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="241da-116"><a href="https://msdn.microsoft.com/library/bb609163(v=office.15)">DayOfWeekMask</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241da-117">olRecursMonthly</span><span class="sxs-lookup"><span data-stu-id="241da-117">olRecursMonthly</span></span></p></td>
<td><p><span data-ttu-id="241da-118"><a href="https://msdn.microsoft.com/library/bb622604(v=office.15)">DayOfMonth</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="241da-118"><a href="https://msdn.microsoft.com/library/bb622604(v=office.15)">DayOfMonth</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241da-119">olRecursMonthNth</span><span class="sxs-lookup"><span data-stu-id="241da-119">olRecursMonthNth</span></span></p></td>
<td><p><span data-ttu-id="241da-120">DayOfWeekMask, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb645269(v=office.15)">Instance</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="241da-120">DayOfWeekMask, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb645269(v=office.15)">Instance</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="241da-121">olRecursYearly</span><span class="sxs-lookup"><span data-stu-id="241da-121">olRecursYearly</span></span></p></td>
<td><p><span data-ttu-id="241da-122">DayOfMonth, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb610515(v=office.15)">MonthOfYear</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="241da-122">DayOfMonth, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb610515(v=office.15)">MonthOfYear</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="241da-123">olRecursYearNth</span><span class="sxs-lookup"><span data-stu-id="241da-123">olRecursYearNth</span></span></p></td>
<td><p><span data-ttu-id="241da-124">DayOfWeekMask, Duration, EndTime, Interval, Instance, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span><span class="sxs-lookup"><span data-stu-id="241da-124">DayOfWeekMask, Duration, EndTime, Interval, Instance, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="241da-125">Lorsque vous travaillez avec des éléments de rendez-vous périodiques, vous devez libérer les références antérieures, obtenir de nouvelles références à l'élément de rendez-vous périodique avant d'accéder à l'élément ou de le modifier, et libérer ces références dès que vous avez terminé et enregistré les modifications.</span><span class="sxs-lookup"><span data-stu-id="241da-125">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="241da-126">Cette pratique s’applique à l’objet **AppointmentItem** périodique, ainsi qu’aux objets [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) ou [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="241da-126">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="241da-127">Pour publier une référence dans Visual Basic, définissez cet objet existant sur Rien.</span><span class="sxs-lookup"><span data-stu-id="241da-127">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="241da-128">Dans C\#, libérez explicitement la mémoire pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="241da-128">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="241da-p103">Notez que même après la libération de votre référence et la tentative d'obtention d'une nouvelle référence, s'il y a toujours une référence active (détenue par un autre complément ou Outlook) à l'un des objets ci-dessus, la nouvelle référence pointera toujours vers une copie obsolète de l'objet. Par conséquent, il est important que vous libériez vos références dès que vous avez terminé le rendez-vous périodique.</span><span class="sxs-lookup"><span data-stu-id="241da-p103">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference (held by another add-in or Outlook) to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="241da-131">Dans l’exemple de code suivant, RecurringAppointmentEveryMondayWednesdayFriday crée un objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), puis appelle [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) pour obtenir l’objet RecurrencePattern du rendez-vous nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="241da-131">In the following code example, RecurringAppointmentEveryMondayWednesdayFriday creates an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object, and then calls [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) to get the newly created appointment’s RecurrencePattern object.</span></span> <span data-ttu-id="241da-132">RecurringAppointmentEveryMondayWednesdayFriday définit ensuite les propriétés RecurrenceType, DayOfWeekMask, PatternStartDate, PatternEndDate, Duration, StartTime, EndTime et Subject, enregistre le rendez-vous, puis l’affiche selon le schéma « A lieu tous les lundis, mercredis et vendredis à compter du 10/07/2006 jusqu’au 25/08/2006 de 14:00 à 15:00 ».</span><span class="sxs-lookup"><span data-stu-id="241da-132">RecurringAppointmentEveryMondayWednesdayFriday then sets the RecurrenceType, DayOfWeekMask, PatternStartDate, PatternEndDate, Duration, StartTime, EndTime, and Subject properties, saves the appointment, and finally displays the appointment with the pattern "Occurs every Monday, Wednesday, and Friday effective 7/10/2006 until 8/25/2006 from 2:00 PM to 3:00 PM."</span></span>

<span data-ttu-id="241da-133">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="241da-133">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="241da-134">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="241da-134">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="241da-135">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="241da-135">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="241da-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="241da-136">See also</span></span>

- [<span data-ttu-id="241da-137">Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="241da-137">Appointments</span></span>](appointments.md)

