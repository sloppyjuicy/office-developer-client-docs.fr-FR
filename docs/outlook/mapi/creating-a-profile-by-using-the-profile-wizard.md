---
title: Création d’un profil à l’aide de l’Assistant profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 29a135264772847a624e1a4558b68bcf822b18df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783103"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a><span data-ttu-id="32391-103">Création d’un profil à l’aide de l’Assistant profil</span><span class="sxs-lookup"><span data-stu-id="32391-103">Creating a Profile by Using the Profile Wizard</span></span>

  
  
<span data-ttu-id="32391-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="32391-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="32391-105">L’Assistant profil est une fonctionnalité MAPI qui permet à un utilisateur de créer un profil dans le plus simple possible.</span><span class="sxs-lookup"><span data-stu-id="32391-105">The Profile Wizard is a MAPI feature that enables a user to create a profile in the easiest possible way.</span></span> <span data-ttu-id="32391-106">L’Assistant profil affiche une série de boîtes de dialogue qui invite l’utilisateur à sélectionner les services de messagerie et entrez des valeurs pour quelques-unes des propriétés essentielles de configuration.</span><span class="sxs-lookup"><span data-stu-id="32391-106">The Profile Wizard displays a series of dialog boxes which prompt the user to select message services and enter values for a few of the most essential configuration properties.</span></span> <span data-ttu-id="32391-107">Pour la plupart des autres propriétés requises, l’Assistant profil utilise les valeurs par défaut fournies.</span><span class="sxs-lookup"><span data-stu-id="32391-107">For most of the other required properties, the Profile Wizard uses default values provided.</span></span> <span data-ttu-id="32391-108">Pour appeler l’Assistant profil, appelez **LaunchWizard**, une fonction basée sur le prototype [LAUNCHWIZARDENTRY](launchwizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="32391-108">To invoke the Profile Wizard, call **LaunchWizard**, a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) prototype.</span></span> 
  
<span data-ttu-id="32391-109">L’utilisateur peut ajouter uniquement les services de messagerie et les fournisseurs de services pour le nouveau profil qui prennent en charge de l’Assistant profil.</span><span class="sxs-lookup"><span data-stu-id="32391-109">The user can add only those message services and service providers to the new profile that support the Profile Wizard.</span></span> <span data-ttu-id="32391-110">Étant donné que chaque service de message peut nécessiter plus de propriétés à définir que l’Assistant profil peut gérer, sachez que si vous utilisez cette approche, il est possible pour une ou plusieurs des services sélectionnés ou des fournisseurs pour incomplète.</span><span class="sxs-lookup"><span data-stu-id="32391-110">Because each message service might require more properties to be set than the Profile Wizard can handle, be aware that if you use this approach, it is possible for one or more of the selected services or providers to be incompletely configured.</span></span>
  

