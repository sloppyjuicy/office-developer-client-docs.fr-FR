---
title: Concernant l’OSC avec Outlook et les réseaux sociaux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: L’Outlook Social Connector (OSC) peut afficher dans le volet personnes d’Outlook et de la carte de visite Office activités, état ou mises à jour de la photo d’un collègue, friend ou toute personne qui que vous sont associés.
ms.openlocfilehash: 6dc6221b89eca5303e7cf6a201927659d4ac9107
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787708"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a><span data-ttu-id="f049d-103">Concernant l’OSC avec Outlook et les réseaux sociaux</span><span class="sxs-lookup"><span data-stu-id="f049d-103">Relating the OSC with Outlook and social networks</span></span>

<span data-ttu-id="f049d-104">L’Outlook Social Connector (OSC) peut afficher dans le volet personnes d’Outlook et de la carte de visite Office activités, état ou mises à jour de la photo d’un collègue, friend ou toute personne qui que vous sont associés.</span><span class="sxs-lookup"><span data-stu-id="f049d-104">The Outlook Social Connector (OSC) can display in the Office Contact Card and Outlook People Pane activities, status, or photo updates for a coworker, friend, or any person you are associated with.</span></span> <span data-ttu-id="f049d-105">Par défaut, l’OSC affiche les courriers électroniques Outlook, les pièces jointes, et les demandes de réunion provenant d’une personne sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="f049d-105">By default, the OSC displays the Outlook emails, attachments, and meeting requests received from a selected person.</span></span> <span data-ttu-id="f049d-106">Si la personne sélectionnée et que l’utilisateur Office collaborent sur un site SharePoint, l’OSC affiche également les mises à jour du document et autres activités de site à partir de ce site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f049d-106">If the selected person and the Office user collaborate on a SharePoint site, the OSC also displays document updates and other site activities from that SharePoint site.</span></span> <span data-ttu-id="f049d-107">Selon les contextes d’association est intéressée par l’utilisateur d’Office, l’utilisateur d’Office peut installer fournisseurs OSC line-of-business applications, des sites Web d’entreprise internes ou une variété de sites de réseau social Professionnel, tels que LinkedIn, Facebook et Windows Live.</span><span class="sxs-lookup"><span data-stu-id="f049d-107">Depending on the contexts of association that the Office user is interested in, the Office user can install OSC providers for line-of-business applications, internal corporate websites, or a variety of professional and social network sites, such as LinkedIn, Facebook, and Windows Live.</span></span>
  
<span data-ttu-id="f049d-108">Pour prendre en charge le partage des fonctionnalités entre les applications clientes Office, le moteur de base OSC est implémenté dans le cadre d’un composant partagé d’Office et le volet personnes est implémenté sous la forme d’un complément Outlook.</span><span class="sxs-lookup"><span data-stu-id="f049d-108">To support sharing of functionality across Office client applications, the OSC core engine is implemented as part of an Office shared component, and the People Pane is implemented as an Outlook add-in.</span></span> <span data-ttu-id="f049d-109">Pour utiliser l’OSC, un utilisateur d’Office doit avoir installé Outlook sur l’ordinateur client et configurer Outlook avec un profil, afin que l’OSC peut mettre en cache les contacts d’un dossier Contacts.</span><span class="sxs-lookup"><span data-stu-id="f049d-109">To use the OSC, an Office user must have installed Outlook on that client computer and configured Outlook with a profile, so that the OSC can cache contacts in a Contacts folder.</span></span> 
  
<span data-ttu-id="f049d-110">Un fournisseur OSC est un composant COM (Object Model) DLL qui permet à l’OSC accéder aux données de réseau social de façon indépendante des API de chaque réseau social.</span><span class="sxs-lookup"><span data-stu-id="f049d-110">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="f049d-111">Un fournisseur OSC DLL doit être installé localement sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="f049d-111">An OSC provider DLL must be installed locally on a client computer.</span></span> <span data-ttu-id="f049d-112">Fournisseur OSC d’un réseau social connecte OSC, ce qui fait partie d’Outlook, avec le réseaux sociaux sur Internet.</span><span class="sxs-lookup"><span data-stu-id="f049d-112">A social network's OSC provider connects the OSC, which is part of Outlook, with the social network on the Internet.</span></span>
  
