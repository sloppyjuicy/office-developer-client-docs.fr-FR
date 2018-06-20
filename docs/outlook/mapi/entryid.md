---
title: PROPRIÉTÉ ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ENTRYID
api_type:
- COM
ms.assetid: 8ebb21ca-5ad1-4dcc-97b6-2390664b5d8d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1b55703c9ad12e3645e6e9cb3dcfcbdf21b90d25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783254"
---
# <a name="entryid"></a><span data-ttu-id="bf14e-103">PROPRIÉTÉ ENTRYID</span><span class="sxs-lookup"><span data-stu-id="bf14e-103">ENTRYID</span></span>

  
  
<span data-ttu-id="bf14e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bf14e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bf14e-105">Contient un identificateur d’entrée pour un objet MAPI.</span><span class="sxs-lookup"><span data-stu-id="bf14e-105">Contains an entry identifier for a MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bf14e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="bf14e-106">Header file:</span></span>  <br/> |<span data-ttu-id="bf14e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bf14e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="bf14e-108">Macros connexes :</span><span class="sxs-lookup"><span data-stu-id="bf14e-108">Related macros:</span></span>  <br/> |<span data-ttu-id="bf14e-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span><span class="sxs-lookup"><span data-stu-id="bf14e-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a><span data-ttu-id="bf14e-110">Membres</span><span class="sxs-lookup"><span data-stu-id="bf14e-110">Members</span></span>

 <span data-ttu-id="bf14e-111">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="bf14e-111">**abFlags**</span></span>
  
> <span data-ttu-id="bf14e-112">Masque de bits des indicateurs qui fournissent des informations décrivant l’objet.</span><span class="sxs-lookup"><span data-stu-id="bf14e-112">Bitmask of flags that provide information that describes the object.</span></span> <span data-ttu-id="bf14e-113">Seul le premier octet des indicateurs, **abFlags [0]**, peut-être être défini par le fournisseur ; les trois autres sont réservés.</span><span class="sxs-lookup"><span data-stu-id="bf14e-113">Only the first byte of the flags, **abFlags[0]**, may be set by the provider; the other three are reserved.</span></span> <span data-ttu-id="bf14e-114">Ces indicateurs ne doivent pas être définis pour les identificateurs d’entrée définitive ; ils sont définis uniquement pour les identificateurs d’entrée à court terme.</span><span class="sxs-lookup"><span data-stu-id="bf14e-114">These flags must not be set for permanent entry identifiers; they are only set for short-term entry identifiers.</span></span> <span data-ttu-id="bf14e-115">Pour les clients, cette structure est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="bf14e-115">To clients, this structure is read-only.</span></span> <span data-ttu-id="bf14e-116">Les indicateurs suivants peuvent être définis dans **abFlags [0]**:</span><span class="sxs-lookup"><span data-stu-id="bf14e-116">The following flags can be set in **abFlags[0]**:</span></span>
    
<span data-ttu-id="bf14e-117">MAPI_NOTRECIP</span><span class="sxs-lookup"><span data-stu-id="bf14e-117">MAPI_NOTRECIP</span></span> 
  
> <span data-ttu-id="bf14e-118">L’identificateur d’entrée ne peut pas être utilisé en tant que destinataire d’un message.</span><span class="sxs-lookup"><span data-stu-id="bf14e-118">The entry identifier cannot be used as a recipient on a message.</span></span>
    
<span data-ttu-id="bf14e-119">MAPI_NOTRESERVED</span><span class="sxs-lookup"><span data-stu-id="bf14e-119">MAPI_NOTRESERVED</span></span> 
  
> <span data-ttu-id="bf14e-120">Les autres utilisateurs ne peuvent pas accéder à l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="bf14e-120">Other users cannot access the entry identifier.</span></span>
    
<span data-ttu-id="bf14e-121">MAPI_NOW</span><span class="sxs-lookup"><span data-stu-id="bf14e-121">MAPI_NOW</span></span> 
  
