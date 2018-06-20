---
title: Test des personnes suivantes et stop-suivant
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: Cette rubrique décrit les scénarios pour tester la capacité du fournisseur Outlook Social Connector (OSC) à suivre un ami et pour arrêter le suivi d’un ami sur le réseaux sociaux.
ms.openlocfilehash: 09652b658a2c20301b8b0568d373ae6fe841fe2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787701"
---
# <a name="testing-following-and-stop-following-persons"></a><span data-ttu-id="119bb-103">Test des personnes suivantes et stop-suivant</span><span class="sxs-lookup"><span data-stu-id="119bb-103">Testing following and stop-following persons</span></span>

<span data-ttu-id="119bb-104">Cette rubrique décrit les scénarios pour tester la capacité du fournisseur Outlook Social Connector (OSC) à suivre un ami et pour arrêter le suivi d’un ami sur le réseaux sociaux.</span><span class="sxs-lookup"><span data-stu-id="119bb-104">This topic describes scenarios to test the Outlook Social Connector (OSC) provider's ability to follow a friend, and to stop following a friend on the social network.</span></span>
  
## <a name="following-a-person"></a><span data-ttu-id="119bb-105">Suivi d’une personne</span><span class="sxs-lookup"><span data-stu-id="119bb-105">Following a person</span></span>

<span data-ttu-id="119bb-106">Pour suivre une personne consiste à ajouter une personne comme un ami sur le réseaux sociaux, à l’aide de l’adresse SMTP fourni par l’élément Outlook sélectionné.</span><span class="sxs-lookup"><span data-stu-id="119bb-106">To follow a person is to add a person as a friend on the social network, using the SMTP address provided by the selected Outlook item.</span></span> <span data-ttu-id="119bb-107">Une personne suit généralement sur un réseau social implique la demande d’autorisation de cette personne par un message électronique à cette adresse SMTP.</span><span class="sxs-lookup"><span data-stu-id="119bb-107">Following someone on a social network usually involves requesting permission from that person by an email to that SMTP address.</span></span> <span data-ttu-id="119bb-108">Pour accorder l’autorisation, cette personne doit avoir déjà incluse dans son compte de réseau social d’adresse SMTP, soit être prêt à ajouter à un compte de réseau social SMTP.</span><span class="sxs-lookup"><span data-stu-id="119bb-108">In order to grant permission, that person must either have that SMTP address already included in his or her social network account, or be willing to add that SMTP to a social network account.</span></span> <span data-ttu-id="119bb-109">Tester chacune des scénarios suivants pour vérifier que votre fournisseur OSC se comporte correctement.</span><span class="sxs-lookup"><span data-stu-id="119bb-109">Test each of the following scenarios to verify that your OSC provider behaves correctly.</span></span>
  
|<span data-ttu-id="119bb-110">**Scénario**</span><span class="sxs-lookup"><span data-stu-id="119bb-110">**Scenario**</span></span>|<span data-ttu-id="119bb-111">**Comportement attendu**</span><span class="sxs-lookup"><span data-stu-id="119bb-111">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="119bb-112">Essayez de suivre une personne sur le réseau social qui existe sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="119bb-112">Attempting to follow a person on the social network who exists on the social network.</span></span>  <br/> |<span data-ttu-id="119bb-113">Pour un réseau social qui ne nécessite pas l’autorisation de la personne, le réseaux sociaux ajoute immédiatement la personne comme un ami.</span><span class="sxs-lookup"><span data-stu-id="119bb-113">For a social network that does not require permission from the person, the social network immediately adds the person as a friend.</span></span>  <br/> <span data-ttu-id="119bb-114">Pour un réseau qui requiert une autorisation de cette personne, le réseaux sociaux envoie une notification.</span><span class="sxs-lookup"><span data-stu-id="119bb-114">For a network that requires permission from that person, the social network sends a notification.</span></span> <span data-ttu-id="119bb-115">Le volet personnes Outlook affiche une icône en attente pour cette personne.</span><span class="sxs-lookup"><span data-stu-id="119bb-115">The Outlook People Pane displays a pending icon for that person.</span></span>  <br/> |
|<span data-ttu-id="119bb-116">Essayez de suivre une personne sur le réseau social qui n’existe pas sur le réseaux sociaux.</span><span class="sxs-lookup"><span data-stu-id="119bb-116">Attempting to follow a person on the social network who does not exist on the social network.</span></span>  <br/> |<span data-ttu-id="119bb-117">Le fournisseur OSC permet d’afficher l’erreur appropriée [ISocialSession::FollowPerson](isocialsession-followperson.md) ou [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md).</span><span class="sxs-lookup"><span data-stu-id="119bb-117">The OSC provider displays the appropriate error in [ISocialSession::FollowPerson](isocialsession-followperson.md) or [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md).</span></span>  <br/> |
|<span data-ttu-id="119bb-118">Suivi d’un ami sur le réseaux sociaux.</span><span class="sxs-lookup"><span data-stu-id="119bb-118">Following a friend on the social network.</span></span>  <br/> |<span data-ttu-id="119bb-119">Pour l’ami sélectionné dans le volet personnes, badge du réseau social et l’image de profil d’un ami pour ce réseau social sont également affichés.</span><span class="sxs-lookup"><span data-stu-id="119bb-119">For the friend selected in the People Pane, the social network's badge and the friend's profile picture for that social network are displayed.</span></span>  <br/> |
|<span data-ttu-id="119bb-120">Sélectionnez le lien vers la page de profil d’un ami.</span><span class="sxs-lookup"><span data-stu-id="119bb-120">Selecting the link to the profile page of a friend.</span></span>  <br/> |<span data-ttu-id="119bb-121">Page d’un ami sur le réseau social s’ouvre dans le navigateur par défaut de l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="119bb-121">The friend's page on the social network opens in the logged-on user's default browser.</span></span>  <br/> |
   
## <a name="stop-following-a-person"></a><span data-ttu-id="119bb-122">Arrêter le suivi d’une personne</span><span class="sxs-lookup"><span data-stu-id="119bb-122">Stop following a person</span></span>

<span data-ttu-id="119bb-123">Pour arrêter le suivi d’une personne consiste à supprimer cette personne comme un ami sur le réseaux sociaux.</span><span class="sxs-lookup"><span data-stu-id="119bb-123">To stop following a person is to remove that person as a friend on the social network.</span></span> <span data-ttu-id="119bb-124">Testez le scénario suivant pour vérifier votre cesse de fournisseur OSC correctement suivi d’une personne.</span><span class="sxs-lookup"><span data-stu-id="119bb-124">Test the following scenario to verify your OSC provider stops following a person properly.</span></span>
  
|<span data-ttu-id="119bb-125">**Scénario**</span><span class="sxs-lookup"><span data-stu-id="119bb-125">**Scenario**</span></span>|<span data-ttu-id="119bb-126">**Comportement attendu**</span><span class="sxs-lookup"><span data-stu-id="119bb-126">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="119bb-127">Tentative de suppression d’une personne comme un ami sur le réseaux sociaux.</span><span class="sxs-lookup"><span data-stu-id="119bb-127">Attempting to remove a person as a friend on the social network.</span></span>  <br/> |<span data-ttu-id="119bb-128">Le réseaux sociaux répertorie n’est plus cette personne comme un ami sur le compte de l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="119bb-128">The social network no longer lists that person as a friend on the logged on user's account.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="119bb-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="119bb-129">See also</span></span>

- [<span data-ttu-id="119bb-130">Prise en main de la publication d'un fournisseur OSC</span><span class="sxs-lookup"><span data-stu-id="119bb-130">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

