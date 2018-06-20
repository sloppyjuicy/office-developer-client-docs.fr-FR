---
title: Objets du fournisseur de transport MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 2d7311857ff54ef253fd00634671f4a510443f19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784722"
---
# <a name="mapi-transport-provider-objects"></a>Objets du fournisseur de transport MAPI
  
**S’applique à**: Outlook 
  
Outre le fournisseur standard et objets d’ouverture de session implémentées par tous les fournisseurs de services, les fournisseurs de transport sont requis pour implémenter un objet d’état. Pour les autres types de fournisseur de service, l’implémentation d’un objet d’état est facultative. Toutefois, MAPI exige des fournisseurs de transport. Fournisseurs de transport qui prennent en charge le téléchargement des en-têtes des messages à partir d’un serveur distant également implémentent un dossier et une table. 
  
L’illustration suivante montre chacun des objets qui implémentent des fournisseurs de transport peuvent avec leurs interfaces correspondantes. L’illustration indique également si MAPI ou un client est utilisateur de l’objet.
  
![Objets qui implémentent des fournisseurs de transport] (media/amapi_66.gif "Objets qui implémentent des fournisseurs de transport")
  
## <a name="see-also"></a>Voir aussi

- [Objets du fournisseur de services MAPI](mapi-service-provider-objects.md)

