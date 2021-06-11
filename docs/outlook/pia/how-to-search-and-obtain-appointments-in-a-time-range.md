---
title: Effectuer des recherches et obtenir des rendez-vous dans un intervalle de temps
TOCTitle: Search and obtain appointments in a time range
ms:assetid: ce5205ad-6967-4f21-8a9d-503b731dbd40
ms:mtpsurl: https://msdn.microsoft.com/library/Gg619398(v=office.15)
ms:contentKeyID: 55119927
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9088da5f2deb4b3d4ccb1c2bc5409e0ff280ed24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316088"
---
# <a name="search-and-obtain-appointments-in-a-time-range"></a><span data-ttu-id="4bccc-102">Effectuer des recherches et obtenir des rendez-vous dans un intervalle de temps</span><span class="sxs-lookup"><span data-stu-id="4bccc-102">Search and obtain appointments in a time range</span></span>

<span data-ttu-id="4bccc-103">Cet exemple envoie les rendez-vous dans un intervalle de temps spécifique dans le calendrier Microsoft Outlook par défaut.</span><span class="sxs-lookup"><span data-stu-id="4bccc-103">This example returns appointments in a specific time range in the default Microsoft Outlook calendar.</span></span>

## <a name="example"></a><span data-ttu-id="4bccc-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="4bccc-104">Example</span></span>

<span data-ttu-id="4bccc-105">Cet exemple de code contienne deux méthodes : DemoAppointmentsInRange et GetAppointmentsInRange.</span><span class="sxs-lookup"><span data-stu-id="4bccc-105">This code example contains two methods: DemoAppointmentsInRange and GetAppointmentsInRange.</span></span> <span data-ttu-id="4bccc-106">DemoAppointmentsInRange a obtenu le calendrier par défaut pour le profil d’Outlook connecté, avec une plage de dates de 5 jours à partir de 00:00.</span><span class="sxs-lookup"><span data-stu-id="4bccc-106">DemoAppointmentsInRange obtains the default calendar for the current signed-in Outlook profile, sets a date range of 5 days from 12:00 A.M.</span></span> <span data-ttu-id="4bccc-107">Aujourd'hui, appellez GetAppointmentsInRange pour obtenir des rendez-vous qui se trouvent dans cet intervalle de temps et affiche l’objet et le début de chaque rendez-vous envoyés.</span><span class="sxs-lookup"><span data-stu-id="4bccc-107">today, calls GetAppointmentsInRange to obtain appointments that fall in that time range, and displays the subject and start time of each of the returned appointments.</span></span>

<span data-ttu-id="4bccc-108">GetAppointmentsInRange accepte un dossier Outlook et les valeurs de début et fin **DateTime** de l’intervalle de temps en tant que paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4bccc-108">GetAppointmentsInRange accepts an Outlook folder, and the start and end **DateTime** values of the time range as input parameters.</span></span> <span data-ttu-id="4bccc-109">Cette méthode utilise la méthode [Restrict(String)](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) et une chaîne de filtre dans format Jet qui envoie les rendez-vous qui commencent et se terminent au sein de la plage horaire donnée.</span><span class="sxs-lookup"><span data-stu-id="4bccc-109">This method uses the [Restrict(String)](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) method and a string filter in Jet format that returns appointments that start and end within the specified time range.</span></span> <span data-ttu-id="4bccc-110">En supposant que \[début\] et \[fin\] sont l’heure de début et l’heure de fin d’un rendez-vous et startTime et endTime sont l’heure de début et de fin de la plage horaire donnée, GetAppointmentsInRange configure un filtre qui recherche les rendez-vous avec `[Start]>=startTime`, et `[End]<=endTime`.</span><span class="sxs-lookup"><span data-stu-id="4bccc-110">Assuming \[Start\] and \[End\] are the start time and end time of an appointment, and startTime and endTime are the beginning and end time of the specified time range, GetAppointmentsInRange sets up a filter  that looks for appointments with `[Start]>=startTime`, and `[End]<=endTime`.</span></span> <span data-ttu-id="4bccc-111">Le code suivant montre le filtre Jet dans C\#.</span><span class="sxs-lookup"><span data-stu-id="4bccc-111">The following code shows the Jet filter in C\#.</span></span>

```csharp
string filter = "[Start] >= '"
    + startTime.ToString("g")
    + "' AND [End] <= '"
    + endTime.ToString("g") + "'";
```

<span data-ttu-id="4bccc-112">Avant d’appeler la méthode **Items.Restrict** pour rechercher des rendez-vous, GetAppointmentsInRange procède à deux autres actions pour inclure les rendez-vous périodiques qui se produisent dans l’intervalle de temps spécifié :</span><span class="sxs-lookup"><span data-stu-id="4bccc-112">Before calling the **Items.Restrict** method to search for appointments, GetAppointmentsInRange does two other things to include recurring appointments that occur in the specified time range:</span></span>

