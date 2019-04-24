---
title: Propriété canonique PidTagStoreUnicodeMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreUnicodeMask
api_type:
- COM
ms.assetid: a6082162-2a74-4850-a0df-4bdbc67b41d8
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e15c259003ed2cb425eb181f4383f3054967b993
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339318"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a><span data-ttu-id="c2954-103">Propriété canonique PidTagStoreUnicodeMask</span><span class="sxs-lookup"><span data-stu-id="c2954-103">PidTagStoreUnicodeMask Canonical Property</span></span>

  
  
<span data-ttu-id="c2954-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2954-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2954-105">Contient un masque de réindicateur des indicateurs que les applications clientes doivent interroger pour déterminer les caractéristiques d'une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="c2954-105">Contains a bitmask of flags that client applications should query to determine the characteristics of a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c2954-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c2954-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c2954-107">PR_STORE_UNICODE_MASK</span><span class="sxs-lookup"><span data-stu-id="c2954-107">PR_STORE_UNICODE_MASK</span></span>  <br/> |
|<span data-ttu-id="c2954-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c2954-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c2954-109">0x340F</span><span class="sxs-lookup"><span data-stu-id="c2954-109">0x340F</span></span>  <br/> |
|<span data-ttu-id="c2954-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c2954-110">Data type:</span></span>  <br/> |<span data-ttu-id="c2954-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c2954-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c2954-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="c2954-112">Area:</span></span>  <br/> |<span data-ttu-id="c2954-113">Banque de messages MAPI</span><span class="sxs-lookup"><span data-stu-id="c2954-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2954-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c2954-114">Remarks</span></span>

<span data-ttu-id="c2954-115">Cette propriété permet de divulguer les fonctionnalités d'une banque de messages aux applications clientes qui envisagent de les envoyer à un message.</span><span class="sxs-lookup"><span data-stu-id="c2954-115">This property discloses the capabilities of a message store to client applications planning to send it a message.</span></span> <span data-ttu-id="c2954-116">Les indicateurs peuvent faciliter les décisions d'un client ou d'un autre magasin, par exemple s'il faut envoyer des **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) ou seulement **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c2954-116">The flags can facilitate decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="c2954-117">Un client ne doit jamais définir cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c2954-117">A client should never set this property.</span></span> <span data-ttu-id="c2954-118">Une tentative renvoie **MAPI_E_COMPUTED**.</span><span class="sxs-lookup"><span data-stu-id="c2954-118">An attempt returns **MAPI_E_COMPUTED**.</span></span> 
  
<span data-ttu-id="c2954-119">Un ou plusieurs des indicateurs suivants peuvent être définis pour cette propriété:</span><span class="sxs-lookup"><span data-stu-id="c2954-119">One or more of the following flags can be set for this property:</span></span> 
  
<span data-ttu-id="c2954-120">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="c2954-120">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="c2954-121">(131072, 0x00020000) La Banque de messages prend en charge les propriétés contenant des caractères ANSI (American National Standards Institute) (8 bits).</span><span class="sxs-lookup"><span data-stu-id="c2954-121">(131072, 0x00020000) The message store supports properties that contain American National Standards Institute (ANSI) (8-bit) characters.</span></span>
    
<span data-ttu-id="c2954-122">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="c2954-122">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="c2954-123">(32, 0x00000020) La Banque de messages prend en charge les pièces jointes OLE (Object Linking and Embedding) ou non-OLE pour les messages.</span><span class="sxs-lookup"><span data-stu-id="c2954-123">(32, 0x00000020) The message store supports Object Linking and Embedding (OLE) or non-OLE attachments to messages.</span></span> 
    
