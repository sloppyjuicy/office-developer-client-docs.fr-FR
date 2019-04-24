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
# <a name="create-a-recurring-appointment-by-using-the-default-recurrence-pattern"></a>Création d’un rendez-vous périodique selon une périodicité par défaut

Cet exemple montre comment créer un rendez-vous périodique selon une périodicité par défaut.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Lorsque vous créez un rendez-vous dans Outlook, vous créez un objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)). Votre rendez-vous est un rendez-vous périodique si la propriété [IsRecurring](https://msdn.microsoft.com/library/bb609491\(v=office.15\)) de l’objet AppointmentItem est définie sur True. Vous ne pouvez pas définir IsRecurring directement. 

Néanmoins, vous pouvez créer un rendez-vous périodique à l’aide de l’objet [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Pour créer un rendez-vous périodique par programme, créez un objet **AppointmentItem**, appelez la méthode [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) de l’objet **AppointmentItem**, puis enregistrez l’objet **AppointmentItem**. Cela crée un rendez-vous qui utilise la périodicité par défaut, qui a lieu de façon hebdomadaire le jour pour lequel le rendez-vous a été créé, et n’a aucune date de fin. L’objet RecurrencePattern permet de créer des rendez-vous périodiques à des intervalles spécifiés — quotidien, hebdomadaire, mensuel ou annuel. Si vous ne spécifiez pas d’intervalles pour l’objet RecurrencePattern, Outlook utilise la périodicité par défaut.

Lorsque vous travaillez avec des éléments de rendez-vous périodiques, vous devez libérer les références antérieures, obtenir de nouvelles références à l'élément de rendez-vous périodique avant d'accéder à l'élément ou de le modifier, et libérer ces références dès que vous avez terminé et enregistré les modifications. Cette pratique s’applique à l’objet **AppointmentItem** périodique, ainsi qu’aux objets [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) ou [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)). Pour publier une référence dans Visual Basic, définissez cet objet existant sur Rien. Dans C\#, libérez explicitement la mémoire pour cet objet.

Notez que même après la libération de votre référence et la tentative d'obtention d'une nouvelle référence, s'il y a toujours une référence active (détenue par un autre complément ou Outlook) à l'un des objets ci-dessus, la nouvelle référence pointera toujours vers une copie obsolète de l'objet. Par conséquent, il est important que vous libériez vos références dès que vous avez terminé le rendez-vous périodique.

Dans l’exemple suivant, la méthode CreateRecurringAppointment crée un objet **AppointmentItem**. Elle appelle ensuite GetRecurrencePattern. GetRecurrencePattern renvoie un objet RecurrencePattern et l’objet AppointmentItem est enregistré. Cela crée un rendez-vous périodique qui utilise la périodicité par défaut.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

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

## <a name="see-also"></a>Voir aussi

- [Rendez-vous](appointments.md)

