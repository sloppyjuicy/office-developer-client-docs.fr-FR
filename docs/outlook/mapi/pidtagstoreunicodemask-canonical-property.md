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
ms.openlocfilehash: 010b17de08ee5836a26c56f300b36822df2e981e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786846"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a><span data-ttu-id="051bd-103">Propriété canonique PidTagStoreUnicodeMask</span><span class="sxs-lookup"><span data-stu-id="051bd-103">PidTagStoreUnicodeMask Canonical Property</span></span>

  
  
<span data-ttu-id="051bd-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="051bd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="051bd-105">Contient un masque de bits d’indicateurs applications clientes doivent interroger pour déterminer les caractéristiques d’une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="051bd-105">Contains a bitmask of flags that client applications should query to determine the characteristics of a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="051bd-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="051bd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="051bd-107">PR_STORE_UNICODE_MASK</span><span class="sxs-lookup"><span data-stu-id="051bd-107">PR_STORE_UNICODE_MASK</span></span>  <br/> |
|<span data-ttu-id="051bd-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="051bd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="051bd-109">0x340F</span><span class="sxs-lookup"><span data-stu-id="051bd-109">0x340F</span></span>  <br/> |
|<span data-ttu-id="051bd-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="051bd-110">Data type:</span></span>  <br/> |<span data-ttu-id="051bd-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="051bd-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="051bd-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="051bd-112">Area:</span></span>  <br/> |<span data-ttu-id="051bd-113">Banque de messages MAPI</span><span class="sxs-lookup"><span data-stu-id="051bd-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="051bd-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="051bd-114">Remarks</span></span>

<span data-ttu-id="051bd-115">Cette propriété indique les fonctionnalités d’une banque de messages vers des applications clientes envoyer un message de planification.</span><span class="sxs-lookup"><span data-stu-id="051bd-115">This property discloses the capabilities of a message store to client applications planning to send it a message.</span></span> <span data-ttu-id="051bd-116">Les indicateurs peuvent faciliter les décisions par un client ou un autre magasin, telles que s’il faut envoyer **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) ou uniquement **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="051bd-116">The flags can facilitate decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="051bd-117">Un client ne doit jamais définir cette propriété.</span><span class="sxs-lookup"><span data-stu-id="051bd-117">A client should never set this property.</span></span> <span data-ttu-id="051bd-118">Une tentative renvoie **MAPI_E_COMPUTED**.</span><span class="sxs-lookup"><span data-stu-id="051bd-118">An attempt returns **MAPI_E_COMPUTED**.</span></span> 
  
<span data-ttu-id="051bd-119">Un ou plusieurs des indicateurs suivants peuvent être définie pour cette propriété :</span><span class="sxs-lookup"><span data-stu-id="051bd-119">One or more of the following flags can be set for this property:</span></span> 
  
<span data-ttu-id="051bd-120">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="051bd-120">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="051bd-121">(131072, 0 x 00020000) La banque de messages prend en charge les propriétés qui contiennent des caractères National Institute ANSI (American Standards) (8 bits).</span><span class="sxs-lookup"><span data-stu-id="051bd-121">(131072, 0x00020000) The message store supports properties that contain American National Standards Institute (ANSI) (8-bit) characters.</span></span>
    
<span data-ttu-id="051bd-122">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="051bd-122">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="051bd-123">(32, 0 x 00000020) La banque de messages prend en charge Object Linking et Embedding (OLE) ou non-OLE pièces jointes aux messages.</span><span class="sxs-lookup"><span data-stu-id="051bd-123">(32, 0x00000020) The message store supports Object Linking and Embedding (OLE) or non-OLE attachments to messages.</span></span> 
    
