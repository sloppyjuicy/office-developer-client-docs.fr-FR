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
ms.openlocfilehash: b53cdb4fe379405018555f1cca9fa40ddc5d0fa8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592485"
---
# <a name="mapi-forms"></a><span data-ttu-id="a1b17-103">Formulaires MAPI</span><span class="sxs-lookup"><span data-stu-id="a1b17-103">MAPI Forms</span></span>

  
  
<span data-ttu-id="a1b17-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1b17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1b17-105">Après avoir lu cette vue d’ensemble de l’architecture de formulaire MAPI, vous devez comprendre quels sont les formulaires MAPI et comment ils interagissent avec les autres composants du sous-système MAPI.</span><span class="sxs-lookup"><span data-stu-id="a1b17-105">After reading this overview of the MAPI form architecture, you will have an understanding of what MAPI forms are and how they interact with other components of the MAPI subsystem.</span></span> <span data-ttu-id="a1b17-106">L’objectif de cette section est de vous donner les connaissances conceptuelle, vous devez implémenter votre propre formulaire MAPI des serveurs.</span><span class="sxs-lookup"><span data-stu-id="a1b17-106">The purpose of this section is to give you the conceptual knowledge you need to implement your own MAPI form servers.</span></span>
  
<span data-ttu-id="a1b17-107">Avant de lire cette section, vous devez vous familiariser avec le matériel dans la rubrique [Vue d’ensemble des formulaires MAPI](mapi-forms-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="a1b17-107">Before reading this section, you should familiarize yourself with the material in the [MAPI Forms Overview](mapi-forms-overview.md) topic.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a1b17-108">Étant donné que l’architecture de formulaire MAPI est basé sur le composant COM (Object Model), développement d’applications de serveur formulaire nécessite une connaissance de la programmation COM.</span><span class="sxs-lookup"><span data-stu-id="a1b17-108">Because the MAPI form architecture is based on the Component Object Model (COM), developing form server applications requires knowledge of COM programming.</span></span> <span data-ttu-id="a1b17-109">Pour plus d’informations sur COM, consultez la section COM et ActiveX Object Services dans le SDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="a1b17-109">For more information about COM, see the COM and ActiveX Object Services section in the Windows SDK.</span></span> 
  

