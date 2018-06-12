---
title: Référence du fournisseur Outlook Social Connector
manager: soliver
ms.date: 04/04/2016
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13661393-adf6-4870-86c4-303262317675
description: Outlook Social Connector 2013 fournit un concentrateur de communication pour les communications personnelles et professionnelles.
ms.openlocfilehash: 32a9eb88b7724f8735d0eb8623bb3716ad836a7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787700"
---
# <a name="outlook-social-connector-provider-reference"></a><span data-ttu-id="a550e-103">Référence du fournisseur Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="a550e-103">Outlook Social Connector provider reference</span></span>

<span data-ttu-id="a550e-104">Outlook Social Connector 2013 fournit un concentrateur de communication pour les communications personnelles et professionnelles.</span><span class="sxs-lookup"><span data-stu-id="a550e-104">The Outlook Social Connector 2013 provides a communication hub for personal and professional communications.</span></span> <span data-ttu-id="a550e-105">Outlook Social Connector (OSC) fonctionne avec SharePoint Server, SharePoint Workspace, le client Lync et toutes les applications clientes Office qui prennent en charge les informations de présence et la Carte de visite prenant en charge OSC.</span><span class="sxs-lookup"><span data-stu-id="a550e-105">The Outlook Social Connector (OSC) works with SharePoint Server, SharePoint Workspace, Lync client, and all Office client applications that support presence information and the Contact Card support the OSC.</span></span> 

<span data-ttu-id="a550e-106">Dans Outlook en particulier, en sélectionnant simplement un élément Outlook comme un message électronique ou une demande de réunion et en cliquant sur l'expéditeur ou un destinataire au sein de cet élément, sans quitter Outlook, les utilisateurs peuvent voir les activités du volet Personnes, les photos et les mises à jour de statut de cette personne sur leurs réseaux sociaux favoris.</span><span class="sxs-lookup"><span data-stu-id="a550e-106">In Outlook in particular, just by selecting an Outlook item such as an email or meeting request and clicking the sender or a recipient in that item, without leaving Outlook, users can see in the People Pane activities, photos, and status updates of this person on their favorite social networks.</span></span> <span data-ttu-id="a550e-107">Les utilisateurs peuvent sans problème voir tous les messages électroniques, pièces jointes et réunions Outlook provenant de cette personne.</span><span class="sxs-lookup"><span data-stu-id="a550e-107">Users can conveniently see all the Outlook emails, attachments, and meetings received from this person.</span></span> <span data-ttu-id="a550e-108">Dans un environnement professionnel, les utilisateurs sur un site SharePoint peuvent également voir, dans le volet Personnes, les mises à jour de documents et d'autres activités de site pour cette personne sur le site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a550e-108">In an organizational environment, users on a SharePoint site can also see in the People Pane document updates and other site activities of this person on the SharePoint site.</span></span>
  
<span data-ttu-id="a550e-p103">Un réseau social peut développer un fournisseur pour qu'OSC synchronise et expose les mises à jour de réseaux sociaux dans les applications et serveurs de prise en charge. Les réseaux sociaux populaires, comme LinkedIn, Facebook et Windows Live, offrent les fournisseurs pour OSC.</span><span class="sxs-lookup"><span data-stu-id="a550e-p103">A social network can develop a provider for the OSC to synchronize and surface social network updates in supporting servers and applications. Popular social networks such as LinkedIn, Facebook, and Windows Live are offering providers for the OSC.</span></span> 
  
<span data-ttu-id="a550e-111">Le fournisseur de référence Outlook Social Connector 2013 décrit comment développer un fournisseur OSC à l'aide de l'extensibilité du fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="a550e-111">The Outlook Social Connector 2013 Provider Reference describes how to develop an OSC provider using OSC provider extensibility.</span></span> 
  
