---
title: Création d’un rendez-vous exceptionnel dans une série de rendez-vous périodiques
TOCTitle: Create an exception appointment in a recurring appointment series
ms:assetid: b7cd0975-4f44-453a-b878-ec55feeedc4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184635(v=office.15)
ms:contentKeyID: 55119813
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70e491069fd3f178371e9e8e3e6bcd8dc08e729e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356433"
---
# <a name="create-an-exception-appointment-in-a-recurring-appointment-series"></a><span data-ttu-id="e68cc-102">Création d’un rendez-vous exceptionnel dans une série de rendez-vous périodiques</span><span class="sxs-lookup"><span data-stu-id="e68cc-102">Create an exception appointment in a recurring appointment series</span></span>

<span data-ttu-id="e68cc-103">Cet exemple utilise un objet [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) pour créer une exception à la périodicité standard d’un rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="e68cc-103">This example uses an [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) object to create an exception to a standard recurrence pattern for an appointment.</span></span>

## <a name="example"></a><span data-ttu-id="e68cc-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="e68cc-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="e68cc-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="e68cc-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="e68cc-106">Quand vous supprimez ou modifiez une instance d’un rendez-vous périodique, Outlook crée un objet [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="e68cc-106">Once you delete or change one appointment instance of a recurring appointment, Outlook creates an [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) object.</span></span> <span data-ttu-id="e68cc-107">L’objet Exception vous permet de créer une exception selon une périodicité standard.</span><span class="sxs-lookup"><span data-stu-id="e68cc-107">The Exception object allows you to create an exception to a standard recurrence pattern.</span></span> <span data-ttu-id="e68cc-108">Les propriétés de l’objet contiennent les modifications apportées à l’instance de rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="e68cc-108">The object’s properties contain the changes that were made to the appointment instance.</span></span> <span data-ttu-id="e68cc-109">La collection [Exceptions](https://msdn.microsoft.com/library/bb647601\(v=office.15\)) contient tous les objets Exception d’un rendez-vous périodique et est associée avec l’objet [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) du rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="e68cc-109">The [Exceptions](https://msdn.microsoft.com/library/bb647601\(v=office.15\)) collection contains all of the Exception objects for a recurring appointment, and is associated with the appointment’s [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span>

<span data-ttu-id="e68cc-110">Pour obtenir l’objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) représentant l’exception à la périodicité d’origine du rendez-vous périodique, utilisez la propriété [AppointmentItem](https://msdn.microsoft.com/library/bb645648\(v=office.15\)) de l’objet Exception.</span><span class="sxs-lookup"><span data-stu-id="e68cc-110">To get the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object that represents the exception to the original recurrence pattern of the recurring appointment, use the [AppointmentItem](https://msdn.microsoft.com/library/bb645648\(v=office.15\)) property of the Exception.</span></span> <span data-ttu-id="e68cc-111">En utilisant les méthodes et les propriétés de la propriété AppointmentItem renvoyée, vous pouvez définir les propriétés de l’exception de rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="e68cc-111">By using the methods and properties of the returned AppointmentItem, you can set the properties of the appointment exception.</span></span>

<span data-ttu-id="e68cc-112">Lorsque vous travaillez avec des éléments de rendez-vous périodiques, vous devez libérer les références antérieures, obtenir de nouvelles références à l'élément de rendez-vous périodique avant d'accéder à l'élément ou de le modifier, et libérer ces références dès que vous avez terminé et enregistré les modifications.</span><span class="sxs-lookup"><span data-stu-id="e68cc-112">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="e68cc-113">Cette pratique s’applique à l’objet **AppointmentItem** périodique, ainsi qu’aux objets [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) ou [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="e68cc-113">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="e68cc-114">Pour publier une référence dans Visual Basic, définissez cet objet existant sur Rien.</span><span class="sxs-lookup"><span data-stu-id="e68cc-114">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="e68cc-115">Dans C\#, libérez explicitement la mémoire pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="e68cc-115">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="e68cc-p104">Notez que même après avoir libéré votre référence et tenté d’obtenir une nouvelle référence, s’il existe encore une référence active détenue par un autre complément ou par Outlook vers un des objets mentionnés ci-dessus, votre nouvelle référence pointera encore vers une copie périmée de l’objet. Il est donc important de libérer vos références dès que vous en avez terminé avec le rendez-vous périodique.</span><span class="sxs-lookup"><span data-stu-id="e68cc-p104">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference, held by another add-in or Outlook, to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="e68cc-118">Dans l’exemple de code suivant, CreateExceptionExample change l’objet du rendez-vous périodique créé dans la rubrique [Trouver un rendez-vous spécifique dans une série de rendez-vous périodiques](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md), puis utilise la propriété AppointmentItem de l’objet Exception résultant pour récupérer l’objet AppointmentItem qui correspond à l’exception de rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="e68cc-118">In the following code example, CreateExceptionExample changes the subject of the recurring appointment that was created in the topic [Find a Specific Appointment in a Recurring Appointment Series](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md), and then uses the AppointmentItem property of the resulting Exception object to retrieve the AppointmentItem that corresponds to the appointment exception.</span></span> <span data-ttu-id="e68cc-119">CreateExceptionExample modifie ensuite les heures de début et de fin de l’exception de rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="e68cc-119">CreateExceptionExample then changes the start and end times of the appointment exception.</span></span>

<span data-ttu-id="e68cc-120">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="e68cc-120">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="e68cc-121">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="e68cc-121">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="e68cc-122">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="e68cc-122">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="e68cc-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e68cc-123">See also</span></span>

- [<span data-ttu-id="e68cc-124">Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="e68cc-124">Appointments</span></span>](appointments.md)

