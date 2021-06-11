---
title: Formulaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41d35370-495d-40fe-80bc-6c3bfc995b85
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 951a1c88d2fd4291ee0b48924de6eda8f43c3e47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409971"
---
# <a name="mapi-forms"></a><span data-ttu-id="caf7b-103">Formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="caf7b-103">MAPI Forms</span></span>

  
  
<span data-ttu-id="caf7b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="caf7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="caf7b-105">Après avoir lu cette vue d’ensemble de l’architecture de formulaire MAPI, vous comprendrez ce que sont les formulaires MAPI et la façon dont ils interagissent avec d’autres composants du sous-système MAPI.</span><span class="sxs-lookup"><span data-stu-id="caf7b-105">After reading this overview of the MAPI form architecture, you will have an understanding of what MAPI forms are and how they interact with other components of the MAPI subsystem.</span></span> <span data-ttu-id="caf7b-106">L’objectif de cette section est de vous donner les connaissances conceptuelles dont vous avez besoin pour implémenter vos propres serveurs de formulaire MAPI.</span><span class="sxs-lookup"><span data-stu-id="caf7b-106">The purpose of this section is to give you the conceptual knowledge you need to implement your own MAPI form servers.</span></span>
  
<span data-ttu-id="caf7b-107">Avant de lire cette section, familiarisez-vous avec les documents de la rubrique Vue d’ensemble des [formulaires MAPI.](mapi-forms-overview.md)</span><span class="sxs-lookup"><span data-stu-id="caf7b-107">Before reading this section, you should familiarize yourself with the material in the [MAPI Forms Overview](mapi-forms-overview.md) topic.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="caf7b-108">Étant donné que l’architecture de formulaire MAPI est basée sur le modèle objet composant (COM), le développement d’applications serveur de formulaires nécessite une connaissance de la programmation COM.</span><span class="sxs-lookup"><span data-stu-id="caf7b-108">Because the MAPI form architecture is based on the Component Object Model (COM), developing form server applications requires knowledge of COM programming.</span></span> <span data-ttu-id="caf7b-109">Pour plus d’informations sur COM, voir la section COM et ActiveX Object Services dans Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="caf7b-109">For more information about COM, see the COM and ActiveX Object Services section in the Windows SDK.</span></span> 
  

