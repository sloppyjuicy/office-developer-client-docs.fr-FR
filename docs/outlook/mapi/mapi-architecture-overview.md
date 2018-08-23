---
title: Vue d’ensemble de l’architecture MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00d2993c-d66a-4a00-9fb2-98696d29a007
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a0f2efc17ca8790502f11d677498013cbe10205d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579353"
---
# <a name="mapi-architecture-overview"></a>Vue d’ensemble de l’architecture MAPI
 
**S’applique à**: Outlook 2013 | Outlook 2016 
  
MAPI définit une architecture modulaire, comme indiqué dans l’illustration suivante.  
  
![Architecture Outlook 2010] (media/amapi_43.gif "Architecture Outlook 2010")
  
L’application MAPI est appelée une application cliente car il s’agit d’un client du sous-système MAPI. Applications de messagerie utilisent la messagerie dans le cadre de leur traitement centrale et offrent des fonctionnalités de messagerie étendues, telles que l’échange d’informations de différents types dans différents formats et la possibilité d’enregistrer et organiser les informations localement. Message électronique, la planification, et les applications de flux de travail sont des exemples d’applications de messagerie.
  
Le sous-système MAPI est composé d’une interface utilisateur commune et les interfaces de programmation. L’interface utilisateur courants est un ensemble de boîtes de dialogue qui offre aux applications clientes en uniformiser l’apparence et les utilisateurs fonctionnent de manière cohérente.
  
MAPI a des interfaces qui sont utilisés par le sous-système MAPI, les développeurs de logiciels clients et par les développeurs de fournisseur de service de programmation. L’interface de programmation MAPI est l’interface de programmation orientée objet principal. L’interface de programmation MAPI est similaire au modèle d’objet OLE composant et est utilisée par le sous-système MAPI et les applications clientes de messagerie écrites en C ou C++. 
  
En tant que développeur de logiciels clients, effectuer des appels MAPI directement par le biais de l’interface de programmation MAPI. Vous pouvez implémenter de messagerie avec une interface de client MAPI unique ou une combinaison des interfaces. Une seule application pouvez émettre des appels aux méthodes ou aux fonctions appartenant à une des interfaces.
  
## <a name="see-also"></a>Voir aussi

-[Architecture et des fonctionnalités MAPI](mapi-features-and-architecture.md)

