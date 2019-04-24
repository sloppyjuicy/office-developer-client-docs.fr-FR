---
title: Formulaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41d35370-495d-40fe-80bc-6c3bfc995b85
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 951a1c88d2fd4291ee0b48924de6eda8f43c3e47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351344"
---
# <a name="mapi-forms"></a><span data-ttu-id="3e251-103">Formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="3e251-103">MAPI Forms</span></span>

  
  
<span data-ttu-id="3e251-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e251-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e251-105">Après avoir lu cette vue d'ensemble de l'architecture des formulaires MAPI, vous aurez une bonne compréhension des formulaires MAPI et de leur interaction avec d'autres composants du sous-système MAPI.</span><span class="sxs-lookup"><span data-stu-id="3e251-105">After reading this overview of the MAPI form architecture, you will have an understanding of what MAPI forms are and how they interact with other components of the MAPI subsystem.</span></span> <span data-ttu-id="3e251-106">L'objectif de cette section est de vous donner les connaissances conceptuelles dont vous avez besoin pour implémenter vos propres serveurs de formulaires MAPI.</span><span class="sxs-lookup"><span data-stu-id="3e251-106">The purpose of this section is to give you the conceptual knowledge you need to implement your own MAPI form servers.</span></span>
  
<span data-ttu-id="3e251-107">Avant de lire cette section, vous devez vous familiariser avec le matériel figurant dans la rubrique [vue d'ensemble des formulaires MAPI](mapi-forms-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="3e251-107">Before reading this section, you should familiarize yourself with the material in the [MAPI Forms Overview](mapi-forms-overview.md) topic.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3e251-108">Étant donné que l'architecture des formulaires MAPI est basée sur le modèle COM (Component Object Model), le développement d'applications de serveur de formulaire nécessite une connaissance de la programmation COM.</span><span class="sxs-lookup"><span data-stu-id="3e251-108">Because the MAPI form architecture is based on the Component Object Model (COM), developing form server applications requires knowledge of COM programming.</span></span> <span data-ttu-id="3e251-109">Pour plus d'informations sur COM, voir la section COM and ActiveX Object Services dans le kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="3e251-109">For more information about COM, see the COM and ActiveX Object Services section in the Windows SDK.</span></span> 
  

