---
title: Propriété canonique PidTagMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageStatus
api_type:
- HeaderDef
ms.assetid: e479e863-a8de-4f7e-9eae-3f721cd16e9a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: dacd759d978394a5f4ed028915ed1c717bf6efe5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355719"
---
# <a name="pidtagmessagestatus-canonical-property"></a><span data-ttu-id="bcfe9-103">Propriété canonique PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="bcfe9-103">PidTagMessageStatus Canonical Property</span></span>

  
  
<span data-ttu-id="bcfe9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcfe9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcfe9-105">Contient un masque de bits 32 bits des indicateurs qui définissent l'état d'un message dans une table des matières.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-105">Contains a 32-bit bitmask of flags that defines the status of a message in a contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bcfe9-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="bcfe9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bcfe9-107">PR_MSG_STATUS</span><span class="sxs-lookup"><span data-stu-id="bcfe9-107">PR_MSG_STATUS</span></span>  <br/> |
|<span data-ttu-id="bcfe9-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="bcfe9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bcfe9-109">0x0E17</span><span class="sxs-lookup"><span data-stu-id="bcfe9-109">0x0E17</span></span>  <br/> |
|<span data-ttu-id="bcfe9-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="bcfe9-110">Data type:</span></span>  <br/> |<span data-ttu-id="bcfe9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bcfe9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bcfe9-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="bcfe9-112">Area:</span></span>  <br/> |<span data-ttu-id="bcfe9-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="bcfe9-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bcfe9-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="bcfe9-114">Remarks</span></span>

<span data-ttu-id="bcfe9-115">Un message peut exister dans une table des matières et dans une ou plusieurs tables de résultats de recherche, et chaque instance du message peut avoir un état différent.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-115">A message can exist in a contents table and in one or more search-results tables, and each instance of the message can have a different status.</span></span> <span data-ttu-id="bcfe9-116">Cette propriété ne doit pas être considérée comme une propriété dans un message, mais une colonne dans une table de contenu.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-116">This property should not be considered a property on a message but a column in a contents table.</span></span> 
  
<span data-ttu-id="bcfe9-117">Une application cliente peut définir un ou plusieurs des indicateurs suivants dans cette propriété:</span><span class="sxs-lookup"><span data-stu-id="bcfe9-117">A client application can set one or more of the following flags in this property:</span></span> 
  
<span data-ttu-id="bcfe9-118">MSGSTATUS_ANSWERED</span><span class="sxs-lookup"><span data-stu-id="bcfe9-118">MSGSTATUS_ANSWERED</span></span> 
  
> <span data-ttu-id="bcfe9-119">Le message a été répondu à.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-119">The message has been replied to.</span></span> 
    
<span data-ttu-id="bcfe9-120">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="bcfe9-120">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="bcfe9-121">Le message a été marqué pour suppression ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-121">The message has been marked for subsequent deletion.</span></span> 
    
<span data-ttu-id="bcfe9-122">MSGSTATUS_DRAFT</span><span class="sxs-lookup"><span data-stu-id="bcfe9-122">MSGSTATUS_DRAFT</span></span> 
  
> <span data-ttu-id="bcfe9-123">Le message est à l'état de révision de brouillon.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-123">The message is in draft revision status.</span></span> 
    
<span data-ttu-id="bcfe9-124">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="bcfe9-124">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="bcfe9-125">Le message doit être supprimé des affichages des dossiers des destinataires.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-125">The message is to be suppressed from recipients' folder displays.</span></span> 
    
<span data-ttu-id="bcfe9-126">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="bcfe9-126">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="bcfe9-127">Le message doit être mis en surbrillance dans les affichages des dossiers des destinataires.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-127">The message is to be highlighted in recipients' folder displays.</span></span> 
    
<span data-ttu-id="bcfe9-128">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="bcfe9-128">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="bcfe9-129">Le message a été marqué pour suppression dans le magasin de messages distant sans téléchargement vers le client local.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-129">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span> 
    
<span data-ttu-id="bcfe9-130">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="bcfe9-130">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="bcfe9-131">Le message a été marqué pour téléchargement depuis le magasin de messages distant vers le client local.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-131">The message has been marked for downloading from the remote message store to the local client.</span></span> 
    
<span data-ttu-id="bcfe9-132">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="bcfe9-132">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="bcfe9-133">Le message a été marqué pour un objectif défini par le client.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-133">The message has been tagged for a client-defined purpose.</span></span>
    
