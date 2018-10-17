---
title: Création d’un rappel pour un élément de rendez-vous
TOCTitle: Create a reminder for an appointment item
ms:assetid: 85e772f0-65ac-4abc-8286-9099882a2400
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184623(v=office.15)
ms:contentKeyID: 55119814
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 164e744e03ab0984265736673c71d2d0bf57bf45
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405972"
---
# <a name="create-a-reminder-for-an-appointment-item"></a><span data-ttu-id="8c5cf-102">Création d’un rappel pour un élément de rendez-vous</span><span class="sxs-lookup"><span data-stu-id="8c5cf-102">Create a reminder for an appointment item</span></span>

<span data-ttu-id="8c5cf-103">Cet exemple montre comment utiliser la propriété [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) pour créer un rappel pour un élément de rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-103">This example shows how to use the [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) property to create a reminder for an appointment item.</span></span>

## <a name="example"></a><span data-ttu-id="8c5cf-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="8c5cf-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="8c5cf-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="8c5cf-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="8c5cf-106">Outlook permet de définir facilement un rappel pour un rendez-vous à l’aide de la propriété [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) de l’objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="8c5cf-106">Microsoft Outlook provides a way to set a reminder for an appointment by using the [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) property of the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span> <span data-ttu-id="8c5cf-107">Cette propriété indique si un rappel a été créé pour le rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-107">This property indicates whether a reminder has been created for the appointment.</span></span> <span data-ttu-id="8c5cf-108">Le fait de définir la propriété ReminderSet sur true crée un rappel, et sa définition sur false supprime le rappel.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-108">Setting the ReminderSet property to true creates a reminder, and setting it to false removes the reminder.</span></span>

<span data-ttu-id="8c5cf-109">Dans l’exemple de code suivant, ReminderExample crée un rappel sur un rendez-vous privé pour une dégustation de vin à Napa, Californie et définit le rappel pour qu’il se déclenche deux heures avant le début du rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-109">In the following code example, ReminderExample creates a reminder on a private appointment for wine tasting in Napa, California, and sets the reminder to occur two hours before the appointment starts.</span></span> <span data-ttu-id="8c5cf-110">Tout d’abord, ReminderExample crée un objet **AppointmentItem** Outlook.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-110">First, ReminderExample creates an Outlook **AppointmentItem** object.</span></span> <span data-ttu-id="8c5cf-111">Il définit ensuite la propriété [sensibilité](https://msdn.microsoft.com/library/bb623503\(v=office.15\)) de l’élément sur [olPrivate](https://msdn.microsoft.com/library/bb645125\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="8c5cf-111">It then sets the [Sensitivity](https://msdn.microsoft.com/library/bb623503\(v=office.15\)) property for the item to [olPrivate](https://msdn.microsoft.com/library/bb645125\(v=office.15\)).</span></span> <span data-ttu-id="8c5cf-112">Ceci indique que le rendez-vous est un rendez-vous privé.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-112">This indicates that the appointment is a private appointment.</span></span> <span data-ttu-id="8c5cf-113">Une fois que les autres propriétés du rendez-vous sont définies, telles que les heures de [début](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) et de [fin](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), ReminderExample définit la propriété [ReminderMinutesBeforeStart](https://msdn.microsoft.com/library/bb644528\(v=office.15\)) pour indiquer le nombre de minutes au bout desquelles le rappel doit apparaître avant le début du rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-113">After setting other properties of the appointment, such as [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) and [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) times, ReminderExample sets the [ReminderMinutesBeforeStart](https://msdn.microsoft.com/library/bb644528\(v=office.15\)) property to indicate the number of minutes that the reminder will appear before the start of the appointment.</span></span> <span data-ttu-id="8c5cf-114">Dans ce cas, ReminderMinutesBeforeStart est défini sur 120 minutes (deux heures).</span><span class="sxs-lookup"><span data-stu-id="8c5cf-114">In this case, ReminderMinutesBeforeStart is set to 120 minutes (two hours).</span></span>

<span data-ttu-id="8c5cf-115">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-115">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="8c5cf-116">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-116">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="8c5cf-117">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-117">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void ReminderExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Wine Tasting";
    appt.Location = "Napa CA";
    appt.Sensitivity = Outlook.OlSensitivity.olPrivate;
    appt.Start = DateTime.Parse("10/21/2006 10:00 AM");
    appt.End = DateTime.Parse("10/21/2006 3:00 PM");
    appt.ReminderSet = true;
    appt.ReminderMinutesBeforeStart = 120;
    appt.Save();
}
```

## <a name="see-also"></a><span data-ttu-id="8c5cf-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c5cf-118">See also</span></span>

- [<span data-ttu-id="8c5cf-119">Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="8c5cf-119">Appointments</span></span>](appointments.md)

