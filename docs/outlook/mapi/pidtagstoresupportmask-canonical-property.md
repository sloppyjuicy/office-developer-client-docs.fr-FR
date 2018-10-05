---
title: Propriété canonique PidTagStoreSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreSupportMask
api_type:
- COM
ms.assetid: ada5694a-b5b1-471f-be33-906fc052681a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 143e7f0d2cd89cd4e7956cdda05d1bd512db4027
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392332"
---
# <a name="pidtagstoresupportmask-canonical-property"></a><span data-ttu-id="15228-103">Propriété canonique PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="15228-103">PidTagStoreSupportMask Canonical Property</span></span>

  
  
<span data-ttu-id="15228-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15228-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15228-105">Contient un masque binaire composé des indicateurs de cette requête d’applications client pour déterminer les caractéristiques d’une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="15228-105">Contains a bitmask of flags that client applications query to determine the characteristics of a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15228-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="15228-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="15228-107">PR_STORE_SUPPORT_MASK</span><span class="sxs-lookup"><span data-stu-id="15228-107">PR_STORE_SUPPORT_MASK</span></span>  <br/> |
|<span data-ttu-id="15228-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="15228-108">Identifier:</span></span>  <br/> |<span data-ttu-id="15228-109">0x340D</span><span class="sxs-lookup"><span data-stu-id="15228-109">0x340D</span></span>  <br/> |
|<span data-ttu-id="15228-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="15228-110">Data type:</span></span>  <br/> |<span data-ttu-id="15228-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="15228-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="15228-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="15228-112">Area:</span></span>  <br/> |<span data-ttu-id="15228-113">Divers</span><span class="sxs-lookup"><span data-stu-id="15228-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15228-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="15228-114">Remarks</span></span>

<span data-ttu-id="15228-115">Cette propriété indique les fonctionnalités d’une banque de messages pour les applications clientes qui envisagent d’envoyer un message.</span><span class="sxs-lookup"><span data-stu-id="15228-115">This property discloses the capabilities of a message store to client applications that are planning to send it a message.</span></span> <span data-ttu-id="15228-116">Les indicateurs peuvent prendre en charge des décisions par un client ou un autre magasin, telles que s’il faut envoyer **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) ou uniquement **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="15228-116">The flags can support decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="15228-117">Un client ne doit jamais défini **PR_STORE_SUPPORT_MASK**; une tentative de définir cet indicateur renvoie MAPI_E_COMPUTED.</span><span class="sxs-lookup"><span data-stu-id="15228-117">A client should never set **PR_STORE_SUPPORT_MASK**; an attempt to set this flag returns MAPI_E_COMPUTED.</span></span> 
  
<span data-ttu-id="15228-118">Un ou plusieurs des indicateurs suivants peuvent être définies pour le masque de bits **PR_STORE_SUPPORT_MASK** :</span><span class="sxs-lookup"><span data-stu-id="15228-118">One or more of the following flags can be set for the **PR_STORE_SUPPORT_MASK** bitmask:</span></span> 
  
<span data-ttu-id="15228-119">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="15228-119">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="15228-120">(131072, 0 x 00020000) La banque de messages prend en charge les propriétés qui contiennent des caractères ANSI (8 bits).</span><span class="sxs-lookup"><span data-stu-id="15228-120">(131072, 0x00020000) The message store supports properties that contain ANSI (8-bit) characters.</span></span>
    
<span data-ttu-id="15228-121">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="15228-121">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="15228-122">(32, 0 x 00000020) La banque de messages prend en charge les pièces jointes (OLE ou non OLE) pour les messages.</span><span class="sxs-lookup"><span data-stu-id="15228-122">(32, 0x00000020) The message store supports attachments (OLE or non-OLE) to messages.</span></span> 
    
<span data-ttu-id="15228-123">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="15228-123">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="15228-124">(1024, 0 x 00000400) La banque de messages prend en charge les affichages, voir les tableaux.</span><span class="sxs-lookup"><span data-stu-id="15228-124">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="15228-125">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="15228-125">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="15228-126">(16, 0 x 00000010) La banque de messages prend en charge la création de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="15228-126">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="15228-127">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="15228-127">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="15228-128">(1, 0 x 00000001) Identificateurs d’entrée pour les objets dans la banque de messages sont uniques, autrement dit, jamais réutilisé pendant la durée de vie de la banque.</span><span class="sxs-lookup"><span data-stu-id="15228-128">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="15228-129">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="15228-129">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="15228-130">(65536, 0 x 00010000) La banque de messages prend en charge des messages HTML, stockées dans la propriété **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="15228-130">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="15228-131">Si votre environnement de développement utilise un MAPIDEFS. Fichier H qui n’inclut pas STORE_HTML_OK, utilisez plutôt la valeur 0 x 00010000.</span><span class="sxs-lookup"><span data-stu-id="15228-131">If your development environment uses a MAPIDEFS.H file that does not include STORE_HTML_OK, use the value 0x00010000 instead.</span></span> 
    