> <span data-ttu-id="bf14e-122">L’identificateur d’entrée ne peut pas être utilisé à d’autres moments.</span><span class="sxs-lookup"><span data-stu-id="bf14e-122">The entry identifier cannot be used at other times.</span></span>
    
<span data-ttu-id="bf14e-123">MAPI_SHORTTERM</span><span class="sxs-lookup"><span data-stu-id="bf14e-123">MAPI_SHORTTERM</span></span> 
  
> <span data-ttu-id="bf14e-124">L’identificateur d’entrée est à court terme.</span><span class="sxs-lookup"><span data-stu-id="bf14e-124">The entry identifier is short-term.</span></span> <span data-ttu-id="bf14e-125">Toutes les autres valeurs dans cet octet doivent être définies à moins que les autres utilisations de l’identificateur d’entrée sont activées.</span><span class="sxs-lookup"><span data-stu-id="bf14e-125">All other values in this byte must be set unless other uses of the entry identifier are enabled.</span></span>
    
<span data-ttu-id="bf14e-126">MAPI_THISSESSION</span><span class="sxs-lookup"><span data-stu-id="bf14e-126">MAPI_THISSESSION</span></span> 
  
> <span data-ttu-id="bf14e-127">L’identificateur d’entrée ne peut pas être utilisé sur d’autres sessions.</span><span class="sxs-lookup"><span data-stu-id="bf14e-127">The entry identifier cannot be used on other sessions.</span></span>
    
 <span data-ttu-id="bf14e-128">**Carnet d’adresses**</span><span class="sxs-lookup"><span data-stu-id="bf14e-128">**ab**</span></span>
  
> <span data-ttu-id="bf14e-129">Indique un tableau de données binaires qui sont utilisées par les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="bf14e-129">Indicates an array of binary data that is used by service providers.</span></span> <span data-ttu-id="bf14e-130">L’application cliente ne peut pas utiliser ce tableau.</span><span class="sxs-lookup"><span data-stu-id="bf14e-130">The client application cannot use this array.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bf14e-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="bf14e-131">Remarks</span></span>

<span data-ttu-id="bf14e-132">La structure de la **propriété ENTRYID** est utilisée par message stocker et pour construire des identificateurs uniques pour leurs objets des fournisseurs de carnet de d'adresses.</span><span class="sxs-lookup"><span data-stu-id="bf14e-132">The **ENTRYID** structure is used by message store and address book providers to construct unique identifiers for their objects.</span></span> <span data-ttu-id="bf14e-133">Identificateurs d’entrée sont utilisés pour identifier les types d’objets suivants :</span><span class="sxs-lookup"><span data-stu-id="bf14e-133">Entry identifiers are used to identify the following types of objects:</span></span> 
  
- <span data-ttu-id="bf14e-134">Banques de messages</span><span class="sxs-lookup"><span data-stu-id="bf14e-134">Message stores</span></span>
    
- <span data-ttu-id="bf14e-135">Dossiers</span><span class="sxs-lookup"><span data-stu-id="bf14e-135">Folders</span></span>
    
- <span data-ttu-id="bf14e-136">Messages</span><span class="sxs-lookup"><span data-stu-id="bf14e-136">Messages</span></span>
    
- <span data-ttu-id="bf14e-137">Conteneurs de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="bf14e-137">Address book containers</span></span>
    
- <span data-ttu-id="bf14e-138">Listes de distribution</span><span class="sxs-lookup"><span data-stu-id="bf14e-138">Distribution lists</span></span>
    
- <span data-ttu-id="bf14e-139">Les utilisateurs de messagerie</span><span class="sxs-lookup"><span data-stu-id="bf14e-139">Messaging users</span></span>
    
- <span data-ttu-id="bf14e-140">Objets d’état</span><span class="sxs-lookup"><span data-stu-id="bf14e-140">Status objects</span></span>
    
- <span data-ttu-id="bf14e-141">Sections de profil</span><span class="sxs-lookup"><span data-stu-id="bf14e-141">Profile sections</span></span>
    
