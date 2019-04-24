---
title: Importation des données XML d’un rendez-vous dans les objets de rendez-vous Outlook
TOCTitle: Import appointment XML data into Outlook appointment objects
ms:assetid: 166a648a-1c48-4984-8889-a7614cc277b1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462092(v=office.15)
ms:contentKeyID: 55119821
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0af86772fced3e69d1d28cf8d98a544e3b4d90d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320061"
---
# <a name="import-appointment-xml-data-into-outlook-appointment-objects"></a><span data-ttu-id="da435-102">Importation des données XML d’un rendez-vous dans les objets de rendez-vous Outlook</span><span class="sxs-lookup"><span data-stu-id="da435-102">Import appointment XML data into Outlook appointment objects</span></span>

<span data-ttu-id="da435-103">Cette rubrique montre comment lire des données de rendez-vous au format XML, enregistrer les données dans des objets Outlook [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) dans le calendrier par défaut, puis renvoyer les objets de rendez-vous dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="da435-103">This topic shows how to read appointment data formatted in XML, save the data to Outlook [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) objects in the default calendar, and return the appointment objects in an array.</span></span>

## <a name="example"></a><span data-ttu-id="da435-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="da435-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="da435-105">Helmut Obertanner a fourni les exemples de code suivants.</span><span class="sxs-lookup"><span data-stu-id="da435-105">Helmut Obertanner provided the following code examples.</span></span> <span data-ttu-id="da435-106">L’expertise de Helmut se trouve dans les outils de développement Office pour Visual Studio et Outlook.</span><span class="sxs-lookup"><span data-stu-id="da435-106">Helmut's expertise is in Office Developer Tools for Visual Studio and Outlook.</span></span> 


