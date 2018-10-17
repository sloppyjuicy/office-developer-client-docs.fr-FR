---
title: Définition de l’étendue des variables dans les gestionnaires d’événements
TOCTitle: Scoping variables appropriately in event handlers
ms:assetid: 95b71535-abfd-43f1-a471-2026b522eac1
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646475(v=office.15)
ms:contentKeyID: 55119788
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: ac26dfb245dd9b4621093a91ff36846c686f6e41
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407603"
---
# <a name="scoping-variables-appropriately-in-event-handlers"></a>Définition de l’étendue des variables dans les gestionnaires d’événements

Une erreur revient fréquemment lors de la programmation de gestionnaires d'événements : le gestionnaire d'événements est connecté à un objet qui a été déclaré avec une portée trop limitée pour la gestion de l'événement. La durée de vie de l'objet doit couvrir non seulement la fonction qui connecte la méthode de rappel en tant que gestionnaire d'événements de l'objet, mais aussi la méthode de rappel elle-même dans laquelle l'événement est géré. Dans le cas contraire, si l'objet est hors de portée et n'est plus défini dans la méthode de rappel, la méthode de rappel n'est pas appelée et l'événement n'est pas géré comme souhaité.

L’exemple suivant essaie de connecter la méthode de rappel MyNewInspector à l’événement [NewInspector](https://msdn.microsoft.com/library/bb612750\(v=office.15\)). Toutefois, la méthode de rappel est raccordée dans l'exemple de code à l'événement NewInspector d'un objet [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) dont la portée est limitée à la fonction Connect. Quand la méthode de rappel est finalement appelée, la fonction Connect est déjà fermée, l’objet Inspectors a déjà fait l’objet d’un nettoyage de la mémoire et MyNewInspector n’est jamais appelé.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

class MyClass
{
    private Outlook.Application MyApp;

    public MyClass(Outlook.Application appOutlook)
    {
        MyApp = appOutlook;
    }

    // Connects the NewInspector event to my callback method
    public void Connect()
    {
        MyApp.Inspectors.NewInspector += new Outlook.
            InspectorsEvents_NewInspectorEventHandler(
            MyNewInspector);
    }

    public void MyNewInspector(Outlook.Inspector inspector)
    {
        MessageBox.Show("
            My event handler caught a NewInspector event");
    }
}
```

<br/>

Dans cette situation, vous devez stocker l’objet Inspectors dans une variable plus permanente dont la durée de vie couvre l’ensemble de MyClass, y compris la méthode de rappel MyNewInspector. Dans l’exemple suivant, la portée de MyInspectors est l’ensemble de MyClass et la méthode de rappel est connectée pour la durée de vie de la classe.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

class MyClass
{
    private Outlook.Application MyApp;
    private Outlook.Inspectors MyInspectors;

    public MyClass(Outlook.Application appOutlook)
    {
        MyApp = appOutlook;
    }

    // Connects the NewInspector event to my callback method
    public void Connect()
    {
        MyInspectors = MyApp.Inspectors;
        MyInspectors.NewInspector += new Outlook.
            InspectorsEvents_NewInspectorEventHandler(
            MyNewInspector);
    }

    public void MyNewInspector(Outlook.Inspector inspector)
    {
        MessageBox.Show("
            My event handler caught a NewInspector event");
    }
}
```

<br/>

En raison des différences syntaxiques dans la manière dont les différents langages connectent les gestionnaires d'événements, ce problème est moins courant dans les langages comme Visual Basic dans lesquels vous pouvez connecter un événement en spécifiant une instance de l'objet parent et définir la méthode de rappel en même temps. L’exemple suivant en Visual Basic utilise le mot clé Handles pour connecter la méthode de rappel Region\_Expanded à l’événement [Expanded](https://msdn.microsoft.com/library/bb609515\(v=office.15\)). Une instance de l’objet parent, Region, a une portée couvrant MyClass, y compris la méthode de rappel Region\_Expanded.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook

Public Class MyClass
    ' The Region object has a lifetime spanning the class 
    ' including the callback method Region_Expanded
    Private WithEvents Region As Outlook.FormRegion
    ...
    Private Sub Region_Expanded() Handles Region.Expanded
        MsgBox("My EventHandler caught an Expanded event.")
    End Sub
End Class
```

Dans cet exemple, dans la mesure où la méthode de rappel Region\_Expanded est connectée à l’événement Expanded pour la durée de vie de la classe, la méthode de rappel est appelée si nécessaire.

## <a name="see-also"></a>Voir aussi

- [Connexion à des gestionnaires d’événements personnalisés](connecting-to-custom-event-handlers.md)

