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
# <a name="create-a-reminder-for-an-appointment-item"></a>Création d’un rappel pour un élément de rendez-vous

Cet exemple montre comment utiliser la propriété [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) pour créer un rappel pour un élément de rendez-vous.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Outlook permet de définir facilement un rappel pour un rendez-vous à l’aide de la propriété [ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) de l’objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)). Cette propriété indique si un rappel a été créé pour le rendez-vous. Le fait de définir la propriété ReminderSet sur true crée un rappel, et sa définition sur false supprime le rappel.

Dans l’exemple de code suivant, ReminderExample crée un rappel sur un rendez-vous privé pour une dégustation de vin à Napa, Californie et définit le rappel pour qu’il se déclenche deux heures avant le début du rendez-vous. Tout d’abord, ReminderExample crée un objet **AppointmentItem** Outlook. Il définit ensuite la propriété [sensibilité](https://msdn.microsoft.com/library/bb623503\(v=office.15\)) de l’élément sur [olPrivate](https://msdn.microsoft.com/library/bb645125\(v=office.15\)). Ceci indique que le rendez-vous est un rendez-vous privé. Une fois que les autres propriétés du rendez-vous sont définies, telles que les heures de [début](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) et de [fin](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), ReminderExample définit la propriété [ReminderMinutesBeforeStart](https://msdn.microsoft.com/library/bb644528\(v=office.15\)) pour indiquer le nombre de minutes au bout desquelles le rappel doit apparaître avant le début du rendez-vous. Dans ce cas, ReminderMinutesBeforeStart est défini sur 120 minutes (deux heures).

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.

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

## <a name="see-also"></a>Voir aussi

- [Rendez-vous](appointments.md)

