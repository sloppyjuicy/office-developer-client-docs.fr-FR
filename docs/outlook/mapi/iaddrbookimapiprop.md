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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: da71e9dd5f2fc20bb1daf528f4466ea29507bf06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429823"
---
# <a name="iaddrbook--imapiprop"></a><span data-ttu-id="aefcf-103">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="aefcf-103">IAddrBook : IMAPIProp</span></span>

  
  
<span data-ttu-id="aefcf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aefcf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aefcf-105">Prend en charge l’accès au carnet d’adresses MAPI et inclut des opérations telles que l’affichage de boîtes de dialogue courantes ; ouverture de conteneurs, d’utilisateurs de messagerie et de listes de distribution ; et d’effectuer une résolution de nom.</span><span class="sxs-lookup"><span data-stu-id="aefcf-105">Supports access to the MAPI address book and includes operations such as displaying common dialog boxes; opening containers, messaging users, and distribution lists; and performing name resolution.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aefcf-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="aefcf-106">Header file:</span></span>  <br/> |<span data-ttu-id="aefcf-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="aefcf-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="aefcf-108">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="aefcf-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="aefcf-109">Objets de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="aefcf-109">Address book objects</span></span>  <br/> |
|<span data-ttu-id="aefcf-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="aefcf-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="aefcf-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="aefcf-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="aefcf-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="aefcf-112">Called by:</span></span>  <br/> |<span data-ttu-id="aefcf-113">Applications clientes, fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="aefcf-113">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="aefcf-114">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="aefcf-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="aefcf-115">IID_IAddrBook</span><span class="sxs-lookup"><span data-stu-id="aefcf-115">IID_IAddrBook</span></span>  <br/> |
|<span data-ttu-id="aefcf-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="aefcf-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="aefcf-117">LPADRBOOK</span><span class="sxs-lookup"><span data-stu-id="aefcf-117">LPADRBOOK</span></span>  <br/> |
|<span data-ttu-id="aefcf-118">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="aefcf-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="aefcf-119">Non accessible en writable</span><span class="sxs-lookup"><span data-stu-id="aefcf-119">Not writable</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="aefcf-120">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="aefcf-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="aefcf-121">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="aefcf-121">OpenEntry</span></span>](iaddrbook-openentry.md) <br/> |<span data-ttu-id="aefcf-122">Ouvre une entrée de carnet d’adresses et renvoie un pointeur vers une interface qui peut être utilisée pour accéder à l’entrée.</span><span class="sxs-lookup"><span data-stu-id="aefcf-122">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>  <br/> |
|[<span data-ttu-id="aefcf-123">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="aefcf-123">CompareEntryIDs</span></span>](iaddrbook-compareentryids.md) <br/> |<span data-ttu-id="aefcf-124">Compare deux identificateurs d’entrée appartenant à un fournisseur de carnet d’adresses particulier pour déterminer s’ils font référence au même objet de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="aefcf-124">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span>  <br/> |
|[<span data-ttu-id="aefcf-125">Conseiller</span><span class="sxs-lookup"><span data-stu-id="aefcf-125">Advise</span></span>](iaddrbook-advise.md) <br/> |<span data-ttu-id="aefcf-126">Enregistre un client ou un fournisseur de services pour recevoir des notifications concernant les modifications apportées à une ou plusieurs entrées dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="aefcf-126">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>  <br/> |
|[<span data-ttu-id="aefcf-127">Unadvise</span><span class="sxs-lookup"><span data-stu-id="aefcf-127">Unadvise</span></span>](iaddrbook-unadvise.md) <br/> |<span data-ttu-id="aefcf-128">Annule l’inscription d’une notification précédemment établie pour une entrée de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="aefcf-128">Cancels a notification registration previously established for an address book entry.</span></span>  <br/> |
|[<span data-ttu-id="aefcf-129">CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="aefcf-129">CreateOneOff</span></span>](iaddrbook-createoneoff.md) <br/> |<span data-ttu-id="aefcf-130">Crée un identificateur d’entrée pour une adresse unique.</span><span class="sxs-lookup"><span data-stu-id="aefcf-130">Creates an entry identifier for a one-off address.</span></span>  <br/> |
|[<span data-ttu-id="aefcf-131">NewEntry</span><span class="sxs-lookup"><span data-stu-id="aefcf-131">NewEntry</span></span>](iaddrbook-newentry.md) <br/> |<span data-ttu-id="aefcf-132">Ajoute un nouveau destinataire à un conteneur de carnet d’adresses ou à la liste des destinataires d’un message sortant.</span><span class="sxs-lookup"><span data-stu-id="aefcf-132">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="aefcf-133">ResolveName</span><span class="sxs-lookup"><span data-stu-id="aefcf-133">ResolveName</span></span>](iaddrbook-resolvename.md) <br/> |<span data-ttu-id="aefcf-134">Effectue la résolution de noms, en attribuant des identificateurs d’entrée aux destinataires d’une liste de destinataires.</span><span class="sxs-lookup"><span data-stu-id="aefcf-134">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>  <br/> |
|[<span data-ttu-id="aefcf-135">Address</span><span class="sxs-lookup"><span data-stu-id="aefcf-135">Address</span></span>](iaddrbook-address.md) <br/> |<span data-ttu-id="aefcf-136">Affiche la boîte de dialogue carnet d’adresses Outlook.</span><span class="sxs-lookup"><span data-stu-id="aefcf-136">Displays the Outlook address book dialog box.</span></span>  <br/> |
|[<span data-ttu-id="aefcf-137">Détails</span><span class="sxs-lookup"><span data-stu-id="aefcf-137">Details</span></span>](iaddrbook-details.md) <br/> |<span data-ttu-id="aefcf-138">Affiche une boîte de dialogue qui affiche des détails sur une entrée de carnet d’adresses particulière.</span><span class="sxs-lookup"><span data-stu-id="aefcf-138">Displays a dialog box that shows details about a particular address book entry.</span></span>  <br/> |
|<span data-ttu-id="aefcf-139">**RecipOptions**</span><span class="sxs-lookup"><span data-stu-id="aefcf-139">**RecipOptions**</span></span> <br/> | <span data-ttu-id="aefcf-140">*Non pris en charge ou documenté.*</span><span class="sxs-lookup"><span data-stu-id="aefcf-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="aefcf-141">**QueryDefaultRecipOpt**</span><span class="sxs-lookup"><span data-stu-id="aefcf-141">**QueryDefaultRecipOpt**</span></span> <br/> | <span data-ttu-id="aefcf-142">*Non pris en charge ou documenté.*</span><span class="sxs-lookup"><span data-stu-id="aefcf-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="aefcf-143">GetPAB</span><span class="sxs-lookup"><span data-stu-id="aefcf-143">GetPAB</span></span>](iaddrbook-getpab.md) <br/> |<span data-ttu-id="aefcf-144">Renvoie l’identificateur d’entrée du conteneur désigné comme carnet d’adresses personnel .</span><span class="sxs-lookup"><span data-stu-id="aefcf-144">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="aefcf-145">SetPAB</span><span class="sxs-lookup"><span data-stu-id="aefcf-145">SetPAB</span></span>](iaddrbook-setpab.md) <br/> |<span data-ttu-id="aefcf-146">Désigne un conteneur particulier en tant que carnet d’adresses personnel (PAB).</span><span class="sxs-lookup"><span data-stu-id="aefcf-146">Designates a particular container as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="aefcf-147">GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="aefcf-147">GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md) <br/> |<span data-ttu-id="aefcf-148">Renvoie l’identificateur d’entrée pour le conteneur de carnet d’adresses initial.</span><span class="sxs-lookup"><span data-stu-id="aefcf-148">Returns the entry identifier for the initial address book container.</span></span>  <br/> |
|[<span data-ttu-id="aefcf-149">SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="aefcf-149">SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md) <br/> |<span data-ttu-id="aefcf-150">Établit le conteneur spécifié en tant que conteneur de carnet d’adresses par défaut initialement disponible.</span><span class="sxs-lookup"><span data-stu-id="aefcf-150">Establishes the specified container as the default address book container that is initially made available.</span></span>  <br/> |
|[<span data-ttu-id="aefcf-151">GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="aefcf-151">GetSearchPath</span></span>](iaddrbook-getsearchpath.md) <br/> |<span data-ttu-id="aefcf-152">Renvoie une liste ordonnée d’identificateurs d’entrée des conteneurs à inclure dans le processus de résolution de noms initié par la [méthode ResolveName.](iaddrbook-resolvename.md)</span><span class="sxs-lookup"><span data-stu-id="aefcf-152">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [ResolveName](iaddrbook-resolvename.md) method.</span></span>  <br/> |
|[<span data-ttu-id="aefcf-153">SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="aefcf-153">SetSearchPath</span></span>](iaddrbook-setsearchpath.md) <br/> |<span data-ttu-id="aefcf-154">Définit un nouveau chemin de recherche dans le profil utilisé pour le processus de résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="aefcf-154">Sets a new search path in the profile that is used for the name resolution process.</span></span>  <br/> |
|[<span data-ttu-id="aefcf-155">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="aefcf-155">PrepareRecips</span></span>](iaddrbook-preparerecips.md) <br/> |<span data-ttu-id="aefcf-156">Prépare une liste de destinataires pour une utilisation ultérieure par le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="aefcf-156">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aefcf-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aefcf-157">See also</span></span>



[<span data-ttu-id="aefcf-158">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="aefcf-158">MAPI Interfaces</span></span>](mapi-interfaces.md)

