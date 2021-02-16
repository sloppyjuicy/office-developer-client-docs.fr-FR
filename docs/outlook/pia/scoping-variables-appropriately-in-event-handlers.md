---
title: Définition de l’étendue des variables dans les gestionnaires d’événements
TOCTitle: Scoping variables appropriately in event handlers
ms:assetid: 95b71535-abfd-43f1-a471-2026b522eac1
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646475(v=office.15)
ms:contentKeyID: 55119788
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c8a1a418a315167cc96be5b9b5f65a0f4cd9ce44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342251"
---
# <a name="scoping-variables-appropriately-in-event-handlers"></a><span data-ttu-id="47155-102">Définition de l’étendue des variables dans les gestionnaires d’événements</span><span class="sxs-lookup"><span data-stu-id="47155-102">Scoping variables appropriately in event handlers</span></span>

<span data-ttu-id="47155-p101">Une erreur revient fréquemment lors de la programmation de gestionnaires d'événements : le gestionnaire d'événements est connecté à un objet qui a été déclaré avec une portée trop limitée pour la gestion de l'événement. La durée de vie de l'objet doit couvrir non seulement la fonction qui connecte la méthode de rappel en tant que gestionnaire d'événements de l'objet, mais aussi la méthode de rappel elle-même dans laquelle l'événement est géré. Dans le cas contraire, si l'objet est hors de portée et n'est plus défini dans la méthode de rappel, la méthode de rappel n'est pas appelée et l'événement n'est pas géré comme souhaité.</span><span class="sxs-lookup"><span data-stu-id="47155-p101">A common mistake in programming event handlers is connecting the event handler to an object that has been declared with a scope too limited for the purpose of handling the event. The object must have a life that spans not just over the function that connects the callback method as an event handler of the object, but also over the callback method itself where the event is actually handled. Otherwise, if the object is out of scope and is no longer defined in the callback method, the callback method is not called and the event is not handled as desired.</span></span>

<span data-ttu-id="47155-106">L’exemple suivant essaie de connecter la méthode de rappel MyNewInspector à l’événement [NewInspector](https://msdn.microsoft.com/library/bb612750\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="47155-106">The following example attempts to connect the MyNewInspector callback method to the [NewInspector](https://msdn.microsoft.com/library/bb612750\(v=office.15\)) event.</span></span> <span data-ttu-id="47155-107">Toutefois, la méthode de rappel est raccordée dans l'exemple de code à l'événement NewInspector d'un objet [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) dont la portée est limitée à la fonction Connect.</span><span class="sxs-lookup"><span data-stu-id="47155-107">However, the callback method is hooked up in the code sample to the NewInspector event of an [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) object that has a scope limited to the Connect function.</span></span> <span data-ttu-id="47155-108">Quand la méthode de rappel est finalement appelée, la fonction Connect est déjà fermée, l’objet Inspectors a déjà fait l’objet d’un nettoyage de la mémoire et MyNewInspector n’est jamais appelé.</span><span class="sxs-lookup"><span data-stu-id="47155-108">When the callback method is eventually called, the Connect function has already exited, the Inspectors object has already been garbage collected, and so MyNewInspector is never called.</span></span>

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

<span data-ttu-id="47155-p103">Dans cette situation, vous devez stocker l’objet Inspectors dans une variable plus permanente dont la durée de vie couvre l’ensemble de MyClass, y compris la méthode de rappel MyNewInspector. Dans l’exemple suivant, la portée de MyInspectors est l’ensemble de MyClass et la méthode de rappel est connectée pour la durée de vie de la classe.</span><span class="sxs-lookup"><span data-stu-id="47155-p103">The correct thing to do in this case is to store the Inspectors object in a more permanent variable whose lifetime spans over the entire MyClass, including the MyNewInspector callback method. In the following example, MyInspectors has a scope of the entire MyClass and ensures that the callback method is connected for the lifetime of the class.</span></span>

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

<span data-ttu-id="47155-111">En raison des différences syntaxiques dans la manière dont les différents langages connectent les gestionnaires d'événements, ce problème est moins courant dans les langages comme Visual Basic dans lesquels vous pouvez connecter un événement en spécifiant une instance de l'objet parent et définir la méthode de rappel en même temps.</span><span class="sxs-lookup"><span data-stu-id="47155-111">By virtue of the syntactic differences in how various languages connect event handlers, this issue is less common in languages such as Visual Basic where you can connect an event specifying an instance of the parent object, and define the callback method at the same time.</span></span> <span data-ttu-id="47155-112">L’exemple suivant en Visual Basic utilise le mot clé Handles pour connecter la méthode de rappel Region\_Expanded à l’événement [Expanded](https://msdn.microsoft.com/library/bb609515\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="47155-112">The following example in Visual Basic uses the Handles keyword to connect the Region\_Expanded callback method to the [Expanded](https://msdn.microsoft.com/library/bb609515\(v=office.15\)) event.</span></span> <span data-ttu-id="47155-113">Une instance de l’objet parent, Region, a une portée couvrant MyClass, y compris la méthode de rappel Region\_Expanded.</span><span class="sxs-lookup"><span data-stu-id="47155-113">An instance of the parent object, Region, has a scope that spans MyClass including the Region\_Expanded callback method.</span></span>

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

<span data-ttu-id="47155-114">Dans cet exemple, dans la mesure où la méthode de rappel Region\_Expanded est connectée à l’événement Expanded pour la durée de vie de la classe, la méthode de rappel est appelée si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="47155-114">In this example, because the Region\_Expanded callback method is connected to the Expanded event for the lifetime of the class, the callback method is called as appropriate.</span></span>

## <a name="see-also"></a><span data-ttu-id="47155-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47155-115">See also</span></span>

- [<span data-ttu-id="47155-116">Connexion à des gestionnaires d’événements personnalisés</span><span class="sxs-lookup"><span data-stu-id="47155-116">Connecting to custom event handlers</span></span>](connecting-to-custom-event-handlers.md)