<span data-ttu-id="15228-132">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="15228-132">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="15228-133">(2097152, 0 x 00200000) Dans une banque de dossiers personnels encapsulée, indique que, lorsqu’un nouveau message arrive dans le magasin, le magasin effectue règles et le filtre de courrier indésirable séparément de traitement du message.</span><span class="sxs-lookup"><span data-stu-id="15228-133">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store performs rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="15228-134">Les appels de magasin [IMAPISupport::Notify](imapisupport-notify.md), le paramètre **fnevNewMail** dans la structure [NOTIFICATION](notification.md) qui est transmise en tant que paramètre, puis transmet les détails du message pour le client d’écoute.</span><span class="sxs-lookup"><span data-stu-id="15228-134">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="15228-135">Par la suite, lorsque le client d’écoute reçoit la notification, il ne traite pas de règles dans le message.</span><span class="sxs-lookup"><span data-stu-id="15228-135">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="15228-136">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="15228-136">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="15228-137">(524288, 0 x 00080000) Cet indicateur est réservé et ne doit pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="15228-137">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="15228-138">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="15228-138">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="15228-139">(8, 0 x 00000008) La banque de messages prend en charge la modification de ses messages existants.</span><span class="sxs-lookup"><span data-stu-id="15228-139">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="15228-140">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="15228-140">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="15228-141">(512, 0 x 00000200) La banque de messages prend en charge les propriétés à valeurs multiples, garantit la stabilité d’ordre de valeur dans une propriété à valeurs multiples dans un enregistrement opération et prend en charge l’instanciation des propriétés à valeurs multiples dans les tableaux.</span><span class="sxs-lookup"><span data-stu-id="15228-141">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="15228-142">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="15228-142">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="15228-143">(256, 0 x 00000100) La banque de messages prend en charge les notifications.</span><span class="sxs-lookup"><span data-stu-id="15228-143">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="15228-144">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="15228-144">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="15228-145">(64, 0 x 00000040) La banque de messages prend en charge les pièces jointes OLE.</span><span class="sxs-lookup"><span data-stu-id="15228-145">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="15228-146">Les données OLE est accessible via une interface **IStorage** , par exemple celui disponibles par le biais de la propriété **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="15228-146">The OLE data can be accessed through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="15228-147">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="15228-147">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="15228-148">(16384, 0x00004000) Les dossiers de cette banque sont public (multi-utilisateur), non privée (éventuellement plusieurs instances, mais pas avec plusieurs utilisateurs).</span><span class="sxs-lookup"><span data-stu-id="15228-148">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="15228-149">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="15228-149">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="15228-150">(8388608, 0 x 00800000) Le Gestionnaire de protocole MAPI ne sera pas analyser le magasin et le magasin est responsable de l’envoi des modifications via les notifications à l’indexeur que les messages indexés.</span><span class="sxs-lookup"><span data-stu-id="15228-150">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible for pushing any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="15228-151">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="15228-151">STORE_READONLY</span></span> 
  
> <span data-ttu-id="15228-152">(2, 0 x 00000002) Toutes les interfaces pour la banque de messages ont un niveau d’accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="15228-152">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="15228-153">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="15228-153">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="15228-154">(4096, 0 x 00001000) La banque de messages prend en charge les restrictions.</span><span class="sxs-lookup"><span data-stu-id="15228-154">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="15228-155">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="15228-155">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="15228-156">(2048, 0x00000800) La banque de messages prend en charge les messages RTF (RICH Text Format), généralement compressés, et la banque elle-même conserve **PR_BODY** et **PR_RTF_COMPRESSED** synchronisés.</span><span class="sxs-lookup"><span data-stu-id="15228-156">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="15228-157">STORE_RULES_OK</span><span class="sxs-lookup"><span data-stu-id="15228-157">STORE_RULES_OK</span></span>
  