<span data-ttu-id="bf14e-142">Chaque fournisseur utilise un format de la structure **ENTRYID** significatif pour ce fournisseur.</span><span class="sxs-lookup"><span data-stu-id="bf14e-142">Each provider uses a format for the **ENTRYID** structure that makes sense for that provider.</span></span> 
  
<span data-ttu-id="bf14e-143">Identificateurs d’entrée ne peut pas être comparées directement, car un objet peut être représenté par deux valeurs binaires différentes.</span><span class="sxs-lookup"><span data-stu-id="bf14e-143">Entry identifiers cannot be compared directly because one object can be represented by two different binary values.</span></span> <span data-ttu-id="bf14e-144">Pour déterminer si deux identificateurs d’entrée représentent le même objet, appelez la méthode [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) .</span><span class="sxs-lookup"><span data-stu-id="bf14e-144">To determine whether two entry identifiers represent the same object, call the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
<span data-ttu-id="bf14e-145">Lorsqu’un client appelle la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) d’un objet à récupérer son identificateur d’entrée, l’objet retourne la forme plus définitive de l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="bf14e-145">When a client calls an object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its entry identifier, the object returns the most permanent form of the entry identifier.</span></span> <span data-ttu-id="bf14e-146">Un client peut vérifier qu’un identificateur d’entrée est à long terme en vérifiant qu’aucun des indicateurs sont définis dans le premier octet du membre **abFlags** .</span><span class="sxs-lookup"><span data-stu-id="bf14e-146">A client can verify that an entry identifier is long-term by checking that none of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="bf14e-147">Lorsqu’un client accède à un identificateur d’entrée à une colonne dans une table, probablement que cet identificateur d’entrée est à court terme au lieu à long terme.</span><span class="sxs-lookup"><span data-stu-id="bf14e-147">When a client accesses an entry identifier through a column in a table, most likely this entry identifier is short-term instead of long-term.</span></span> <span data-ttu-id="bf14e-148">Identificateurs d’entrée à court terme peuvent servir à ouvrir les objets correspondants uniquement dans la session MAPI en cours.</span><span class="sxs-lookup"><span data-stu-id="bf14e-148">Short-term entry identifiers can be used to open their corresponding objects only in the current MAPI session.</span></span> <span data-ttu-id="bf14e-149">Un client peut vérifier qu’un identificateur d’entrée est à court terme en vérifiant que tous les indicateurs sont définis dans le premier octet du membre **abFlags** .</span><span class="sxs-lookup"><span data-stu-id="bf14e-149">A client can verify that an entry identifier is short-term by checking that all of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="bf14e-150">Identificateurs d’entrée sont à court terme, mais utilisez à long terme.</span><span class="sxs-lookup"><span data-stu-id="bf14e-150">Some entry identifiers are short-term, but have long-term use.</span></span> <span data-ttu-id="bf14e-151">Identificateur entrée aura une ou plusieurs des indicateurs appropriés définis dans le premier octet de ses membres **abFlags** .</span><span class="sxs-lookup"><span data-stu-id="bf14e-151">Such an entry identifier will have one or more of the appropriate flags set in the first byte of its **abFlags** member.</span></span> 
  
<span data-ttu-id="bf14e-152">Une structure **ENTRYID** ressemble à une structure [FLATENTRY](flatentry.md) .</span><span class="sxs-lookup"><span data-stu-id="bf14e-152">An **ENTRYID** structure resembles a [FLATENTRY](flatentry.md) structure.</span></span> <span data-ttu-id="bf14e-153">Toutefois, il existe quelques différences :</span><span class="sxs-lookup"><span data-stu-id="bf14e-153">However, there are some differences:</span></span> 
  
- <span data-ttu-id="bf14e-154">Une structure **ENTRYID** n’incluent pas la taille de l’identificateur d’entrée. une structure **FLATENTRY** fait.</span><span class="sxs-lookup"><span data-stu-id="bf14e-154">An **ENTRYID** structure does not store the size of the entry identifier; a **FLATENTRY** structure does.</span></span> 
    
