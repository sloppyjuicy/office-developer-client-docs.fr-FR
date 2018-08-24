---
title: Propriété canonique PidTagRpcOverHttpFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c8b30768-cf83-450d-9fe2-567a5e0c2f57
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b36f71958528b25829b1ff85b29572b3590f9d4f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594816"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a><span data-ttu-id="ffd68-103">Propriété canonique PidTagRpcOverHttpFlags</span><span class="sxs-lookup"><span data-stu-id="ffd68-103">PidTagRpcOverHttpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="ffd68-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffd68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffd68-105">Contient les paramètres d’un profil utilisé par Microsoft Office Outlook pour se connecter à Microsoft Exchange Server à l’aide d’un appel de procédure distante (RPC) sur protocole HTTP (Hypertext Transfer).</span><span class="sxs-lookup"><span data-stu-id="ffd68-105">Contains the settings in a profile used by Microsoft Office Outlook to connect to Microsoft Exchange Server by using a remote procedure call (RPC) over Hypertext Transfer Protocol (HTTP).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ffd68-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ffd68-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ffd68-107">PR_ROH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ffd68-107">PR_ROH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="ffd68-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ffd68-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ffd68-109">0x6623</span><span class="sxs-lookup"><span data-stu-id="ffd68-109">0x6623</span></span>  <br/> |
|<span data-ttu-id="ffd68-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ffd68-110">Data type:</span></span>  <br/> |<span data-ttu-id="ffd68-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ffd68-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ffd68-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ffd68-112">Area:</span></span>  <br/> |<span data-ttu-id="ffd68-113">Divers</span><span class="sxs-lookup"><span data-stu-id="ffd68-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffd68-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ffd68-114">Remarks</span></span>

<span data-ttu-id="ffd68-115">La propriété **PR_ROH_FLAGS** est stockée dans la Section profil globale d’un profil MAPI Messaging Application Programming Interface ().</span><span class="sxs-lookup"><span data-stu-id="ffd68-115">The **PR_ROH_FLAGS** property is stored in the Global Profile Section of a Messaging Application Programming Interface (MAPI) profile.</span></span> <span data-ttu-id="ffd68-116">La valeur de **PR_ROH_FLAGS** est un masque de bits qui est composée d’un ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="ffd68-116">The value of **PR_ROH_FLAGS** is a bitmask that is made up of one or more of the following flags.</span></span> 
  
