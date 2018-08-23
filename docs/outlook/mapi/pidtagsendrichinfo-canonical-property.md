---
title: Propriété canonique PidTagSendRichInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendRichInfo
api_type:
- COM
ms.assetid: e85fc766-197a-484f-b600-68cd28a052a2
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: a1db4ba7a70695b17631ca13f1728043be8164bd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575965"
---
# <a name="pidtagsendrichinfo-canonical-property"></a><span data-ttu-id="c9146-103">Propriété canonique PidTagSendRichInfo</span><span class="sxs-lookup"><span data-stu-id="c9146-103">PidTagSendRichInfo Canonical Property</span></span>

  
  
<span data-ttu-id="c9146-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9146-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9146-105">Contient la valeur TRUE si le destinataire peut recevoir le contenu du message, y compris le Format RTF (RICH Text Format) et les objets Object Linking and Embedding (OLE).</span><span class="sxs-lookup"><span data-stu-id="c9146-105">Contains TRUE if the recipient can receive all message content, including Rich Text Format (RTF) and Object Linking and Embedding (OLE) objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9146-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c9146-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c9146-107">PR_SEND_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="c9146-107">PR_SEND_RICH_INFO</span></span>  <br/> |
|<span data-ttu-id="c9146-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c9146-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c9146-109">0x3A40</span><span class="sxs-lookup"><span data-stu-id="c9146-109">0x3A40</span></span>  <br/> |
|<span data-ttu-id="c9146-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c9146-110">Data type:</span></span>  <br/> |<span data-ttu-id="c9146-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c9146-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c9146-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="c9146-112">Area:</span></span>  <br/> |<span data-ttu-id="c9146-113">Address</span><span class="sxs-lookup"><span data-stu-id="c9146-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9146-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c9146-114">Remarks</span></span>

<span data-ttu-id="c9146-115">Il est recommandé que la liste de distribution et des objets utilisateur de messagerie exposent cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c9146-115">It is recommended that distribution list and messaging user objects expose this property.</span></span> 
  
<span data-ttu-id="c9146-116">Cette propriété indique si l’expéditeur considère que le destinataire doit être compatible MAPI.</span><span class="sxs-lookup"><span data-stu-id="c9146-116">This property indicates whether the sender considers the recipient to be MAPI-enabled.</span></span> 
  
<span data-ttu-id="c9146-117">Lorsque cette propriété est définie sur TRUE, le transport et la passerelle peuvent transmettre l’intégralité du contenu du message, y compris les objets RTF et OLE.</span><span class="sxs-lookup"><span data-stu-id="c9146-117">When this property is set to TRUE, the transport and gateway can transmit the full content of the message, including RTF and OLE objects.</span></span> <span data-ttu-id="c9146-118">Le fournisseur de transport et de la passerelle doivent utiliser Neutral Encapsulation Format TNEF (Transport) pour encapsuler des propriétés qui ne sont pas natives à tous les systèmes de messagerie nécessaires.</span><span class="sxs-lookup"><span data-stu-id="c9146-118">The transport provider and gateway should use Transport Neutral Encapsulation Format (TNEF) to encapsulate any properties that are not native to all the messaging systems involved.</span></span> 
  
<span data-ttu-id="c9146-119">Lorsque cette propriété est définie sur FALSE, le fournisseur de transport et la passerelle sont libres d’ignorer le contenu des messages que leurs clients natifs ne peut pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="c9146-119">When this property is set to FALSE, the transport provider and gateway are free to discard message content that their native clients cannot use.</span></span> <span data-ttu-id="c9146-120">Par exemple, lorsque les clients ne prennent pas en charge au format RTF, le fournisseur de transport peut envoyer uniquement du texte brut.</span><span class="sxs-lookup"><span data-stu-id="c9146-120">For example, when the clients do not support RTF, the transport provider can send only plain text.</span></span> 
  
<span data-ttu-id="c9146-121">Lorsque cette propriété n’est pas définie, le comportement par défaut est déterminé par l’implémentation du fournisseur de transport, message transfert agent d’ou de passerelle.</span><span class="sxs-lookup"><span data-stu-id="c9146-121">When this property is not set, default behavior is determined by the implementation of the transport provider, message transfer agent (MTA), or gateway.</span></span> <span data-ttu-id="c9146-122">Fournisseurs de carnet d’adresses ne sont pas nécessaire pour prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c9146-122">Address book providers are not required to support this property.</span></span> <span data-ttu-id="c9146-123">Par exemple, un fournisseur de transport et le carnet d’adresses étroitement couplés peut choisir d’envoyer TNEF mais jamais utiliser le format RTF.</span><span class="sxs-lookup"><span data-stu-id="c9146-123">For example, a tightly coupled address book and transport provider can choose to send TNEF but never use RTF.</span></span> 
  