<span data-ttu-id="da435-107">Les exemples de code suivants contiennent la méthode CreateAppointmentsFromXml de la classe Sample, implémentée dans le cadre d’un projet de complément Outlook.</span><span class="sxs-lookup"><span data-stu-id="da435-107">The following code examples contain the CreateAppointmentsFromXml method of the Sample class, implemented as part of an Outlook add-in project.</span></span> <span data-ttu-id="da435-108">Chaque projet ajoute une référence à l’assembly PIA (Primary Interop Assembly) Outlook, qui est basé sur l’espace de noms [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="da435-108">Each project adds a reference to the Outlook Primary Interop Assembly, which is based on the [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) namespace.</span></span>

<span data-ttu-id="da435-109">La méthode CreateAppointmentsFromXml accepte deux paramètres d’entrée :</span><span class="sxs-lookup"><span data-stu-id="da435-109">The CreateAppointmentsFromXml method accepts two input parameters:</span></span>

  - <span data-ttu-id="da435-110">l’application est un objet [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) Outlook approuvé.</span><span class="sxs-lookup"><span data-stu-id="da435-110">application is a trusted Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object.</span></span>

  - <span data-ttu-id="da435-p103">xml est une chaîne XML ou une chaîne qui représente un chemin d’accès à un fichier XML valide. Dans les exemples de code suivants, le code XML délimite les données de rendez-vous en utilisant les balises XML suivantes :</span><span class="sxs-lookup"><span data-stu-id="da435-p103">xml is either an XML string, or a string that represents a path to a valid XML file. For the purpose of the following code examples, the XML delimits appointment data by using the following XML tags:</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="da435-113">Données de rendez-vous</span><span class="sxs-lookup"><span data-stu-id="da435-113">Appointment data</span></span></p></th>
    <th><p><span data-ttu-id="da435-114">Balise XML de délimitation</span><span class="sxs-lookup"><span data-stu-id="da435-114">Delimiting XML tag</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="da435-115">Ensemble de données de rendez-vous</span><span class="sxs-lookup"><span data-stu-id="da435-115">Entire set of appointment data</span></span></p></td>
    <td><p><span data-ttu-id="da435-116">rendez-vous ;</span><span class="sxs-lookup"><span data-stu-id="da435-116">appointments</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="da435-117">Chaque rendez-vous de l’ensemble de données</span><span class="sxs-lookup"><span data-stu-id="da435-117">Each appointment in the set</span></span></p></td>
    <td><p><span data-ttu-id="da435-118">rendez-vous</span><span class="sxs-lookup"><span data-stu-id="da435-118">appointment</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="da435-119">Heure de début d’un rendez-vous</span><span class="sxs-lookup"><span data-stu-id="da435-119">Start time of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="da435-120">starttime</span><span class="sxs-lookup"><span data-stu-id="da435-120">starttime</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="da435-121">Heure de fin d’un rendez-vous</span><span class="sxs-lookup"><span data-stu-id="da435-121">End time of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="da435-122">endtime</span><span class="sxs-lookup"><span data-stu-id="da435-122">endtime</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="da435-123">Titre d’un rendez-vous</span><span class="sxs-lookup"><span data-stu-id="da435-123">Title of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="da435-124">subject</span><span class="sxs-lookup"><span data-stu-id="da435-124">subject</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="da435-125">Emplacement d’un rendez-vous</span><span class="sxs-lookup"><span data-stu-id="da435-125">Location of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="da435-126">location</span><span class="sxs-lookup"><span data-stu-id="da435-126">location</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="da435-127">Détails d’un rendez-vous</span><span class="sxs-lookup"><span data-stu-id="da435-127">Details of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="da435-128">body</span><span class="sxs-lookup"><span data-stu-id="da435-128">body</span></span></p></td>
    </tr>
    </tbody>
    </table>


<span data-ttu-id="da435-129">L’exemple suivant montre les données d’entrée du paramètre *xml*.</span><span class="sxs-lookup"><span data-stu-id="da435-129">The following example shows input data for the *xml* parameter.</span></span>

```xml
<?xml version="1.0" encoding="utf-8" ?> 
<appointments>
    <appointment>
        <starttime>2009-06-01T15:00:00</starttime>
        <endtime>2009-06-01T16:15:00</endtime>
        <subject>This is a Test-Appointment</subject>
        <location>At your Desk</location>
        <body>Here is the Bodytext</body>
    </appointment>
    <appointment>
        <starttime>2009-06-01T17:00:00</starttime>
        <endtime>2009-06-01T17:15:00</endtime>
        <subject>This is a second Test-Appointment</subject>
        <location>At your Desk</location>
        <body>Here is the Bodytext</body>
    </appointment>
    <appointment>
        <starttime>2009-06-01T17:00:00</starttime>
        <endtime>2009-06-01T18:15:00</endtime>
        <subject>This is a third Test-Appointment</subject>
        <location>At your Desk</location>
        <body>Here is the Bodytext</body>
    </appointment>
</appointments>
```

<span data-ttu-id="da435-p104">La méthode CreateAppointmentsFromXml utilise la mise en œuvre Microsoft COM du modèle XML DOM (Document Object Model) pour charger et traiter les données XML que xml fournit. CreateAppointmentsFromXml vérifie d’abord si xml spécifie une source de données XML valide. Si c’est le cas, il charge les données dans un document XML, [DOMDocument](https://msdn.microsoft.com/library/ms756987\(v=office.15\)). Sinon, CreateAppointmentsFromXml génère une exception. Pour plus d’informations sur XML DOM, consultez [DOM](https://msdn.microsoft.com/library/ms766487\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="da435-p104">The CreateAppointmentsFromXml method uses the Microsoft COM implementation of the XML Document Object Model (DOM) to load and process the XML data that xml provides. CreateAppointmentsFromXml first checks whether xml specifies a valid source of XML data. If so, it loads the data into an XML document, [DOMDocument](https://msdn.microsoft.com/library/ms756987\(v=office.15\)). Otherwise, CreateAppointmentsFromXml throws an exception. For more information about the XML DOM, see [DOM](https://msdn.microsoft.com/library/ms766487\(v=office.15\)).</span></span>

<span data-ttu-id="da435-135">Pour chaque nœud enfant de rendez-vous délimité par la balise de rendez-vous dans les données XML, CreateAppointmentsFromXml recherche des balises spécifiques, utilise le DOM pour extraire les données et affecte les données aux propriétés correspondantes d’un objet **AppointmentItem** : [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)), [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611653\(v=office.15\)), [Location](https://msdn.microsoft.com/library/bb608946\(v=office.15\)), puis [Body](https://msdn.microsoft.com/library/bb644880\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="da435-135">For each appointment child node delimited by the appointment tag in the XML data, CreateAppointmentsFromXml looks for specific tags, uses the DOM to extract the data, and assigns the data to corresponding properties of an **AppointmentItem** object: [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)), [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611653\(v=office.15\)), [Location](https://msdn.microsoft.com/library/bb608946\(v=office.15\)), and [Body](https://msdn.microsoft.com/library/bb644880\(v=office.15\)).</span></span> <span data-ttu-id="da435-136">CreateAppointmentsFromXml enregistre ensuite le rendez-vous dans le calendrier par défaut.</span><span class="sxs-lookup"><span data-stu-id="da435-136">CreateAppointmentsFromXml then saves the appointment to the default calendar.</span></span>

<span data-ttu-id="da435-137">CreateAppointmentsFromXml utilise la méthode [Add](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.add?view=netframework-4.7.2) de la classe [List\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?view=netframework-4.7.2) dans l’espace de noms [System.Collections.Generic](https://docs.microsoft.com/dotnet/api/system.collections.generic?view=netframework-4.7.2) pour agréger ces objets AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="da435-137">CreateAppointmentsFromXml uses the [Add](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.add?view=netframework-4.7.2) method of the [List\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?view=netframework-4.7.2) class in the [System.Collections.Generic](https://docs.microsoft.com/dotnet/api/system.collections.generic?view=netframework-4.7.2) namespace to aggregate these AppointmentItem objects.</span></span> <span data-ttu-id="da435-138">Quand la méthode a traité tous les rendez-vous dans les données XML, elle renvoie les objets AppointmentItem dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="da435-138">When the method has processed all the appointments in the XML data, it returns the AppointmentItem objects in an array.</span></span>

<span data-ttu-id="da435-139">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="da435-139">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="da435-140">L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="da435-140">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="da435-141">Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.</span><span class="sxs-lookup"><span data-stu-id="da435-141">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```



```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

<span data-ttu-id="da435-142">L’exemple suivant est un exemple de code Visual Basic, suivi de l’exemple de code C\#.</span><span class="sxs-lookup"><span data-stu-id="da435-142">The following is the Visual Basic code example, followed by the C\# code example.</span></span>



```vb
Imports System.IO
Imports System.Xml
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample
        Function CreateAppointmentsFromXml(ByVal application As Outlook.Application, _
            ByVal xml As String) As Outlook.AppointmentItem()

            Dim appointments As New List(Of Outlook.AppointmentItem)
            Dim xmlDoc As New XmlDocument()

            ' If xml is an XML string, create the XML document directly.
            If xml.StartsWith("<?xml") Then
                xmlDoc.LoadXml(xml)
            ElseIf (File.Exists(xml)) Then
                xmlDoc.Load(xml)
            Else
                Throw New Exception("The input string is not valid XML data or the specified file doesn't exist.")
            End If


            ' Select all appointment nodes under the root appointments node.
            Dim appointmentNodes As XmlNodeList = xmlDoc.SelectNodes("appointments/appointment")

            For Each appointmentNode As XmlNode In appointmentNodes

                ' Create a new AppointmentItem object.
                Dim newAppointment As Outlook.AppointmentItem = _
                    DirectCast(application.CreateItem(Outlook.OlItemType.olAppointmentItem), _
                    Outlook.AppointmentItem)

                ' Loop over all child nodes, check the node name, and import the data into the appointment fields.

                For Each node As XmlNode In appointmentNode.ChildNodes
                    Select Case (node.Name)

                        Case "starttime"
                            newAppointment.Start = DateTime.Parse(node.InnerText)


                        Case "endtime"
                            newAppointment.End = DateTime.Parse(node.InnerText)


                        Case "subject"
                            newAppointment.Subject = node.InnerText


                        Case "location"
                            newAppointment.Location = node.InnerText


                        Case "body"
                            newAppointment.Body = node.InnerText


                    End Select
                Next

                ' Save the item in the default calendar.
                newAppointment.Save()
                appointments.Add(newAppointment)
            Next

            ' Return an array of new appointments.
            Return appointments.ToArray()
        End Function


    End Class
End Namespace
```



```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Text;
using System.Xml;
using Outlook = Microsoft.Office.Interop.Outlook;

namespace OutlookAddIn1
{
    class Sample
    {
        Outlook.AppointmentItem[] CreateAppointmentsFromXml(Outlook.Application application, 
            string xml)
        {
            // Create a list of appointment objects.
            List<Outlook.AppointmentItem> appointments = new 
                List<Microsoft.Office.Interop.Outlook.AppointmentItem>();
            XmlDocument xmlDoc = new XmlDocument();

            // If xml is an XML string, create the document directly. 
            if (xml.StartsWith("<?xml"))
            {
                xmlDoc.LoadXml(xml);
            }
            else if (File.Exists(xml))
            {
                xmlDoc.Load(xml);
            }
            else
            {
                throw new Exception(
                    "The input string is not valid XML data or the specified file doesn't exist.");
            }

            // Select all appointment nodes under the root appointments node.
            XmlNodeList appointmentNodes = xmlDoc.SelectNodes("appointments/appointment");
            foreach (XmlNode appointmentNode in appointmentNodes)
            {

                // Create a new AppointmentItem object.
                Outlook.AppointmentItem newAppointment = 
                    (Outlook.AppointmentItem)application.CreateItem(Outlook.OlItemType.olAppointmentItem);

                // Loop over all child nodes, check the node name, and import the data into the 
                // appointment fields.
                foreach (XmlNode node in appointmentNode.ChildNodes)
                {
                    switch (node.Name)
                    {

                        case "starttime":
                            newAppointment.Start = DateTime.Parse(node.InnerText);
                            break;

                        case "endtime":
                            newAppointment.End = DateTime.Parse(node.InnerText);
                            break;

                        case "subject":
                            newAppointment.Subject = node.InnerText;
                            break;

                        case "location":
                            newAppointment.Location = node.InnerText;
                            break;

                        case "body":
                            newAppointment.Body = node.InnerText;
                            break;

                    }
                }

                // Save the item in the default calendar.
                newAppointment.Save();
                appointments.Add(newAppointment);
            }

            // Return an array of new appointments.
            return appointments.ToArray();
        }

    }
}
```

## <a name="see-also"></a><span data-ttu-id="da435-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da435-143">See also</span></span>

- [<span data-ttu-id="da435-144">Rendez-vous</span><span class="sxs-lookup"><span data-stu-id="da435-144">Appointments</span></span>](appointments.md)

