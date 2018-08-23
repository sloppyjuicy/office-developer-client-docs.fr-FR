---
title: Architecture et des fonctionnalités MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 34bae703-a979-437c-9d86-8b91e9822a54
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: fbba349fd81240a33c08c5adb910c1236222fb30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568195"
---
# <a name="mapi-features-and-architecture"></a><span data-ttu-id="8808d-103">Architecture et des fonctionnalités MAPI</span><span class="sxs-lookup"><span data-stu-id="8808d-103">MAPI Features and Architecture</span></span>

  
  
<span data-ttu-id="8808d-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8808d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8808d-105">Messaging API (MAPI) se compose d’un ensemble d’interfaces de programmation d’application commune et un composant de bibliothèque de liens dynamiques (DLL).</span><span class="sxs-lookup"><span data-stu-id="8808d-105">Messaging API (MAPI) is composed of a set of common application programming interfaces and a dynamic-link library (DLL) component.</span></span> <span data-ttu-id="8808d-106">Les interfaces sont utilisées pour créer et accéder à diverses applications de messagerie et systèmes de messagerie, qui offre un environnement de développement et d’utilisation uniform et fourniture d’indépendance true pour les deux.</span><span class="sxs-lookup"><span data-stu-id="8808d-106">The interfaces are used to create and access diverse messaging applications and messaging systems, offering a uniform environment for development and use, and providing true independence for both.</span></span> <span data-ttu-id="8808d-107">La DLL contient le sous-système MAPI, qui gère l’interaction entre les applications de messagerie frontale et les systèmes de messagerie principale et fournit une interface utilisateur commune pour les tâches fréquentes.</span><span class="sxs-lookup"><span data-stu-id="8808d-107">The DLL contains the MAPI subsystem, which manages the interaction between front-end messaging applications and back-end messaging systems and provides a common user interface for frequent tasks.</span></span> <span data-ttu-id="8808d-108">Le sous-système MAPI fonctionne comme un centre d’échanges central d’unifier les différents systèmes de messagerie et de protéger les clients de leurs différences.</span><span class="sxs-lookup"><span data-stu-id="8808d-108">The MAPI subsystem acts as a central clearinghouse to unify the various messaging systems and shield clients from their differences.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8808d-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8808d-109">See also</span></span>



[<span data-ttu-id="8808d-110">Concepts MAPI</span><span class="sxs-lookup"><span data-stu-id="8808d-110">MAPI Concepts</span></span>](mapi-concepts.md)

