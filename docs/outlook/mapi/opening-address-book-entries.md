---
title: Ouverture des entrées du carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6ebd6009700742e9b1159bc95ff0496c423e512c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422158"
---
# <a name="opening-address-book-entries"></a><span data-ttu-id="16228-103">Ouverture des entrées du carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="16228-103">Opening address book entries</span></span>

<span data-ttu-id="16228-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16228-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16228-105">Lorsqu’un client ou un fournisseur a demandé l’ouverture d’un de vos objets, MAPI appelle la méthode [IABLogon::OpenEntry](iablogon-openentry.md) de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="16228-105">When a client or provider has requested that one of your objects be opened, MAPI calls your provider's [IABLogon::OpenEntry](iablogon-openentry.md) method.</span></span> <span data-ttu-id="16228-106">MAPI détermine que l’identificateur d’entrée représentant l’objet cible appartient à votre fournisseur en examinant la partie [MAPIUID](mapiuid.md) de l’identificateur d’entrée et en la faisant correspondre au **MAPIUID** que votre fournisseur a inscrit dans l’appel à **IMAPISupport::SetProviderUID**.</span><span class="sxs-lookup"><span data-stu-id="16228-106">MAPI determines that the entry identifier representing the target object belongs to your provider by examining the [MAPIUID](mapiuid.md) portion of the entry identifier and matching it to the **MAPIUID** that your provider registered in the call to **IMAPISupport::SetProviderUID**.</span></span> <span data-ttu-id="16228-107">MAPI appelle ensuite votre **méthode OpenEntry.**</span><span class="sxs-lookup"><span data-stu-id="16228-107">MAPI then calls your **OpenEntry** method.</span></span> <span data-ttu-id="16228-108">Votre fournisseur doit répondre en récupérant l’objet correspondant ( conteneur, liste de distribution ou utilisateur de messagerie).</span><span class="sxs-lookup"><span data-stu-id="16228-108">Your provider must respond by retrieving the corresponding object — a container, distribution list, or messaging user.</span></span> 
  
<span data-ttu-id="16228-109">Un identificateur d’entrée NULL indique une demande d’ouverture du conteneur racine du fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="16228-109">A NULL entry identifier indicates a request to open the address book provider's root container.</span></span> <span data-ttu-id="16228-110">Les clients ouvrent le conteneur racine pour accéder à sa table hiérarchique et à ses destinataires.</span><span class="sxs-lookup"><span data-stu-id="16228-110">Clients open the root container to access its hierarchy table and its recipients.</span></span> <span data-ttu-id="16228-111">Les fournisseurs de carnet d’adresses qui fournissent uniquement des modèles pour la création de destinataires unique ne prennent pas en charge l’appel **OpenEntry** pour le conteneur racine.</span><span class="sxs-lookup"><span data-stu-id="16228-111">Address book providers that only supply templates for creating one-off recipients do not support the **OpenEntry** call for the root container.</span></span> 
  
### <a name="to-implement-iablogonopenentry"></a><span data-ttu-id="16228-112">Pour implémenter IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="16228-112">To implement IABLogon::OpenEntry</span></span>
  
1. <span data-ttu-id="16228-113">Vérifiez que l’identificateur d’entrée est un identificateur valide que votre fournisseur prend en charge.</span><span class="sxs-lookup"><span data-stu-id="16228-113">Check that the entry identifier is a valid identifier that your provider supports.</span></span> <span data-ttu-id="16228-114">S’il ne s’agit pas d’un identificateur d’entrée valide, MAPI_E_INVALID_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="16228-114">If it is not a valid entry identifier, return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="16228-115">Vérifiez l’indicateur transmis avec le _paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="16228-115">Check the flag that is passed in with the  _ulFlags_ parameter.</span></span> <span data-ttu-id="16228-116">Si MAPI est passé dans MAPI_MODIFY et que votre fournisseur n’autorise pas la modification de ses objets, échouez et renvoyez la valeur MAPI_E_ACCESS_DENIED’erreur.</span><span class="sxs-lookup"><span data-stu-id="16228-116">If MAPI has passed in MAPI_MODIFY and your provider does not allow its objects to be modified, fail and return the MAPI_E_ACCESS_DENIED error value.</span></span> 
    
3. <span data-ttu-id="16228-117">Vérifiez que l’interface demandée dans  _le paramètre lpInterface_ est valide pour le type d’objet que votre fournisseur a été invité à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="16228-117">Check that the interface requested in the  _lpInterface_ parameter is valid for the type of object your provider has been asked to open.</span></span> <span data-ttu-id="16228-118">Si un paramètre non valide a été passé, échouez et renvoyez la valeur MAPI_E_INTERFACE_NOT_SUPPORTED’erreur.</span><span class="sxs-lookup"><span data-stu-id="16228-118">If an invalid parameter has been passed in, fail and return the MAPI_E_INTERFACE_NOT_SUPPORTED error value.</span></span> 
    
4. <span data-ttu-id="16228-119">Si le  _paramètre cbEntryID_ est zéro, il s’agit d’une demande d’ouverture du conteneur racine de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="16228-119">If the  _cbEntryID_ parameter is zero, this is a request to open your provider's root container.</span></span> <span data-ttu-id="16228-120">Créez le conteneur racine et renvoyez un pointeur vers son **implémentation d’interface IABContainer.**</span><span class="sxs-lookup"><span data-stu-id="16228-120">Create the root container and return a pointer to its **IABContainer** interface implementation.</span></span> 
    
5. <span data-ttu-id="16228-121">Si votre fournisseur implémente plusieurs objets d’inscription, chacun avec son propre **MAPIUID** enregistré, mapmez le **MAPIUID** contenu dans l’identificateur d’entrée avec l’objet d' logon approprié.</span><span class="sxs-lookup"><span data-stu-id="16228-121">If your provider implements several logon objects, each with its own registered **MAPIUID**, map the **MAPIUID** contained in the entry identifier with the appropriate logon object.</span></span> 
    
6. <span data-ttu-id="16228-122">Déterminez le type d’objet représenté par l’identificateur d’entrée : un utilisateur de messagerie, une liste de distribution ou un conteneur appartenant à votre fournisseur ou un utilisateur de messagerie unique ou une liste de distribution afin que la valeur appropriée puisse être définie pour le paramètre _lpulObjectType._</span><span class="sxs-lookup"><span data-stu-id="16228-122">Determine which type of object the entry identifier represents: a messaging user, distribution list, or container belonging to your provider or a one-off messaging user or distribution list so that the appropriate value can be set for the  _lpulObjectType_ parameter.</span></span> 
    
7. <span data-ttu-id="16228-123">Créez l’objet du type approprié et définissez les propriétés de base suivantes :</span><span class="sxs-lookup"><span data-stu-id="16228-123">Create the object of the appropriate type and set the following basic properties:</span></span>
    
    - <span data-ttu-id="16228-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="16228-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    - <span data-ttu-id="16228-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="16228-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    - <span data-ttu-id="16228-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="16228-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    - <span data-ttu-id="16228-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="16228-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
8. <span data-ttu-id="16228-128">Calculez **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) et **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) à partir des informations dans l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="16228-128">Calculate **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) and **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from information in the entry identifier.</span></span>
    
9. <span data-ttu-id="16228-129">Renvoyer un pointeur vers l’implémentation de l’interface pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="16228-129">Return a pointer to the interface implementation for the object.</span></span> 
    

