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
ms.openlocfilehash: cf1f3b4d72426fb5f80decdc074a622b140657c8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388265"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a><span data-ttu-id="fc17e-103">Propriété canonique PidTagRpcOverHttpFlags</span><span class="sxs-lookup"><span data-stu-id="fc17e-103">PidTagRpcOverHttpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="fc17e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc17e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc17e-105">Contient les paramètres d’un profil utilisé par Microsoft Office Outlook pour se connecter à Microsoft Exchange Server à l’aide d’un appel de procédure distante (RPC) sur protocole HTTP (Hypertext Transfer).</span><span class="sxs-lookup"><span data-stu-id="fc17e-105">Contains the settings in a profile used by Microsoft Office Outlook to connect to Microsoft Exchange Server by using a remote procedure call (RPC) over Hypertext Transfer Protocol (HTTP).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fc17e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="fc17e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fc17e-107">PR_ROH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="fc17e-107">PR_ROH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="fc17e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="fc17e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fc17e-109">0x6623</span><span class="sxs-lookup"><span data-stu-id="fc17e-109">0x6623</span></span>  <br/> |
|<span data-ttu-id="fc17e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="fc17e-110">Data type:</span></span>  <br/> |<span data-ttu-id="fc17e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fc17e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fc17e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="fc17e-112">Area:</span></span>  <br/> |<span data-ttu-id="fc17e-113">Divers</span><span class="sxs-lookup"><span data-stu-id="fc17e-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc17e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="fc17e-114">Remarks</span></span>

<span data-ttu-id="fc17e-115">La propriété **PR_ROH_FLAGS** est stockée dans la Section profil globale d’un profil MAPI Messaging Application Programming Interface ().</span><span class="sxs-lookup"><span data-stu-id="fc17e-115">The **PR_ROH_FLAGS** property is stored in the Global Profile Section of a Messaging Application Programming Interface (MAPI) profile.</span></span> <span data-ttu-id="fc17e-116">La valeur de **PR_ROH_FLAGS** est un masque de bits qui est composée d’un ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="fc17e-116">The value of **PR_ROH_FLAGS** is a bitmask that is made up of one or more of the following flags.</span></span> 
  
|<span data-ttu-id="fc17e-117">**Nom**</span><span class="sxs-lookup"><span data-stu-id="fc17e-117">**Name**</span></span>|<span data-ttu-id="fc17e-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="fc17e-118">**Value**</span></span>|<span data-ttu-id="fc17e-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="fc17e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fc17e-120">**ROHFLAGS_USE_ROH**</span><span class="sxs-lookup"><span data-stu-id="fc17e-120">**ROHFLAGS_USE_ROH**</span></span> <br/> |<span data-ttu-id="fc17e-121">0 x 1</span><span class="sxs-lookup"><span data-stu-id="fc17e-121">0x1</span></span>  <br/> |<span data-ttu-id="fc17e-122">Connectez-vous au serveur Exchange en utilisant RPC sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="fc17e-122">Connect to the Exchange Server using RPC over HTTP.</span></span>  <br/> |
|<span data-ttu-id="fc17e-123">**ROHFLAGS_SSL_ONLY**</span><span class="sxs-lookup"><span data-stu-id="fc17e-123">**ROHFLAGS_SSL_ONLY**</span></span> <br/> |<span data-ttu-id="fc17e-124">0 x 2</span><span class="sxs-lookup"><span data-stu-id="fc17e-124">0x2</span></span>  <br/> |<span data-ttu-id="fc17e-125">Connectez-vous au serveur Exchange à l’aide de Secure Sockets Layer (SSL) uniquement.</span><span class="sxs-lookup"><span data-stu-id="fc17e-125">Connect to the Exchange Server using Secure Socket Layer (SSL) only.</span></span>  <br/> |
|<span data-ttu-id="fc17e-126">**ROHFLAGS_MUTUAL_AUTH**</span><span class="sxs-lookup"><span data-stu-id="fc17e-126">**ROHFLAGS_MUTUAL_AUTH**</span></span> <br/> |<span data-ttu-id="fc17e-127">0 x 4</span><span class="sxs-lookup"><span data-stu-id="fc17e-127">0x4</span></span>  <br/> |<span data-ttu-id="fc17e-128">Authentifier mutuellement la session lors de la connexion à l’aide de SSL.</span><span class="sxs-lookup"><span data-stu-id="fc17e-128">Mutually authenticate the session when connecting by using SSL.</span></span>  <br/> |
|<span data-ttu-id="fc17e-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span><span class="sxs-lookup"><span data-stu-id="fc17e-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span></span> <br/> |<span data-ttu-id="fc17e-130">0 x 8</span><span class="sxs-lookup"><span data-stu-id="fc17e-130">0x8</span></span>  <br/> |<span data-ttu-id="fc17e-131">Sur des réseaux rapides, se connecter via le protocole HTTP.</span><span class="sxs-lookup"><span data-stu-id="fc17e-131">On fast networks, connect by using HTTP first.</span></span> <span data-ttu-id="fc17e-132">Ensuite, connectez-vous à l’aide de TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="fc17e-132">Then, connect by using TCP/IP.</span></span>  <br/> |
|<span data-ttu-id="fc17e-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span><span class="sxs-lookup"><span data-stu-id="fc17e-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span></span> <br/> |<span data-ttu-id="fc17e-134">0 x 20</span><span class="sxs-lookup"><span data-stu-id="fc17e-134">0x20</span></span>  <br/> |<span data-ttu-id="fc17e-135">Sur des réseaux lents, se connecter via le protocole HTTP.</span><span class="sxs-lookup"><span data-stu-id="fc17e-135">On slow networks, connect by using HTTP first.</span></span> <span data-ttu-id="fc17e-136">Ensuite, connectez-vous à l’aide de TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="fc17e-136">Then, connect by using TCP/IP.</span></span>  <br/> |
   
<span data-ttu-id="fc17e-137">Par exemple, pour définir le **PR_ROH_FLAGS** propriété pour activer RPC sur HTTP, pour exiger le chiffrement SSL et pour indiquer que le protocole HTTP doit être utilisé tout d’abord sur Mes connexions lentes, définie la valeur de la propriété **PR_ROH_FLAGS** à `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` qui est égal à 0 x 23.</span><span class="sxs-lookup"><span data-stu-id="fc17e-137">For example, to set the **PR_ROH_FLAGS** property to turn on RPC over HTTP, to require SSL, and to specify that the HTTP protocol should be used first on slow connections, set the value of the **PR_ROH_FLAGS** property to  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` which is equal to 0x23.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fc17e-138">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="fc17e-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fc17e-139">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="fc17e-139">Protocol specifications</span></span>

<span data-ttu-id="fc17e-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc17e-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc17e-141">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="fc17e-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fc17e-142">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc17e-142">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc17e-143">Définit les structures de base de données qui sont utilisés dans les opérations à distance.</span><span class="sxs-lookup"><span data-stu-id="fc17e-143">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="fc17e-144">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc17e-144">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc17e-145">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="fc17e-145">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fc17e-146">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="fc17e-146">Header files</span></span>

<span data-ttu-id="fc17e-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fc17e-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="fc17e-148">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="fc17e-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="fc17e-149">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="fc17e-149">Mapitags.h</span></span>
  
> <span data-ttu-id="fc17e-150">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="fc17e-150">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc17e-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc17e-151">See also</span></span>



[<span data-ttu-id="fc17e-152">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="fc17e-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fc17e-153">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="fc17e-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fc17e-154">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="fc17e-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fc17e-155">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="fc17e-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

