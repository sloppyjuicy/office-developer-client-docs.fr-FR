---
title: Vue d'ensemble de l'architecture MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00d2993c-d66a-4a00-9fb2-98696d29a007
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 98a723528a714918ad7e0f10534efb0d38ef139a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410076"
---
# <a name="mapi-architecture-overview"></a>Vue d'ensemble de l'architecture MAPI
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI définit une architecture modulaire, comme illustré dans l'illustration suivante.  
  
![Architecture d'Outlook 2010] (media/amapi_43.gif "Architecture d'Outlook 2010")
  
L'application MAPI est appelée application cliente, car il s'agit d'un client du sous-système MAPI. Les applications de messagerie utilisent la messagerie en tant que partie centrale de leur traitement et offrent des fonctionnalités de messagerie étendues, telles que l'échange d'informations de différents types dans différents formats et la possibilité d'enregistrer et d'organiser les informations localement. Les applications de messagerie, de planification et de flux de travail sont des exemples d'applications basées sur la messagerie.
  
Le sous-système MAPI est constitué d'une interface utilisateur commune et des interfaces de programmation. L'interface utilisateur commune est un ensemble de boîtes de dialogue qui donne aux applications client une apparence cohérente et des utilisateurs de manière cohérente.
  
MAPI dispose d'interfaces de programmation qui sont utilisées par le sous-système MAPI, par les développeurs de logiciels clients et par les développeurs de fournisseurs de services. L'interface de programmation MAPI est l'interface de programmation principale basée sur les objets. L'interface de programmation MAPI est similaire au modèle objet de composant OLE et est utilisée par le sous-système MAPI et les applications clientes basées sur la messagerie écrites en C ou C++. 
  
En tant que développeur de logiciels client, vous effectuez des appels MAPI directement via l'interface de programmation MAPI. Vous pouvez implémenter la messagerie avec une seule interface client MAPI ou une combinaison d'interfaces. Une seule application peut effectuer des appels à des méthodes ou des fonctions appartenant à l'une des interfaces.
  
## <a name="see-also"></a>Voir aussi

-[Architecture et fonctionnalités MAPI](mapi-features-and-architecture.md)