<span data-ttu-id="051bd-124">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="051bd-124">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="051bd-125">(1024, 0 x 00000400) La banque de messages prend en charge les affichages, voir les tableaux.</span><span class="sxs-lookup"><span data-stu-id="051bd-125">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="051bd-126">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="051bd-126">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="051bd-127">(16, 0 x 00000010) La banque de messages prend en charge la création de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="051bd-127">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="051bd-128">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="051bd-128">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="051bd-129">(1, 0 x 00000001) Identificateurs d’entrée pour les objets dans la banque de messages sont uniques, autrement dit, jamais réutilisé pendant la durée de vie de la banque.</span><span class="sxs-lookup"><span data-stu-id="051bd-129">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="051bd-130">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="051bd-130">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="051bd-131">(65536, 0 x 00010000) La banque de messages prend en charge des messages HTML, stockées dans la propriété **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="051bd-131">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="051bd-132">Notez que **STORE_HTML_OK** n’est pas définie dans les versions de MAPIDEFS. H qui sont inclus avec Microsoft Exchange 2000 Server et les versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="051bd-132">Note that **STORE_HTML_OK** is not defined in versions of MAPIDEFS.H that are included with Microsoft Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="051bd-133">Si votre environnement de développement utilise un MAPIDEFS. Fichier H ne pas inclure **STORE_HTML_OK**, utilisez la valeur « 0 x 00010000 » à la place.</span><span class="sxs-lookup"><span data-stu-id="051bd-133">If your development environment uses a MAPIDEFS.H file that does not include **STORE_HTML_OK**, use the value "0x00010000" instead.</span></span> 
    
<span data-ttu-id="051bd-134">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="051bd-134">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="051bd-135">(2097152, 0 x 00200000) Dans une banque de dossiers personnels encapsulée, indique que lorsqu’un nouveau message arrive dans le magasin, magasin fait règles et le courrier indésirable filtrer séparément de traitement du message.</span><span class="sxs-lookup"><span data-stu-id="051bd-135">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store does rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="051bd-136">Les appels de magasin [IMAPISupport::Notify](imapisupport-notify.md), le paramètre **fnevNewMail** dans la structure [NOTIFICATION](notification.md) qui est transmise en tant que paramètre, puis transmet les détails du message pour le client d’écoute.</span><span class="sxs-lookup"><span data-stu-id="051bd-136">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="051bd-137">Par la suite, lorsque le client d’écoute reçoit la notification, il ne traite pas de règles dans le message.</span><span class="sxs-lookup"><span data-stu-id="051bd-137">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="051bd-138">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="051bd-138">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="051bd-139">(524288, 0 x 00080000) Cet indicateur est réservé et ne doit pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="051bd-139">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="051bd-140">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="051bd-140">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="051bd-141">(8, 0 x 00000008) La banque de messages prend en charge la modification de ses messages existants.</span><span class="sxs-lookup"><span data-stu-id="051bd-141">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="051bd-142">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="051bd-142">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="051bd-143">(512, 0 x 00000200) La banque de messages prend en charge les propriétés à valeurs multiples, garantit la stabilité d’ordre de valeur dans une propriété à valeurs multiples dans un enregistrement opération et prend en charge l’instanciation des propriétés à valeurs multiples dans les tableaux.</span><span class="sxs-lookup"><span data-stu-id="051bd-143">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="051bd-144">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="051bd-144">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="051bd-145">(256, 0 x 00000100) La banque de messages prend en charge les notifications.</span><span class="sxs-lookup"><span data-stu-id="051bd-145">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="051bd-146">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="051bd-146">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="051bd-147">(64, 0 x 00000040) La banque de messages prend en charge les pièces jointes OLE.</span><span class="sxs-lookup"><span data-stu-id="051bd-147">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="051bd-148">Les données OLE sont accessibles via une interface **IStorage** , telle que disponibles via la propriété **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="051bd-148">The OLE data is accessible through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="051bd-149">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="051bd-149">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="051bd-150">(16384, 0x00004000) Les dossiers de cette banque sont public (multi-utilisateur), non privée (éventuellement plusieurs instances, mais pas avec plusieurs utilisateurs).</span><span class="sxs-lookup"><span data-stu-id="051bd-150">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="051bd-151">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="051bd-151">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="051bd-152">(8388608, 0 x 00800000) Le Gestionnaire de protocole MAPI ne sera pas analyser le magasin et le magasin est responsable pour acheminer les modifications via les notifications à l’indexeur que les messages indexés.</span><span class="sxs-lookup"><span data-stu-id="051bd-152">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="051bd-153">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="051bd-153">STORE_READONLY</span></span> 
  
