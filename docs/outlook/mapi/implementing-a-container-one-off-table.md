---
title: Implémentation d'une table ponctuelle de conteneur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 72dc73b6ed8519be2d8010544fdd5dc5b7b0f759
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332885"
---
# <a name="implementing-a-container-one-off-table"></a><span data-ttu-id="fcff1-103">Implémentation d'une table ponctuelle de conteneur</span><span class="sxs-lookup"><span data-stu-id="fcff1-103">Implementing a Container One-Off Table</span></span>

  
  
<span data-ttu-id="fcff1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcff1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcff1-105">Pour accéder à la table ponctuelle appartenant à l'un de vos conteneurs, MAPI appelle la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) du conteneur pour ouvrir la **propriété PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) avec la méthode **IMAPITable** . Lip.</span><span class="sxs-lookup"><span data-stu-id="fcff1-105">To access the one-off table belonging to one of your containers, MAPI calls the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> <span data-ttu-id="fcff1-106">Votre conteneur est invité à retourner sa table One-Off lorsqu'une application cliente tente d'ajouter un destinataire au conteneur.</span><span class="sxs-lookup"><span data-stu-id="fcff1-106">Your container is asked to return its one-off table when a client application is trying to add a recipient to the container.</span></span> <span data-ttu-id="fcff1-107">Si le conteneur autorise des destinataires, votre fournisseur peut renvoyer sa propre implémentation de table ou appeler [IMAPISupport:: GetOneOffTable](imapisupport-getoneofftable.md) pour retourner l'implémentation MAPI.</span><span class="sxs-lookup"><span data-stu-id="fcff1-107">If the container allows any recipients, your provider can either return its own table implementation or call [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) to return the MAPI implementation.</span></span> 
  
<span data-ttu-id="fcff1-108">L'ensemble des modèles de la table ponctuelle conteneur doit refléter le type de destinataire que le conteneur particulier peut conserver.</span><span class="sxs-lookup"><span data-stu-id="fcff1-108">The set of templates in the container one-off table should reflect the type of recipients that the particular container can hold.</span></span> <span data-ttu-id="fcff1-109">En règle générale, cela inclut un ou deux modèles, des modèles pour la création d'un utilisateur de messagerie individuel ou d'une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="fcff1-109">Typically, this includes one or two templates, templates for creating an individual messaging user or a distribution list.</span></span> <span data-ttu-id="fcff1-110">Les identificateurs d'entrée de ces modèles sont conservés dans les propriétés **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) et **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fcff1-110">The entry identifiers for these templates are held in the **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) and **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) properties.</span></span> <span data-ttu-id="fcff1-111">Toutefois, les conteneurs ne sont pas limités à ces types d'entrées.</span><span class="sxs-lookup"><span data-stu-id="fcff1-111">However, containers are by no means limited to these types of entries.</span></span> <span data-ttu-id="fcff1-112">Ils peuvent contenir d'autres types de destinataires ou d'entrées autres que des destinataires, tels que des annuaires.</span><span class="sxs-lookup"><span data-stu-id="fcff1-112">They can hold other types of recipients or non-recipient entries such as directories.</span></span> 
  

