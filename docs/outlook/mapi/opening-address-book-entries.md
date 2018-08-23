---
title: Entrées de carnet d’adresses de l’ouverture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: cd86b9cc86f30aac75b732b97208933de4d336e9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566430"
---
# <a name="opening-address-book-entries"></a><span data-ttu-id="dfa65-103">Entrées de carnet d’adresses de l’ouverture</span><span class="sxs-lookup"><span data-stu-id="dfa65-103">Opening address book entries</span></span>

<span data-ttu-id="dfa65-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfa65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfa65-105">Lorsqu’un client ou le fournisseur a demandé qu’un de vos objets s’ouvre, MAPI appelle la méthode [IABLogon::OpenEntry](iablogon-openentry.md) de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="dfa65-105">When a client or provider has requested that one of your objects be opened, MAPI calls your provider's [IABLogon::OpenEntry](iablogon-openentry.md) method.</span></span> <span data-ttu-id="dfa65-106">MAPI détermine que l’identificateur d’entrée qui représente l’objet cible appartient à votre fournisseur en examinant la partie [MAPIUID](mapiuid.md) de l’identificateur d’entrée et en correspondance avec la **MAPIUID** que votre fournisseur inscrit dans l’appel à ** IMAPISupport::SetProviderUID**.</span><span class="sxs-lookup"><span data-stu-id="dfa65-106">MAPI determines that the entry identifier representing the target object belongs to your provider by examining the [MAPIUID](mapiuid.md) portion of the entry identifier and matching it to the **MAPIUID** that your provider registered in the call to **IMAPISupport::SetProviderUID**.</span></span> <span data-ttu-id="dfa65-107">MAPI appelle ensuite la méthode **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="dfa65-107">MAPI then calls your **OpenEntry** method.</span></span> <span data-ttu-id="dfa65-108">Votre fournisseur doit répondre en récupérant l’objet correspondant, un conteneur, une liste de distribution ou un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="dfa65-108">Your provider must respond by retrieving the corresponding object — a container, distribution list, or messaging user.</span></span> 
  
<span data-ttu-id="dfa65-109">Un identificateur d’entrée NULL indique une demande pour ouvrir le conteneur de racine du fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="dfa65-109">A NULL entry identifier indicates a request to open the address book provider's root container.</span></span> <span data-ttu-id="dfa65-110">Clients d’ouvrir le conteneur racine pour accéder à la table de hiérarchie et ses destinataires.</span><span class="sxs-lookup"><span data-stu-id="dfa65-110">Clients open the root container to access its hierarchy table and its recipients.</span></span> <span data-ttu-id="dfa65-111">Fournisseurs de carnet d’adresses qui fournit uniquement des modèles pour la création de destinataires uniques ne prennent pas en charge l’appel de **OpenEntry** pour le conteneur racine.</span><span class="sxs-lookup"><span data-stu-id="dfa65-111">Address book providers that only supply templates for creating one-off recipients do not support the **OpenEntry** call for the root container.</span></span> 
  
### <a name="to-implement-iablogonopenentry"></a><span data-ttu-id="dfa65-112">Pour mettre en œuvre IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="dfa65-112">To implement IABLogon::OpenEntry</span></span>
  
1. <span data-ttu-id="dfa65-113">Vérifiez que l’identificateur d’entrée est un identificateur valid de votre fournisseur prend en charge.</span><span class="sxs-lookup"><span data-stu-id="dfa65-113">Check that the entry identifier is a valid identifier that your provider supports.</span></span> <span data-ttu-id="dfa65-114">Si elle n’est pas un identificateur d’entrée valide, renvoyer MAPI_E_INVALID_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="dfa65-114">If it is not a valid entry identifier, return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="dfa65-115">Vérifiez l’indicateur qui est passé avec le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="dfa65-115">Check the flag that is passed in with the  _ulFlags_ parameter.</span></span> <span data-ttu-id="dfa65-116">Si MAPI n’a passé et votre fournisseur n’autorise pas ses objets à modifier, échouer et retourner la valeur d’erreur MAPI_E_ACCESS_DENIED.</span><span class="sxs-lookup"><span data-stu-id="dfa65-116">If MAPI has passed in MAPI_MODIFY and your provider does not allow its objects to be modified, fail and return the MAPI_E_ACCESS_DENIED error value.</span></span> 
    
3. <span data-ttu-id="dfa65-117">Vérifiez que l’interface demandée dans le paramètre _lpInterface_ est valide pour le type d’objet de que votre fournisseur a été invité à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="dfa65-117">Check that the interface requested in the  _lpInterface_ parameter is valid for the type of object your provider has been asked to open.</span></span> <span data-ttu-id="dfa65-118">Si un paramètre non valide a été passé, échouer et retourner la valeur d’erreur MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="dfa65-118">If an invalid parameter has been passed in, fail and return the MAPI_E_INTERFACE_NOT_SUPPORTED error value.</span></span> 
    
4. <span data-ttu-id="dfa65-119">Si le paramètre _cbEntryID_ est égale à zéro, il s’agit d’une demande d’ouverture du conteneur racine de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="dfa65-119">If the  _cbEntryID_ parameter is zero, this is a request to open your provider's root container.</span></span> <span data-ttu-id="dfa65-120">Créer le conteneur racine et renvoyer un pointeur vers son implémentation d’interface **IABContainer** .</span><span class="sxs-lookup"><span data-stu-id="dfa65-120">Create the root container and return a pointer to its **IABContainer** interface implementation.</span></span> 
    
5. <span data-ttu-id="dfa65-121">Si votre fournisseur implémente plusieurs objets d’ouverture de session, chacun avec son propre inscrit **MAPIUID**, carte la **MAPIUID** contenus dans l’identificateur d’entrée avec l’objet d’ouverture de session approprié.</span><span class="sxs-lookup"><span data-stu-id="dfa65-121">If your provider implements several logon objects, each with its own registered **MAPIUID**, map the **MAPIUID** contained in the entry identifier with the appropriate logon object.</span></span> 
    
6. <span data-ttu-id="dfa65-122">Déterminer le type d’objet l’identificateur d’entrée représente : un utilisateur, liste de distribution ou conteneur appartenant à votre fournisseur ou une liste unique d’utilisateur ou de distribution de messagerie afin que la valeur appropriée peut être définie pour le _lpulObjectType_ de messagerie paramètre.</span><span class="sxs-lookup"><span data-stu-id="dfa65-122">Determine which type of object the entry identifier represents: a messaging user, distribution list, or container belonging to your provider or a one-off messaging user or distribution list so that the appropriate value can be set for the  _lpulObjectType_ parameter.</span></span> 
    
7. <span data-ttu-id="dfa65-123">Créer l’objet du type approprié et définissez les propriétés de base suivantes :</span><span class="sxs-lookup"><span data-stu-id="dfa65-123">Create the object of the appropriate type and set the following basic properties:</span></span>
    
    - <span data-ttu-id="dfa65-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dfa65-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    - <span data-ttu-id="dfa65-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dfa65-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    - <span data-ttu-id="dfa65-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dfa65-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    - <span data-ttu-id="dfa65-127">**TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dfa65-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
8. <span data-ttu-id="dfa65-128">Calculer **ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) et **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) à partir des informations dans l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="dfa65-128">Calculate **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) and **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from information in the entry identifier.</span></span>
    
9. <span data-ttu-id="dfa65-129">Retourne un pointeur vers l’implémentation d’interface pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="dfa65-129">Return a pointer to the interface implementation for the object.</span></span> 
    

