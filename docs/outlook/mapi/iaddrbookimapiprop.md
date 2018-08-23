---
title: IAddrBook IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook
api_type:
- COM
ms.assetid: 9ccacbc0-10d5-40f9-a12b-d090a21d0d49
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 44bc6de420953bd665bd3caa336b76b15c1effd6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579458"
---
# <a name="iaddrbook--imapiprop"></a><span data-ttu-id="1191c-103">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1191c-103">IAddrBook : IMAPIProp</span></span>

  
  
<span data-ttu-id="1191c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1191c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1191c-105">Prend en charge l’accès au carnet d’adresses MAPI et inclut des opérations, telles que l’affichage des boîtes de dialogue courantes ; conteneurs de l’ouverture, messagerie, les utilisateurs et les listes de distribution ; et la résolution de nom.</span><span class="sxs-lookup"><span data-stu-id="1191c-105">Supports access to the MAPI address book and includes operations such as displaying common dialog boxes; opening containers, messaging users, and distribution lists; and performing name resolution.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1191c-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="1191c-106">Header file:</span></span>  <br/> |<span data-ttu-id="1191c-107">MAPIX.h</span><span class="sxs-lookup"><span data-stu-id="1191c-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="1191c-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="1191c-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="1191c-109">Objets de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="1191c-109">Address book objects</span></span>  <br/> |
|<span data-ttu-id="1191c-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="1191c-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="1191c-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="1191c-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="1191c-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="1191c-112">Called by:</span></span>  <br/> |<span data-ttu-id="1191c-113">Applications clientes, les fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="1191c-113">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="1191c-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="1191c-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1191c-115">IID_IAddrBook</span><span class="sxs-lookup"><span data-stu-id="1191c-115">IID_IAddrBook</span></span>  <br/> |
|<span data-ttu-id="1191c-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="1191c-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="1191c-117">LPADRBOOK</span><span class="sxs-lookup"><span data-stu-id="1191c-117">LPADRBOOK</span></span>  <br/> |
|<span data-ttu-id="1191c-118">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="1191c-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="1191c-119">Pas accessible en écriture</span><span class="sxs-lookup"><span data-stu-id="1191c-119">Not writable</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1191c-120">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="1191c-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1191c-121">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="1191c-121">OpenEntry</span></span>](iaddrbook-openentry.md) <br/> |<span data-ttu-id="1191c-122">Ouvre une entrée de carnet d’adresses et retourne un pointeur vers une interface qui peut servir à accéder à l’entrée.</span><span class="sxs-lookup"><span data-stu-id="1191c-122">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>  <br/> |
|[<span data-ttu-id="1191c-123">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="1191c-123">CompareEntryIDs</span></span>](iaddrbook-compareentryids.md) <br/> |<span data-ttu-id="1191c-124">Compare deux identificateurs d’entrée qui appartiennent à un fournisseur de carnet d’adresse spécifique afin de déterminer si elles font référence à l’objet de carnet d’adresses même.</span><span class="sxs-lookup"><span data-stu-id="1191c-124">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span>  <br/> |
|[<span data-ttu-id="1191c-125">Conseiller</span><span class="sxs-lookup"><span data-stu-id="1191c-125">Advise</span></span>](iaddrbook-advise.md) <br/> |<span data-ttu-id="1191c-126">Enregistre un fournisseur de service ou client pour recevoir des notifications sur les modifications apportées à une ou plusieurs entrées dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="1191c-126">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>  <br/> |
|[<span data-ttu-id="1191c-127">L’avertissement</span><span class="sxs-lookup"><span data-stu-id="1191c-127">Unadvise</span></span>](iaddrbook-unadvise.md) <br/> |<span data-ttu-id="1191c-128">Annule l’inscription d’une notification précédemment établie pour une entrée de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="1191c-128">Cancels a notification registration previously established for an address book entry.</span></span>  <br/> |
|[<span data-ttu-id="1191c-129">CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="1191c-129">CreateOneOff</span></span>](iaddrbook-createoneoff.md) <br/> |<span data-ttu-id="1191c-130">Crée un identificateur d’entrée pour une adresse unique.</span><span class="sxs-lookup"><span data-stu-id="1191c-130">Creates an entry identifier for a one-off address.</span></span>  <br/> |
|[<span data-ttu-id="1191c-131">NewEntry</span><span class="sxs-lookup"><span data-stu-id="1191c-131">NewEntry</span></span>](iaddrbook-newentry.md) <br/> |<span data-ttu-id="1191c-132">Ajoute un destinataire à un conteneur de carnet d’adresses ou à la liste des destinataires d’un message sortant.</span><span class="sxs-lookup"><span data-stu-id="1191c-132">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="1191c-133">ResolveName</span><span class="sxs-lookup"><span data-stu-id="1191c-133">ResolveName</span></span>](iaddrbook-resolvename.md) <br/> |<span data-ttu-id="1191c-134">Effectue la résolution de noms, affectation d’identificateurs d’entrée aux destinataires dans une liste de destinataires.</span><span class="sxs-lookup"><span data-stu-id="1191c-134">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>  <br/> |
|[<span data-ttu-id="1191c-135">Adresse</span><span class="sxs-lookup"><span data-stu-id="1191c-135">Address</span></span>](iaddrbook-address.md) <br/> |<span data-ttu-id="1191c-136">Affiche la boîte de dialogue de carnet d’adresse Outlook.</span><span class="sxs-lookup"><span data-stu-id="1191c-136">Displays the Outlook address book dialog box.</span></span>  <br/> |
|[<span data-ttu-id="1191c-137">Détails</span><span class="sxs-lookup"><span data-stu-id="1191c-137">Details</span></span>](iaddrbook-details.md) <br/> |<span data-ttu-id="1191c-138">Affiche une boîte de dialogue qui affiche des informations sur une entrée de carnet d’adresses particulière.</span><span class="sxs-lookup"><span data-stu-id="1191c-138">Displays a dialog box that shows details about a particular address book entry.</span></span>  <br/> |
|<span data-ttu-id="1191c-139">**RecipOptions**</span><span class="sxs-lookup"><span data-stu-id="1191c-139">**RecipOptions**</span></span> <br/> | <span data-ttu-id="1191c-140">*Non pris en charge ou documentés.*</span><span class="sxs-lookup"><span data-stu-id="1191c-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="1191c-141">**QueryDefaultRecipOpt**</span><span class="sxs-lookup"><span data-stu-id="1191c-141">**QueryDefaultRecipOpt**</span></span> <br/> | <span data-ttu-id="1191c-142">*Non pris en charge ou documentés.*</span><span class="sxs-lookup"><span data-stu-id="1191c-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="1191c-143">GetPAB</span><span class="sxs-lookup"><span data-stu-id="1191c-143">GetPAB</span></span>](iaddrbook-getpab.md) <br/> |<span data-ttu-id="1191c-144">Renvoie l’identificateur d’entrée du conteneur qui est désigné comme le carnet d’adresses personnel (CAP).</span><span class="sxs-lookup"><span data-stu-id="1191c-144">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="1191c-145">SetPAB</span><span class="sxs-lookup"><span data-stu-id="1191c-145">SetPAB</span></span>](iaddrbook-setpab.md) <br/> |<span data-ttu-id="1191c-146">Désigne un conteneur spécifique comme le carnet d’adresses personnel (CAP).</span><span class="sxs-lookup"><span data-stu-id="1191c-146">Designates a particular container as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="1191c-147">GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="1191c-147">GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md) <br/> |<span data-ttu-id="1191c-148">Renvoie l’identificateur d’entrée pour le conteneur de carnet d’adresses initiale.</span><span class="sxs-lookup"><span data-stu-id="1191c-148">Returns the entry identifier for the initial address book container.</span></span>  <br/> |
|[<span data-ttu-id="1191c-149">SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="1191c-149">SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md) <br/> |<span data-ttu-id="1191c-150">Définit le conteneur spécifié comme le conteneur de carnet d’adresses par défaut qui est initialement disponible.</span><span class="sxs-lookup"><span data-stu-id="1191c-150">Establishes the specified container as the default address book container that is initially made available.</span></span>  <br/> |
|[<span data-ttu-id="1191c-151">GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="1191c-151">GetSearchPath</span></span>](iaddrbook-getsearchpath.md) <br/> |<span data-ttu-id="1191c-152">Renvoie une liste triée des identificateurs d’entrée des conteneurs à inclure dans le processus de résolution de noms initié par la méthode [ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="1191c-152">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [ResolveName](iaddrbook-resolvename.md) method.</span></span>  <br/> |
|[<span data-ttu-id="1191c-153">SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="1191c-153">SetSearchPath</span></span>](iaddrbook-setsearchpath.md) <br/> |<span data-ttu-id="1191c-154">Définit un nouveau chemin d’accès de la recherche dans le profil qui est utilisé pour le processus de résolution de nom.</span><span class="sxs-lookup"><span data-stu-id="1191c-154">Sets a new search path in the profile that is used for the name resolution process.</span></span>  <br/> |
|[<span data-ttu-id="1191c-155">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="1191c-155">PrepareRecips</span></span>](iaddrbook-preparerecips.md) <br/> |<span data-ttu-id="1191c-156">Prépare une liste de destinataires pour une utilisation ultérieure par le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="1191c-156">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1191c-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1191c-157">See also</span></span>



[<span data-ttu-id="1191c-158">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="1191c-158">MAPI Interfaces</span></span>](mapi-interfaces.md)