|<span data-ttu-id="ffd68-117">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ffd68-117">**Name**</span></span>|<span data-ttu-id="ffd68-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="ffd68-118">**Value**</span></span>|<span data-ttu-id="ffd68-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="ffd68-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ffd68-120">**ROHFLAGS_USE_ROH**</span><span class="sxs-lookup"><span data-stu-id="ffd68-120">**ROHFLAGS_USE_ROH**</span></span> <br/> |<span data-ttu-id="ffd68-121">0 x 1</span><span class="sxs-lookup"><span data-stu-id="ffd68-121">0x1</span></span>  <br/> |<span data-ttu-id="ffd68-122">Connectez-vous au serveur Exchange en utilisant RPC sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="ffd68-122">Connect to the Exchange Server using RPC over HTTP.</span></span>  <br/> |
|<span data-ttu-id="ffd68-123">**ROHFLAGS_SSL_ONLY**</span><span class="sxs-lookup"><span data-stu-id="ffd68-123">**ROHFLAGS_SSL_ONLY**</span></span> <br/> |<span data-ttu-id="ffd68-124">0 x 2</span><span class="sxs-lookup"><span data-stu-id="ffd68-124">0x2</span></span>  <br/> |<span data-ttu-id="ffd68-125">Connectez-vous au serveur Exchange à l’aide de Secure Sockets Layer (SSL) uniquement.</span><span class="sxs-lookup"><span data-stu-id="ffd68-125">Connect to the Exchange Server using Secure Socket Layer (SSL) only.</span></span>  <br/> |
|<span data-ttu-id="ffd68-126">**ROHFLAGS_MUTUAL_AUTH**</span><span class="sxs-lookup"><span data-stu-id="ffd68-126">**ROHFLAGS_MUTUAL_AUTH**</span></span> <br/> |<span data-ttu-id="ffd68-127">0 x 4</span><span class="sxs-lookup"><span data-stu-id="ffd68-127">0x4</span></span>  <br/> |<span data-ttu-id="ffd68-128">Authentifier mutuellement la session lors de la connexion à l’aide de SSL.</span><span class="sxs-lookup"><span data-stu-id="ffd68-128">Mutually authenticate the session when connecting by using SSL.</span></span>  <br/> |
|<span data-ttu-id="ffd68-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span><span class="sxs-lookup"><span data-stu-id="ffd68-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span></span> <br/> |<span data-ttu-id="ffd68-130">0 x 8</span><span class="sxs-lookup"><span data-stu-id="ffd68-130">0x8</span></span>  <br/> |<span data-ttu-id="ffd68-131">Sur des réseaux rapides, se connecter via le protocole HTTP.</span><span class="sxs-lookup"><span data-stu-id="ffd68-131">On fast networks, connect by using HTTP first.</span></span> <span data-ttu-id="ffd68-132">Ensuite, connectez-vous à l’aide de TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="ffd68-132">Then, connect by using TCP/IP.</span></span>  <br/> |
|<span data-ttu-id="ffd68-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span><span class="sxs-lookup"><span data-stu-id="ffd68-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span></span> <br/> |<span data-ttu-id="ffd68-134">0 x 20</span><span class="sxs-lookup"><span data-stu-id="ffd68-134">0x20</span></span>  <br/> |<span data-ttu-id="ffd68-135">Sur des réseaux lents, se connecter via le protocole HTTP.</span><span class="sxs-lookup"><span data-stu-id="ffd68-135">On slow networks, connect by using HTTP first.</span></span> <span data-ttu-id="ffd68-136">Ensuite, connectez-vous à l’aide de TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="ffd68-136">Then, connect by using TCP/IP.</span></span>  <br/> |
   
<span data-ttu-id="ffd68-137">Par exemple, pour définir le **PR_ROH_FLAGS** propriété pour activer RPC sur HTTP, pour exiger le chiffrement SSL et pour indiquer que le protocole HTTP doit être utilisé tout d’abord sur Mes connexions lentes, définie la valeur de la propriété **PR_ROH_FLAGS** à `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` qui est égal à 0 x 23.</span><span class="sxs-lookup"><span data-stu-id="ffd68-137">For example, to set the **PR_ROH_FLAGS** property to turn on RPC over HTTP, to require SSL, and to specify that the HTTP protocol should be used first on slow connections, set the value of the **PR_ROH_FLAGS** property to  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` which is equal to 0x23.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ffd68-138">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ffd68-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ffd68-139">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="ffd68-139">Protocol specifications</span></span>

<span data-ttu-id="ffd68-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffd68-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffd68-141">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="ffd68-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ffd68-142">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffd68-142">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffd68-143">Définit les structures de base de données qui sont utilisés dans les opérations à distance.</span><span class="sxs-lookup"><span data-stu-id="ffd68-143">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="ffd68-144">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ffd68-144">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ffd68-145">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="ffd68-145">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ffd68-146">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ffd68-146">Header files</span></span>

<span data-ttu-id="ffd68-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ffd68-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="ffd68-148">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ffd68-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="ffd68-149">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ffd68-149">Mapitags.h</span></span>
  
> <span data-ttu-id="ffd68-150">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="ffd68-150">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ffd68-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffd68-151">See also</span></span>



[<span data-ttu-id="ffd68-152">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ffd68-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ffd68-153">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ffd68-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ffd68-154">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ffd68-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ffd68-155">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ffd68-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

