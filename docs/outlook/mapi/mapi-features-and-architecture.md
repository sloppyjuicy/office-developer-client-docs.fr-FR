---
title: Architecture et fonctionnalités MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 34bae703-a979-437c-9d86-8b91e9822a54
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 8156cb53fc81f4861e4a66da4960df0458ec6c91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351547"
---
# <a name="mapi-features-and-architecture"></a><span data-ttu-id="8d8f1-103">Architecture et fonctionnalités MAPI</span><span class="sxs-lookup"><span data-stu-id="8d8f1-103">MAPI Features and Architecture</span></span>

  
  
<span data-ttu-id="8d8f1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d8f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d8f1-105">L'API de messagerie (MAPI) est composée d'un ensemble d'interfaces de programmation d'applications communes et d'un composant de bibliothèque de liens dynamiques (DLL).</span><span class="sxs-lookup"><span data-stu-id="8d8f1-105">Messaging API (MAPI) is composed of a set of common application programming interfaces and a dynamic-link library (DLL) component.</span></span> <span data-ttu-id="8d8f1-106">Les interfaces permettent de créer et d'accéder à divers systèmes de messagerie et applications de messagerie, offrant un environnement uniforme pour le développement et l'utilisation, et offrant une véritable indépendance pour les deux.</span><span class="sxs-lookup"><span data-stu-id="8d8f1-106">The interfaces are used to create and access diverse messaging applications and messaging systems, offering a uniform environment for development and use, and providing true independence for both.</span></span> <span data-ttu-id="8d8f1-107">La DLL contient le sous-système MAPI, qui gère l'interaction entre les applications de messagerie frontale et les systèmes de messagerie principaux et fournit une interface utilisateur commune pour les tâches fréquentes.</span><span class="sxs-lookup"><span data-stu-id="8d8f1-107">The DLL contains the MAPI subsystem, which manages the interaction between front-end messaging applications and back-end messaging systems and provides a common user interface for frequent tasks.</span></span> <span data-ttu-id="8d8f1-108">Le sous-système MAPI agit comme un centre d'administration central pour unifier les différents systèmes de messagerie et protéger les clients contre leurs différences.</span><span class="sxs-lookup"><span data-stu-id="8d8f1-108">The MAPI subsystem acts as a central clearinghouse to unify the various messaging systems and shield clients from their differences.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8d8f1-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d8f1-109">See also</span></span>



[<span data-ttu-id="8d8f1-110">Concepts MAPI</span><span class="sxs-lookup"><span data-stu-id="8d8f1-110">MAPI Concepts</span></span>](mapi-concepts.md)

