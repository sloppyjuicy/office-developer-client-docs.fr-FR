---
title: Lien de l’OSC avec Outlook et les réseaux sociaux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Outlook Social Connector (OSC) peut être affiché dans la carte de visite Office et les activités du volet contacts Outlook, État ou mises à jour de photo pour un collègue, un ami ou toute personne à laquelle vous êtes associé.
ms.openlocfilehash: 0ee9451e64f12e8ba371c1ba91a1379cff257313
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329255"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a><span data-ttu-id="12359-103">Lien de l’OSC avec Outlook et les réseaux sociaux</span><span class="sxs-lookup"><span data-stu-id="12359-103">Relating the OSC with Outlook and social networks</span></span>

<span data-ttu-id="12359-104">Outlook Social Connector (OSC) peut être affiché dans la carte de visite Office et les activités du volet contacts Outlook, État ou mises à jour de photo pour un collègue, un ami ou toute personne à laquelle vous êtes associé.</span><span class="sxs-lookup"><span data-stu-id="12359-104">The Outlook Social Connector (OSC) can display in the Office Contact Card and Outlook People Pane activities, status, or photo updates for a coworker, friend, or any person you are associated with.</span></span> <span data-ttu-id="12359-105">Par défaut, OSC affiche les courriers électroniques, les pièces jointes et les demandes de réunion Outlook reçus d'une personne sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="12359-105">By default, the OSC displays the Outlook emails, attachments, and meeting requests received from a selected person.</span></span> <span data-ttu-id="12359-106">Si la personne sélectionnée et l'utilisateur Office collaborent sur un site SharePoint, OSC affiche également les mises à jour de documents et d'autres activités de site à partir de ce site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="12359-106">If the selected person and the Office user collaborate on a SharePoint site, the OSC also displays document updates and other site activities from that SharePoint site.</span></span> <span data-ttu-id="12359-107">En fonction des contextes d'association qui intéressent l'utilisateur Office, l'utilisateur Office peut installer des fournisseurs OSC pour les applications métier, les sites Web d'entreprise internes ou un large éventail de sites professionnels et de réseaux sociaux, tels que LinkedIn, Facebook et Windows Live.</span><span class="sxs-lookup"><span data-stu-id="12359-107">Depending on the contexts of association that the Office user is interested in, the Office user can install OSC providers for line-of-business applications, internal corporate websites, or a variety of professional and social network sites, such as LinkedIn, Facebook, and Windows Live.</span></span>
  
<span data-ttu-id="12359-108">Pour prendre en charge le partage des fonctionnalités dans les applications clientes Office, le moteur de base OSC est implémenté dans le cadre d'un composant partagé Office et le volet de personnes est implémenté en tant que complément Outlook.</span><span class="sxs-lookup"><span data-stu-id="12359-108">To support sharing of functionality across Office client applications, the OSC core engine is implemented as part of an Office shared component, and the People Pane is implemented as an Outlook add-in.</span></span> <span data-ttu-id="12359-109">Pour utiliser le OSC, un utilisateur Office doit avoir installé Outlook sur cet ordinateur client et configuré Outlook avec un profil, afin que le OSC puisse mettre en cache les contacts dans un dossier de contacts.</span><span class="sxs-lookup"><span data-stu-id="12359-109">To use the OSC, an Office user must have installed Outlook on that client computer and configured Outlook with a profile, so that the OSC can cache contacts in a Contacts folder.</span></span> 
  
<span data-ttu-id="12359-110">Un fournisseur OSC est une DLL COM (Component Object Model) qui permet à l'objet OSC d'accéder aux données de réseau social d'une manière indépendante des API de chaque réseau social.</span><span class="sxs-lookup"><span data-stu-id="12359-110">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="12359-111">Une DLL de fournisseur OSC doit être installée localement sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="12359-111">An OSC provider DLL must be installed locally on a client computer.</span></span> <span data-ttu-id="12359-112">Le fournisseur OSC d'un réseau social connecte le OSC, qui fait partie d'Outlook, avec le réseau social sur Internet.</span><span class="sxs-lookup"><span data-stu-id="12359-112">A social network's OSC provider connects the OSC, which is part of Outlook, with the social network on the Internet.</span></span>
  