> <span data-ttu-id="15228-158">(268435456, 0 x 10000000) Indique que les règles doivent être stockés dans cette banque de dossiers personnels, même s’il n’est pas la banque par défaut.</span><span class="sxs-lookup"><span data-stu-id="15228-158">(268435456, 0x10000000) Indicates that rules should be stored in this PST store even if it is not the default store.</span></span> <span data-ttu-id="15228-159">Lorsque **STORE_RULES_OK** est utilisée conjointement avec **NON_EMS_XP_SAVE**, les règles sont en mesure de s’exécuter sur les magasins de PST encapsulé non par défaut.</span><span class="sxs-lookup"><span data-stu-id="15228-159">When **STORE_RULES_OK** is used in conjunction with **NON_EMS_XP_SAVE**, rules are able to run on non-default PST wrapped stores.</span></span>
    
<span data-ttu-id="15228-160">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="15228-160">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="15228-161">(4, 0 x 00000004) La banque de messages prend en charge les dossiers de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="15228-161">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="15228-162">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="15228-162">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="15228-163">(8 192, 0 x 00002000) La banque de messages prend en charge le tri des vues de tables.</span><span class="sxs-lookup"><span data-stu-id="15228-163">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="15228-164">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="15228-164">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="15228-165">(128, 0x00000080) La banque de messages prend en charge le marquage d’un message pour son envoi.</span><span class="sxs-lookup"><span data-stu-id="15228-165">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="15228-166">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="15228-166">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="15228-167">(32768, 0x00008000) La banque de messages prend en charge le stockage des messages au format RTF sous forme non compressée.</span><span class="sxs-lookup"><span data-stu-id="15228-167">(32768, 0x00008000) The message store supports storage of RTF messages in uncompressed form.</span></span> <span data-ttu-id="15228-168">Un flux de données au format RTF décompressé est identifié par la valeur **dwMagicUncompressedRTF** dans l’en-tête du flux.</span><span class="sxs-lookup"><span data-stu-id="15228-168">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="15228-169">La valeur **dwMagicUncompressedRTF** est définie dans le RTFLIB. Fichier H.</span><span class="sxs-lookup"><span data-stu-id="15228-169">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="15228-170">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="15228-170">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="15228-171">(262144, 0 x 00040000) Indique que la banque de messages prend en charge le stockage Unicode.</span><span class="sxs-lookup"><span data-stu-id="15228-171">(262144, 0x00040000) Indicates that the message store supports Unicode storage.</span></span> <span data-ttu-id="15228-172">Un client peut rechercher la présence de l’indicateur à décider s’il convient de demander ou d’enregistrer les informations de Unicode dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="15228-172">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span> 
    
<span data-ttu-id="15228-173">Une version au format RTF d’un message peut être stockée toujours, même si la banque de messages est non compatibles RTF.</span><span class="sxs-lookup"><span data-stu-id="15228-173">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="15228-174">Si le bit STORE_RTF_OK n’est pas défini pour un magasin particulier, un client de gestion des versions RTF doit lui-même appeler la fonction [RTFSync](rtfsync.md) pour conserver les versions **PR_BODY** et **PR_RTF_COMPRESSED** synchronisées pour le contenu de texte.</span><span class="sxs-lookup"><span data-stu-id="15228-174">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="15228-175">Format RTF est toujours stocké dans **PR_RTF_COMPRESSED**, si elle est réellement compressé ou non.</span><span class="sxs-lookup"><span data-stu-id="15228-175">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="15228-176">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="15228-176">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="15228-177">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="15228-177">Protocol specifications</span></span>

<span data-ttu-id="15228-178">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15228-178">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15228-179">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="15228-179">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="15228-180">[[MS-OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15228-180">[[MS-OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15228-181">Décrit le format des messages utilisé pour envoyer des informations relatives au partage de dossiers sur le client.</span><span class="sxs-lookup"><span data-stu-id="15228-181">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="15228-182">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="15228-182">Header files</span></span>

<span data-ttu-id="15228-183">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="15228-183">Mapidefs.h</span></span>
  
> <span data-ttu-id="15228-184">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="15228-184">Provides data type definitions.</span></span>
    
<span data-ttu-id="15228-185">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="15228-185">Mapitags.h</span></span>
  
> <span data-ttu-id="15228-186">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="15228-186">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15228-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15228-187">See also</span></span>



[<span data-ttu-id="15228-188">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="15228-188">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="15228-189">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="15228-189">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="15228-190">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="15228-190">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="15228-191">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="15228-191">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

