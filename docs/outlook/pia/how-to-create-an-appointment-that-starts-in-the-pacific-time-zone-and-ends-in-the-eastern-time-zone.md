---
title: Création d’un rendez-vous qui commence dans le fuseau horaire Pacifique et se termine dans le fuseau horaire Est
TOCTitle: Create an appointment that starts in the Pacific Time Zone and ends in the Eastern Time Zone
ms:assetid: ba19532b-df31-4384-8816-e64e6eecbe53
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623388(v=office.15)
ms:contentKeyID: 55119808
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e9a1b9d5f65d8683c08821d4cf0851f599f32030
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349454"
---
# <a name="create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone"></a><span data-ttu-id="af1aa-102">Création d’un rendez-vous qui commence dans le fuseau horaire Pacifique et se termine dans le fuseau horaire Est</span><span class="sxs-lookup"><span data-stu-id="af1aa-102">Create an appointment that starts in the Pacific Time Zone and ends in the Eastern Time Zone</span></span>

<span data-ttu-id="af1aa-p101">Un rendez-vous peut parfois s’étendre sur une période de temps pendant laquelle l’utilisateur peut être amené à voyager et à changer de fuseau horaire par rapport à celui du début du rendez-vous. Cet exemple crée un rendez-vous qui commence dans le fuseau horaire Pacifique (UTC-8) et se termine dans le fuseau horaire Est (UTC-5).</span><span class="sxs-lookup"><span data-stu-id="af1aa-p101">Occasionally, an appointment may span over a period of time during which the user may have traveled to a different time zone than when the appointment starts. This example creates an appointment that begins in the Pacific Time Zone (UTC-8) and ends in the Eastern Time Zone (UTC-5).</span></span>

## <a name="example"></a><span data-ttu-id="af1aa-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="af1aa-105">Example</span></span>

<span data-ttu-id="af1aa-106">Cet exemple de code utilise l'objet [TimeZones](https://msdn.microsoft.com/library/bb611081\(v=office.15\)) qui représente tous les fuseaux horaires reconnus dans Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="af1aa-106">This code sample uses the [TimeZones](https://msdn.microsoft.com/library/bb611081\(v=office.15\)) object that represents all the time zones recognized in Microsoft Windows.</span></span> <span data-ttu-id="af1aa-107">Elle utilise également l'objet [TimeZone](https://msdn.microsoft.com/library/bb646259\(v=office.15\)) pour définir ou obtenir la propriété [StartTimeZone](https://msdn.microsoft.com/library/bb623657\(v=office.15\)) et la propriété [EndTimeZone](https://msdn.microsoft.com/library/bb612198\(v=office.15\)) sur l'objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="af1aa-107">It also uses the [TimeZone](https://msdn.microsoft.com/library/bb646259\(v=office.15\)) object to set or get the [StartTimeZone](https://msdn.microsoft.com/library/bb623657\(v=office.15\)) property and the [EndTimeZone](https://msdn.microsoft.com/library/bb612198\(v=office.15\)) property on the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span>

<span data-ttu-id="af1aa-108">Outlook affiche toutes les dates en heure locale, qui est exprimée dans le fuseau horaire actuel de l’utilisateur, lui-même contrôlé par les paramètres de l’utilisateur dans le Panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="af1aa-108">Outlook displays all dates in local time, which is expressed in the user's current time zone, controlled by the user's settings in the Windows Control Panel.</span></span> <span data-ttu-id="af1aa-109">Outlook définit ou obtient également les propriétés, telles que [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) et [end](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), en heure locale.</span><span class="sxs-lookup"><span data-stu-id="af1aa-109">Outlook also sets or gets properties, such as [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) and [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), in local time.</span></span> <span data-ttu-id="af1aa-110">Toutefois, Outlook stocke les valeurs de date et heure au format UTC (Coordinated Universal Time) et non en heure locale.</span><span class="sxs-lookup"><span data-stu-id="af1aa-110">However, Outlook stores date and time values as Coordinated Universal Time (UTC) rather than local time.</span></span> <span data-ttu-id="af1aa-111">Si vous examinez la valeur interne de rendez-vous. Start by using the [propertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) Object, vous trouverez que la valeur de date et d'heure interne est égale à la valeur de date et d'heure locale convertie en valeur de date et d'heure UTC équivalente.</span><span class="sxs-lookup"><span data-stu-id="af1aa-111">If you examine the internal value of Appointment.Start by using the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object, you would find the internal date and time value is equal to the local date and time value converted to the equivalent UTC date and time value.</span></span>

<span data-ttu-id="af1aa-112">Outlook utilise les informations de fuseau horaire pour mapper le rendez-vous à l’heure UTC correcte lorsqu’il enregistre un rendez-vous et à l’heure locale actuelle lorsqu’il affiche l’élément dans le calendrier.</span><span class="sxs-lookup"><span data-stu-id="af1aa-112">Outlook uses the time zone information to map the appointment to the correct UTC time when it saves an appointment, and into the correct local time when it displays the item in the calendar.</span></span> <span data-ttu-id="af1aa-113">La modification de StartTimeZone affecte la valeur de rendez-vous. Start, qui est toujours exprimée dans le fuseau horaire local, représenté par la propriété [CurrentTimeZone](https://msdn.microsoft.com/library/bb612024\(v=office.15\)) de l'objet retourné par [TimeZones](https://msdn.microsoft.com/library/bb645170\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="af1aa-113">Changing StartTimeZone affects the value of Appointment.Start, which is always expressed in the local time zone, represented by the [CurrentTimeZone](https://msdn.microsoft.com/library/bb612024\(v=office.15\)) property of the object returned by [TimeZones](https://msdn.microsoft.com/library/bb645170\(v=office.15\)).</span></span> <span data-ttu-id="af1aa-114">De la même manière, le fait de modifier EndTimeZone affecte la valeur d’Appointment.End, laquelle est toujours exprimée dans le fuseau horaire local, représenté par la propriété CurrentTimeZone de l’objet retourné par Application.TimeZones.</span><span class="sxs-lookup"><span data-stu-id="af1aa-114">Similarly, changing EndTimeZone affects the value of Appointment.End, which is always expressed in the local time zone, represented by the CurrentTimeZone property of the object returned by Application.TimeZones.</span></span>

<span data-ttu-id="af1aa-115">Vous pouvez récupérer un objet TimeZone spécifique à partir de l’objet TimeZones en utilisant la clé indépendante des paramètres régionaux pour TimeZone dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="af1aa-115">You can retrieve a specific TimeZone from the TimeZones object by using the locale-independent key for the TimeZone in the Windows registry.</span></span> <span data-ttu-id="af1aa-116">Les clés de fuseau horaire indépendantes des paramètres régionaux sont répertoriées sous `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\TimeZones`la clé suivante:.</span><span class="sxs-lookup"><span data-stu-id="af1aa-116">Locale-independent TimeZone keys are listed under the following key: `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\TimeZones`.</span></span>

<span data-ttu-id="af1aa-117">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="af1aa-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="af1aa-118">L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="af1aa-118">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="af1aa-119">Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.</span><span class="sxs-lookup"><span data-stu-id="af1aa-119">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>


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

## <a name="see-also"></a><span data-ttu-id="af1aa-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af1aa-120">See also</span></span>

- [<span data-ttu-id="af1aa-121">Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="af1aa-121">Appointments</span></span>](appointments.md)

