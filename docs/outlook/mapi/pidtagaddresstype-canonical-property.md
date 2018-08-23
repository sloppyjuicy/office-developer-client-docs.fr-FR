---
title: Propriété canonique PidTagAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAddressType
api_type:
- HeaderDef
ms.assetid: 986719d2-8837-46b4-8d04-c24508f5e19a
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 464121a969beea06294049985052eb150651765f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580088"
---
# <a name="pidtagaddresstype-canonical-property"></a><span data-ttu-id="b6c9e-103">Propriété canonique PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="b6c9e-103">PidTagAddressType Canonical Property</span></span>

<span data-ttu-id="b6c9e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6c9e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6c9e-105">Contient le type d’adresse de messagerie de l’utilisateur de messagerie, tels que SMTP.</span><span class="sxs-lookup"><span data-stu-id="b6c9e-105">Contains the messaging user's email address type, such as SMTP.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b6c9e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b6c9e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b6c9e-107">TYPEADR_PR, PR_ADDRTYPE_A, PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="b6c9e-107">PR_ADDRTYPE, PR_ADDRTYPE_A, PR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="b6c9e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b6c9e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b6c9e-109">0x3002</span><span class="sxs-lookup"><span data-stu-id="b6c9e-109">0x3002</span></span>  <br/> |
|<span data-ttu-id="b6c9e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b6c9e-110">Data type:</span></span>  <br/> |<span data-ttu-id="b6c9e-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="b6c9e-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="b6c9e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="b6c9e-112">Area:</span></span>  <br/> |<span data-ttu-id="b6c9e-113">Address</span><span class="sxs-lookup"><span data-stu-id="b6c9e-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6c9e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b6c9e-114">Remarks</span></span>

<span data-ttu-id="b6c9e-115">Ces propriétés sont des exemples de propriétés d’adresse de base communes à tous les utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b6c9e-115">These properties are examples of the base address properties common to all messaging users.</span></span> <span data-ttu-id="b6c9e-116">Il spécifie le système de messagerie MAPI utilise pour gérer un message donné.</span><span class="sxs-lookup"><span data-stu-id="b6c9e-116">It specifies which messaging system MAPI uses to handle a given message.</span></span>
  
<span data-ttu-id="b6c9e-117">Cette propriété détermine également le format de la chaîne d’adresse dans le **PR_EMAIL_ADRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b6c9e-117">This property also determines the format of the address string in the **PR_EMAIL_ADRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span></span> <span data-ttu-id="b6c9e-118">Il fournit la chaîne de peut contenir uniquement les caractères alphabétiques majuscules de A à Z et les chiffres de 0 à 9.</span><span class="sxs-lookup"><span data-stu-id="b6c9e-118">The string it provides can contain only the uppercase alphabetic characters from A through Z and the numbers from 0 through 9.</span></span>
  
<span data-ttu-id="b6c9e-119">Voici des exemples valides pour la chaîne :</span><span class="sxs-lookup"><span data-stu-id="b6c9e-119">Valid examples for the string include:</span></span> 
  
```cpp
FAX
MHS
PROFS
SMTP
X400

```

## <a name="related-resources"></a><span data-ttu-id="b6c9e-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b6c9e-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b6c9e-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="b6c9e-121">Protocol specifications</span></span>

<span data-ttu-id="b6c9e-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6c9e-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6c9e-123">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="b6c9e-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b6c9e-124">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6c9e-124">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6c9e-125">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="b6c9e-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="b6c9e-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6c9e-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6c9e-127">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="b6c9e-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="b6c9e-128">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6c9e-128">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6c9e-129">Gère les communications d’un client avec un serveur NSPI Name Service Provider Interface ().</span><span class="sxs-lookup"><span data-stu-id="b6c9e-129">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="b6c9e-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6c9e-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6c9e-131">Définit les structures de base de données qui sont utilisés dans les opérations à distance.</span><span class="sxs-lookup"><span data-stu-id="b6c9e-131">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="b6c9e-132">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6c9e-132">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6c9e-133">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="b6c9e-133">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="b6c9e-134">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6c9e-134">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6c9e-135">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="b6c9e-135">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="b6c9e-136">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6c9e-136">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6c9e-137">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="b6c9e-137">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="b6c9e-138">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6c9e-138">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6c9e-139">Spécifie les opérations autorisées pour les objets de banque de messages principale.</span><span class="sxs-lookup"><span data-stu-id="b6c9e-139">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="b6c9e-140">[[MS-OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6c9e-140">[[MS-OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6c9e-141">Spécifie les propriétés et les opérations qui sont autorisées pour les modèles de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="b6c9e-141">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="b6c9e-142">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6c9e-142">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6c9e-143">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="b6c9e-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="b6c9e-144">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6c9e-144">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6c9e-145">Manipule les messages électroniques entrants sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="b6c9e-145">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="b6c9e-146">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6c9e-146">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6c9e-147">Spécifie les propriétés et opérations pour la manipulation d’une configuration de liste de dossier de recherche.</span><span class="sxs-lookup"><span data-stu-id="b6c9e-147">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b6c9e-148">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b6c9e-148">Header files</span></span>

<span data-ttu-id="b6c9e-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b6c9e-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="b6c9e-150">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b6c9e-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="b6c9e-151">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="b6c9e-151">Mapitags.h</span></span>
  
> <span data-ttu-id="b6c9e-152">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="b6c9e-152">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b6c9e-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6c9e-153">See also</span></span>



[<span data-ttu-id="b6c9e-154">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b6c9e-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b6c9e-155">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b6c9e-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b6c9e-156">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b6c9e-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b6c9e-157">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="b6c9e-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
  
[<span data-ttu-id="b6c9e-158">Types d’adresses MAPI</span><span class="sxs-lookup"><span data-stu-id="b6c9e-158">MAPI Address Types</span></span>](mapi-address-types.md)

