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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 143e7f0d2cd89cd4e7956cdda05d1bd512db4027
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340970"
---
# <a name="pidtagstoresupportmask-canonical-property"></a><span data-ttu-id="5c6fb-103">Propriété canonique PidTagStoreSupportMask</span><span class="sxs-lookup"><span data-stu-id="5c6fb-103">PidTagStoreSupportMask Canonical Property</span></span>

  
  
<span data-ttu-id="5c6fb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c6fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c6fb-105">Contient un masque de réindicateur des indicateurs que les applications clientes interrogent afin de déterminer les caractéristiques d'une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-105">Contains a bitmask of flags that client applications query to determine the characteristics of a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c6fb-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5c6fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5c6fb-107">PR_STORE_SUPPORT_MASK</span><span class="sxs-lookup"><span data-stu-id="5c6fb-107">PR_STORE_SUPPORT_MASK</span></span>  <br/> |
|<span data-ttu-id="5c6fb-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5c6fb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5c6fb-109">0x340D</span><span class="sxs-lookup"><span data-stu-id="5c6fb-109">0x340D</span></span>  <br/> |
|<span data-ttu-id="5c6fb-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5c6fb-110">Data type:</span></span>  <br/> |<span data-ttu-id="5c6fb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5c6fb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5c6fb-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5c6fb-112">Area:</span></span>  <br/> |<span data-ttu-id="5c6fb-113">Divers</span><span class="sxs-lookup"><span data-stu-id="5c6fb-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c6fb-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5c6fb-114">Remarks</span></span>

<span data-ttu-id="5c6fb-115">Cette propriété permet de divulguer les fonctionnalités d'une banque de messages aux applications clientes qui envisagent de lui envoyer un message.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-115">This property discloses the capabilities of a message store to client applications that are planning to send it a message.</span></span> <span data-ttu-id="5c6fb-116">Les indicateurs peuvent prendre en charge des décisions d'un client ou d'un autre magasin, par exemple s'il faut envoyer des **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) ou seulement **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5c6fb-116">The flags can support decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="5c6fb-117">Un client ne doit jamais définir **PR_STORE_SUPPORT_MASK**; une tentative de définition de cet indicateur renvoie MAPI_E_COMPUTED.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-117">A client should never set **PR_STORE_SUPPORT_MASK**; an attempt to set this flag returns MAPI_E_COMPUTED.</span></span> 
  
<span data-ttu-id="5c6fb-118">Un ou plusieurs des indicateurs suivants peuvent être définis pour le masque de masque **PR_STORE_SUPPORT_MASK** :</span><span class="sxs-lookup"><span data-stu-id="5c6fb-118">One or more of the following flags can be set for the **PR_STORE_SUPPORT_MASK** bitmask:</span></span> 
  
<span data-ttu-id="5c6fb-119">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="5c6fb-119">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="5c6fb-120">(131072, 0x00020000) La Banque de messages prend en charge les propriétés qui contiennent des caractères ANSI (8 bits).</span><span class="sxs-lookup"><span data-stu-id="5c6fb-120">(131072, 0x00020000) The message store supports properties that contain ANSI (8-bit) characters.</span></span>
    
<span data-ttu-id="5c6fb-121">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="5c6fb-121">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="5c6fb-122">(32, 0x00000020) La Banque de messages prend en charge les pièces jointes (OLE ou non-OLE) pour les messages.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-122">(32, 0x00000020) The message store supports attachments (OLE or non-OLE) to messages.</span></span> 
    
