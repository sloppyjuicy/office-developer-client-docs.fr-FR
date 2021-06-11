---
title: Lien de l’OSC avec Outlook et les réseaux sociaux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Le connecteur Outlook Social Connector (OSC) peut s’afficher dans la carte de visite Office Outlook et les activités, l’état ou les mises à jour de photos d’un collègue, d’un ami ou de toute personne à qui vous êtes associé.
ms.openlocfilehash: 0ee9451e64f12e8ba371c1ba91a1379cff257313
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428010"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a><span data-ttu-id="5615a-103">Lien de l’OSC avec Outlook et les réseaux sociaux</span><span class="sxs-lookup"><span data-stu-id="5615a-103">Relating the OSC with Outlook and social networks</span></span>

<span data-ttu-id="5615a-104">Le connecteur Outlook Social Connector (OSC) peut s’afficher dans la carte de visite Office Outlook et les activités, l’état ou les mises à jour de photos d’un collègue, d’un ami ou de toute personne à qui vous êtes associé.</span><span class="sxs-lookup"><span data-stu-id="5615a-104">The Outlook Social Connector (OSC) can display in the Office Contact Card and Outlook People Pane activities, status, or photo updates for a coworker, friend, or any person you are associated with.</span></span> <span data-ttu-id="5615a-105">Par défaut, l’OSC affiche les messages Outlook, les pièces jointes et les demandes de réunion reçues d’une personne sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="5615a-105">By default, the OSC displays the Outlook emails, attachments, and meeting requests received from a selected person.</span></span> <span data-ttu-id="5615a-106">Si la personne sélectionnée et l’utilisateur Office collaborent sur un site SharePoint, l’OSC affiche également les mises à jour de documents et d’autres activités de site à partir de ce site SharePoint site.</span><span class="sxs-lookup"><span data-stu-id="5615a-106">If the selected person and the Office user collaborate on a SharePoint site, the OSC also displays document updates and other site activities from that SharePoint site.</span></span> <span data-ttu-id="5615a-107">Selon les contextes d’association qui intéressent l’utilisateur Office, l’utilisateur Office peut installer des fournisseurs OSC pour des applications métier, des sites web d’entreprise internes ou divers sites de réseaux sociaux et professionnels, tels que LinkedIn, Facebook et Windows Live.</span><span class="sxs-lookup"><span data-stu-id="5615a-107">Depending on the contexts of association that the Office user is interested in, the Office user can install OSC providers for line-of-business applications, internal corporate websites, or a variety of professional and social network sites, such as LinkedIn, Facebook, and Windows Live.</span></span>
  
<span data-ttu-id="5615a-108">Pour prendre en charge le partage de fonctionnalités entre les applications clientes Office, le moteur principal OSC est implémenté dans le cadre d’un composant partagé Office, et le volet Personnes est implémenté en tant que Outlook.</span><span class="sxs-lookup"><span data-stu-id="5615a-108">To support sharing of functionality across Office client applications, the OSC core engine is implemented as part of an Office shared component, and the People Pane is implemented as an Outlook add-in.</span></span> <span data-ttu-id="5615a-109">Pour utiliser OSC, un utilisateur Office doit avoir installé des Outlook sur cet ordinateur client et configuré des Outlook avec un profil, afin que l’OSC puisse mettre en cache les contacts dans un dossier Contacts.</span><span class="sxs-lookup"><span data-stu-id="5615a-109">To use the OSC, an Office user must have installed Outlook on that client computer and configured Outlook with a profile, so that the OSC can cache contacts in a Contacts folder.</span></span> 
  
<span data-ttu-id="5615a-110">Un fournisseur OSC est une DLL COM (Component Object Model) qui permet à l’OSC d’accéder aux données de réseau social d’une manière indépendante des API de chaque réseau social.</span><span class="sxs-lookup"><span data-stu-id="5615a-110">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="5615a-111">Une DLL de fournisseur OSC doit être installée localement sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="5615a-111">An OSC provider DLL must be installed locally on a client computer.</span></span> <span data-ttu-id="5615a-112">Le fournisseur OSC d’un réseau social connecte OSC, qui fait partie de Outlook, au réseau social sur Internet.</span><span class="sxs-lookup"><span data-stu-id="5615a-112">A social network's OSC provider connects the OSC, which is part of Outlook, with the social network on the Internet.</span></span>
  