<span data-ttu-id="c9146-124">Le client ne doit pas utiliser le fournisseur de transport et passerelle utilisera TNEF sur leur propre initiative.</span><span class="sxs-lookup"><span data-stu-id="c9146-124">The client should not assume the transport provider and gateway will use TNEF on their own initiative.</span></span> <span data-ttu-id="c9146-125">Certains fournisseurs de transport et les passerelles qui prennent en charge TNEF transmettent, indépendamment de la valeur de cette propriété, mais d’autres personnes refuser construire ou envoyer TNEF si elle n’est pas définie sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="c9146-125">Some transport providers and gateways that support TNEF transmit it without regard to the value of this property, but others decline to construct or send TNEF if it is not set to TRUE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c9146-126">La valeur de cette propriété et les décisions en fonction de sa valeur, se trouvent sur une base par destinataire.</span><span class="sxs-lookup"><span data-stu-id="c9146-126">The setting of this property, and the decisions based on its value, are on a per-recipient basis.</span></span> 
  
<span data-ttu-id="c9146-127">Par défaut, MAPI définit la valeur True.</span><span class="sxs-lookup"><span data-stu-id="c9146-127">By default, MAPI sets the value to TRUE.</span></span> <span data-ttu-id="c9146-128">Un client appelant [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) ou un fournisseur de l’appel [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) pouvez définir le bit **MAPI_SEND_NO_RICH_INFO** dans le paramètre _ulFlags_ , ce qui fait que MAPI définir cette propriété sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="c9146-128">A client calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) or a provider calling [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) can set the **MAPI_SEND_NO_RICH_INFO** bit in the  _ulFlags_ parameter, which causes MAPI to set this property to FALSE.</span></span> <span data-ttu-id="c9146-129">Uniques créés par l’interface utilisateur utilisent la valeur spécifiée par le modèle de création.</span><span class="sxs-lookup"><span data-stu-id="c9146-129">One-offs created by the user interface use the value specified by the creating template.</span></span> 
  
<span data-ttu-id="c9146-130">Pour les appels à la méthode [IAddrBook::ResolveName](iaddrbook-resolvename.md) lorsque le nom ne peut pas être résolu, mais peut être interprété comme une adresse Internet (SMTP), cette propriété est définie sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="c9146-130">On calls to the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method when the name cannot be resolved but can be interpreted as an Internet address (SMTP), this property is set to FALSE.</span></span> <span data-ttu-id="c9146-131">Pour être interprété comme une adresse Internet, le nom complet de l’entrée non résolue doit être au format X@Y. Z, tel que « pete@pinecone.com ».</span><span class="sxs-lookup"><span data-stu-id="c9146-131">To be construed as an Internet address, the display name of the unresolved entry must be in the format X@Y.Z, such as "pete@pinecone.com".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c9146-132">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c9146-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c9146-133">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="c9146-133">Protocol specifications</span></span>

<span data-ttu-id="c9146-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9146-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9146-135">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="c9146-135">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c9146-136">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9146-136">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9146-137">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="c9146-137">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="c9146-138">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9146-138">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9146-139">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="c9146-139">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="c9146-140">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c9146-140">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c9146-141">des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="c9146-141">from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c9146-142">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c9146-142">Header files</span></span>

<span data-ttu-id="c9146-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9146-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="c9146-144">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c9146-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="c9146-145">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="c9146-145">Mapitags.h</span></span>
  
> <span data-ttu-id="c9146-146">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="c9146-146">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9146-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9146-147">See also</span></span>



[<span data-ttu-id="c9146-148">Propriété canonique PidTagAttachDataObject</span><span class="sxs-lookup"><span data-stu-id="c9146-148">PidTagAttachDataObject Canonical Property</span></span>](pidtagattachdataobject-canonical-property.md)


[<span data-ttu-id="c9146-149">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c9146-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c9146-150">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c9146-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c9146-151">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c9146-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c9146-152">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="c9146-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

