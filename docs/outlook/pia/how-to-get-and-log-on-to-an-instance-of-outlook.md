---
title: Obtention d’une instance d’Outlook pour s’y connecter
TOCTitle: Get and sign in to an instance of Outlook
ms:assetid: 7f5057dc-4232-4dc7-b597-16ff5f7bcd7d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462097(v=office.15)
ms:contentKeyID: 55119926
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 6aa4ecb0b6d9a3082759c7a3b0b4a5f677d1556e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406462"
---
# <a name="get-and-sign-in-to-an-instance-of-outlook"></a><span data-ttu-id="25953-102">Obtention d’une instance d’Outlook pour s’y connecter</span><span class="sxs-lookup"><span data-stu-id="25953-102">Get and sign in to an instance of Outlook</span></span>

<span data-ttu-id="25953-103">Cette rubrique explique comment obtenir un objet [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) qui représente une instance active de Microsoft Outlook, s’il en existe une s’exécutant sur l’ordinateur local, ou comment créer une nouvelle instance d’Outlook, se connecter au profil par défaut, et renvoyer cette instance d’Outlook.</span><span class="sxs-lookup"><span data-stu-id="25953-103">This topic shows how to obtain an [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object that represents an active instance of Microsoft Outlook, if there is one running on the local computer, or to create a new instance of Outlook, log on to the default profile, and return that instance of Outlook.</span></span>

## <a name="example"></a><span data-ttu-id="25953-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="25953-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="25953-105">Helmut Obertanner a fourni les exemples de code suivants.</span><span class="sxs-lookup"><span data-stu-id="25953-105">Helmut Obertanner provided the following code examples.</span></span> <span data-ttu-id="25953-106">L’expertise de Helmut se trouve dans les outils de développement Office pour Visual Studio et Outlook.</span><span class="sxs-lookup"><span data-stu-id="25953-106">Helmut's expertise is in Office Developer Tools for Visual Studio and Outlook.</span></span> 

<span data-ttu-id="25953-107">Les exemples de code suivants contiennent la méthode GetApplicationObject de la classe Sample, mise en œuvre dans le cadre d’un projet de complément Outlook.</span><span class="sxs-lookup"><span data-stu-id="25953-107">The following code examples contain the   method of the   class, implemented as part of an Outlook add-in project.</span></span> <span data-ttu-id="25953-108">Chaque projet ajoute une référence à l’assembly PIA (Primary Interop Assembly) Outlook, qui est basé sur l’espace de noms [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="25953-108">Each project adds a reference to the Outlook Primary Interop Assembly, which is based on the [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) namespace.</span></span>

<span data-ttu-id="25953-109">La méthode GetApplicationObject utilise les classes de la bibliothèque de classes .NET Framework pour vérifier et obtenir les processus Outlook s’exécutant sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="25953-109">The   method uses classes in the .NET Framework class library to check and obtain any Outlook process running on the local computer.</span></span> <span data-ttu-id="25953-110">Elle utilise d'abord la méthode [GetProcessesByName](https://msdn.microsoft.com/fr-FR/library/wbt7d3cy) de la classe [Process](https://msdn.microsoft.com/fr-FR/library/ccf1tfx0) dans l'espace de noms [System.Diagnostics](https://msdn.microsoft.com/fr-FR/library/15t15zda) pour obtenir un tableau des composants de processus sur l'ordinateur local qui partagent le nom de processus « OUTLOOK ».</span><span class="sxs-lookup"><span data-stu-id="25953-110">It first uses the [GetProcessesByName](https://msdn.microsoft.com/fr-FR/library/wbt7d3cy) method of the [Process](https://msdn.microsoft.com/fr-FR/library/ccf1tfx0) class in the [System.Diagnostics](https://msdn.microsoft.com/fr-FR/library/15t15zda) namespace to obtain an array of process components on the local computer that share the process name "OUTLOOK".</span></span> <span data-ttu-id="25953-111">Pour vérifier si le tableau contient au moins un processus Outlook, GetApplicationObject utilise LINQ (Microsoft Language Integrated Query).</span><span class="sxs-lookup"><span data-stu-id="25953-111">To check whether the array does contain at least one Outlook process,   uses Microsoft Language Integrated Query (LINQ).</span></span> <span data-ttu-id="25953-112">La classe [Enumerable](https://msdn.microsoft.com/fr-FR/library/bb345746) dans l'espace de noms [System.Linq](https://msdn.microsoft.com/fr-FR/library/bb336768) fournit un ensemble de méthodes, dont la méthode [Count](https://msdn.microsoft.com/fr-FR/library/bb357758) , qui implémentent l'interface générique [IEnumerable\<T\>](https://msdn.microsoft.com/fr-FR/library/9eekhta0) .</span><span class="sxs-lookup"><span data-stu-id="25953-112">The [Enumerable](https://msdn.microsoft.com/fr-FR/library/bb345746) class in the [System.Linq](https://msdn.microsoft.com/fr-FR/library/bb336768) namespace provides a set of methods, including the [Count](https://msdn.microsoft.com/fr-FR/library/bb357758) method, that implement the [IEnumerable\<T\>](https://msdn.microsoft.com/fr-FR/library/9eekhta0) generic interface.</span></span> <span data-ttu-id="25953-113">Comme la classe [Array](https://msdn.microsoft.com/fr-FR/library/czz5hkty) implémente l’interface **IEnumerable(T)**, GetApplicationObject peut appliquer la méthode **Count** au tableau renvoyé par **GetProcessesByName** pour vérifier si un processus Outlook s’exécute.</span><span class="sxs-lookup"><span data-stu-id="25953-113">Because the Array class implements the IEnumerable(T) interface,   can apply the Count method to the array returned by GetProcessesByName to see whether there is an Outlook process running.</span></span> <span data-ttu-id="25953-114">Si c’est le cas, GetApplicationObject utilise la méthode [GetActiveObject](https://msdn.microsoft.com/fr-FR/library/xt620x09) de la classe [Marshal](https://msdn.microsoft.com/fr-FR/library/asx0thw2) dans l’espace de noms [System.Runtime.InteropServices](https://msdn.microsoft.com/library/9esea608\(v=office.15\)) pour obtenir cette instance d’Outlook et diffuse cet objet à un objet [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) Outlook.</span><span class="sxs-lookup"><span data-stu-id="25953-114">If there is,   uses the GetActiveObject method of the Marshal class in the System.Runtime.InteropServices namespace to obtain that instance of Outlook, and casts that object to an Outlook Application object.</span></span>

<span data-ttu-id="25953-115">Si Outlook ne s’exécute pas sur l’ordinateur local, GetApplicationObject crée une nouvelle instance d’Outlook, utilise la méthode [Logon(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb646718\(v=office.15\)) de l’objet [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) pour se connecter au profil par défaut, et renvoie cette nouvelle instance d’Outlook.</span><span class="sxs-lookup"><span data-stu-id="25953-115">If Outlook is not running on the local computer,   creates a new instance of Outlook, uses the Logon(Object, Object, Object, Object) method of the NameSpace object to log on to the default profile, and returns that new instance of Outlook.</span></span>

<span data-ttu-id="25953-116">L’exemple suivant est un exemple de code Visual Basic, suivi de l’exemple de code C\#.</span><span class="sxs-lookup"><span data-stu-id="25953-116">The following is the Visual Basic code example, followed by the C# code example.</span></span>

<span data-ttu-id="25953-117">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="25953-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="25953-118">L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="25953-118">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="25953-119">Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.</span><span class="sxs-lookup"><span data-stu-id="25953-119">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="25953-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25953-120">See also</span></span>

- [<span data-ttu-id="25953-121">Sessions</span><span class="sxs-lookup"><span data-stu-id="25953-121">Sessions</span></span>](sessions.md)

