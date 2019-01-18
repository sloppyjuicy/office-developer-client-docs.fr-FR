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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705385"
---
# <a name="import-appointment-xml-data-into-outlook-appointment-objects"></a>Importation des données XML d’un rendez-vous dans les objets de rendez-vous Outlook

Cette rubrique montre comment lire des données de rendez-vous au format XML, enregistrer les données dans des objets Outlook [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) dans le calendrier par défaut, puis renvoyer les objets de rendez-vous dans un tableau.

## <a name="example"></a>Exemple

> [!NOTE] 
> Helmut Obertanner a fourni les exemples de code suivants. L’expertise de Helmut se trouve dans les outils de développement Office pour Visual Studio et Outlook. 


Les exemples de code suivants contiennent la méthode CreateAppointmentsFromXml de la classe Sample, implémentée dans le cadre d’un projet de complément Outlook. Chaque projet ajoute une référence à l’assembly PIA (Primary Interop Assembly) Outlook, qui est basé sur l’espace de noms [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)).

La méthode CreateAppointmentsFromXml accepte deux paramètres d’entrée :

  - l’application est un objet [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) Outlook approuvé.

  - xml est une chaîne XML ou une chaîne qui représente un chemin d’accès à un fichier XML valide. Dans les exemples de code suivants, le code XML délimite les données de rendez-vous en utilisant les balises XML suivantes :
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p>Données de rendez-vous</p></th>
    <th><p>Balise XML de délimitation</p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>Ensemble de données de rendez-vous</p></td>
    <td><p>rendez-vous ;</p></td>
    </tr>
    <tr class="even">
    <td><p>Chaque rendez-vous de l’ensemble de données</p></td>
    <td><p>rendez-vous</p></td>
    </tr>
    <tr class="odd">
    <td><p>Heure de début d’un rendez-vous</p></td>
    <td><p>starttime</p></td>
    </tr>
    <tr class="even">
    <td><p>Heure de fin d’un rendez-vous</p></td>
    <td><p>endtime</p></td>
    </tr>
    <tr class="odd">
    <td><p>Titre d’un rendez-vous</p></td>
    <td><p>subject</p></td>
    </tr>
    <tr class="even">
    <td><p>Emplacement d’un rendez-vous</p></td>
    <td><p>location</p></td>
    </tr>
    <tr class="odd">
    <td><p>Détails d’un rendez-vous</p></td>
    <td><p>body</p></td>
    </tr>
    </tbody>
    </table>


L’exemple suivant montre les données d’entrée du paramètre *xml*.

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

La méthode CreateAppointmentsFromXml utilise la mise en œuvre Microsoft COM du modèle XML DOM (Document Object Model) pour charger et traiter les données XML que xml fournit. CreateAppointmentsFromXml vérifie d’abord si xml spécifie une source de données XML valide. Si c’est le cas, il charge les données dans un document XML, [DOMDocument](https://msdn.microsoft.com/library/ms756987\(v=office.15\)). Sinon, CreateAppointmentsFromXml génère une exception. Pour plus d’informations sur XML DOM, consultez [DOM](https://msdn.microsoft.com/library/ms766487\(v=office.15\)).

Pour chaque nœud enfant de rendez-vous délimité par la balise de rendez-vous dans les données XML, CreateAppointmentsFromXml recherche des balises spécifiques, utilise le DOM pour extraire les données et affecte les données aux propriétés correspondantes d’un objet **AppointmentItem** : [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)), [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611653\(v=office.15\)), [Location](https://msdn.microsoft.com/library/bb608946\(v=office.15\)), puis [Body](https://msdn.microsoft.com/library/bb644880\(v=office.15\)). CreateAppointmentsFromXml enregistre ensuite le rendez-vous dans le calendrier par défaut.

CreateAppointmentsFromXml utilise la méthode [Add](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.add?view=netframework-4.7.2) de la classe [List\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?view=netframework-4.7.2) dans l’espace de noms [System.Collections.Generic](https://docs.microsoft.com/dotnet/api/system.collections.generic?view=netframework-4.7.2) pour agréger ces objets AppointmentItem. Quand la méthode a traité tous les rendez-vous dans les données XML, elle renvoie les objets AppointmentItem dans un tableau.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```



```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

L’exemple suivant est un exemple de code Visual Basic, suivi de l’exemple de code C\#.



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

## <a name="see-also"></a>Voir aussi

- [Rendez-vous](appointments.md)