- <span data-ttu-id="bf14e-155">Une structure **ENTRYID** stocke les données d’indicateur et le reste de l’identificateur d’entrée séparément ; une structure **FLATENTRY** stocke les données d’indicateur avec le reste de l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="bf14e-155">An **ENTRYID** structure stores the flag data and the rest of the entry identifier separately; a **FLATENTRY** structure stores the flag data with the rest of the entry identifier.</span></span> 
    
- <span data-ttu-id="bf14e-156">Une structure **ENTRYID** est transmise en tant que paramètre aux méthodes de l’interface [IMAPIProp](imapipropiunknown.md) et aux méthodes **OpenEntry** suivantes : [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry ](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="bf14e-156">An **ENTRYID** structure is passed as a parameter to the methods of the [IMAPIProp](imapipropiunknown.md) interface and to the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="bf14e-157">Une structure **ENTRYID** est utilisée pour stocker un identificateur d’entrée sur le disque.</span><span class="sxs-lookup"><span data-stu-id="bf14e-157">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> <span data-ttu-id="bf14e-158">Une structure **FLATENTRY** sert à stocker un identificateur d’entrée dans un fichier ou passez-la dans un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="bf14e-158">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> 
    
<span data-ttu-id="bf14e-159">Clients doivent toujours passer dans les identificateurs d’entrée aligné naturellement.</span><span class="sxs-lookup"><span data-stu-id="bf14e-159">Clients should always pass in naturally aligned entry identifiers.</span></span> <span data-ttu-id="bf14e-160">Bien que les fournisseurs doivent gérer les identificateurs d’entrée arbitrairement aligné, clients pas ce comportement sont normal.</span><span class="sxs-lookup"><span data-stu-id="bf14e-160">Although providers should handle arbitrarily aligned entry identifiers, clients should not expect this behavior.</span></span> <span data-ttu-id="bf14e-161">Passer un identificateur d’entrée aligné bonne à une méthode peut provoquer une erreur d’alignement sur les processeurs RISC.</span><span class="sxs-lookup"><span data-stu-id="bf14e-161">Failure to pass a good aligned entry identifier to a method can cause an alignment fault on RISC processors.</span></span> 
  
<span data-ttu-id="bf14e-162">Le facteur d’alignement naturel, généralement 8 octets, est le plus grand type de données pris en charge par l’UC et généralement le même facteur d’alignement utilisé par l’allocation de mémoire système.</span><span class="sxs-lookup"><span data-stu-id="bf14e-162">The natural alignment factor, typically 8 bytes, is the largest data type supported by the CPU, and usually the same alignment factor used by the system memory allocator.</span></span> <span data-ttu-id="bf14e-163">Une adresse de la mémoire alignée naturellement permet de l’UC accéder à n’importe quel type de données que pris en charge à l’adresse sans générer une erreur d’alignement.</span><span class="sxs-lookup"><span data-stu-id="bf14e-163">A naturally aligned memory address allows the CPU to access any data type it supports at that address without generating an alignment fault.</span></span> <span data-ttu-id="bf14e-164">Pour les processeurs RISC, un type de données de taille N doit généralement être aligné sur un multiple de N octets, avec l’adresse est un multiple de N.</span><span class="sxs-lookup"><span data-stu-id="bf14e-164">For RISC CPUs, a data type of size N bytes must usually be aligned on an even multiple of N bytes, with the address being an even multiple of N.</span></span>
  
<span data-ttu-id="bf14e-165">Pour plus d’informations, voir [Identificateurs d’entrée](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="bf14e-165">For more information, see [Entry Identifiers](mapi-entry-identifiers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bf14e-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf14e-166">See also</span></span>



[<span data-ttu-id="bf14e-167">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="bf14e-167">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="bf14e-168">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="bf14e-168">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="bf14e-169">Propriété canonique PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="bf14e-169">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)


[<span data-ttu-id="bf14e-170">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="bf14e-170">MAPI Structures</span></span>](mapi-structures.md)

