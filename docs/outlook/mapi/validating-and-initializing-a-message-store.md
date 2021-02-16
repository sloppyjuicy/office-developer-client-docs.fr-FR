---
title: Validation et initialisation d’une magasin de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 77b3f707fc36a868de5acd7c7ba4642a1da4e3c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433688"
---
# <a name="validating-and-initializing-a-message-store"></a><span data-ttu-id="e75f8-103">Validation et initialisation d’une magasin de messages</span><span class="sxs-lookup"><span data-stu-id="e75f8-103">Validating and Initializing a Message Store</span></span>

  
  
<span data-ttu-id="e75f8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e75f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e75f8-105">Lorsque vous ouvrez une magasin de messages via la méthode [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) sans définir l’indicateur MDB_NO_MAIL, MAPI crée plusieurs dossiers et leur attribue des noms et des rôles par défaut.</span><span class="sxs-lookup"><span data-stu-id="e75f8-105">When you open a message store through the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method without setting the MDB_NO_MAIL flag, MAPI creates several folders and assigns them default names and roles.</span></span> <span data-ttu-id="e75f8-106">MAPI est responsable de la création de ces dossiers afin d’éviter les incompatibilités qui seraient inévitablement présentes si les clients ou les fournisseurs de magasins de messages étaient responsables de la création.</span><span class="sxs-lookup"><span data-stu-id="e75f8-106">MAPI is responsible for creating these folders to avoid the incompatibilities that would inevitably occur if either clients or message store providers were responsible for the creation.</span></span> 
  
