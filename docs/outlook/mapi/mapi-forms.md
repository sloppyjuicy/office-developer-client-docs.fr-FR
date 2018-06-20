---
title: Formulaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41d35370-495d-40fe-80bc-6c3bfc995b85
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e3f35126f3887bc1f2979721deb90891b97c9322
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784621"
---
# <a name="mapi-forms"></a><span data-ttu-id="35f6e-103">Formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="35f6e-103">MAPI Forms</span></span>

  
  
<span data-ttu-id="35f6e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="35f6e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="35f6e-105">Après avoir lu cette vue d’ensemble de l’architecture de formulaire MAPI, vous devez comprendre quels sont les formulaires MAPI et comment ils interagissent avec les autres composants du sous-système MAPI.</span><span class="sxs-lookup"><span data-stu-id="35f6e-105">After reading this overview of the MAPI form architecture, you will have an understanding of what MAPI forms are and how they interact with other components of the MAPI subsystem.</span></span> <span data-ttu-id="35f6e-106">L’objectif de cette section est de vous donner les connaissances conceptuelle, vous devez implémenter votre propre formulaire MAPI des serveurs.</span><span class="sxs-lookup"><span data-stu-id="35f6e-106">The purpose of this section is to give you the conceptual knowledge you need to implement your own MAPI form servers.</span></span>
  
<span data-ttu-id="35f6e-107">Avant de lire cette section, vous devez vous familiariser avec le matériel dans la rubrique [Vue d’ensemble des formulaires MAPI](mapi-forms-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="35f6e-107">Before reading this section, you should familiarize yourself with the material in the [MAPI Forms Overview](mapi-forms-overview.md) topic.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="35f6e-108">Étant donné que l’architecture de formulaire MAPI est basé sur le composant COM (Object Model), développement d’applications de serveur formulaire nécessite une connaissance de la programmation COM.</span><span class="sxs-lookup"><span data-stu-id="35f6e-108">Because the MAPI form architecture is based on the Component Object Model (COM), developing form server applications requires knowledge of COM programming.</span></span> <span data-ttu-id="35f6e-109">Pour plus d’informations sur COM, consultez la section COM et ActiveX Object Services dans le SDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="35f6e-109">For more information about COM, see the COM and ActiveX Object Services section in the Windows SDK.</span></span> 
  