<span data-ttu-id="12359-113">Un fournisseur OSC doit implémenter un ensemble d'interfaces, défini dans le cadre de l'extensibilité du fournisseur OSC, pour communiquer avec le OSC.</span><span class="sxs-lookup"><span data-stu-id="12359-113">An OSC provider must implement a set of interfaces, defined as part of the OSC provider extensibility, to communicate with the OSC.</span></span> <span data-ttu-id="12359-114">L'extensibilité du fournisseur OSC est disponible sous forme de plateforme ouverte.</span><span class="sxs-lookup"><span data-stu-id="12359-114">OSC provider extensibility is available as an open platform.</span></span>
  
<span data-ttu-id="12359-115">L'architecture du fournisseur du OSC permet à plusieurs fournisseurs de travailler avec le moteur de base OSC et d'agréger des informations sociales, telles que des amis et des activités.</span><span class="sxs-lookup"><span data-stu-id="12359-115">The provider architecture of the OSC enables multiple providers to work with the OSC core engine and aggregate social information such as friends and activities.</span></span> <span data-ttu-id="12359-116">La figure 1 illustre l'architecture du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="12359-116">Figure 1 illustrates the OSC provider architecture.</span></span>
  
<span data-ttu-id="12359-117">**Figure 1. Architecture du fournisseur Outlook Social Connector**</span><span class="sxs-lookup"><span data-stu-id="12359-117">**Figure 1. Outlook Social Connector provider architecture**</span></span>

![Réseaux sociaux, fournisseurs OSC, OSC et Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a><span data-ttu-id="12359-119">Terminologie</span><span class="sxs-lookup"><span data-stu-id="12359-119">Terminology</span></span>

<span data-ttu-id="12359-120">Dans cette référence de fournisseur Outlook Social Connector, un réseau social est utilisé pour faire référence aux types de sites suivants:</span><span class="sxs-lookup"><span data-stu-id="12359-120">In this Outlook Social Connector Provider Reference, a social network is used to refer to the following types of sites:</span></span> 
  
- <span data-ttu-id="12359-121">Sites collaboratifs tels que SharePoint.</span><span class="sxs-lookup"><span data-stu-id="12359-121">Collaborative sites such as SharePoint.</span></span>
    
- <span data-ttu-id="12359-122">Sites de réseau social comme Facebook et Windows Live.</span><span class="sxs-lookup"><span data-stu-id="12359-122">Social network sites such as Facebook and Windows Live.</span></span>
    
- <span data-ttu-id="12359-123">Les sites de réseau professionnels tels que LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="12359-123">Professional network sites such as LinkedIn.</span></span>
    
- <span data-ttu-id="12359-124">Autres applications métiers ou sites Web internes d'entreprise utilisés pour la mise en réseau.</span><span class="sxs-lookup"><span data-stu-id="12359-124">Other line-of-business applications or corporate internal websites used for networking.</span></span>
    
<span data-ttu-id="12359-125">Le terme Friend est généralement utilisé pour inclure les amis, la famille, les collègues, les connexions et tout autre utilisateur auquel un utilisateur Office est associé dans un contexte collaboratif tel que SharePoint, ou qui a été ajouté au compte de réseau social de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="12359-125">The term friend is used generally to include friends, family, colleagues, connections, and anyone else an Office user is associated with in a collaborative context like SharePoint, or has added to the user's social network account.</span></span> <span data-ttu-id="12359-126">Les non-amis sont des personnes référencées dans les mises à jour des activités des amis, mais pas des amis qui ont été ajoutés au compte de réseau social de l'utilisateur Office.</span><span class="sxs-lookup"><span data-stu-id="12359-126">Non-friends are people referenced in friends' activity updates but are not friends who have been added to the Office user's social network account.</span></span> <span data-ttu-id="12359-127">Les contacts sont des personnes dans un dossier de contacts Outlook.</span><span class="sxs-lookup"><span data-stu-id="12359-127">Contacts are people in an Outlook contact folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="12359-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12359-128">See also</span></span>

- [<span data-ttu-id="12359-129">Prise en main du développement d'un fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="12359-129">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

