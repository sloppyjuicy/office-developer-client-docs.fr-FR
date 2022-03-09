---
title: Objets de fournisseur de transport MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
ms.openlocfilehash: 6c239c014eaf77273d2d5c1ad97c9141406dfe32
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375390"
---
# <a name="mapi-transport-provider-objects"></a>Objets de fournisseur de transport MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Outre les objets fournisseur et d’accès standard implémentés par tous les fournisseurs de services, les fournisseurs de transport sont requis pour implémenter un objet d’état. Pour les autres types de fournisseurs de services, l’implémentation d’un objet d’état est facultative. Toutefois, MAPI l’exige pour les fournisseurs de transport. Les fournisseurs de transport qui supportent le téléchargement des en-têtes de message à partir d’un serveur distant implémentent également un dossier et une table. 
  
L’illustration suivante montre chacun des objets que les fournisseurs de transport peuvent implémenter avec leurs interfaces correspondantes. L’illustration indique également si MAPI ou un client est l’utilisateur de l’objet.
  
![Objets implémentés par les fournisseurs de transport](media/amapi_66.gif "Objets implémentés par les fournisseurs de transport")
  
## <a name="see-also"></a>Voir aussi

- [Objets du fournisseur de services MAPI](mapi-service-provider-objects.md)