<span data-ttu-id="e75f8-107">Il est parfois nécessaire de vérifier que les dossiers appropriés ont été créés et qu’ils sont valides.</span><span class="sxs-lookup"><span data-stu-id="e75f8-107">Sometimes it is necessary to verify that the appropriate folders have been created and that they are valid.</span></span> <span data-ttu-id="e75f8-108">La [fonction HrValidateIPMSubtree](hrvalidateipmsubtree.md) est disponible à cet effet.</span><span class="sxs-lookup"><span data-stu-id="e75f8-108">The [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function is available for this purpose.</span></span> <span data-ttu-id="e75f8-109">Si vous validez la boutique de messages par défaut, passez l’MAPI_FULL_IPM_TREE message.</span><span class="sxs-lookup"><span data-stu-id="e75f8-109">If you are validating the default message store, pass the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="e75f8-110">Un groupe plus étendu de dossiers est créé pour la magasin de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="e75f8-110">A more extensive group of folders is created for the default message store.</span></span> <span data-ttu-id="e75f8-111">Lorsque **HrValidateIPMSubtree** reçoit l’indicateur MAPI_FULL_IPM_TREE, il recherche les dossiers suivants :</span><span class="sxs-lookup"><span data-stu-id="e75f8-111">When **HrValidateIPMSubtree** receives the MAPI_FULL_IPM_TREE flag, it checks for the following folders:</span></span> 
  
- <span data-ttu-id="e75f8-112">Dossier racine de la sous-arbre IPM</span><span class="sxs-lookup"><span data-stu-id="e75f8-112">Root folder for the IPM subtree</span></span>
    
- <span data-ttu-id="e75f8-113">Dossier Éléments supprimés dans le dossier racine IPM</span><span class="sxs-lookup"><span data-stu-id="e75f8-113">Deleted Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="e75f8-114">Dossier boîte de réception dans le dossier racine IPM</span><span class="sxs-lookup"><span data-stu-id="e75f8-114">Inbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="e75f8-115">Dossier boîte d’envoi dans le dossier racine IPM</span><span class="sxs-lookup"><span data-stu-id="e75f8-115">Outbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="e75f8-116">Dossier Éléments envoyés dans le dossier racine IPM</span><span class="sxs-lookup"><span data-stu-id="e75f8-116">Sent Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="e75f8-117">Affichages des dossiers dans le dossier racine de la boutique de messages</span><span class="sxs-lookup"><span data-stu-id="e75f8-117">Folder views in the message store's root folder</span></span>
    
- <span data-ttu-id="e75f8-118">Affichages communs dans le dossier racine de la boutique de messages</span><span class="sxs-lookup"><span data-stu-id="e75f8-118">Common views in the message store's root folder</span></span>
    
- <span data-ttu-id="e75f8-119">Dossier de recherche dans le dossier racine de la boutique de messages</span><span class="sxs-lookup"><span data-stu-id="e75f8-119">Search folder in the message store's root folder</span></span>
    
<span data-ttu-id="e75f8-120">Si la magasin de messages n’est pas la valeur par défaut, vous pouvez définir ou non l’MAPI_FULL_IPM_TREE de message.</span><span class="sxs-lookup"><span data-stu-id="e75f8-120">If the message store is not the default, you can either set or not set the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="e75f8-121">Lorsque cet indicateur n’est pas définie, **HrValidateIPMSubtree** vérifie uniquement le dossier racine de la sous-arbre, le dossier Éléments supprimés et le dossier racine pour les résultats de recherche de la magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="e75f8-121">When this flag is not set, **HrValidateIPMSubtree** checks for only the root folder for the subtree, the Deleted Items folder, and the root folder for message store search results.</span></span> 
  
<span data-ttu-id="e75f8-122">Pour initialiser une magasin de messages, stockez les propriétés suivantes en mémoire afin qu’elles soient facilement disponibles :</span><span class="sxs-lookup"><span data-stu-id="e75f8-122">To initialize a message store, store the following properties in memory so that they are readily available:</span></span>
  
- <span data-ttu-id="e75f8-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e75f8-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span></span>
    
- <span data-ttu-id="e75f8-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="e75f8-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>
    
<span data-ttu-id="e75f8-125">Ces propriétés sont des masques de bits qui décrivent les fonctionnalités de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="e75f8-125">These properties are bitmasks that describe features of the message store.</span></span> <span data-ttu-id="e75f8-126">**PR_VALID_FOLDER_MASK** a un bit pour chaque dossier spécial qui existe dans la magasin de messages et possède un identificateur d’entrée attribué valide.</span><span class="sxs-lookup"><span data-stu-id="e75f8-126">**PR_VALID_FOLDER_MASK** has one bit set for every special folder that exists in the message store and has an assigned entry identifier that is valid.</span></span> <span data-ttu-id="e75f8-127">Pour plus d’informations sur l’accès à ces dossiers et à leurs identificateurs d’entrée, voir [Ouverture d’un dossier de la boutique de messages.](opening-a-message-store-folder.md)</span><span class="sxs-lookup"><span data-stu-id="e75f8-127">For more information about accessing these folders and their entry identifiers, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span> 
  
 <span data-ttu-id="e75f8-128">**PR_STORE_SUPPORT_MASK** a un bit pour chaque fonctionnalité prise en charge dans la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="e75f8-128">**PR_STORE_SUPPORT_MASK** has one bit set for every feature supported in the message store.</span></span> <span data-ttu-id="e75f8-129">Par exemple, si une magasin de messages  prend en charge les notifications et le texte mis en forme, son PR_STORE_SUPPORT_MASK les bits STORE_NOTIFY_OK et STORE_RTF_OK sont définies.</span><span class="sxs-lookup"><span data-stu-id="e75f8-129">For example, if a message store supports notification and formatted text, its **PR_STORE_SUPPORT_MASK** will have the STORE_NOTIFY_OK and STORE_RTF_OK bits set.</span></span> 
  
<span data-ttu-id="e75f8-130">Les autres propriétés qui doivent être stockées localement incluent les identificateurs d’entrée pour les dossiers que la **propriété PR_VALID_FOLDER_MASK** décrit comme valides.</span><span class="sxs-lookup"><span data-stu-id="e75f8-130">Other properties that should be stored locally include the entry identifiers for the folders that the **PR_VALID_FOLDER_MASK** property describes as valid.</span></span> <span data-ttu-id="e75f8-131">Chacun de ces dossiers spéciaux, à l’exception du dossier Boîte de réception, est associé à une propriété d’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e75f8-131">Each of these special folders, except for the Inbox folder, has an entry identifier property associated with it.</span></span> <span data-ttu-id="e75f8-132">Par exemple, l’identificateur d’entrée pour le dossier Boîte d’envoi est **PR_IPM_OUTBOX_ENTRYID** propriété ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e75f8-132">For example, the entry identifier for the Outbox folder is its **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="e75f8-133">Étant donné que ces dossiers sont les dossiers qui seront ouverts fréquemment, il est bon d’avoir leurs identificateurs d’entrée facilement disponibles.</span><span class="sxs-lookup"><span data-stu-id="e75f8-133">Because these folders are the folders that will be opened frequently, it is a good idea to have their entry identifiers readily available.</span></span>
  

