---
title: Création d’un rendez-vous sur toute la journée
TOCTitle: Create an appointment that is an all-day event
ms:assetid: a0d3baeb-6ed5-41b6-bef5-d6c1bb56fee3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184629(v=office.15)
ms:contentKeyID: 55119806
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5065395afe39247f8113bc5223b0e3e403a02fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349475"
---
# <a name="create-an-appointment-that-is-an-all-day-event"></a><span data-ttu-id="d1de0-102">Création d’un rendez-vous sur toute la journée</span><span class="sxs-lookup"><span data-stu-id="d1de0-102">Create an appointment that is an all-day event</span></span>

<span data-ttu-id="d1de0-103">Cet exemple montre comment utiliser la propriété [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) pour créer un rendez-vous qui est un événement planifié sur une journée entière.</span><span class="sxs-lookup"><span data-stu-id="d1de0-103">This example shows how use the [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) property to create an appointment that is an all-day event.</span></span>

## <a name="example"></a><span data-ttu-id="d1de0-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="d1de0-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="d1de0-105">L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="d1de0-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="d1de0-p101">Un événement est différent d’un rendez-vous normal car il s’agit d’une activité qui dure 24 heures ou plus. Les salons, les séminaires ou les vacances sont des exemples d’événements. Les événements et les événements annuels n’apparaissent pas comme des blocs de temps occupés dans le calendrier de l’utilisateur, mais sous la forme de bannières. Les bannières sont représentées en haut de l’affichage quotidien ou hebdomadaire d’un calendrier. Par défaut, le temps de l’utilisateur est affiché aux autres utilisateurs comme occupé pour un rendez-vous d’une journée entière, mais comme libre pour un événement ou un événement annuel.</span><span class="sxs-lookup"><span data-stu-id="d1de0-p101">An event is different from a regular appointment because it is an activity that lasts 24 hours or longer. Examples of events include trade shows, seminars, or vacations. Events and annual events do not appear as occupied blocks of time in the user’s calendar. Instead, they appear as banners. You can see the banners at the top of a calendar day or week view. For an all-day appointment, by default, the user’s time is displayed as busy when viewed by other people, but the user’s time is displayed as free for an event or annual event.</span></span>

<span data-ttu-id="d1de0-112">Pour créer par programme un événement d’une journée entière, définissez la propriété [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) de l’objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) sur True.</span><span class="sxs-lookup"><span data-stu-id="d1de0-112">To create an all-day event programmatically, set the [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) property of the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object to true.</span></span> <span data-ttu-id="d1de0-113">Définissez ensuite les propriétés [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) et [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) de l’objet AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="d1de0-113">Then set the [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) and [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) properties of the AppointmentItem.</span></span> <span data-ttu-id="d1de0-114">Si vous définissez la propriété AllDayEvent sur true et ne définissez pas les propriétés Start et End, l'événement se produira aujourd'hui et sera un rendez-vous avec le statut occupé sur votre calendrier.</span><span class="sxs-lookup"><span data-stu-id="d1de0-114">If you set the AllDayEvent property to true and do not set the Start and End properties, the event will occur today, and it will be an appointment, showing a busy status on your calendar.</span></span> <span data-ttu-id="d1de0-115">Vous devez définir les propriétés Start et End si vous souhaitez que l’événement se produise à une date ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d1de0-115">You must set the Start and End properties if you want the event to occur on a future date.</span></span>

> [!NOTE]
> <span data-ttu-id="d1de0-116">Pour que le rendez-vous soit un événement planifié sur une journée entière, vous devez définir la propriété Start sur 00:00:00</span><span class="sxs-lookup"><span data-stu-id="d1de0-116">To make the appointment an all-day event, you must set the Start property to 12:00 A.M.</span></span> <span data-ttu-id="d1de0-117">(minuit) le jour où vous souhaitez que l’événement commence, et définir la propriété End sur 00:00:00</span><span class="sxs-lookup"><span data-stu-id="d1de0-117">(midnight) on the day you want the event to begin, and set End property to 12:00 A.M.</span></span> <span data-ttu-id="d1de0-118">le jour qui suit le jour de fin de l’événement.</span><span class="sxs-lookup"><span data-stu-id="d1de0-118">on the day after you want the event to end.</span></span> <span data-ttu-id="d1de0-119">Si vous définissez l’heure de début ou de fin sur une valeur autre que 00:00:00, le rendez-vous deviendra un rendez-vous planifié sur plusieurs jours plutôt qu’un événement planifié sur une journée entière.</span><span class="sxs-lookup"><span data-stu-id="d1de0-119">If you set the Start or End time to a date and time value other than 12:00 A.M., the appointment will become a multiday appointment instead of an all-day event.</span></span> 
>
> <span data-ttu-id="d1de0-120">Par exemple, si la durée de votre événement est d’un jour seulement, définissez la propriété Start sur 00:00:00.</span><span class="sxs-lookup"><span data-stu-id="d1de0-120">For example, if your event duration is only one day, set the Start property to 12:00 A.M.</span></span> <span data-ttu-id="d1de0-121">le jour où vous souhaitez que l’événement commence, et définissez la propriété End sur 00:00:00</span><span class="sxs-lookup"><span data-stu-id="d1de0-121">on the day you want the event to begin, and set the End property to 12:00 A.M.</span></span> <span data-ttu-id="d1de0-122">le jour suivant.</span><span class="sxs-lookup"><span data-stu-id="d1de0-122">on the following day.</span></span> <span data-ttu-id="d1de0-123">Vous devez toujours définir la propriété End sur 00:00:00</span><span class="sxs-lookup"><span data-stu-id="d1de0-123">You should always set the End property to 12:00 A.M.</span></span> <span data-ttu-id="d1de0-124">à une date postérieure au lendemain de la date de début.</span><span class="sxs-lookup"><span data-stu-id="d1de0-124">on a date that is more than one day after the start date.</span></span>

<span data-ttu-id="d1de0-p105">Dans l’exemple de code suivant, AllDayEventExample crée un événement d’une journée entière qui commence le 11 juin 2007 et se termine le 15 juin 2007. Notez que la propriété End du rendez-vous est définie sur 00h00, le 16 juin 2007.</span><span class="sxs-lookup"><span data-stu-id="d1de0-p105">In the following code example, AllDayEventExample creates an all-day event that begins on June 11, 2007, and ends on June 15, 2007. Note that the End property for the appointment is set to 12:00 A.M. on June 16, 2007.</span></span>

<span data-ttu-id="d1de0-128">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="d1de0-128">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="d1de0-129">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="d1de0-129">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="d1de0-130">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="d1de0-130">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void AllDayEventExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Developer's Conference";
    appt.AllDayEvent = true;
    appt.Start = DateTime.Parse("6/11/2007 12:00 AM");
    appt.End = DateTime.Parse("6/16/2007 12:00 AM");
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="d1de0-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1de0-131">See also</span></span>

- [<span data-ttu-id="d1de0-132">Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="d1de0-132">Appointments</span></span>](appointments.md)

