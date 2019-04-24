---
title: Objets du fournisseur de transport MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 3f05e5b4b45e18d580737d37250e183c4cead881
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357374"
---
# <a name="mapi-transport-provider-objects"></a>Objets du fournisseur de transport MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
En plus du fournisseur standard et des objets d'ouverture de session implémentés par tous les fournisseurs de services, les fournisseurs de transport sont requis pour implémenter un objet d'État. Pour les autres types de fournisseurs de services, l'implémentation d'un objet Status est facultative. Toutefois, MAPI l'exige pour les fournisseurs de transport. Les fournisseurs de transport qui prennent en charge le téléchargement des en-têtes de message à partir d'un serveur distant implémentent également un dossier et un tableau. 
  
L'illustration suivante montre chacun des objets que les fournisseurs de transport peuvent implémenter avec leurs interfaces correspondantes. L'illustration indique également si MAPI ou un client est l'utilisateur de l'objet.
  
![Objets implémentés par les fournisseurs de transport] (media/amapi_66.gif "Objets implémentés par les fournisseurs de transport")
  
## <a name="see-also"></a>Voir aussi

- [Objets du fournisseur de services MAPI](mapi-service-provider-objects.md)