<span data-ttu-id="5615a-113">Un fournisseur OSC doit implémenter un ensemble d’interfaces, définies dans le cadre de l’extensibilité du fournisseur OSC, pour communiquer avec l’OSC.</span><span class="sxs-lookup"><span data-stu-id="5615a-113">An OSC provider must implement a set of interfaces, defined as part of the OSC provider extensibility, to communicate with the OSC.</span></span> <span data-ttu-id="5615a-114">L’extensibilité du fournisseur OSC est disponible en tant que plateforme ouverte.</span><span class="sxs-lookup"><span data-stu-id="5615a-114">OSC provider extensibility is available as an open platform.</span></span>
  
<span data-ttu-id="5615a-115">L’architecture de fournisseur de l’OSC permet à plusieurs fournisseurs de travailler avec le moteur principal OSC et d’agréger des informations sociales telles que des amis et des activités.</span><span class="sxs-lookup"><span data-stu-id="5615a-115">The provider architecture of the OSC enables multiple providers to work with the OSC core engine and aggregate social information such as friends and activities.</span></span> <span data-ttu-id="5615a-116">La figure 1 illustre l’architecture du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="5615a-116">Figure 1 illustrates the OSC provider architecture.</span></span>
  
<span data-ttu-id="5615a-117">**Figure 1. Outlook Architecture du fournisseur Social Connector**</span><span class="sxs-lookup"><span data-stu-id="5615a-117">**Figure 1. Outlook Social Connector provider architecture**</span></span>

![Réseaux sociaux, fournisseurs OSC, OSC et Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a><span data-ttu-id="5615a-119">Terminologie</span><span class="sxs-lookup"><span data-stu-id="5615a-119">Terminology</span></span>

<span data-ttu-id="5615a-120">Dans cette Outlook référence du fournisseur social Connector, un réseau social est utilisé pour faire référence aux types de sites suivants :</span><span class="sxs-lookup"><span data-stu-id="5615a-120">In this Outlook Social Connector Provider Reference, a social network is used to refer to the following types of sites:</span></span> 
  
- <span data-ttu-id="5615a-121">Sites de collaboration tels que SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5615a-121">Collaborative sites such as SharePoint.</span></span>
    
- <span data-ttu-id="5615a-122">Sites de réseaux sociaux tels que Facebook et Windows Live.</span><span class="sxs-lookup"><span data-stu-id="5615a-122">Social network sites such as Facebook and Windows Live.</span></span>
    
- <span data-ttu-id="5615a-123">Professional sites réseau tels que LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="5615a-123">Professional network sites such as LinkedIn.</span></span>
    
- <span data-ttu-id="5615a-124">Autres applications métier ou sites web internes d’entreprise utilisés pour la mise en réseau.</span><span class="sxs-lookup"><span data-stu-id="5615a-124">Other line-of-business applications or corporate internal websites used for networking.</span></span>
    
<span data-ttu-id="5615a-125">Le terme « ami » est généralement utilisé pour inclure des amis, une famille, des collègues, des connexions et toute autre personne à qui un utilisateur Office est associé dans un contexte de collaboration tel que SharePoint, ou a été ajouté au compte de réseau social de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5615a-125">The term friend is used generally to include friends, family, colleagues, connections, and anyone else an Office user is associated with in a collaborative context like SharePoint, or has added to the user's social network account.</span></span> <span data-ttu-id="5615a-126">Les non-amis sont des personnes référencés dans les mises à jour d’activité des amis, mais pas des amis qui ont été ajoutés au compte de réseau social de l’Office de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5615a-126">Non-friends are people referenced in friends' activity updates but are not friends who have been added to the Office user's social network account.</span></span> <span data-ttu-id="5615a-127">Les contacts sont des personnes qui se Outlook dossier de contacts.</span><span class="sxs-lookup"><span data-stu-id="5615a-127">Contacts are people in an Outlook contact folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5615a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5615a-128">See also</span></span>

- [<span data-ttu-id="5615a-129">Prise en main du développement d'un fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="5615a-129">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

