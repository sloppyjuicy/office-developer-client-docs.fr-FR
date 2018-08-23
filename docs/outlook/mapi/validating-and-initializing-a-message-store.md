---
title: Validation et initialisation d’une banque de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7a5a5045594e87953d967fddbdeefd5ac18c8a3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581971"
---
# <a name="validating-and-initializing-a-message-store"></a><span data-ttu-id="5d663-103">Validation et initialisation d’une banque de messages</span><span class="sxs-lookup"><span data-stu-id="5d663-103">Validating and Initializing a Message Store</span></span>

  
  
<span data-ttu-id="5d663-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d663-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d663-105">Lorsque vous ouvrez une banque de messages par le biais de la méthode [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) sans définir l’indicateur MDB_NO_MAIL, MAPI crée plusieurs dossiers et attribue les rôles et les noms par défaut.</span><span class="sxs-lookup"><span data-stu-id="5d663-105">When you open a message store through the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method without setting the MDB_NO_MAIL flag, MAPI creates several folders and assigns them default names and roles.</span></span> <span data-ttu-id="5d663-106">MAPI est responsable de la création de ces dossiers pour éviter les incompatibilités inévitablement cas de clients ou fournisseurs de banque de message ont été responsables de la création.</span><span class="sxs-lookup"><span data-stu-id="5d663-106">MAPI is responsible for creating these folders to avoid the incompatibilities that would inevitably occur if either clients or message store providers were responsible for the creation.</span></span> 
  
<span data-ttu-id="5d663-107">Il est parfois nécessaire de vérifier que les dossiers appropriés ont été créés et qu’ils sont valides.</span><span class="sxs-lookup"><span data-stu-id="5d663-107">Sometimes it is necessary to verify that the appropriate folders have been created and that they are valid.</span></span> <span data-ttu-id="5d663-108">La fonction [HrValidateIPMSubtree](hrvalidateipmsubtree.md) est disponible à cet effet.</span><span class="sxs-lookup"><span data-stu-id="5d663-108">The [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function is available for this purpose.</span></span> <span data-ttu-id="5d663-109">Si vous validez la banque de messages par défaut, passez l’indicateur MAPI_FULL_IPM_TREE.</span><span class="sxs-lookup"><span data-stu-id="5d663-109">If you are validating the default message store, pass the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="5d663-110">Un groupe de dossiers plus étendu est créé pour la banque de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="5d663-110">A more extensive group of folders is created for the default message store.</span></span> <span data-ttu-id="5d663-111">Lorsque **HrValidateIPMSubtree** reçoit l’indicateur MAPI_FULL_IPM_TREE, il recherche les dossiers suivants :</span><span class="sxs-lookup"><span data-stu-id="5d663-111">When **HrValidateIPMSubtree** receives the MAPI_FULL_IPM_TREE flag, it checks for the following folders:</span></span> 
  
- <span data-ttu-id="5d663-112">Dossier racine de la sous-arborescence IPM</span><span class="sxs-lookup"><span data-stu-id="5d663-112">Root folder for the IPM subtree</span></span>
    
- <span data-ttu-id="5d663-113">Dossier éléments supprimés dans le dossier racine IPM</span><span class="sxs-lookup"><span data-stu-id="5d663-113">Deleted Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="5d663-114">Dossier boîte de réception dans le dossier racine IPM</span><span class="sxs-lookup"><span data-stu-id="5d663-114">Inbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="5d663-115">Dossier dans le dossier racine IPM boîte d’envoi</span><span class="sxs-lookup"><span data-stu-id="5d663-115">Outbox folder in the IPM root folder</span></span>
    
- <span data-ttu-id="5d663-116">Dossier éléments envoyés dans le dossier racine IPM</span><span class="sxs-lookup"><span data-stu-id="5d663-116">Sent Items folder in the IPM root folder</span></span>
    
- <span data-ttu-id="5d663-117">Vues de dossiers dans le dossier racine de la banque messages</span><span class="sxs-lookup"><span data-stu-id="5d663-117">Folder views in the message store's root folder</span></span>
    
- <span data-ttu-id="5d663-118">Affichages courantes dans le dossier racine de la banque messages</span><span class="sxs-lookup"><span data-stu-id="5d663-118">Common views in the message store's root folder</span></span>
    
- <span data-ttu-id="5d663-119">Dossier de recherche dans le dossier racine de la banque messages</span><span class="sxs-lookup"><span data-stu-id="5d663-119">Search folder in the message store's root folder</span></span>
    
<span data-ttu-id="5d663-120">Si la banque de messages n’est pas la valeur par défaut, vous pouvez définir ou pas définir l’indicateur MAPI_FULL_IPM_TREE.</span><span class="sxs-lookup"><span data-stu-id="5d663-120">If the message store is not the default, you can either set or not set the MAPI_FULL_IPM_TREE flag.</span></span> <span data-ttu-id="5d663-121">Lorsque cet indicateur n’est pas défini, **HrValidateIPMSubtree** vérifie uniquement le dossier racine de la sous-arborescence, le dossier éléments supprimés et le dossier racine de message stockent les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="5d663-121">When this flag is not set, **HrValidateIPMSubtree** checks for only the root folder for the subtree, the Deleted Items folder, and the root folder for message store search results.</span></span> 
  
<span data-ttu-id="5d663-122">Pour initialiser une banque de messages, stocker les propriétés suivantes dans la mémoire, afin qu’ils soient disponibles :</span><span class="sxs-lookup"><span data-stu-id="5d663-122">To initialize a message store, store the following properties in memory so that they are readily available:</span></span>
  
- <span data-ttu-id="5d663-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d663-123">**PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))</span></span>
    
