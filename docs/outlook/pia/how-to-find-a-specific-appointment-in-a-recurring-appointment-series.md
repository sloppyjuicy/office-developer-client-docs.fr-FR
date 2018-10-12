---
title: Trouver un rendez-vous spécifique dans une série de rendez-vous périodiques
TOCTitle: Find a specific appointment in a recurring appointment series
ms:assetid: 01f55f04-7245-4325-a354-50a6eb270a31
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184586(v=office.15)
ms:contentKeyID: 55119812
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: ab245fc0ff9b60862cebe57fbb2d996735442b89
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405867"
---
# <a name="find-a-specific-appointment-in-a-recurring-appointment-series"></a><span data-ttu-id="e6bbc-102">Trouver un rendez-vous spécifique dans une série de rendez-vous périodiques</span><span class="sxs-lookup"><span data-stu-id="e6bbc-102">Find a specific appointment in a recurring appointment series</span></span>

<span data-ttu-id="e6bbc-103">Cet exemple montre comment renvoyer un objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) qui représente un rendez-vous spécifique dans une série de rendez-vous périodiques.</span><span class="sxs-lookup"><span data-stu-id="e6bbc-103">This example shows how to return an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object that represents a specific appointment in a recurring appointment series.</span></span>

## <a name="example"></a><span data-ttu-id="e6bbc-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="e6bbc-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="e6bbc-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="e6bbc-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="e6bbc-106">Pour trouver une instance d'un rendez-vous périodique qui se produit à une date et une heure particulières, utilisez la méthode [GetOccurrence(DateTime)](https://msdn.microsoft.com/library/bb622806\(v=office.15\)) de l'objet [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) pour renvoyer un objet **AppointmentItem**.</span><span class="sxs-lookup"><span data-stu-id="e6bbc-106">To find an instance of a recurring appointment that occurs at a specified date and time, use the [GetOccurrence(DateTime)](https://msdn.microsoft.com/library/bb622806\(v=office.15\)) method of the [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object to return an **AppointmentItem** object.</span></span>

<span data-ttu-id="e6bbc-107">Lorsque vous travaillez avec des éléments de rendez-vous périodiques, vous devez libérer les références antérieures, obtenir de nouvelles références à l'élément de rendez-vous périodique avant d'accéder à l'élément ou de le modifier, et libérer ces références dès que vous avez terminé et enregistré les modifications.</span><span class="sxs-lookup"><span data-stu-id="e6bbc-107">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="e6bbc-108">Cette pratique s’applique à l’objet **AppointmentItem** périodique, ainsi qu’aux objets [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) ou [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="e6bbc-108">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="e6bbc-109">Pour publier une référence dans Visual Basic, définissez cet objet existant sur Rien.</span><span class="sxs-lookup"><span data-stu-id="e6bbc-109">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="e6bbc-110">Dans C\#, libérez explicitement la mémoire pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="e6bbc-110">In C#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="e6bbc-p102">Notez que même après la libération de votre référence et la tentative d'obtention d'une nouvelle référence, s'il y a toujours une référence active (détenue par un autre complément ou Outlook) à l'un des objets ci-dessus, la nouvelle référence pointera toujours vers une copie obsolète de l'objet. Par conséquent, il est important que vous libériez vos références dès que vous avez terminé le rendez-vous périodique.</span><span class="sxs-lookup"><span data-stu-id="e6bbc-p102">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference (held by another add-in or Outlook) to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="e6bbc-113">Dans l’exemple de code suivant, CheckOccurrenceExample utilise le rendez-vous périodique qui a été créé dans l’exemple de code dans [Créer un rendez-vous périodique ayant un modèle hebdomadaire](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md).</span><span class="sxs-lookup"><span data-stu-id="e6bbc-113">In the following code example,   uses the recurring appointment that was created in the code example in How to: Create a Recurring Appointment That Has a Weekly Pattern.</span></span> <span data-ttu-id="e6bbc-114">Il appelle ensuite la méthode GetOccurrence pour déterminer si le rendez-vous périodique commence à la date et à l’heure spécifiées.</span><span class="sxs-lookup"><span data-stu-id="e6bbc-114">It then calls the GetOccurrence method to determine whether the recurring appointment starts on the specified date and time.</span></span> <span data-ttu-id="e6bbc-115">Pour s’assurer que la procédure continue même si les informations fournies ne correspondent pas à la date et à l’heure de début d’une instance du rendez-vous périodique, l’exemple utilise un bloc try…catch.</span><span class="sxs-lookup"><span data-stu-id="e6bbc-115">To ensure that the procedure will continue even if the provided information does not match the start date and time of an instance of the recurring appointment, the example uses a   block.</span></span> <span data-ttu-id="e6bbc-116">Après l’appel de la méthode GetOccurrence sur chaque rendez-vous de la série de rendez-vous périodiques, CheckOccurrenceExample teste la variable singleAppt pour déterminer si elle est définie comme référence nulle, ce qui indiquerait que la méthode a échoué et n’a pas renvoyé d’objet **AppointmentItem**.</span><span class="sxs-lookup"><span data-stu-id="e6bbc-116">After calling the GetOccurrence method on every appointment in the recurring appointment series,   tests the   variable to determine whether it is set to a null reference, indicating that the method failed and did not return an AppointmentItem object.</span></span>

<span data-ttu-id="e6bbc-117">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="e6bbc-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="e6bbc-118">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="e6bbc-118">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="e6bbc-119">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="e6bbc-119">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CheckOccurrenceExample()
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
            Outlook.AppointmentItem singleAppt =
                pattern.GetOccurrence(DateTime.Parse(
                "7/21/2006 2:00 PM"))
                as Outlook.AppointmentItem;
            if (singleAppt != null)
            {
                Debug.WriteLine("7/21/2006 2:00 PM occurrence found.");
            }
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="e6bbc-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6bbc-120">See also</span></span>

- [<span data-ttu-id="e6bbc-121">Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="e6bbc-121">Appointments</span></span>](appointments.md)

