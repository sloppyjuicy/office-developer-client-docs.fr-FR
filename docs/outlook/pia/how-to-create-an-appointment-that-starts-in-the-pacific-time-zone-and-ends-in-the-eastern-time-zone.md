---
title: Création d’un rendez-vous qui commence dans le fuseau horaire Pacifique et se termine dans le fuseau horaire Est
TOCTitle: Create an appointment that starts in the Pacific Time Zone and ends in the Eastern Time Zone
ms:assetid: ba19532b-df31-4384-8816-e64e6eecbe53
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623388(v=office.15)
ms:contentKeyID: 55119808
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 9cb21bddb425adb54082dbe21b32653e1fe3ca75
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406077"
---
# <a name="create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone"></a>Création d’un rendez-vous qui commence dans le fuseau horaire Pacifique et se termine dans le fuseau horaire Est

Un rendez-vous peut parfois s'étendre sur une période de temps pendant laquelle l'utilisateur peut être amené à voyager et à changer de fuseau horaire par rapport à celui du début du rendez-vous. Cet exemple crée un rendez-vous qui commence dans le fuseau horaire Pacifique (UTC-8) et se termine dans le fuseau horaire Est (UTC-5).

## <a name="example"></a>Exemple

Cet exemple de code utilise l'objet [TimeZones](https://msdn.microsoft.com/library/bb611081\(v=office.15\)) qui représente tous les fuseaux horaires reconnus dans Microsoft Windows. Il utilise également l'objet [TimeZone](https://msdn.microsoft.com/library/bb646259\(v=office.15\)) pour définir ou obtenir la propriété [StartTimeZone](https://msdn.microsoft.com/library/bb623657\(v=office.15\)) et la propriété [EndTimeZone](https://msdn.microsoft.com/library/bb612198\(v=office.15\)) de l'objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) .

Outlook affiche toutes les dates en heure locale, qui est exprimée dans le fuseau horaire actuel de l'utilisateur, lui-même contrôlé par les paramètres de l'utilisateur dans le Panneau de configuration. Outlook définit ou obtient également les propriétés, comme [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) et [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), en heure locale. Toutefois, Outlook stocke les valeurs de date et d’heure au format UTC (temps universel coordonné), plutôt qu’en heure locale. Si vous examinez la valeur interne d' Appointment.Start en utilisant l'objet [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) , vous verrez que la valeur de date et heure interne est égale à la valeur de date et heure locale convertie en valeur de date et heure UTC équivalente.

Outlook utilise les informations de fuseau horaire pour mapper le rendez-vous à l'heure UTC correcte lorsqu'il enregistre un rendez-vous et à l'heure locale actuelle lorsqu'il affiche l'élément dans le calendrier. Le fait de modifier StartTimeZone affecte la valeur de Appointment.Start, laquelle est toujours exprimée dans le fuseau horaire local, représenté par la propriété [CurrentTimeZone](https://msdn.microsoft.com/library/bb612024\(v=office.15\)) de l’objet renvoyé par [TimeZones](https://msdn.microsoft.com/library/bb645170\(v=office.15\)). De la même manière, le fait de modifier EndTimeZone affecte la valeur d' Appointment.End, laquelle est toujours exprimée dans le fuseau horaire local, représenté par la propriété CurrentTimeZone de l'objet retourné par Application.TimeZones.

Vous pouvez récupérer un fuseau horaire spécifique à partir de l’objet Timezones à l’aide de la clé indépendante des paramètres régionaux dédiée au fuseau horaire dans le Registre Windows. Les clés TimeZone indépendantes des paramètres régionaux sont répertoriées sous la clé suivante : `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\TimeZones`.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```



```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```



```vb
Private Sub TimeZoneExample()
    Dim appt As Outlook.AppointmentItem = _
        CType(Application.CreateItem( _
        Outlook.OlItemType.olAppointmentItem), Outlook.AppointmentItem)
    Dim tzs As Outlook.TimeZones = Application.TimeZones
    ' Obtain timezone using indexer and locale-independent key
    Dim tzEastern As Outlook.TimeZone = tzs("Eastern Standard Time")
    Dim tzPacific As Outlook.TimeZone = tzs("Pacific Standard Time")
    appt.Subject = "SEA - JFK Flight"
    appt.Start = DateTime.Parse("8/9/2006 8:00 AM")
    appt.StartTimeZone = tzPacific
    appt.End = DateTime.Parse("8/9/2006 5:30 PM")
    appt.EndTimeZone = tzEastern
    appt.Display(False)
End Sub
```



```csharp
private void TimeZoneExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    Outlook.TimeZones tzs = Application.TimeZones;
    // Obtain timezone using indexer and locale-independent key
    Outlook.TimeZone tzEastern = tzs["Eastern Standard Time"];
    Outlook.TimeZone tzPacific = tzs["Pacific Standard Time"];
    appt.Subject = "SEA - JFK Flight";
    appt.Start = DateTime.Parse("8/9/2006 8:00 AM");
    appt.StartTimeZone = tzPacific;
    appt.End = DateTime.Parse("8/9/2006 5:30 PM");
    appt.EndTimeZone = tzEastern; 
    appt.Display(false);
}
```

## <a name="see-also"></a>Voir aussi

- [Rendez-vous](appointments.md)

