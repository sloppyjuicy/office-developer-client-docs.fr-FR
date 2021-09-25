---
title: Liaison de l’assembly PIA Outlook au modèle objet
TOCTitle: Relating the Outlook PIA with the object model
ms:assetid: 2875c324-cead-4250-b81b-3b7458a9f09e
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb609695(v=office.15)
ms:contentKeyID: 55119779
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c1e31485efa80ba636789aa946e4ef0b1aaef6c6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629206"
---
# <a name="relating-the-outlook-pia-with-the-object-model"></a>Liaison de l’assembly PIA Outlook au modèle objet

L’assembly PIA (Primary Interop Assembly) Outlook est un assembly d’interopérabilité officiellement publié par Outlook définissant une interface managée permettant aux compléments managés d’interagir avec le modèle objet COM d’Outlook. [Introduction à l’interopérabilité entre COM et .NET](introduction-to-interoperability-between-com-and-net.md) décrit, du point de vue technique, comment un assembly d’interopérabilité prend en charge une programmation client managée sur une bibliothèque de types COM. Cette rubrique fournit une vue d'ensemble de la façon dont les objets et membres d'un modèle objet COM Outlook sont mappés aux interfaces et classes managées correspondantes dans l'assembly PIA.

## <a name="helper-objects"></a>Objets d’assistance

Lorsque l’on compare les objets de la bibliothèque d’objets Outlook répertoriés dans l’Explorateur d’objets de Visual Basic Editor, comme à la Figure 1, avec les objets de l’assembly PIA répertoriés dans l’Explorateur d’objets de Visual Studio, comme à la Figure 2, on peut être surpris du très grand nombre d’objets d’assistance supplémentaires qui existent dans l’assembly PIA. Vous remarquerez peut-être que certains objets, tels l'objet **Action**, sont mappés à une interface, l'interface [Action](https://msdn.microsoft.com/library/bb646971\(v=office.15\)) , tandis que d'autres objets, tels l'objet **Account**, ne sont pas nécessairement mappés à exactement une interface correspondante dans l'assembly PIA.

**Figure 1. Explorateur d’objets montrant les objets de la bibliothèque d’objets COM d’Outlook**

![Explorateur d’objets montrant les objets de la bibliothèque d’objets COM d’Outlook](media/pia-vba-project.gif)

**Figure 2. Explorateur d’objets montrant les objets d’Outlook**

![Explorateur d’objets montrant les objets de d’Outlook](media/pia-object-browser.jpg)

Parmi ces interfaces, une grande partie ont des noms qui commencent par un caractère de soulignement (’\_’) suivi d’un nom d’objet. Par exemple, l’objet **Account** est mappé à une interface publique \_Account et à une classe publique Account dans l’Explorateur d’objets de Visual Studio. En fait, bien que cela ne soit pas affiché de manière explicite dans l’Explorateur d’objets de Visual Studio, l’objet **Account** est mappé à deux interfaces et à une classe dans l’assembly PIA : une interface [\_Account](https://msdn.microsoft.com/library/bb609471\(v=office.15\)), une coclasse [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) et une classe [AccountClass](https://msdn.microsoft.com/library/bb645768\(v=office.15\)). 

Pour plus d'informations sur ces interfaces, coclasses et classes, sur leur provenance et sur la façon dont les objets sont mappés de la bibliothèque de types vers l'assembly PIA, voir [Objets dans l'assembly PIA Outlook](objects-in-the-outlook-pia.md).

## <a name="separate-event-interfaces"></a>Interfaces d’événements distinctes

Si l'on examine les objets qui ont des événements, on constate que les événements de l'assembly PIA ne sont pas groupés avec d'autres membres de méthodes et propriétés de cet objet, mais sont plutôt regroupés de façon à former leurs propres interfaces, gestionnaires d'événements et classes. 

Pour plus d’informations sur la façon dont les méthodes et propriétés sont mappées de la bibliothèque de types vers l’assembly PIA, reportez-vous à la rubrique [Méthodes et propriétés dans l’assembly PIA Outlook](methods-and-properties-in-the-outlook-pia.md). Pour plus d’informations sur les interfaces d’événements, les délégués et les classes, reportez-vous à la rubrique [Événements dans l’assembly PIA Outlook](events-in-the-outlook-pia.md).

## <a name="hidden-and-deprecated-objects"></a>Objets masqués et obsolètes

L’assembly PIA contient aussi des objets, membres et énumérations qui ont été déconseillés et éventuellement marqués comme masqués dans le modèle objet COM. La plupart de ces objets, membres et énumérations sont exposés dans l'assembly PIA. Toutefois, ils sont exposés uniquement à des fins d'exhaustivité de l'assembly PIA ; ils ne sont plus censés être utilisés par les développeurs de solutions et sont par conséquent très peu documentés. Il existe quelques exceptions telles que les objets **\_DocSiteControl** et **\_RecipientControl**, qui sont masqués dans la bibliothèque de types mais sont exposés et documenté comme objets de première classe dans la référence de l’assembly PIA. 

Pour plus d’informations sur l’objet **\_DocSiteControl**, reportez-vous à [\_DDocSiteControl](https://msdn.microsoft.com/library/bb609520\(v=office.15\)). Pour plus d’informations sur l’objet **\_RecipientControl**, reportez-vous à [\_DRecipientControl](https://msdn.microsoft.com/library/bb609501\(v=office.15\)).