- <span data-ttu-id="5d663-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d663-124">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>
    
<span data-ttu-id="5d663-125">Ces propriétés sont des masques de bits qui décrivent les fonctionnalités de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="5d663-125">These properties are bitmasks that describe features of the message store.</span></span> <span data-ttu-id="5d663-126">**PR_VALID_FOLDER_MASK** a un bit défini pour chaque dossier spécial qui existe dans la banque de messages et possède un identificateur d’entrée affecté est valid.</span><span class="sxs-lookup"><span data-stu-id="5d663-126">**PR_VALID_FOLDER_MASK** has one bit set for every special folder that exists in the message store and has an assigned entry identifier that is valid.</span></span> <span data-ttu-id="5d663-127">Pour plus d’informations sur l’accès à ces dossiers et leurs identificateurs d’entrée, voir [l’ouverture d’un dossier de la banque de messages](opening-a-message-store-folder.md).</span><span class="sxs-lookup"><span data-stu-id="5d663-127">For more information about accessing these folders and their entry identifiers, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span> 
  
 <span data-ttu-id="5d663-128">**PR_STORE_SUPPORT_MASK** a un bit défini pour toutes les fonctionnalités prises en charge dans la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="5d663-128">**PR_STORE_SUPPORT_MASK** has one bit set for every feature supported in the message store.</span></span> <span data-ttu-id="5d663-129">Par exemple, si une banque de messages prend en charge les notifications et texte mis en forme, sa **PR_STORE_SUPPORT_MASK** auront l’ensemble de bits STORE_NOTIFY_OK et STORE_RTF_OK.</span><span class="sxs-lookup"><span data-stu-id="5d663-129">For example, if a message store supports notification and formatted text, its **PR_STORE_SUPPORT_MASK** will have the STORE_NOTIFY_OK and STORE_RTF_OK bits set.</span></span> 
  
<span data-ttu-id="5d663-130">Autres propriétés qui doivent être stockées localement incluent les identificateurs d’entrée pour les dossiers que la propriété **PR_VALID_FOLDER_MASK** décrit comme étant valide.</span><span class="sxs-lookup"><span data-stu-id="5d663-130">Other properties that should be stored locally include the entry identifiers for the folders that the **PR_VALID_FOLDER_MASK** property describes as valid.</span></span> <span data-ttu-id="5d663-131">Chacun de ces dossiers spéciaux, à l’exception du dossier boîte de réception, a une propriété identificateur associée.</span><span class="sxs-lookup"><span data-stu-id="5d663-131">Each of these special folders, except for the Inbox folder, has an entry identifier property associated with it.</span></span> <span data-ttu-id="5d663-132">Par exemple, l’identificateur d’entrée pour le dossier boîte d’envoi est sa propriété **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5d663-132">For example, the entry identifier for the Outbox folder is its **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="5d663-133">Étant donné que ces dossiers sont les dossiers qui seront ouverts fréquemment, il est préférable de leurs identificateurs d’entrée disponibles.</span><span class="sxs-lookup"><span data-stu-id="5d663-133">Because these folders are the folders that will be opened frequently, it is a good idea to have their entry identifiers readily available.</span></span>
  

