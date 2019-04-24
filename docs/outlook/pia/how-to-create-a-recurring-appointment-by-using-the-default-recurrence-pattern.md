---
title: Création d’un rendez-vous périodique selon une périodicité par défaut
TOCTitle: Create a recurring appointment by using the default recurrence pattern
ms:assetid: 157bf1ae-2efe-4783-99ea-606722dde204
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184589(v=office.15)
ms:contentKeyID: 55119809
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: de58523e663349c43cc358f5b76896987a0f23b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332115"
---
# <a name="create-a-recurring-appointment-by-using-the-default-recurrence-pattern"></a><span data-ttu-id="184f7-102">Création d’un rendez-vous périodique selon une périodicité par défaut</span><span class="sxs-lookup"><span data-stu-id="184f7-102">Create a recurring appointment by using the default recurrence pattern</span></span>

<span data-ttu-id="184f7-103">Cet exemple montre comment créer un rendez-vous périodique selon une périodicité par défaut.</span><span class="sxs-lookup"><span data-stu-id="184f7-103">This example shows how to create a recurring appointment by using the default recurrence pattern.</span></span>

## <a name="example"></a><span data-ttu-id="184f7-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="184f7-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="184f7-105">L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="184f7-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="184f7-106">Lorsque vous créez un rendez-vous dans Outlook, vous créez un objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="184f7-106">When you create an appointment in Outlook, you are creating an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span> <span data-ttu-id="184f7-107">Votre rendez-vous est un rendez-vous périodique si la propriété [IsRecurring](https://msdn.microsoft.com/library/bb609491\(v=office.15\)) de l’objet AppointmentItem est définie sur True.</span><span class="sxs-lookup"><span data-stu-id="184f7-107">Your appointment is a recurring appointment if the [IsRecurring](https://msdn.microsoft.com/library/bb609491\(v=office.15\)) property of the AppointmentItem is set to true.</span></span> <span data-ttu-id="184f7-108">Vous ne pouvez pas définir IsRecurring directement.</span><span class="sxs-lookup"><span data-stu-id="184f7-108">IsRecurring cannot be set directly.</span></span> 

<span data-ttu-id="184f7-109">Néanmoins, vous pouvez créer un rendez-vous périodique à l’aide de l’objet [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="184f7-109">However, you can create a recurring appointment by using the [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="184f7-110">Pour créer un rendez-vous périodique par programme, créez un objet **AppointmentItem**, appelez la méthode [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) de l’objet **AppointmentItem**, puis enregistrez l’objet **AppointmentItem**.</span><span class="sxs-lookup"><span data-stu-id="184f7-110">To create a recurring appointment programmatically, create an **AppointmentItem** object, call the [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) method of the **AppointmentItem** object, and then save the **AppointmentItem** object.</span></span> <span data-ttu-id="184f7-111">Cela crée un rendez-vous qui utilise la périodicité par défaut, qui a lieu de façon hebdomadaire le jour pour lequel le rendez-vous a été créé, et n’a aucune date de fin.</span><span class="sxs-lookup"><span data-stu-id="184f7-111">This creates an appointment that uses the default recurrence pattern, which occurs weekly on the day of the week for which the appointment was created, and has no end date.</span></span> <span data-ttu-id="184f7-112">L’objet RecurrencePattern permet de créer des rendez-vous périodiques à des intervalles spécifiés — quotidien, hebdomadaire, mensuel ou annuel.</span><span class="sxs-lookup"><span data-stu-id="184f7-112">The RecurrencePattern object allows you to create recurring appointments at specified intervals—daily, weekly, monthly, or yearly.</span></span> <span data-ttu-id="184f7-113">Si vous ne spécifiez pas d’intervalles pour l’objet RecurrencePattern, Outlook utilise la périodicité par défaut.</span><span class="sxs-lookup"><span data-stu-id="184f7-113">If you do not specify intervals for the RecurrencePattern object, Outlook will use the default recurrence pattern.</span></span>

<span data-ttu-id="184f7-114">Lorsque vous travaillez avec des éléments de rendez-vous périodiques, vous devez libérer les références antérieures, obtenir de nouvelles références à l'élément de rendez-vous périodique avant d'accéder à l'élément ou de le modifier, et libérer ces références dès que vous avez terminé et enregistré les modifications.</span><span class="sxs-lookup"><span data-stu-id="184f7-114">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="184f7-115">Cette pratique s’applique à l’objet **AppointmentItem** périodique, ainsi qu’aux objets [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) ou [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="184f7-115">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="184f7-116">Pour publier une référence dans Visual Basic, définissez cet objet existant sur Rien.</span><span class="sxs-lookup"><span data-stu-id="184f7-116">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="184f7-117">Dans C\#, libérez explicitement la mémoire pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="184f7-117">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="184f7-p104">Notez que même après la libération de votre référence et la tentative d'obtention d'une nouvelle référence, s'il y a toujours une référence active (détenue par un autre complément ou Outlook) à l'un des objets ci-dessus, la nouvelle référence pointera toujours vers une copie obsolète de l'objet. Par conséquent, il est important que vous libériez vos références dès que vous avez terminé le rendez-vous périodique.</span><span class="sxs-lookup"><span data-stu-id="184f7-p104">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference (held by another add-in or Outlook) to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="184f7-120">Dans l’exemple suivant, la méthode CreateRecurringAppointment crée un objet **AppointmentItem**.</span><span class="sxs-lookup"><span data-stu-id="184f7-120">In the following example, CreateRecurringAppointment creates an **AppointmentItem** object.</span></span> <span data-ttu-id="184f7-121">Elle appelle ensuite GetRecurrencePattern.</span><span class="sxs-lookup"><span data-stu-id="184f7-121">It then calls GetRecurrencePattern.</span></span> <span data-ttu-id="184f7-122">GetRecurrencePattern renvoie un objet RecurrencePattern et l’objet AppointmentItem est enregistré.</span><span class="sxs-lookup"><span data-stu-id="184f7-122">GetRecurrencePattern returns a RecurrencePattern object, and the AppointmentItem is saved.</span></span> <span data-ttu-id="184f7-123">Cela crée un rendez-vous périodique qui utilise la périodicité par défaut.</span><span class="sxs-lookup"><span data-stu-id="184f7-123">This creates a recurring appointment that uses the default recurrence pattern.</span></span>

<span data-ttu-id="184f7-124">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="184f7-124">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="184f7-125">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="184f7-125">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="184f7-126">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="184f7-126">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CreateRecurringAppointment()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Weekly Extensibility Team Meeting";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    appt.Save();
}
```

## <a name="see-also"></a><span data-ttu-id="184f7-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="184f7-127">See also</span></span>

- [<span data-ttu-id="184f7-128">Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="184f7-128">Appointments</span></span>](appointments.md)

