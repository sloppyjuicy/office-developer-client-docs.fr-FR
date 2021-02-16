---
title: Connexion de gestionnaires d’événements personnalisés
TOCTitle: Connecting to custom event handlers
ms:assetid: 6e894c16-0fe9-4b86-b798-547b86f44cd8
ms:mtpsurl: https://msdn.microsoft.com/library/Bb610520(v=office.15)
ms:contentKeyID: 55119783
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 58722b8b140f89f0fe29a3e52db578a423a0160a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351421"
---
# <a name="connecting-to-custom-event-handlers"></a><span data-ttu-id="a8cbb-102">Connexion de gestionnaires d’événements personnalisés</span><span class="sxs-lookup"><span data-stu-id="a8cbb-102">Connecting to custom event handlers</span></span>

<span data-ttu-id="a8cbb-p101">Outlook déclenche des événements pour notifier les compléments de quelque chose qui se passe, comme la Boîte de réception qui reçoit un nouvel élément de courrier. Les compléments peuvent indiquer à Outlook qu'en cas d'occurrence d'un événement spécifique, certaines actions doivent être entreprises. Ce mécanisme d'alerte et de rappel est pris en charge par les délégués du .NET Framework. L'assembly PIA (Primary Interop Assembly) Outlook définit les délégués auxquels vous pouvez connecter des méthodes de rappel pour gérer des événements correspondants. Cette rubrique décrit le processus de définition d'une méthode de rappel et de sa connexion à l'objet Outlook en tant que gestionnaire d'événements.</span><span class="sxs-lookup"><span data-stu-id="a8cbb-p101">Outlook raises events to notify add-ins about something happening, such as the Inbox receiving a new mail item. Add-ins can specify to Outlook that upon the occurrence of a specific event, certain actions should take place. This alert and callback mechanism is supported by delegates of the .NET Framework. The Outlook Primary Interop Assembly (PIA) defines delegates to which you can connect callback methods to handle corresponding events. This topic describes this process of defining a callback method and connecting it as an event handler to the Outlook object.</span></span>

## <a name="creating-a-callback-method"></a><span data-ttu-id="a8cbb-108">Création d’une méthode de rappel</span><span class="sxs-lookup"><span data-stu-id="a8cbb-108">Creating a Callback method</span></span>

<span data-ttu-id="a8cbb-p102">Un rappel est une méthode implémentée pour gérer l'occurrence d'un événement spécifique et est exécuté par une source de notification. Dans Outlook, les compléments peuvent implémenter des méthodes de rappel afin de répondre à certains événements déclenchés par Outlook. Cette méthode de rappel doit correspondre à la signature du délégué de cet événement. Par exemple, pour implémenter un gestionnaire d'événements pour l'événement [ItemSend](https://msdn.microsoft.com/library/bb647198\(v=office.15\)), vous devez déclarer la méthode de rappel qui correspond à la signature du délégué correspondant :</span><span class="sxs-lookup"><span data-stu-id="a8cbb-p102">A callback is a method that is implemented to handle the occurrence of a specific event and is executed by a notification source. In Outlook, add-ins can implement callback methods to respond to certain events raised by Outlook. This callback method must match the signature of the delegate of that event. For example, to implement an event handler for the [ItemSend](https://msdn.microsoft.com/library/bb647198\(v=office.15\)) event, you must declare the callback method that matches the signature of the corresponding delegate:</span></span>

```csharp
public delegate void ApplicationEvents_11_ItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Delegate Sub ApplicationEvents_11_ItemSendEventHandler(_
    ByVal Item As Object, ByRef Cancel As Boolean)
```

<span data-ttu-id="a8cbb-p103">Quand vous définissez la méthode de rappel, ignorez le mot clé **Delegate** qui sert à définir un autre délégué. Un exemple de méthode de rappel **MyItemSendEventHandler** est illustré ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="a8cbb-p103">When defining the callback method, ignore the **Delegate** keyword which otherwise would define another delegate. A sample callback method, **MyItemSendEventHandler**, is shown below:</span></span>

```csharp
public void MyItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Sub MyItemSendEventHandler (_
    ByVal Item As Object, ByRef Cancel As Boolean)
…
End Sub
```

## <a name="connecting-a-callback-method"></a><span data-ttu-id="a8cbb-115">Connexion d’une méthode de rappel</span><span class="sxs-lookup"><span data-stu-id="a8cbb-115">Connecting a Callback method</span></span>

<span data-ttu-id="a8cbb-p104">Après avoir implémenté une méthode de rappel pour un événement, vous pouvez la connecter à l'objet Outlook afin qu'Outlook sache qu'il doit appeler cette méthode comme gestionnaire d'événements pour cet événement. Notez qu'un événement peut être géré par plusieurs gestionnaires d'événements, d'où la nécessité de délégués qui affectent la gestion des événements aux gestionnaires d'événements.</span><span class="sxs-lookup"><span data-stu-id="a8cbb-p104">After implementing a callback method for an event, you can connect it to the Outlook object so that Outlook knows to call the method as an event handler of that event. Note that an event can be handled by more than one event handler, and this is where delegates that assign event handling to event handlers come into play.</span></span>

<span data-ttu-id="a8cbb-118">Pour reprendre l’exemple précédent indiquant un gestionnaire pour l’événement **ItemSend** de l’objet **Application**, pour connecter **MyItemSendEventHandler** à l’objet **Application** en C\#, créez une instance de l’objet délégué, transmettez **MyItemSendEventHandler** au constructeur de cet objet, puis ajoutez l’objet délégué à l’événement **ItemSend** en utilisant l’opérateur += :</span><span class="sxs-lookup"><span data-stu-id="a8cbb-118">Continuing with the last example of specifying a event handler for the **ItemSend** event of the **Application** object, to connect **MyItemSendEventHandler** to the **Application** object in C\#, create an instance of the delegate object, pass **MyItemSendEventHandler** to the constructor of the delegate object, and then add this delegate object to the **ItemSend** event using the += operator:</span></span>

```csharp
app.ItemSend += new ApplicationEvents_11_ItemSendEventHandler(MyItemSendEventHandler)
```

<span data-ttu-id="a8cbb-119">Dans Visual Basic, vous utilisez l’instruction **AddHandler** pour associer l’événement **ItemSend** avec le gestionnaire d’événements **MyItemSendEventHandler** :</span><span class="sxs-lookup"><span data-stu-id="a8cbb-119">In Visual Basic, you use the **AddHandler** statement to associate the **ItemSend** event with the **MyItemSendEventHandler** event handler:</span></span>

```vb
AddHandler app.ItemSend, AddressOf MyItemSendEventHandler
```

## <a name="see-also"></a><span data-ttu-id="a8cbb-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8cbb-120">See also</span></span>

- [<span data-ttu-id="a8cbb-121">Événements dans l’assembly PIA Outlook</span><span class="sxs-lookup"><span data-stu-id="a8cbb-121">Events in the Outlook PIA</span></span>](events-in-the-outlook-pia.md)
- [<span data-ttu-id="a8cbb-122">Objets dans l'assembly PIA Outlook</span><span class="sxs-lookup"><span data-stu-id="a8cbb-122">Objects in the Outlook PIA</span></span>](objects-in-the-outlook-pia.md)

