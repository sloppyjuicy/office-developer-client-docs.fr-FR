---
title: Test du suivi et de l’arrêt de suivi de personnes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: Cette rubrique décrit les scénarios permettant de tester la capacité du fournisseur Outlook Social Connector (OSC) à suivre un ami et à arrêter de suivre un ami sur le réseau social.
ms.openlocfilehash: 06a2bc48fa723f4d4513376cace96a195cef9fa3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432449"
---
# <a name="testing-following-and-stop-following-persons"></a><span data-ttu-id="2e383-103">Test du suivi et de l’arrêt de suivi de personnes</span><span class="sxs-lookup"><span data-stu-id="2e383-103">Testing following and stop-following persons</span></span>

<span data-ttu-id="2e383-104">Cette rubrique décrit les scénarios permettant de tester la capacité du fournisseur Outlook Social Connector (OSC) à suivre un ami et à arrêter de suivre un ami sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="2e383-104">This topic describes scenarios to test the Outlook Social Connector (OSC) provider's ability to follow a friend, and to stop following a friend on the social network.</span></span>
  
## <a name="following-a-person"></a><span data-ttu-id="2e383-105">Suivi d'une personne</span><span class="sxs-lookup"><span data-stu-id="2e383-105">Following a person</span></span>

<span data-ttu-id="2e383-106">Pour suivre une personne, il faut ajouter une personne en tant qu'ami sur le réseau social, à l'aide de l'adresse SMTP fournie par l'élément Outlook sélectionné.</span><span class="sxs-lookup"><span data-stu-id="2e383-106">To follow a person is to add a person as a friend on the social network, using the SMTP address provided by the selected Outlook item.</span></span> <span data-ttu-id="2e383-107">Le suivi d'une personne sur un réseau social implique généralement de demander l'autorisation de cette personne par un message électronique à cette adresse SMTP.</span><span class="sxs-lookup"><span data-stu-id="2e383-107">Following someone on a social network usually involves requesting permission from that person by an email to that SMTP address.</span></span> <span data-ttu-id="2e383-108">Pour accorder l'autorisation, cette personne doit avoir cette adresse SMTP déjà incluse dans son compte de réseau social ou être disposé à ajouter ce protocole SMTP à un compte de réseau social.</span><span class="sxs-lookup"><span data-stu-id="2e383-108">In order to grant permission, that person must either have that SMTP address already included in his or her social network account, or be willing to add that SMTP to a social network account.</span></span> <span data-ttu-id="2e383-109">Testez chacun des scénarios suivants pour vérifier que votre fournisseur OSC se comporte correctement.</span><span class="sxs-lookup"><span data-stu-id="2e383-109">Test each of the following scenarios to verify that your OSC provider behaves correctly.</span></span>
  
|<span data-ttu-id="2e383-110">**Scénario**</span><span class="sxs-lookup"><span data-stu-id="2e383-110">**Scenario**</span></span>|<span data-ttu-id="2e383-111">**Comportement attendu**</span><span class="sxs-lookup"><span data-stu-id="2e383-111">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2e383-112">Tentative de suivi d'une personne sur le réseau social qui existe sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="2e383-112">Attempting to follow a person on the social network who exists on the social network.</span></span>  <br/> |<span data-ttu-id="2e383-113">Pour un réseau social qui n'a pas besoin d'autorisation de la part de la personne, le réseau social ajoute immédiatement la personne en tant qu'ami.</span><span class="sxs-lookup"><span data-stu-id="2e383-113">For a social network that does not require permission from the person, the social network immediately adds the person as a friend.</span></span>  <br/> <span data-ttu-id="2e383-114">Pour un réseau qui requiert une autorisation de la part de cette personne, le réseau social envoie une notification.</span><span class="sxs-lookup"><span data-stu-id="2e383-114">For a network that requires permission from that person, the social network sends a notification.</span></span> <span data-ttu-id="2e383-115">Le volet contacts Outlook affiche une icône en attente pour cette personne.</span><span class="sxs-lookup"><span data-stu-id="2e383-115">The Outlook People Pane displays a pending icon for that person.</span></span>  <br/> |
|<span data-ttu-id="2e383-116">Tentative de suivi d'une personne sur le réseau social qui n'existe pas sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="2e383-116">Attempting to follow a person on the social network who does not exist on the social network.</span></span>  <br/> |<span data-ttu-id="2e383-117">Le fournisseur OSC affiche l'erreur appropriée dans [ISocialSession:: followPerson](isocialsession-followperson.md) ou [ISocialSession2:: FollowPersonEx](isocialsession2-followpersonex.md).</span><span class="sxs-lookup"><span data-stu-id="2e383-117">The OSC provider displays the appropriate error in [ISocialSession::FollowPerson](isocialsession-followperson.md) or [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md).</span></span>  <br/> |
|<span data-ttu-id="2e383-118">Suivi d'un ami sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="2e383-118">Following a friend on the social network.</span></span>  <br/> |<span data-ttu-id="2e383-119">Pour l'ami sélectionné dans le volet personnes, le badge du réseau social et l'image de profil de l'ami pour ce réseau social sont affichés.</span><span class="sxs-lookup"><span data-stu-id="2e383-119">For the friend selected in the People Pane, the social network's badge and the friend's profile picture for that social network are displayed.</span></span>  <br/> |
|<span data-ttu-id="2e383-120">Sélection du lien vers la page de profil d'un ami.</span><span class="sxs-lookup"><span data-stu-id="2e383-120">Selecting the link to the profile page of a friend.</span></span>  <br/> |<span data-ttu-id="2e383-121">La page de l'ami sur le réseau social s'ouvre dans le navigateur par défaut de l'utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="2e383-121">The friend's page on the social network opens in the logged-on user's default browser.</span></span>  <br/> |
   
## <a name="stop-following-a-person"></a><span data-ttu-id="2e383-122">Arrêter le suivi d'une personne</span><span class="sxs-lookup"><span data-stu-id="2e383-122">Stop following a person</span></span>

<span data-ttu-id="2e383-123">Pour arrêter le suivi d'une personne, vous pouvez la supprimer en tant qu'ami sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="2e383-123">To stop following a person is to remove that person as a friend on the social network.</span></span> <span data-ttu-id="2e383-124">Testez le scénario suivant pour vérifier que votre fournisseur OSC cesse de suivre correctement une personne.</span><span class="sxs-lookup"><span data-stu-id="2e383-124">Test the following scenario to verify your OSC provider stops following a person properly.</span></span>
  
|<span data-ttu-id="2e383-125">**Scénario**</span><span class="sxs-lookup"><span data-stu-id="2e383-125">**Scenario**</span></span>|<span data-ttu-id="2e383-126">**Comportement attendu**</span><span class="sxs-lookup"><span data-stu-id="2e383-126">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2e383-127">Tentative de suppression d'une personne en tant qu'ami sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="2e383-127">Attempting to remove a person as a friend on the social network.</span></span>  <br/> |<span data-ttu-id="2e383-128">Le réseau social ne répertorie plus cette personne en tant qu'ami sur le compte de l'utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="2e383-128">The social network no longer lists that person as a friend on the logged on user's account.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e383-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e383-129">See also</span></span>

- [<span data-ttu-id="2e383-130">Prise en main de la publication d'un fournisseur OSC</span><span class="sxs-lookup"><span data-stu-id="2e383-130">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