<span data-ttu-id="a550e-112">Si vous débutez en tant que développeur de solutions pour Outlook, consultez [Sélection d'une API ou d'une technologie pour développer des solutions pour Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) pour identifier les API et technologies les plus adaptées à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="a550e-112">If you are new to developing solutions for Outlook, see [Selecting an API or technology for developing solutions for Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="a550e-113">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="a550e-113">In this section</span></span>

- <span data-ttu-id="a550e-114">[Prise en main le développement d’un fournisseur Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md): fournit une vue d’ensemble de l’OSC, notamment les suivants : comment un fournisseur OSC peut être utile, des étapes rapides pour apprendre à développer un fournisseur, les conditions techniques, meilleures pratiques pour développement d’un fournisseur et quelles sont les nouveautés dans cette version.</span><span class="sxs-lookup"><span data-stu-id="a550e-114">[Getting Started with Developing an Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md): Provides an overview of the OSC, including the following: how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span>
    
- <span data-ttu-id="a550e-115">[Exemples de modèles OSC](osc-sample-templates.md): décrit plusieurs modèles Visual Studio pour le développement d’un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a550e-115">[OSC Sample Templates](osc-sample-templates.md): Describes several Visual Studio templates for developing a provider.</span></span>
    
- <span data-ttu-id="a550e-116">[Séquences d’appel classiques OSC](osc-typical-calling-sequences.md): décrit quelques séquences d’appel classiques à l’OSC de membres dans les interfaces d’extensibilité de fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="a550e-116">[OSC Typical Calling Sequences](osc-typical-calling-sequences.md): Describes a few typical calling sequences by the OSC of members in the OSC provider extensibility interfaces.</span></span> <span data-ttu-id="a550e-117">Cela doit vous permettre de mieux comprendre la mise en place de ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="a550e-117">This should enable you to better understand how to implement these interfaces.</span></span>
    
- <span data-ttu-id="a550e-118">[Développement d’un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md): décrit comment les interfaces d’extensibilité fournisseur OSC et du schéma XML OSC sont conçus pour prendre en charge un fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="a550e-118">[Developing a Provider with the OSC XML Schema](developing-a-provider-with-the-osc-xml-schema.md): Describes how the OSC provider extensibility interfaces and OSC XML schema are designed to support an OSC provider.</span></span>
    
- <span data-ttu-id="a550e-119">[Débogage d’un fournisseur](debugging-a-provider.md): propose quelques moyens pour déboguer un fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="a550e-119">[Debugging a Provider](debugging-a-provider.md): Suggests a few ways to help debug an OSC provider.</span></span>
    
- <span data-ttu-id="a550e-120">[Déploiement d’un fournisseur](deploying-a-provider.md): décrit les conditions d’enregistrement pour un fournisseur OSC et fournit une liste de vérification pour l’installation d’un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a550e-120">[Deploying a Provider](deploying-a-provider.md): Describes registration requirements for an OSC provider, and provides a checklist for installing a provider.</span></span>
    
- <span data-ttu-id="a550e-121">[Préparation pour la publication d’un fournisseur OSC](getting-ready-to-release-an-osc-provider.md): suggère des tests, vous pouvez effectuer avant de libérer un fournisseur OSC.</span><span class="sxs-lookup"><span data-stu-id="a550e-121">[Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md): Suggests tests you can do before releasing an OSC provider.</span></span>
    
- <span data-ttu-id="a550e-122">[Référence du fournisseur Outlook Social Connector](outlook-social-connector-provider-reference-0.md): fournit des informations pour les interfaces d’extensibilité fournisseur OSC et schéma XML OSC et listes de codes d’erreur possibles.</span><span class="sxs-lookup"><span data-stu-id="a550e-122">[Outlook Social Connector Provider Reference](outlook-social-connector-provider-reference-0.md): Provides reference information for the OSC provider extensibility interfaces and OSC XML schema, and lists possible error codes.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a550e-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a550e-123">See also</span></span>

- [<span data-ttu-id="a550e-124">Informations de copyright-référence du fournisseur Outlook Social Connector 2013</span><span class="sxs-lookup"><span data-stu-id="a550e-124">Outlook Social Connector 2013 provider reference copyright notice</span></span>](outlook-social-connector-2013-provider-reference-copyright-notice.md) 
- [<span data-ttu-id="a550e-125">Conventions de document</span><span class="sxs-lookup"><span data-stu-id="a550e-125">Document Conventions</span></span>](http://msdn.microsoft.com/en-us/office/aa905365.aspx)   
- [<span data-ttu-id="a550e-126">Accessibilité des produits Microsoft</span><span class="sxs-lookup"><span data-stu-id="a550e-126">Accessibility in Microsoft Products</span></span>](http://www.microsoft.com/enable/products/default.aspx)  
- [<span data-ttu-id="a550e-127">Déclaration de confidentialité Microsoft</span><span class="sxs-lookup"><span data-stu-id="a550e-127">Microsoft Online Privacy Notice</span></span>](https://privacy.microsoft.com/en-us/privacystatement)
    

