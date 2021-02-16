---
title: Mise en œuvre d’une table One-Off conteneur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 72dc73b6ed8519be2d8010544fdd5dc5b7b0f759
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417419"
---
# <a name="implementing-a-container-one-off-table"></a><span data-ttu-id="e1ff7-103">Mise en œuvre d’une table One-Off conteneur</span><span class="sxs-lookup"><span data-stu-id="e1ff7-103">Implementing a Container One-Off Table</span></span>

  
  
<span data-ttu-id="e1ff7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1ff7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1ff7-105">Pour accéder à la table unique appartenant à l’un de vos conteneurs, MAPI appelle la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur pour ouvrir la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) avec l’interface **IMAPITable.**</span><span class="sxs-lookup"><span data-stu-id="e1ff7-105">To access the one-off table belonging to one of your containers, MAPI calls the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> <span data-ttu-id="e1ff7-106">Votre conteneur est invité à retourner sa table one-off lorsqu’une application cliente tente d’ajouter un destinataire au conteneur.</span><span class="sxs-lookup"><span data-stu-id="e1ff7-106">Your container is asked to return its one-off table when a client application is trying to add a recipient to the container.</span></span> <span data-ttu-id="e1ff7-107">Si le conteneur autorise des destinataires, votre fournisseur peut retourner sa propre implémentation de table ou appeler [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) pour renvoyer l’implémentation MAPI.</span><span class="sxs-lookup"><span data-stu-id="e1ff7-107">If the container allows any recipients, your provider can either return its own table implementation or call [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) to return the MAPI implementation.</span></span> 
  
<span data-ttu-id="e1ff7-108">L’ensemble des modèles de la table unique de conteneur doit refléter le type de destinataires que le conteneur particulier peut contenir.</span><span class="sxs-lookup"><span data-stu-id="e1ff7-108">The set of templates in the container one-off table should reflect the type of recipients that the particular container can hold.</span></span> <span data-ttu-id="e1ff7-109">En règle générale, cela inclut un ou deux modèles, des modèles pour la création d’un utilisateur de messagerie individuel ou d’une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="e1ff7-109">Typically, this includes one or two templates, templates for creating an individual messaging user or a distribution list.</span></span> <span data-ttu-id="e1ff7-110">Les identificateurs d’entrée pour ces modèles sont détenus dans les propriétés **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) et **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e1ff7-110">The entry identifiers for these templates are held in the **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) and **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) properties.</span></span> <span data-ttu-id="e1ff7-111">Toutefois, les conteneurs ne sont en aucun cas limités à ces types d’entrées.</span><span class="sxs-lookup"><span data-stu-id="e1ff7-111">However, containers are by no means limited to these types of entries.</span></span> <span data-ttu-id="e1ff7-112">Elles peuvent contenir d’autres types de destinataires ou d’entrées non destinataires, telles que des répertoires.</span><span class="sxs-lookup"><span data-stu-id="e1ff7-112">They can hold other types of recipients or non-recipient entries such as directories.</span></span> 
  

