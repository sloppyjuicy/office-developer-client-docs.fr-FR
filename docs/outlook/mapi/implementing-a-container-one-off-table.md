---
title: L’implémentation d’une Table unique du conteneur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 83351e18750ccbffbe60c4e19f9b04a9c94a42e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784155"
---
# <a name="implementing-a-container-one-off-table"></a><span data-ttu-id="9aa60-103">L’implémentation d’une Table unique du conteneur</span><span class="sxs-lookup"><span data-stu-id="9aa60-103">Implementing a Container One-Off Table</span></span>

  
  
<span data-ttu-id="9aa60-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9aa60-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9aa60-105">Pour accéder à la table unique appartenant à l’une de vos conteneurs, MAPI appelle la méthode de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur pour ouvrir la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) avec **IMAPITable** interface.</span><span class="sxs-lookup"><span data-stu-id="9aa60-105">To access the one-off table belonging to one of your containers, MAPI calls the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> <span data-ttu-id="9aa60-106">Le conteneur est demandé à retourner sa table unique lors d’une application cliente ajouter un destinataire vers le conteneur.</span><span class="sxs-lookup"><span data-stu-id="9aa60-106">Your container is asked to return its one-off table when a client application is trying to add a recipient to the container.</span></span> <span data-ttu-id="9aa60-107">Si le conteneur autorise tous les destinataires, votre fournisseur peut retourner son propre implémentation tableau soit appeler [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) pour retourner l’implémentation MAPI.</span><span class="sxs-lookup"><span data-stu-id="9aa60-107">If the container allows any recipients, your provider can either return its own table implementation or call [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) to return the MAPI implementation.</span></span> 
  
<span data-ttu-id="9aa60-108">L’ensemble des modèles dans la table uniques conteneur doit refléter le type de destinataires conteneur peut contenir.</span><span class="sxs-lookup"><span data-stu-id="9aa60-108">The set of templates in the container one-off table should reflect the type of recipients that the particular container can hold.</span></span> <span data-ttu-id="9aa60-109">En règle générale, cela inclut un ou deux modèles, les modèles pour la création d’un utilisateur de messagerie spécifique ou une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="9aa60-109">Typically, this includes one or two templates, templates for creating an individual messaging user or a distribution list.</span></span> <span data-ttu-id="9aa60-110">Les identificateurs d’entrée de ces modèles sont stockés dans le **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) et les propriétés **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9aa60-110">The entry identifiers for these templates are held in the **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) and **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) properties.</span></span> <span data-ttu-id="9aa60-111">Toutefois, les conteneurs ne sont en aucun cas limités à ces types d’entrées.</span><span class="sxs-lookup"><span data-stu-id="9aa60-111">However, containers are by no means limited to these types of entries.</span></span> <span data-ttu-id="9aa60-112">Ils peuvent contenir d’autres types de destinataires ou entrées non-recipient comme des répertoires.</span><span class="sxs-lookup"><span data-stu-id="9aa60-112">They can hold other types of recipients or non-recipient entries such as directories.</span></span> 
  