<span data-ttu-id="c2954-124">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="c2954-124">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="c2954-125">(1024, 0x00000400) La Banque de messages prend en charge les vues classées des tables.</span><span class="sxs-lookup"><span data-stu-id="c2954-125">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="c2954-126">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="c2954-126">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="c2954-127">(16, 0x00000010) La Banque de messages prend en charge la création de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="c2954-127">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="c2954-128">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="c2954-128">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="c2954-129">(1, 0x00000001) Les identificateurs d'entrée pour les objets dans la Banque de messages sont uniques, c'est-à-dire qu'ils ne sont jamais réutilisés pendant la durée de vie de la Banque.</span><span class="sxs-lookup"><span data-stu-id="c2954-129">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="c2954-130">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="c2954-130">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="c2954-131">(65536, 0x00010000) La Banque de messages prend en charge les messages HTML, stockés dans la propriété **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c2954-131">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="c2954-132">Notez que **STORE_HTML_OK** n'est pas défini dans les versions de MAPIDEFS. H inclus avec le serveur Microsoft Exchange 2000 et versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="c2954-132">Note that **STORE_HTML_OK** is not defined in versions of MAPIDEFS.H that are included with Microsoft Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="c2954-133">Si votre environnement de développement utilise un MAPIDEFS. H qui n'inclut pas **STORE_HTML_OK**, utilisez la valeur «0x00010000» à la place.</span><span class="sxs-lookup"><span data-stu-id="c2954-133">If your development environment uses a MAPIDEFS.H file that does not include **STORE_HTML_OK**, use the value "0x00010000" instead.</span></span> 
    
<span data-ttu-id="c2954-134">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="c2954-134">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="c2954-135">(2097152, 0x00200000) Dans une banque de fichiers PST encapsulée, indique que lorsqu'un nouveau message arrive dans le magasin, le traitement des règles et du filtrage du courrier indésirable est effectué séparément sur le message.</span><span class="sxs-lookup"><span data-stu-id="c2954-135">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store does rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="c2954-136">Le magasin appelle [IMAPISupport:: Notify](imapisupport-notify.md), en définissant **fnevNewMail** dans la structure de [notification](notification.md) qui est transmise en tant que paramètre, puis transmet les détails du nouveau message au client d'écoute.</span><span class="sxs-lookup"><span data-stu-id="c2954-136">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="c2954-137">Par la suite, lorsque le client à l’écoute reçoit la notification, il ne traite pas de règles dans le message.</span><span class="sxs-lookup"><span data-stu-id="c2954-137">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="c2954-138">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="c2954-138">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="c2954-139">(524288, 0x00080000) Cet indicateur est réservé et ne doit pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="c2954-139">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="c2954-140">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="c2954-140">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="c2954-141">(8, 0x00000008) La Banque de messages prend en charge la modification de ses messages existants.</span><span class="sxs-lookup"><span data-stu-id="c2954-141">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="c2954-142">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="c2954-142">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="c2954-143">(512, 0x00000200) La Banque de messages prend en charge les propriétés à valeurs multiples, garantit la stabilité de l'ordre des valeurs dans une propriété à valeurs multiples pendant une opération d'enregistrement et prend en charge l'instanciation de propriétés à valeurs multiples dans des tableaux.</span><span class="sxs-lookup"><span data-stu-id="c2954-143">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="c2954-144">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="c2954-144">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="c2954-145">(256, 0x00000100) La Banque de messages prend en charge les notifications.</span><span class="sxs-lookup"><span data-stu-id="c2954-145">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="c2954-146">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="c2954-146">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="c2954-147">(64, 0x00000040) La Banque de messages prend en charge les pièces jointes OLE.</span><span class="sxs-lookup"><span data-stu-id="c2954-147">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="c2954-148">Les données OLE sont accessibles via une interface **IStorage** , telle que celle disponible via la propriété **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c2954-148">The OLE data is accessible through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="c2954-149">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="c2954-149">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="c2954-150">(16384, 0x00004000) Les dossiers de cette banque sont publics (multi-utilisateurs), et non privés (éventuellement multi-instance, pas multi-utilisateur).</span><span class="sxs-lookup"><span data-stu-id="c2954-150">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="c2954-151">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="c2954-151">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="c2954-152">(8388608, 0x00800000) Le gestionnaire de protocole MAPI n'analyse pas la Banque, et la Banque est responsable de la transmission de toutes les modifications via les notifications à l'indexeur afin de disposer d'un message indexé.</span><span class="sxs-lookup"><span data-stu-id="c2954-152">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="c2954-153">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="c2954-153">STORE_READONLY</span></span> 
  