<span data-ttu-id="5c6fb-123">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="5c6fb-123">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="5c6fb-124">(1024, 0x00000400) La Banque de messages prend en charge les vues classées des tables.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-124">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="5c6fb-125">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="5c6fb-125">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="5c6fb-126">(16, 0x00000010) La Banque de messages prend en charge la création de nouveaux messages.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-126">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="5c6fb-127">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="5c6fb-127">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="5c6fb-128">(1, 0x00000001) Les identificateurs d'entrée pour les objets dans la Banque de messages sont uniques, c'est-à-dire qu'ils ne sont jamais réutilisés pendant la durée de vie de la Banque.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-128">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="5c6fb-129">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="5c6fb-129">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="5c6fb-130">(65536, 0x00010000) La Banque de messages prend en charge les messages HTML, stockés dans la propriété **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5c6fb-130">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="5c6fb-131">Si votre environnement de développement utilise un MAPIDEFS. H qui n'inclut pas STORE_HTML_OK, utilisez la valeur 0x00010000 à la place.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-131">If your development environment uses a MAPIDEFS.H file that does not include STORE_HTML_OK, use the value 0x00010000 instead.</span></span> 
    
<span data-ttu-id="5c6fb-132">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="5c6fb-132">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="5c6fb-133">(2097152, 0x00200000) Dans une banque de fichiers PST encapsulée, indique que lorsqu'un nouveau message arrive dans la Banque, le magasin effectue les règles et le traitement du filtre de courrier indésirable sur le message séparément.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-133">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store performs rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="5c6fb-134">Le magasin appelle [IMAPISupport:: Notify](imapisupport-notify.md), en définissant **fnevNewMail** dans la structure de [notification](notification.md) qui est transmise en tant que paramètre, puis transmet les détails du nouveau message au client d'écoute.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-134">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="5c6fb-135">Par la suite, lorsque le client à l’écoute reçoit la notification, il ne traite pas de règles dans le message.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-135">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="5c6fb-136">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="5c6fb-136">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="5c6fb-137">(524288, 0x00080000) Cet indicateur est réservé et ne doit pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-137">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="5c6fb-138">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="5c6fb-138">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="5c6fb-139">(8, 0x00000008) La Banque de messages prend en charge la modification de ses messages existants.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-139">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="5c6fb-140">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="5c6fb-140">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="5c6fb-141">(512, 0x00000200) La Banque de messages prend en charge les propriétés à valeurs multiples, garantit la stabilité de l'ordre des valeurs dans une propriété à valeurs multiples pendant une opération d'enregistrement et prend en charge l'instanciation de propriétés à valeurs multiples dans des tableaux.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-141">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="5c6fb-142">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="5c6fb-142">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="5c6fb-143">(256, 0x00000100) La Banque de messages prend en charge les notifications.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-143">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="5c6fb-144">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="5c6fb-144">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="5c6fb-145">(64, 0x00000040) La Banque de messages prend en charge les pièces jointes OLE.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-145">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="5c6fb-146">Les données OLE sont accessibles via une interface **IStorage** , telle que celle disponible via la propriété **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5c6fb-146">The OLE data can be accessed through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="5c6fb-147">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="5c6fb-147">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="5c6fb-148">(16384, 0x00004000) Les dossiers de cette banque sont publics (multi-utilisateurs), et non privés (éventuellement multi-instance, pas multi-utilisateur).</span><span class="sxs-lookup"><span data-stu-id="5c6fb-148">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="5c6fb-149">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="5c6fb-149">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="5c6fb-150">(8388608, 0x00800000) Le gestionnaire de protocole MAPI n'analyse pas la Banque d'aide, et la Banque est responsable de l'envoi de toutes les modifications via les notifications à l'indexeur afin que les messages soient indexés.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-150">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible for pushing any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="5c6fb-151">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="5c6fb-151">STORE_READONLY</span></span> 
  
> <span data-ttu-id="5c6fb-152">(2, 0x00000002) Toutes les interfaces de la Banque de messages ont un niveau d'accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-152">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="5c6fb-153">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="5c6fb-153">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="5c6fb-154">(4096, 0x00001000) La Banque de messages prend en charge les restrictions.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-154">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="5c6fb-155">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="5c6fb-155">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="5c6fb-156">(2048, 0x00000800) La Banque de messages prend en charge les messages RTF (Rich Text Format), généralement compressés, et la Banque elle-même conserve la synchronisation de **PR_BODY** et de **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="5c6fb-156">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="5c6fb-157">STORE_RULES_OK</span><span class="sxs-lookup"><span data-stu-id="5c6fb-157">STORE_RULES_OK</span></span>
  
