---
title: Événements dans l'assembly PIA Outlook
TOCTitle: Events in the Outlook PIA
ms:assetid: 1f9eafb3-6645-4e27-81fa-5d73bf94ae40
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb644571(v=office.15)
ms:contentKeyID: 55119782
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 29217a633c02390587a370847291ef62d5621ce8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325788"
---
# <a name="events-in-the-outlook-pia"></a>Événements dans l’assembly PIA Outlook

En parcourant l’assembly PIA (Primary Interop Assembly) Outlook, vous remarquerez peut-être que de nombreuses interfaces et délégués d’événements portent le nom d’objets familiers dans le modèle objet Outlook. Contrairement aux événements dans la bibliothèque de types COM, les événements de l’assembly PIA Outlook ne sont pas définis dans la même interface que les méthodes et propriétés du même objet. Les interfaces, délégués et classes d’assistance de récepteur liés aux événements sont importés ou créés afin de prendre en charge les événements dans l’assembly PIA Outlook. Cette rubrique décrit ces interfaces, délégués et classes d’assistance de récepteur liés aux événements.

## <a name="where-do-the-event-interfaces-delegates-and-sink-helper-classes-come-from"></a>Provenance des interfaces, délégués et classes d’assistance de récepteur liés aux événements

Pour créer l'assembly PIA Outlook, Outlook emploie l'importateur de bibliothèques de types (TLBIMP) dans le .NET Framework pour convertir les définitions de types dans la bibliothèque de types COM en définitions équivalentes dans un assembly CLR (Common Language Runtime). TLBIMP importe les deux types d'interfaces suivants pour chaque objet :

  - L’interface principale (par exemple, l’interface [\_Application](https://msdn.microsoft.com/library/bb611255\(v=office.15\)))

  - L’interface d’événement (par exemple, l’interface [ApplicationEvents\_11](https://msdn.microsoft.com/library/bb609229\(v=office.15\)))

TLBIMP traite les interfaces importées et crée un certain nombre d'interfaces, délégués et classes, y compris les interfaces .NET (par exemple, l'interface [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) ). Si l'objet possède des événements, les éléments suivants sont créés :

  - L’interface d’événement .NET (par exemple, l’interface [ApplicationEvents\_11\_Event](https://msdn.microsoft.com/library/bb622725\(v=office.15\)))

  - Un délégué pour chaque événement (par exemple, le délégué [ApplicationEvents\_11\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb610818\(v=office.15\)))

  - Une classe d’assistance de récepteur (par exemple, la classe [ApplicationEvents\_11\_SinkHelper](https://msdn.microsoft.com/library/bb609842\(v=office.15\)))

### <a name="multiple-versions-of-events"></a>Versions multiples des événements

Certains objets qui existent pour plusieurs versions d'Outlook ont différentes implémentations d'événements d'une version à une autre, et des événements supplémentaires ont été ajoutés lors de la publication des nouvelles versions. Pour prendre en charge les événements qui varient d'une version à une autre, Outlook effectue une distinction entre ces interfaces, délégués et classes liés aux événements en ajoutant un numéro de version à leur nom. Par exemple :

  - Les interfaces d'événements importées de l'objet **Application** incluent :
    
      - La version la plus ancienne pour Outlook 98 et Outlook 2000 : l’interface [ApplicationEvents](https://msdn.microsoft.com/library/bb644093\(v=office.15\))
    
      - La version pour Outlook 2002 : l’interface [ApplicationEvents\_10](https://msdn.microsoft.com/library/bb647702\(v=office.15\))
    
      - La version pour Outlook 2003 et versions ultérieures : l’interface [ApplicationEvents\_11](https://msdn.microsoft.com/library/bb609229\(v=office.15\))

  - Les interfaces événement .NET créées par TLBIMP pour l’objet **Application** incluent :
    
      - La version la plus ancienne pour Outlook 98 et Outlook 2000 : l’interface [ApplicationEvents\_Event](https://msdn.microsoft.com/library/bb609380\(v=office.15\))
    
      - La version pour Outlook 2002 : l’interface [ApplicationEvents\_10\_Event](https://msdn.microsoft.com/library/bb610098\(v=office.15\))
    
      - La version pour Outlook 2003 et versions ultérieures : l’interface [ApplicationEvents\_11\_Event](https://msdn.microsoft.com/library/bb622725\(v=office.15\))

  - Les délégués créés par TLBIMP pour chaque événement dans chaque version de l’objet **Application**, par exemple un délégué pour chaque version de l’événement ItemSend:
    
      - La version la plus ancienne pour Outlook 98 et Outlook 2000 : le délégué [ApplicationEvents\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb622515\(v=office.15\))
    
      - La version pour Outlook 2002 : le délégué [ApplicationEvents\_10\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb646436\(v=office.15\))
    
      - La version pour Outlook 2003 et versions ultérieures : le délégué [ApplicationEvents\_11\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb610818\(v=office.15\))

Logiquement, les événements ajoutés à une version ultérieure n’apparaissent pas dans les interfaces d’événements de versions antérieures et n’ont aucun délégué correspondant dans les versions antérieures. Par exemple, comme l’événement [AttachmentSelectionChange](https://msdn.microsoft.com/library/ff184926\(v=office.15\)) a été ajouté à l’objet [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) dans Outlook 2010, il ne fait pas partie des interfaces d’événements antérieures suivantes pour l’objet Explorer :

  - Interface ExplorerEvents

  - Interface ExplorerEvents\_Event

En revanche, l’événement figure dans l’interface d’événement .NET la plus récente, ExplorerEvents\_10\_Event, et son délégué pour la version Outlook 2010, [ExplorerEvents\_10\_AttachmentSelectionChangeEventHandler](https://msdn.microsoft.com/library/ff185177\(v=office.15\)).

## <a name="what-the-event-interfaces-delegates-and-sink-helper-classes-are-for"></a>Rôle des interfaces, délégués et classes d’assistance de récepteur liés aux événements

À l’aide de l’objet **Application** comme exemple, cette section décrit ce que contient chaque interface et classe listée ci-dessus :

  - L’interface principale, \_Application, définit toutes les méthodes et propriétés de Application. À l’exception d’une des conditions décrite ci-dessous, vous n’utiliserez généralement pas cette interface dans le code.

  - Les interfaces d’événements importées par TLBIMP, telles que ApplicationEvents\_11 et ApplicationEvents\_10, définissent le mappage des méthodes aux événements de Application dans la version correspondante d’Outlook. Vous n’utiliserez pas cette interface dans le code.

  - Les interfaces d’événements importées par TLBIMP, telles que ApplicationEvents\_11\_Event et ApplicationEvents\_10\_Event, définissent tous les événements de Application dans la version correspondante d’Outlook. Lors de la conception d’un gestionnaire d’événements pour un événement dans une version spécifique, vous devez implémenter le gestionnaire d’événements en tant que méthode et connecter la méthode à l’événement défini dans la version correspondante de l’interface d’événements .NET. À l’exception d’une des conditions décrite ci-dessous, vous ne référencerez généralement pas l’interface événements dans le code.

  - L’interface .NET, Application, hérite de l’interface \_Application et de l’interface ApplicationEvents\_11\_Event. En général, il s’agit de l’interface que l’on utilise dans le code managé pour accéder à l’objet, à la méthode, à la propriété et aux membres d’événements les plus récents de l’objet **Application**. Il existe toutefois deux exceptions où l'on n'utilise pas l'interface .NET mais une interface différente pour la connexion à un événement :
    
      - Lorsque vous accédez à un événement qui a le même nom qu'une méthode de cet objet, vous devez effectuer un cast vers l'interface d'événement appropriée afin d'établir la connexion à l'événement. Par exemple, pour vous connecter à l’événement [Quit](https://msdn.microsoft.com/library/bb622595\(v=office.15\)), vous devez effectuer un cast vers l’interface ApplicationEvents\_11\_Event.
    
      - Lorsque vous vous connectez à une version antérieure d’un événement qui a été étendu dans une version ultérieure d’Outlook, connectez-vous à la version de l’événement dans l’interface antérieure. Par exemple, si vous voulez vous connecter à la version de l’événement Quit de l’objet **Application** implémenté pour Outlook 2002 plutôt qu’à la dernière version, connectez-vous à l’événement [Quit](https://msdn.microsoft.com/library/bb609660\(v=office.15\)) défini dans l’interface ApplicationEvents\_10\_Event, au lieu de l’événement Quit défini dans l’interface ApplicationEvents\_11\_Event.

  - Les délégués fournissent une infrastructure vous permettant de créer des gestionnaires d’événements personnalisés pour des événements spécifiques dans une version spécifique d’Outlook. Par exemple, si vous souhaitez ajouter un contrôle vérifiant l’existence d’une ligne d’objet dans un élément Outlook juste avant de l’envoyer, vous devez implémenter ce contrôle dans une méthode de rappel ayant la même signature que le délégué, ApplicationEvents\_11\_ItemSendEventHandler. Ensuite, vous raccordez la méthode de rappel en tant que gestionnaire d’événements pour l’événement ItemSend qui est défini dans l’interface ApplicationEvents\_11\_Event. Pour plus d’informations sur la connexion de la méthode de rappel en tant que gestionnaire d’événements pour un objet, voir [Connexion à des gestionnaires d’événements personnalisés](connecting-to-custom-event-handlers.md).

  - Les classes d’assistance de récepteur créées par TLBIMP, par exemple ApplicationEvents\_11\_SinkHelper et [ApplicationEvents\_10\_SinkHelper](https://msdn.microsoft.com/library/bb644070\(v=office.15\)), sont des objets d’assistance d’événements pour des événements Application dans la version correspondante d’Outlook. N’utilisez pas ces classes dans le code.

## <a name="see-also"></a>Voir aussi

- [Mise en rapport de l’assembly PIA Outlook avec le modèle objet](relating-the-outlook-pia-with-the-object-model.md)
- [Objets dans l’assembly PIA Outlook](objects-in-the-outlook-pia.md)
- [Méthodes et propriétés dans l’assembly PIA Outlook](methods-and-properties-in-the-outlook-pia.md)
- [Développement de compléments managés Outlook à l’aide de l’assembly PIA Outlook](developing-managed-outlook-add-ins-using-the-outlook-pia.md)