- <span data-ttu-id="4bccc-113">Définit la propriété [IncludeRecurrences](https://msdn.microsoft.com/library/bb646522\(v=office.15\)) de la collection [éléments](https://msdn.microsoft.com/library/bb645287\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="4bccc-113">Sets the [IncludeRecurrences](https://msdn.microsoft.com/library/bb646522\(v=office.15\)) property of the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) collection.</span></span>

- <span data-ttu-id="4bccc-114">Trie les éléments de rendez-vous dans le dossier de calendrier donné par la propriété[Démarrer](https://msdn.microsoft.com/library/bb647263\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="4bccc-114">Sorts the appointment items in the given calendar folder by the [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) property.</span></span>

<span data-ttu-id="4bccc-115">Par ailleurs, si vous cherchez également des rendez-vous qui se chevauchent partiellement ou entièrement dans l’intervalle de temps spécifié, vous devez spécifier un filtre différent pour renvoyer les autres types de rendez-vous (comme illustré dans la Figure 1) :</span><span class="sxs-lookup"><span data-stu-id="4bccc-115">Alternatively, if you are also interested in appointments that overlap partially or entirely with the specified time range, you would specify a different filter to return additional types of appointments (as shown in Figure 1):</span></span>

- <span data-ttu-id="4bccc-116">Rendez-vous qui commencent et se terminent dans l’intervalle de temps spécifié (par exemple, rendez-vous A) :</span><span class="sxs-lookup"><span data-stu-id="4bccc-116">Appointments that start and end within the specified time range (for example, appointment A):</span></span><br/><br/>`[Start]>=startTime and [End]<=endTime`

- <span data-ttu-id="4bccc-117">Rendez-vous qui commencent avant mais se terminent dans l’intervalle de temps spécifié (par exemple, rendez-vous B) :</span><span class="sxs-lookup"><span data-stu-id="4bccc-117">Appointments that start before the specified time range but end within the time range (for example, appointment B):</span></span><br/><br/>`[Start]<startTime and [End]<=endTime`

- <span data-ttu-id="4bccc-118">Rendez-vous qui commencent dans mais se terminent après l’intervalle de temps spécifié (par exemple, rendez-vous C) :</span><span class="sxs-lookup"><span data-stu-id="4bccc-118">Appointments that start within the specified time range but end after the time range (for example, appointment C):</span></span><br/><br/>`[Start]>=startTime and [End]>endTime`

- <span data-ttu-id="4bccc-119">Rendez-vous qui commencent avant mais se terminent après l’intervalle de temps spécifié (par exemple, rendez-vous D) :</span><span class="sxs-lookup"><span data-stu-id="4bccc-119">Appointments that start before the specified time range and end after the time range (for example, appointment D):</span></span><br/><br/>`[Start]<startTime and [End]>endTime`

<span data-ttu-id="4bccc-120">**Figure 1. Types de rendez-vous qui se produisent au sein d’un intervalle de temps ou se chevauchent dans ce laps de temps**</span><span class="sxs-lookup"><span data-stu-id="4bccc-120">**Figure 1. Types of appointments that occur within a time range, or overlap with that time range**</span></span>

![Types de rendez-vous qui se produisent au sein d’un intervalle de temps ou se chevauchent dans ce laps de temps](media/pia-appointment-starttime-endtime.gif)
 

<span data-ttu-id="4bccc-122&quot;>Étant donné que dans n’importe quelle plage horaire `startTime<=endTime`, un filtre avec `[Start]<=endTime` et `[End]>=startTime` capturerait les types de rendez-vous précédents de cette plage horaire.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;4bccc-122&quot;>Because in any time range `startTime<=endTime`, a filter with `[Start]<=endTime` and `[End]>=startTime` would capture the preceding types of appointments in that time range.</span></span>

<span data-ttu-id=&quot;4bccc-123&quot;>Dans C\#, vous pouvez exprimer le filtre Jet comme suit.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;4bccc-123&quot;>In C\#, you can express the Jet filter as follows.</span></span>

```csharp
string filter = &quot;[Start] <= '&quot;
    + endTime.ToString(&quot;g")
    + "' AND [End] >= '"
    + startTime.ToString("g") + "'";
```

<span data-ttu-id="4bccc-124">Le code suivant montre l’exemple complet.</span><span class="sxs-lookup"><span data-stu-id="4bccc-124">The following code shows the complete example.</span></span> <span data-ttu-id="4bccc-125">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="4bccc-125">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="4bccc-126">L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="4bccc-126">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="4bccc-127">Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.</span><span class="sxs-lookup"><span data-stu-id="4bccc-127">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoAppointmentsInRange()
{
    Outlook.Folder calFolder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar)
        as Outlook.Folder;
    DateTime start = DateTime.Now;
    DateTime end = start.AddDays(5);
    Outlook.Items rangeAppts = GetAppointmentsInRange(calFolder, start, end);
    if (rangeAppts != null)
    {
        foreach (Outlook.AppointmentItem appt in rangeAppts)
        {
            Debug.WriteLine("Subject: " + appt.Subject 
                + " Start: " + appt.Start.ToString("g"));
        }
    }
}

/// <summary>
/// Get recurring appointments in date range.
/// </summary>
/// <param name="folder"></param>
/// <param name="startTime"></param>
/// <param name="endTime"></param>
/// <returns>Outlook.Items</returns>
private Outlook.Items GetAppointmentsInRange(
    Outlook.Folder folder, DateTime startTime, DateTime endTime)
{
    string filter = "[Start] >= '"
        + startTime.ToString("g")
        + "' AND [End] <= '"
        + endTime.ToString("g") + "'";
    Debug.WriteLine(filter);
    try
    {
        Outlook.Items calItems = folder.Items;
        calItems.IncludeRecurrences = true;
        calItems.Sort("[Start]", Type.Missing);
        Outlook.Items restrictItems = calItems.Restrict(filter);
        if (restrictItems.Count > 0)
        {
            return restrictItems;
        }
        else
        {
            return null;
        }
    }
    catch { return null; }
}
```

## <a name="see-also"></a><span data-ttu-id="4bccc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bccc-128">See also</span></span>

- [<span data-ttu-id="4bccc-129">Rechercher et filtrer</span><span class="sxs-lookup"><span data-stu-id="4bccc-129">Search and filter</span></span>](search-and-filter.md)

