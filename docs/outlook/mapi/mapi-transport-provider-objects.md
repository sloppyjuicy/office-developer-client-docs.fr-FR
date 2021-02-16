---
title: Objets de fournisseur de transport MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3f05e5b4b45e18d580737d37250e183c4cead881
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430356"
---
# <a name="mapi-transport-provider-objects"></a>Objets de fournisseur de transport MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Outre les objets fournisseur et d’accès standard implémentés par tous les fournisseurs de services, les fournisseurs de transport sont requis pour implémenter un objet d’état. Pour les autres types de fournisseurs de services, l’implémentation d’un objet d’état est facultative. Toutefois, MAPI l’exige pour les fournisseurs de transport. Les fournisseurs de transport qui peuvent télécharger des en-têtes de message à partir d’un serveur distant implémentent également un dossier et une table. 
  
L’illustration suivante montre chacun des objets que les fournisseurs de transport peuvent implémenter avec leurs interfaces correspondantes. L’illustration indique également si MAPI ou un client est l’utilisateur de l’objet.
  
![Objets implémentant par les fournisseurs de transport]des objets(media/amapi_66.gif "implémentant par les fournisseurs de transport")
  
## <a name="see-also"></a>Voir aussi

- [Objets du fournisseur de services MAPI](mapi-service-provider-objects.md)

