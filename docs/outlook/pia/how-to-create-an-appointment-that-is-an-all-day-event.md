---
title: Création d’un rendez-vous sur toute la journée
TOCTitle: Create an appointment that is an all-day event
ms:assetid: a0d3baeb-6ed5-41b6-bef5-d6c1bb56fee3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184629(v=office.15)
ms:contentKeyID: 55119806
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9164c4378d369040f809994eef0b1a0a1043ecdc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574754"
---
# <a name="create-an-appointment-that-is-an-all-day-event"></a>Création d’un rendez-vous sur toute la journée

Cet exemple montre comment utiliser la propriété [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) pour créer un rendez-vous qui est un événement planifié sur une journée entière.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Un événement est différent d’un rendez-vous normal car il s’agit d’une activité qui dure 24 heures ou plus. Les salons, les séminaires ou les vacances sont des exemples d’événements. Les événements et les événements annuels n’apparaissent pas comme des blocs de temps occupés dans le calendrier de l’utilisateur, mais sous la forme de bannières. Les bannières sont représentées en haut de l’affichage quotidien ou hebdomadaire d’un calendrier. Par défaut, le temps de l’utilisateur est affiché aux autres utilisateurs comme occupé pour un rendez-vous d’une journée entière, mais comme libre pour un événement ou un événement annuel.

Pour créer par programme un événement d’une journée entière, définissez la propriété [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) de l’objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) sur True. Définissez ensuite les propriétés [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) et [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) de l’objet AppointmentItem. Si vous définissez la propriété AllDayEvent sur true et ne définissez pas les propriétés Start et End, l'événement se produira aujourd'hui et sera un rendez-vous avec le statut occupé sur votre calendrier. Vous devez définir les propriétés Start et End si vous souhaitez que l’événement se produise à une date ultérieure.

> [!NOTE]
> Pour que le rendez-vous soit un événement planifié sur une journée entière, vous devez définir la propriété Start sur 00:00:00 (minuit) le jour où vous souhaitez que l’événement commence, et définir la propriété End sur 00:00:00 le jour qui suit le jour de fin de l’événement. Si vous définissez l’heure de début ou de fin sur une valeur autre que 00:00:00, le rendez-vous deviendra un rendez-vous planifié sur plusieurs jours plutôt qu’un événement planifié sur une journée entière. 
>
> Par exemple, si la durée de votre événement est d’un jour seulement, définissez la propriété Start sur 00:00:00. le jour où vous souhaitez que l’événement commence, et définissez la propriété End sur 00:00:00 le jour suivant. Vous devez toujours définir la propriété End sur 00:00:00 à une date postérieure au lendemain de la date de début.

Dans l’exemple de code suivant, AllDayEventExample crée un événement d’une journée entière qui commence le 11 juin 2007 et se termine le 15 juin 2007. Notez que la propriété End du rendez-vous est définie sur 00h00, le 16 juin 2007.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

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

## <a name="see-also"></a>Voir aussi

- [Rendez-vous](appointments.md)