> <span data-ttu-id="c2954-154">(2, 0x00000002) Toutes les interfaces de la Banque de messages ont un niveau d'accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c2954-154">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="c2954-155">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="c2954-155">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="c2954-156">(4096, 0x00001000) La Banque de messages prend en charge les restrictions.</span><span class="sxs-lookup"><span data-stu-id="c2954-156">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="c2954-157">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="c2954-157">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="c2954-158">(2048, 0x00000800) La Banque de messages prend en charge les messages RTF (Rich Text Format), généralement compressés, et la Banque elle-même conserve la synchronisation de **PR_BODY** et de **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="c2954-158">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="c2954-159">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="c2954-159">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="c2954-160">(4, 0x00000004) La Banque de messages prend en charge les dossiers de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="c2954-160">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="c2954-161">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="c2954-161">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="c2954-162">(8192, 0x00002000) La Banque de messages prend en charge les affichages de tri des tables.</span><span class="sxs-lookup"><span data-stu-id="c2954-162">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="c2954-163">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="c2954-163">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="c2954-164">(128, 0x00000080) La Banque de messages prend en charge le marquage d'un message pour l'envoi.</span><span class="sxs-lookup"><span data-stu-id="c2954-164">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="c2954-165">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="c2954-165">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="c2954-166">(32768, 0x00008000) La Banque de messages prend en charge le stockage des messages au format RTF (Rich Text Format) sous forme non compressée.</span><span class="sxs-lookup"><span data-stu-id="c2954-166">(32768, 0x00008000) The message store supports storage of revisable form text (RTF) messages in uncompressed form.</span></span> <span data-ttu-id="c2954-167">Un flux de contenu RTF non compressé est identifié par la valeur **dwMagicUncompressedRTF** dans l'en-tête de flux.</span><span class="sxs-lookup"><span data-stu-id="c2954-167">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="c2954-168">La valeur **dwMagicUncompressedRTF** est définie dans le RTFLIB. Fichier H.</span><span class="sxs-lookup"><span data-stu-id="c2954-168">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="c2954-169">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="c2954-169">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="c2954-170">(262144, 0x00040000) La Banque de messages prend en charge les propriétés contenant des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="c2954-170">(262144, 0x00040000) The message store supports properties containing Unicode characters.</span></span>
    
<span data-ttu-id="c2954-171">Une version RTF d'un message peut toujours être stockée, même si la Banque de messages n'est pas compatible avec le format RTF.</span><span class="sxs-lookup"><span data-stu-id="c2954-171">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="c2954-172">Si le bit STORE_RTF_OK n'est pas défini pour un magasin particulier, un client qui gère les versions RTF doit appeler la fonction [RTFSync](rtfsync.md) pour que les versions **PR_BODY** et **PR_RTF_COMPRESSED** soient synchronisées pour le contenu de texte.</span><span class="sxs-lookup"><span data-stu-id="c2954-172">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="c2954-173">Le format RTF est toujours stocké dans **PR_RTF_COMPRESSED**, qu'il soit ou non compressé.</span><span class="sxs-lookup"><span data-stu-id="c2954-173">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c2954-174">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="c2954-174">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c2954-175">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="c2954-175">Header files</span></span>

<span data-ttu-id="c2954-176">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c2954-176">Mapidefs.h</span></span>
  
> <span data-ttu-id="c2954-177">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c2954-177">Provides data type definitions.</span></span>
    
<span data-ttu-id="c2954-178">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="c2954-178">Mapitags.h</span></span>
  
> <span data-ttu-id="c2954-179">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="c2954-179">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c2954-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2954-180">See also</span></span>



[<span data-ttu-id="c2954-181">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c2954-181">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c2954-182">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c2954-182">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c2954-183">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c2954-183">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c2954-184">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="c2954-184">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

