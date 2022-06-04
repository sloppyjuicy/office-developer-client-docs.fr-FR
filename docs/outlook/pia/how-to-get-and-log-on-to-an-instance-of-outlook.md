---
title: Obtention d’une instance d’Outlook pour s’y connecter
TOCTitle: Get and sign in to an instance of Outlook
ms:assetid: 7f5057dc-4232-4dc7-b597-16ff5f7bcd7d
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-get-and-log-on-to-an-instance-of-outlook?redirectedfrom=MSDN
ms:contentKeyID: 55119926
ms.date: 12/03/2019
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 978926392955e33d510bbad1b167583453e46336
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894235"
---
# <a name="get-and-sign-in-to-an-instance-of-outlook"></a>Obtention d’une instance d’Outlook pour s’y connecter

Cette rubrique explique comment obtenir un objet [Application](/dotnet/api/microsoft.office.interop.outlook.application) qui représente une instance active de Microsoft Outlook, s’il en existe une s’exécutant sur l’ordinateur local, ou comment créer une nouvelle instance d’Outlook, se connecter au profil par défaut, et renvoyer cette instance d’Outlook.

## <a name="example"></a>Exemple

> [!NOTE] 
> Helmut Obertanner a fourni les exemples de code suivants. L’expertise de Helmut se trouve dans les outils de développement Office pour Visual Studio et Outlook. 

Les exemples de code suivants contiennent la méthode GetApplicationObject de la classe Sample, mise en œuvre dans le cadre d’un projet de complément Outlook. Chaque projet ajoute une référence à l’assembly PIA (Primary Interop Assembly) Outlook, qui est basé sur l’espace de noms [Microsoft.Office.Interop.Outlook](/dotnet/api/microsoft.office.interop.outlook).

La méthode GetApplicationObject utilise les classes de la bibliothèque de classes .NET Framework pour vérifier et obtenir les processus Outlook s’exécutant sur l’ordinateur local. Elle utilise d'abord la méthode [GetProcessesByName](/dotnet/api/system.diagnostics.process.getprocessesbyname) de la classe [Process](/dotnet/api/system.diagnostics.process) dans l'espace de noms [System.Diagnostics](/dotnet/api/system.diagnostics) pour obtenir un tableau des composants de processus sur l'ordinateur local qui partagent le nom de processus « OUTLOOK ». Pour vérifier si le tableau contient au moins un processus Outlook, GetApplicationObject utilise LINQ (Microsoft Language Integrated Query). La classe [Enumerable](https://msdn.microsoft.com/library/bb345746) dans l'espace de noms [System.Linq](https://msdn.microsoft.com/library/bb336768) fournit un ensemble de méthodes, dont la méthode [Count](https://msdn.microsoft.com/library/bb357758) , qui implémentent l'interface générique [IEnumerable\<T\>](https://msdn.microsoft.com/library/9eekhta0) . Comme la classe [Array](https://msdn.microsoft.com/library/czz5hkty) implémente l’interface **IEnumerable(T)**, GetApplicationObject peut appliquer la méthode **Count** au tableau renvoyé par **GetProcessesByName** pour vérifier si un processus Outlook s’exécute. Si c’est le cas, GetApplicationObject utilise la méthode [GetActiveObject](https://msdn.microsoft.com/library/xt620x09) de la classe [Marshal](https://msdn.microsoft.com/library/asx0thw2) dans l’espace de noms [System.Runtime.InteropServices](https://msdn.microsoft.com/library/9esea608\(v=office.15\)) pour obtenir cette instance d’Outlook et diffuse cet objet à un objet [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) Outlook.

Si Outlook ne s’exécute pas sur l’ordinateur local, GetApplicationObject crée une nouvelle instance d’Outlook, utilise la méthode [Logon(Object, Object, Object, Object)](/dotnet/api/microsoft.office.interop.outlook._namespace.logon) de l’objet [NameSpace](/dotnet/api/microsoft.office.interop.outlook.namespace) pour se connecter au profil par défaut, et renvoie cette nouvelle instance d’Outlook.

L’exemple suivant est un exemple de code Visual Basic, suivi de l’exemple de code C\#.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable Outlook lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **Imports** ou **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration de classe publique. Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Imports System.Diagnostics
Imports System.Linq
Imports System.Reflection
Imports System.Runtime.InteropServices
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample

        Function GetApplicationObject() As Outlook.Application

            Dim application As Outlook.Application

            ' Check whether there is an Outlook process running.
            If Process.GetProcessesByName("OUTLOOK").Count() > 0 Then

                ' If so, use the GetActiveObject method to obtain the process and cast it to an Application object.
                application = DirectCast(Marshal.GetActiveObject("Outlook.Application"), Outlook.Application)
            Else

                ' If not, create a new instance of Outlook and sign in to the default profile.
                application = New Outlook.Application()
                Dim ns As Outlook.NameSpace = application.GetNamespace("MAPI")
                ns.Logon("", "", Missing.Value, Missing.Value)
                ns = Nothing
            End If

            ' Return the Outlook Application object.
            Return application
        End Function

    End Class
End Namespace
```


```csharp
using System;
using System.Diagnostics;
using System.Linq;
using System.Reflection;
using System.Runtime.InteropServices;
using Outlook = Microsoft.Office.Interop.Outlook;

namespace OutlookAddIn1
{
    class Sample
    {
        Outlook.Application GetApplicationObject()
        {

            Outlook.Application application = null;

            // Check whether there is an Outlook process running.
            if (Process.GetProcessesByName("OUTLOOK").Count() > 0)
            {

                // If so, use the GetActiveObject method to obtain the process and cast it to an Application object.
                application = Marshal.GetActiveObject("Outlook.Application") as Outlook.Application;
            }
            else
            {

                // If not, create a new instance of Outlook and sign in to the default profile.
                application = new Outlook.Application();
                Outlook.NameSpace nameSpace = application.GetNamespace("MAPI");
                nameSpace.Logon("", "", Missing.Value, Missing.Value);
                nameSpace = null;
            }

            // Return the Outlook Application object.
            return application;
        }

    }
}
```

## <a name="see-also"></a>Voir aussi

- [Sessions](sessions.md)

