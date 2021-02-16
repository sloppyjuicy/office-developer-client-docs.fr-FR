---
title: Création d’un profil à l’aide de l’Assistant Profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a93cfb05d8abfffc9f55a7ea48efc3c3451dddbb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411735"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a><span data-ttu-id="ffced-103">Création d’un profil à l’aide de l’Assistant Profil</span><span class="sxs-lookup"><span data-stu-id="ffced-103">Creating a Profile by Using the Profile Wizard</span></span>

  
  
<span data-ttu-id="ffced-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffced-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffced-105">L’Assistant Profil est une fonctionnalité MAPI qui permet à un utilisateur de créer un profil de la manière la plus simple possible.</span><span class="sxs-lookup"><span data-stu-id="ffced-105">The Profile Wizard is a MAPI feature that enables a user to create a profile in the easiest possible way.</span></span> <span data-ttu-id="ffced-106">L’Assistant Profil affiche une série de boîtes de dialogue qui invitent l’utilisateur à sélectionner les services de message et à entrer des valeurs pour quelques-unes des propriétés de configuration les plus essentielles.</span><span class="sxs-lookup"><span data-stu-id="ffced-106">The Profile Wizard displays a series of dialog boxes which prompt the user to select message services and enter values for a few of the most essential configuration properties.</span></span> <span data-ttu-id="ffced-107">Pour la plupart des autres propriétés requises, l’Assistant Profil utilise les valeurs par défaut fournies.</span><span class="sxs-lookup"><span data-stu-id="ffced-107">For most of the other required properties, the Profile Wizard uses default values provided.</span></span> <span data-ttu-id="ffced-108">Pour appeler l’Assistant Profil, appelez **LaunchWizard**, une fonction basée sur le prototype [LAUNCHWIZARDENTRY.](launchwizardentry.md)</span><span class="sxs-lookup"><span data-stu-id="ffced-108">To invoke the Profile Wizard, call **LaunchWizard**, a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) prototype.</span></span> 
  
<span data-ttu-id="ffced-109">L’utilisateur peut ajouter uniquement ces services de messagerie et fournisseurs de services au nouveau profil qui permet de prendre en charge l’Assistant Profil.</span><span class="sxs-lookup"><span data-stu-id="ffced-109">The user can add only those message services and service providers to the new profile that support the Profile Wizard.</span></span> <span data-ttu-id="ffced-110">Étant donné que chaque service de messagerie peut nécessiter plus de propriétés que ce que l’Assistant Profil peut gérer, sachez que si vous utilisez cette approche, un ou plusieurs des services ou fournisseurs sélectionnés peuvent être configurés de manière incomplète.</span><span class="sxs-lookup"><span data-stu-id="ffced-110">Because each message service might require more properties to be set than the Profile Wizard can handle, be aware that if you use this approach, it is possible for one or more of the selected services or providers to be incompletely configured.</span></span>
  

