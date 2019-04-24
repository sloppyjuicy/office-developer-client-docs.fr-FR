---
title: Résolution d'un nom de destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: a3faed3dda2461cab749c824fc97c2074e62375f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328671"
---
# <a name="resolving-a-recipient-name"></a><span data-ttu-id="ec6c2-103">Résolution d'un nom de destinataire</span><span class="sxs-lookup"><span data-stu-id="ec6c2-103">Resolving a Recipient Name</span></span>

  
  
<span data-ttu-id="ec6c2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec6c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec6c2-105">Lorsqu'un message est adressé, une liste de destinataires est créée avec des propriétés relatives à chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-105">When a message is addressed, a recipient list is built with properties relating to each recipient.</span></span> <span data-ttu-id="ec6c2-106">Lors de l'envoi du message, l'une de ces propriétés doit être l'identificateur d'entrée à long terme du destinataire.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-106">By the time the message is sent, one of those properties must be the recipient's long-term entry identifier.</span></span> <span data-ttu-id="ec6c2-107">Pour vous assurer que chaque destinataire inclut la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), transmettez la structure [ADRLIST](adrlist.md) décrivant votre liste de destinataires dans le contenu du paramètre _lpAdrList_ dans un appel à [IAddrBook:: ResolveName](iaddrbook-resolvename.md).</span><span class="sxs-lookup"><span data-stu-id="ec6c2-107">To ensure that each recipient includes the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, pass the [ADRLIST](adrlist.md) structure describing your recipient list in the contents of the  _lpAdrList_ parameter in a call to [IAddrBook::ResolveName](iaddrbook-resolvename.md).</span></span>
  
 <span data-ttu-id="ec6c2-108">**ResolveName** commence le traitement en ignorant les entrées de la structure **ADRLIST** qui ont déjà été résolues, comme indiqué par la présence d'un identificateur d'entrée dans le **SPropValue** de la structure [ADRENTRY](adrentry.md) correspondante. Tableau.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-108">**ResolveName** begins processing by ignoring the entries in the **ADRLIST** structure that have already been resolved, as indicated by the presence of an entry identifier in the corresponding [ADRENTRY](adrentry.md) structure's **SPropValue** array.</span></span> <span data-ttu-id="ec6c2-109">Ensuite, **ResolveName** affecte automatiquement des identificateurs d'entrée uniques à deux types de destinataires:</span><span class="sxs-lookup"><span data-stu-id="ec6c2-109">Next, **ResolveName** automatically assigns one-off entry identifiers to two types of recipients:</span></span> 
  
- <span data-ttu-id="ec6c2-110">Destinataires avec une adresse au format d'adresse Internet</span><span class="sxs-lookup"><span data-stu-id="ec6c2-110">Recipients with an address formatted as an Internet address</span></span>
    
- <span data-ttu-id="ec6c2-111">Destinataires dont l'adresse est formatée comme suit:</span><span class="sxs-lookup"><span data-stu-id="ec6c2-111">Recipients with an address formatted as follows:</span></span>
    
     `displayname[address type:email address]`
    
<span data-ttu-id="ec6c2-112">Pour toutes les entrées restantes, **ResolveName** recherche dans le carnet d'adresses une correspondance exacte sur le nom complet.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-112">For all remaining entries, **ResolveName** searches the address book for an exact match on the display name.</span></span> <span data-ttu-id="ec6c2-113">**ResolveName** utilise la propriété **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) pour déterminer l'ensemble de conteneurs à rechercher et l'ordre de recherche.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-113">**ResolveName** uses the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property to determine the set of containers to search and the search order.</span></span> <span data-ttu-id="ec6c2-114">MAPI appelle la méthode [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) de chaque conteneur pour tenter de résoudre tous les noms.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-114">MAPI calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method of every container to attempt to resolve all of the names.</span></span> <span data-ttu-id="ec6c2-115">Étant donné que certains conteneurs ne prennent pas en charge **ResolveNames**, si le conteneur renvoie MAPI_E_NO_SUPPORT, MAPI applique une restriction de propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) par rapport à sa table de contenu.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-115">Because some containers do not support **ResolveNames**, if the container returns MAPI_E_NO_SUPPORT, MAPI applies a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction against its contents table.</span></span> <span data-ttu-id="ec6c2-116">Tous les conteneurs de carnet d'adresses sont requis pour prendre en charge la résolution de noms avec cette restriction.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-116">All address book containers are required to support name resolution with this restriction.</span></span> <span data-ttu-id="ec6c2-117">Une fois que tous les noms sont résolus, aucun autre appel de conteneur n'est effectué.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-117">Once all the names are resolved, no further container calls are made.</span></span> <span data-ttu-id="ec6c2-118">Si tous les conteneurs ont été appelés, mais que les noms ambigus ou non résolus restent, MAPI affiche une boîte de dialogue si possible pour inviter l'utilisateur à résoudre les noms restants.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-118">If all the containers have been called, but ambiguous or unresolved names remain, MAPI displays a dialog box if possible to prompt the user to resolve the remaining names.</span></span>
  
<span data-ttu-id="ec6c2-119">La restriction **PR_ANR** établit une correspondance entre la valeur de la propriété **PR_ANR** et le nom complet de la structure **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="ec6c2-119">The **PR_ANR** restriction matches the value of the **PR_ANR** property against the display name in the **ADRLIST** structure.</span></span> <span data-ttu-id="ec6c2-120">En limitant la vue de la table des matières d'un conteneur à l'aide de la restriction de propriété **PR_ANR** , le fournisseur de carnet d'adresses exécute un type de recherche «meilleure estimation», avec la mise en correspondance avec la propriété qui est logique pour le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-120">Limiting the view of a container's contents table with the **PR_ANR** property restriction causes the address book provider to perform a "best guess" type of search, matching against the property that makes sense for the provider.</span></span> <span data-ttu-id="ec6c2-121">Par exemple, un fournisseur de carnet d'adresses peut toujours faire correspondre les noms de la liste des destinataires avec **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), tandis qu'un autre peut autoriser un administrateur à sélectionner la propriété.</span><span class="sxs-lookup"><span data-stu-id="ec6c2-121">For example, one address book provider might always match names in the recipient list against **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) while another might allow an administrator to select the property.</span></span>
  
 <span data-ttu-id="ec6c2-122">**Pour définir une restriction de propriété PR_ANR sur une table des matières d'un conteneur de carnet d'adresses**</span><span class="sxs-lookup"><span data-stu-id="ec6c2-122">**To set a PR_ANR property restriction on an address book container's contents table**</span></span>
  
1. <span data-ttu-id="ec6c2-123">Créez une structure [SRestriction](srestriction.md) comme illustré dans le code suivant:</span><span class="sxs-lookup"><span data-stu-id="ec6c2-123">Create an [SRestriction](srestriction.md) structure as shown in the following code:</span></span> 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. <span data-ttu-id="ec6c2-124">Appelez la méthode [IMAPITable:: Restrict](imapitable-restrict.md) du tableau contents, en transmettant la structure **SRestriction** en tant que paramètre _lpRestriction_ .</span><span class="sxs-lookup"><span data-stu-id="ec6c2-124">Call the contents table's [IMAPITable::Restrict](imapitable-restrict.md) method, passing the **SRestriction** structure as the  _lpRestriction_ parameter.</span></span> 
    

