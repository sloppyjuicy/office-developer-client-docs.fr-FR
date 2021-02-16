---
title: Trouver un rendez-vous spécifique dans une série de rendez-vous périodiques
TOCTitle: Find a specific appointment in a recurring appointment series
ms:assetid: 01f55f04-7245-4325-a354-50a6eb270a31
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184586(v=office.15)
ms:contentKeyID: 55119812
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 19502895996d4777f2d1a6887aa80883a5398a09
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320250"
---
# <a name="find-a-specific-appointment-in-a-recurring-appointment-series"></a>Trouver un rendez-vous spécifique dans une série de rendez-vous périodiques

Cet exemple montre comment renvoyer un objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) qui représente un rendez-vous spécifique dans une série de rendez-vous périodiques.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Pour trouver une instance d'un rendez-vous périodique qui se produit à une date et une heure particulières, utilisez la méthode [GetOccurrence(DateTime)](https://msdn.microsoft.com/library/bb622806\(v=office.15\)) de l'objet [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) pour renvoyer un objet **AppointmentItem**.

Lorsque vous travaillez avec des éléments de rendez-vous périodiques, vous devez libérer les références antérieures, obtenir de nouvelles références à l'élément de rendez-vous périodique avant d'accéder à l'élément ou de le modifier, et libérer ces références dès que vous avez terminé et enregistré les modifications. Cette pratique s’applique à l’objet **AppointmentItem** périodique, ainsi qu’aux objets [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) ou [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Pour publier une référence dans Visual Basic, définissez cet objet existant sur Rien. Dans C\#, libérez explicitement la mémoire pour cet objet.

Notez que même après la libération de votre référence et la tentative d'obtention d'une nouvelle référence, s'il y a toujours une référence active (détenue par un autre complément ou Outlook) à l'un des objets ci-dessus, la nouvelle référence pointera toujours vers une copie obsolète de l'objet. Par conséquent, il est important que vous libériez vos références dès que vous avez terminé le rendez-vous périodique.

Dans l’exemple de code suivant, CheckOccurrenceExample utilise le rendez-vous périodique qui a été créé dans l’exemple de code dans [Créer un rendez-vous périodique ayant un modèle hebdomadaire](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md). Il appelle ensuite la méthode GetOccurrence pour déterminer si le rendez-vous périodique commence à la date et à l’heure spécifiées. Pour s’assurer que la procédure continue même si les informations fournies ne correspondent pas à la date et à l’heure de début d’une instance du rendez-vous périodique, l’exemple utilise un bloc try…catch. Après l’appel de la méthode GetOccurrence sur chaque rendez-vous de la série de rendez-vous périodiques, CheckOccurrenceExample teste la variable singleAppt pour déterminer si elle est définie comme référence nulle, ce qui indiquerait que la méthode a échoué et n’a pas renvoyé d’objet **AppointmentItem**.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

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

## <a name="see-also"></a>Voir aussi

- [Rendez-vous](appointments.md)