> <span data-ttu-id="5c6fb-158">(268435456, 0x10000000) Indique que les règles doivent être stockées dans ce magasin PST même si ce n'est pas la Banque par défaut.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-158">(268435456, 0x10000000) Indicates that rules should be stored in this PST store even if it is not the default store.</span></span> <span data-ttu-id="5c6fb-159">Lorsque **STORE_RULES_OK** est utilisé avec **NON_EMS_XP_SAVE**, les règles peuvent s'exécuter sur des magasins de fichiers PST non par défaut.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-159">When **STORE_RULES_OK** is used in conjunction with **NON_EMS_XP_SAVE**, rules are able to run on non-default PST wrapped stores.</span></span>
    
<span data-ttu-id="5c6fb-160">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="5c6fb-160">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="5c6fb-161">(4, 0x00000004) La Banque de messages prend en charge les dossiers de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-161">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="5c6fb-162">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="5c6fb-162">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="5c6fb-163">(8192, 0x00002000) La Banque de messages prend en charge les affichages de tri des tables.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-163">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="5c6fb-164">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="5c6fb-164">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="5c6fb-165">(128, 0x00000080) La Banque de messages prend en charge le marquage d'un message pour l'envoi.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-165">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="5c6fb-166">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="5c6fb-166">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="5c6fb-167">(32768, 0x00008000) La Banque de messages prend en charge le stockage des messages RTF sous forme non compressée.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-167">(32768, 0x00008000) The message store supports storage of RTF messages in uncompressed form.</span></span> <span data-ttu-id="5c6fb-168">Un flux de contenu RTF non compressé est identifié par la valeur **dwMagicUncompressedRTF** dans l'en-tête de flux.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-168">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="5c6fb-169">La valeur **dwMagicUncompressedRTF** est définie dans le RTFLIB. Fichier H.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-169">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="5c6fb-170">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="5c6fb-170">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="5c6fb-171">(262144, 0x00040000) Indique que la Banque de messages prend en charge le stockage Unicode.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-171">(262144, 0x00040000) Indicates that the message store supports Unicode storage.</span></span> <span data-ttu-id="5c6fb-172">Un client peut rechercher la présence de l’indicateur pour décider s’il doit demander des informations Unicode à la banque ou les y enregistrer.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-172">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span> 
    
<span data-ttu-id="5c6fb-173">Une version RTF d'un message peut toujours être stockée, même si la Banque de messages n'est pas compatible avec le format RTF.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-173">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="5c6fb-174">Si le bit STORE_RTF_OK n'est pas défini pour un magasin particulier, un client qui gère les versions RTF doit appeler la fonction [RTFSync](rtfsync.md) pour que les versions **PR_BODY** et **PR_RTF_COMPRESSED** soient synchronisées pour le contenu de texte.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-174">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="5c6fb-175">Le format RTF est toujours stocké dans **PR_RTF_COMPRESSED**, qu'il soit ou non compressé.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-175">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5c6fb-176">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="5c6fb-176">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5c6fb-177">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="5c6fb-177">Protocol specifications</span></span>

<span data-ttu-id="5c6fb-178">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c6fb-178">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c6fb-179">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-179">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5c6fb-180">[[MS-OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c6fb-180">[[MS-OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c6fb-181">Décrit le format des messages utilisés pour envoyer des informations relatives aux dossiers de partage sur le client.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-181">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5c6fb-182">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="5c6fb-182">Header files</span></span>

<span data-ttu-id="5c6fb-183">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5c6fb-183">Mapidefs.h</span></span>
  
> <span data-ttu-id="5c6fb-184">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-184">Provides data type definitions.</span></span>
    
<span data-ttu-id="5c6fb-185">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5c6fb-185">Mapitags.h</span></span>
  
> <span data-ttu-id="5c6fb-186">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="5c6fb-186">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c6fb-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c6fb-187">See also</span></span>



[<span data-ttu-id="5c6fb-188">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5c6fb-188">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5c6fb-189">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5c6fb-189">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5c6fb-190">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5c6fb-190">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5c6fb-191">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5c6fb-191">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