<span data-ttu-id="bcfe9-134">Les indicateurs **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**et **MSGSTATUS_TAGGED** sont définis par le client.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-134">The **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**, and **MSGSTATUS_TAGGED** flags are defined by the client.</span></span> <span data-ttu-id="bcfe9-135">Les fournisseurs de transport et de magasin transmettent ces bits sans action.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-135">Transport and store providers pass these bits without any action.</span></span> 
  
<span data-ttu-id="bcfe9-136">Les clients peuvent interpréter ces valeurs de n'importe quelle façon appropriée pour leurs applications.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-136">Clients can interpret these values in any way that is appropriate for their applications.</span></span> <span data-ttu-id="bcfe9-137">Un grand nombre de clients utilisent cette propriété pour afficher les messages marqués pour suppression avec une icône représentant.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-137">One way that many clients use this property is to display messages marked for deletion with a representative icon.</span></span> 
  
<span data-ttu-id="bcfe9-138">Un client de visionneuse distant peut définir **MSGSTATUS_REMOTE_DELETE** ou **MSGSTATUS_REMOTE_DOWNLOAD** sur les messages dans le dossier d'en-tête qui lui est présenté par le fournisseur de transport distant.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-138">A remote viewer client can set **MSGSTATUS_REMOTE_DELETE** or **MSGSTATUS_REMOTE_DOWNLOAD** on messages in the header folder presented to it by the remote transport provider.</span></span> <span data-ttu-id="bcfe9-139">L'application cliente peut examiner chaque en-tête de message dans ce dossier pour déterminer si le message doit être téléchargé ou supprimé au niveau de la Banque de messages distante.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-139">The client application can examine each message header in this folder to determine whether the message should be downloaded or deleted at the remote message store.</span></span> <span data-ttu-id="bcfe9-140">Il utilise ensuite la méthode [IMAPIFolder:: SetMessageStatus](imapifolder-setmessagestatus.md) pour définir l'indicateur approprié.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-140">It then uses the [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) method to set the appropriate flag.</span></span> <span data-ttu-id="bcfe9-141">**SetMessageStatus** est le seul moyen de définir les indicateurs de cette propriété; la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) ne peut pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-141">**SetMessageStatus** is the only way to set any of the flags in this property; the [IMAPIProp::SetProps](imapiprop-setprops.md) method cannot be used.</span></span> <span data-ttu-id="bcfe9-142">Pour récupérer cette propriété, les clients appellent [IMAPIFolder:: GetMessageStatus](imapifolder-getmessagestatus.md) au lieu de [IMAPIProp:: GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="bcfe9-142">To retrieve this property, clients call [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) rather than [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
  
<span data-ttu-id="bcfe9-143">Les bits 16 à 31 (0x10000 à 0x80000000) de cette propriété peuvent être utilisés par l'application cliente de message interpersonnel (IPM).</span><span class="sxs-lookup"><span data-stu-id="bcfe9-143">Bits 16 through 31 (0x10000 through 0x80000000) of this property are available for use by the interpersonal message (IPM) client application.</span></span> <span data-ttu-id="bcfe9-144">Tous les autres bits sont réservés à l'usage de MAPI; ceux qui ne sont pas définis dans le tableau précédent doivent être initialement définis sur zéro et ne pas être modifiés par la suite.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-144">All other bits are reserved for use by MAPI; those not defined in the preceding table should be initially set to zero and not altered subsequently.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bcfe9-145">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="bcfe9-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bcfe9-146">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="bcfe9-146">Protocol specifications</span></span>

<span data-ttu-id="bcfe9-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bcfe9-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bcfe9-148">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-148">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bcfe9-149">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bcfe9-149">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bcfe9-150">Gère la synchronisation des données d'objet de messagerie entre un serveur et un client.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-150">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bcfe9-151">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="bcfe9-151">Header files</span></span>

<span data-ttu-id="bcfe9-152">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bcfe9-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="bcfe9-153">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="bcfe9-154">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="bcfe9-154">Mapitags.h</span></span>
  
> <span data-ttu-id="bcfe9-155">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="bcfe9-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bcfe9-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcfe9-156">See also</span></span>



[<span data-ttu-id="bcfe9-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="bcfe9-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)


[<span data-ttu-id="bcfe9-158">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="bcfe9-158">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bcfe9-159">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="bcfe9-159">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bcfe9-160">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="bcfe9-160">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bcfe9-161">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="bcfe9-161">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

