---
title: Connexion de gestionnaires d’événements personnalisés
TOCTitle: Connecting to custom event handlers
ms:assetid: 6e894c16-0fe9-4b86-b798-547b86f44cd8
ms:mtpsurl: https://msdn.microsoft.com/library/Bb610520(v=office.15)
ms:contentKeyID: 55119783
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 31e9a5453bbfbd4a51132fa6af71b86889b4b32e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406105"
---
# <a name="connecting-to-custom-event-handlers"></a>Connexion de gestionnaires d’événements personnalisés

Outlook déclenche des événements pour notifier les compléments de quelque chose qui se passe, comme la Boîte de réception qui reçoit un nouvel élément de courrier. Les compléments peuvent indiquer à Outlook qu'en cas d'occurrence d'un événement spécifique, certaines actions doivent être entreprises. Ce mécanisme d'alerte et de rappel est pris en charge par les délégués du .NET Framework. L'assembly PIA (Primary Interop Assembly) Outlook définit les délégués auxquels vous pouvez connecter des méthodes de rappel pour gérer des événements correspondants. Cette rubrique décrit le processus de définition d'une méthode de rappel et de sa connexion à l'objet Outlook en tant que gestionnaire d'événements.

## <a name="creating-a-callback-method"></a>Création d’une méthode de rappel

Un rappel est une méthode implémentée pour gérer l'occurrence d'un événement spécifique et est exécuté par une source de notification. Dans Outlook, les compléments peuvent implémenter des méthodes de rappel afin de répondre à certains événements déclenchés par Outlook. Cette méthode de rappel doit correspondre à la signature du délégué de cet événement. Par exemple, pour implémenter un gestionnaire d'événements pour l'événement [ItemSend](https://msdn.microsoft.com/library/bb647198\(v=office.15\)), vous devez déclarer la méthode de rappel qui correspond à la signature du délégué correspondant :

```csharp
public delegate void ApplicationEvents_11_ItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Delegate Sub ApplicationEvents_11_ItemSendEventHandler(_
    ByVal Item As Object, ByRef Cancel As Boolean)
```

Quand vous définissez la méthode de rappel, ignorez le mot clé **Delegate** qui sert à définir un autre délégué. Un exemple de méthode de rappel **MyItemSendEventHandler** est illustré ci-dessous :

```csharp
public void MyItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Sub MyItemSendEventHandler (_
    ByVal Item As Object, ByRef Cancel As Boolean)
…
End Sub
```

## <a name="connecting-a-callback-method"></a>Connexion d’une méthode de rappel

Après avoir implémenté une méthode de rappel pour un événement, vous pouvez la connecter à l'objet Outlook afin qu'Outlook sache qu'il doit appeler cette méthode comme gestionnaire d'événements pour cet événement. Notez qu'un événement peut être géré par plusieurs gestionnaires d'événements, d'où la nécessité de délégués qui affectent la gestion des événements aux gestionnaires d'événements.

Pour reprendre l’exemple précédent indiquant un gestionnaire pour l’événement **ItemSend** de l’objet **Application**, pour connecter **MyItemSendEventHandler** à l’objet **Application** en C\#, créez une instance de l’objet délégué, transmettez **MyItemSendEventHandler** au constructeur de cet objet, puis ajoutez l’objet délégué à l’événement **ItemSend** en utilisant l’opérateur += :

```csharp
app.ItemSend += new ApplicationEvents_11_ItemSendEventHandler(MyItemSendEventHandler)
```

Dans Visual Basic, vous utilisez l’instruction **AddHandler** pour associer l’événement **ItemSend** avec le gestionnaire d’événements **MyItemSendEventHandler** :

```vb
AddHandler app.ItemSend, AddressOf MyItemSendEventHandler
```

## <a name="see-also"></a>Voir aussi

- [Événements dans l’assembly PIA Outlook](events-in-the-outlook-pia.md)
- [Objets dans l'assembly PIA Outlook](objects-in-the-outlook-pia.md)

