---
title: Résolution d’un nom de destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d9b52edf7f4633fdf9c925a8d8db4953590713b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562931"
---
# <a name="resolving-a-recipient-name"></a><span data-ttu-id="4a832-103">Résolution d’un nom de destinataire</span><span class="sxs-lookup"><span data-stu-id="4a832-103">Resolving a Recipient Name</span></span>

  
  
<span data-ttu-id="4a832-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a832-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a832-105">Lorsqu’un message est adressé, une liste de destinataires est générée avec les propriétés relatives à chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="4a832-105">When a message is addressed, a recipient list is built with properties relating to each recipient.</span></span> <span data-ttu-id="4a832-106">Au moment où que le message est envoyé, une de ces propriétés doit être l’identificateur d’entrée du destinataire à long terme.</span><span class="sxs-lookup"><span data-stu-id="4a832-106">By the time the message is sent, one of those properties must be the recipient's long-term entry identifier.</span></span> <span data-ttu-id="4a832-107">Pour vous assurer que chaque destinataire inclut la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), passez la structure [ADRLIST](adrlist.md) décrivant votre liste de destinataires dans le contenu du paramètre _lpAdrList_ dans un appel à [IAddrBook :: ResolveName](iaddrbook-resolvename.md).</span><span class="sxs-lookup"><span data-stu-id="4a832-107">To ensure that each recipient includes the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, pass the [ADRLIST](adrlist.md) structure describing your recipient list in the contents of the  _lpAdrList_ parameter in a call to [IAddrBook::ResolveName](iaddrbook-resolvename.md).</span></span>
  
 <span data-ttu-id="4a832-108">**ResolveName** commence le traitement en ignorant les entrées de la structure **ADRLIST** qui ont déjà été résolues, comme indiqué par la présence d’un identificateur d’entrée dans la structure [ADRENTRY](adrentry.md) correspondant **SPropValue** tableau.</span><span class="sxs-lookup"><span data-stu-id="4a832-108">**ResolveName** begins processing by ignoring the entries in the **ADRLIST** structure that have already been resolved, as indicated by the presence of an entry identifier in the corresponding [ADRENTRY](adrentry.md) structure's **SPropValue** array.</span></span> <span data-ttu-id="4a832-109">Ensuite, **ResolveName** affecte automatiquement les identificateurs d’entrée unique à deux types de destinataires :</span><span class="sxs-lookup"><span data-stu-id="4a832-109">Next, **ResolveName** automatically assigns one-off entry identifiers to two types of recipients:</span></span> 
  
- <span data-ttu-id="4a832-110">Destinataires dont l’adresse mise en forme comme une adresse Internet</span><span class="sxs-lookup"><span data-stu-id="4a832-110">Recipients with an address formatted as an Internet address</span></span>
    
- <span data-ttu-id="4a832-111">Destinataires dont l’adresse mise en forme comme suit :</span><span class="sxs-lookup"><span data-stu-id="4a832-111">Recipients with an address formatted as follows:</span></span>
    
     `displayname[address type:email address]`
    
<span data-ttu-id="4a832-112">Pour toutes les entrées restantes, **ResolveName** recherche une correspondance exacte sur le nom complet du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="4a832-112">For all remaining entries, **ResolveName** searches the address book for an exact match on the display name.</span></span> <span data-ttu-id="4a832-113">**ResolveName** utilise la propriété **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) pour déterminer l’ensemble des conteneurs à la recherche et l’ordre de recherche.</span><span class="sxs-lookup"><span data-stu-id="4a832-113">**ResolveName** uses the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property to determine the set of containers to search and the search order.</span></span> <span data-ttu-id="4a832-114">La méthode [IABContainer::ResolveNames](iabcontainer-resolvenames.md) de chaque conteneur pour essayer de résoudre tous les noms des appels MAPI.</span><span class="sxs-lookup"><span data-stu-id="4a832-114">MAPI calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method of every container to attempt to resolve all of the names.</span></span> <span data-ttu-id="4a832-115">Étant donné que certains conteneurs ne prennent pas en charge **ResolveNames**, si le conteneur renvoie MAPI_E_NO_SUPPORT, MAPI applique une restriction de propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) par rapport à sa table des matières.</span><span class="sxs-lookup"><span data-stu-id="4a832-115">Because some containers do not support **ResolveNames**, if the container returns MAPI_E_NO_SUPPORT, MAPI applies a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction against its contents table.</span></span> <span data-ttu-id="4a832-116">Tous les conteneurs de carnet d’adresses sont requis pour prendre en charge la résolution de noms avec cette restriction.</span><span class="sxs-lookup"><span data-stu-id="4a832-116">All address book containers are required to support name resolution with this restriction.</span></span> <span data-ttu-id="4a832-117">Une fois que tous les noms sont résolus, aucune autre conteneur appels sont effectuées.</span><span class="sxs-lookup"><span data-stu-id="4a832-117">Once all the names are resolved, no further container calls are made.</span></span> <span data-ttu-id="4a832-118">Si tous les conteneurs ont été appelées, mais restent noms ambigus ou non résolues, MAPI affiche une boîte de dialogue si possible pour inviter l’utilisateur à résoudre les noms restants.</span><span class="sxs-lookup"><span data-stu-id="4a832-118">If all the containers have been called, but ambiguous or unresolved names remain, MAPI displays a dialog box if possible to prompt the user to resolve the remaining names.</span></span>
  
<span data-ttu-id="4a832-119">La restriction de **PR_ANR** correspond à la valeur de la propriété **PR_ANR** sur le nom complet de la structure **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="4a832-119">The **PR_ANR** restriction matches the value of the **PR_ANR** property against the display name in the **ADRLIST** structure.</span></span> <span data-ttu-id="4a832-120">Limitation de l’affichage du tableau de contenu d’un conteneur avec la restriction de propriété **PR_ANR** entraîne le fournisseur de carnet d’adresses effectuer un type de « deviner mieux » de la recherche, en correspondance avec la propriété qui est significatif pour le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4a832-120">Limiting the view of a container's contents table with the **PR_ANR** property restriction causes the address book provider to perform a "best guess" type of search, matching against the property that makes sense for the provider.</span></span> <span data-ttu-id="4a832-121">Par exemple, un fournisseur de carnet d’adresses peut toujours correspondre les noms dans la liste de destinataires par rapport à **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) tandis qu’une autre peut autoriser un administrateur à sélectionner la propriété.</span><span class="sxs-lookup"><span data-stu-id="4a832-121">For example, one address book provider might always match names in the recipient list against **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) while another might allow an administrator to select the property.</span></span>
  
 <span data-ttu-id="4a832-122">**Pour définir une restriction de propriété PR_ANR sur tableau de contenu d’un conteneur carnet d’adresses**</span><span class="sxs-lookup"><span data-stu-id="4a832-122">**To set a PR_ANR property restriction on an address book container's contents table**</span></span>
  
1. <span data-ttu-id="4a832-123">Créez une structure [SRestriction](srestriction.md) comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="4a832-123">Create an [SRestriction](srestriction.md) structure as shown in the following code:</span></span> 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. <span data-ttu-id="4a832-124">Appelez le contenu [IMAPITable](imapitable-restrict.md) méthode du tableau, en passant la structure **SRestriction** en tant que paramètre _lpRestriction_ .</span><span class="sxs-lookup"><span data-stu-id="4a832-124">Call the contents table's [IMAPITable::Restrict](imapitable-restrict.md) method, passing the **SRestriction** structure as the  _lpRestriction_ parameter.</span></span> 
    