> <span data-ttu-id="051bd-154">(2, 0 x 00000002) Toutes les interfaces pour la banque de messages ont un niveau d’accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="051bd-154">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="051bd-155">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="051bd-155">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="051bd-156">(4096, 0 x 00001000) La banque de messages prend en charge les restrictions.</span><span class="sxs-lookup"><span data-stu-id="051bd-156">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="051bd-157">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="051bd-157">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="051bd-158">(2048, 0x00000800) La banque de messages prend en charge les messages RTF (RICH Text Format), généralement compressés, et la banque elle-même conserve **PR_BODY** et **PR_RTF_COMPRESSED** synchronisés.</span><span class="sxs-lookup"><span data-stu-id="051bd-158">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="051bd-159">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="051bd-159">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="051bd-160">(4, 0 x 00000004) La banque de messages prend en charge les dossiers de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="051bd-160">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="051bd-161">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="051bd-161">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="051bd-162">(8 192, 0 x 00002000) La banque de messages prend en charge le tri des vues de tables.</span><span class="sxs-lookup"><span data-stu-id="051bd-162">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="051bd-163">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="051bd-163">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="051bd-164">(128, 0x00000080) La banque de messages prend en charge le marquage d’un message pour son envoi.</span><span class="sxs-lookup"><span data-stu-id="051bd-164">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="051bd-165">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="051bd-165">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="051bd-166">(32768, 0x00008000) La banque de messages prend en charge le stockage des messages de texte (RTF) sous forme révisable sous forme non compressée.</span><span class="sxs-lookup"><span data-stu-id="051bd-166">(32768, 0x00008000) The message store supports storage of revisable form text (RTF) messages in uncompressed form.</span></span> <span data-ttu-id="051bd-167">Un flux de données au format RTF décompressé est identifié par la valeur **dwMagicUncompressedRTF** dans l’en-tête du flux.</span><span class="sxs-lookup"><span data-stu-id="051bd-167">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="051bd-168">La valeur **dwMagicUncompressedRTF** est définie dans le RTFLIB. Fichier H.</span><span class="sxs-lookup"><span data-stu-id="051bd-168">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="051bd-169">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="051bd-169">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="051bd-170">(262144, 0 x 00040000) La banque de messages prend en charge les propriétés contenant des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="051bd-170">(262144, 0x00040000) The message store supports properties containing Unicode characters.</span></span>
    
<span data-ttu-id="051bd-171">Une version au format RTF d’un message peut être stockée toujours, même si la banque de messages est non compatibles RTF.</span><span class="sxs-lookup"><span data-stu-id="051bd-171">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="051bd-172">Si le bit STORE_RTF_OK n’est pas défini pour un magasin particulier, un client de gestion des versions RTF doit lui-même appeler la fonction [RTFSync](rtfsync.md) pour conserver les versions **PR_BODY** et **PR_RTF_COMPRESSED** synchronisées pour le contenu de texte.</span><span class="sxs-lookup"><span data-stu-id="051bd-172">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="051bd-173">Format RTF est toujours stocké dans **PR_RTF_COMPRESSED**, si elle est réellement compressé ou non.</span><span class="sxs-lookup"><span data-stu-id="051bd-173">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="051bd-174">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="051bd-174">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="051bd-175">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="051bd-175">Header files</span></span>

<span data-ttu-id="051bd-176">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="051bd-176">Mapidefs.h</span></span>
  
> <span data-ttu-id="051bd-177">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="051bd-177">Provides data type definitions.</span></span>
    
<span data-ttu-id="051bd-178">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="051bd-178">Mapitags.h</span></span>
  
> <span data-ttu-id="051bd-179">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="051bd-179">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="051bd-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="051bd-180">See also</span></span>



[<span data-ttu-id="051bd-181">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="051bd-181">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="051bd-182">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="051bd-182">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="051bd-183">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="051bd-183">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="051bd-184">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="051bd-184">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