<span data-ttu-id="f049d-113">Un fournisseur OSC doit implémenter un ensemble d’interfaces, définies dans le cadre de l’extensibilité de fournisseur OSC, de communiquer avec l’OSC.</span><span class="sxs-lookup"><span data-stu-id="f049d-113">An OSC provider must implement a set of interfaces, defined as part of the OSC provider extensibility, to communicate with the OSC.</span></span> <span data-ttu-id="f049d-114">Extensibilité du fournisseur OSC est disponible comme une plate-forme ouverte.</span><span class="sxs-lookup"><span data-stu-id="f049d-114">OSC provider extensibility is available as an open platform.</span></span>
  
<span data-ttu-id="f049d-115">L’architecture du fournisseur de l’OSC permet de plusieurs fournisseurs travailler avec le moteur de base OSC et compilent les informations telles que des amis et activités sociales.</span><span class="sxs-lookup"><span data-stu-id="f049d-115">The provider architecture of the OSC enables multiple providers to work with the OSC core engine and aggregate social information such as friends and activities.</span></span> <span data-ttu-id="f049d-116">La figure 1 illustre l’architecture de fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="f049d-116">Figure 1 illustrates the OSC provider architecture.</span></span>
  
<span data-ttu-id="f049d-117">**La figure 1. Architecture du fournisseur Outlook Social Connector**</span><span class="sxs-lookup"><span data-stu-id="f049d-117">**Figure 1. Outlook Social Connector provider architecture**</span></span>

![Réseaux sociaux, fournisseurs OSC, OSC et Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a><span data-ttu-id="f049d-119">Terminologie</span><span class="sxs-lookup"><span data-stu-id="f049d-119">Terminology</span></span>

<span data-ttu-id="f049d-120">Dans cette référence Outlook Social Connector fournisseur, un réseau social est utilisé pour faire référence aux types de sites suivants :</span><span class="sxs-lookup"><span data-stu-id="f049d-120">In this Outlook Social Connector Provider Reference, a social network is used to refer to the following types of sites:</span></span> 
  
- <span data-ttu-id="f049d-121">Sites de collaboration tels que SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f049d-121">Collaborative sites such as SharePoint.</span></span>
    
- <span data-ttu-id="f049d-122">Sites de réseau social tel que Facebook et Windows Live.</span><span class="sxs-lookup"><span data-stu-id="f049d-122">Social network sites such as Facebook and Windows Live.</span></span>
    
- <span data-ttu-id="f049d-123">Sites de réseau professionnel tels que LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="f049d-123">Professional network sites such as LinkedIn.</span></span>
    
- <span data-ttu-id="f049d-124">Autres applications métier d’ou entreprise internes sites Web utilisés pour la mise en réseau.</span><span class="sxs-lookup"><span data-stu-id="f049d-124">Other line-of-business applications or corporate internal websites used for networking.</span></span>
    
<span data-ttu-id="f049d-125">Votre ami termes est généralement utilisé pour inclure des amis, famille, collègues, les connexions et quiconque un utilisateur d’Office est associée dans un contexte de collaboration tels que SharePoint, ou a ajouté au compte de réseau social de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f049d-125">The term friend is used generally to include friends, family, colleagues, connections, and anyone else an Office user is associated with in a collaborative context like SharePoint, or has added to the user's social network account.</span></span> <span data-ttu-id="f049d-126">Non-amis sont les personnes référencées dans les mises à jour des activités de vos amis, mais ne sont pas des amis qui ont été ajoutés au compte de réseau social de l’utilisateur d’Office.</span><span class="sxs-lookup"><span data-stu-id="f049d-126">Non-friends are people referenced in friends' activity updates but are not friends who have been added to the Office user's social network account.</span></span> <span data-ttu-id="f049d-127">Les contacts sont des personnes dans un dossier de contacts Outlook.</span><span class="sxs-lookup"><span data-stu-id="f049d-127">Contacts are people in an Outlook contact folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f049d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f049d-128">See also</span></span>

- [<span data-ttu-id="f049d-129">Prise en main du développement d'un fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="f049d-129">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

