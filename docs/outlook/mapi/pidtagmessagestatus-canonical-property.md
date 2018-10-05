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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dacd759d978394a5f4ed028915ed1c717bf6efe5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382805"
---
# <a name="pidtagmessagestatus-canonical-property"></a><span data-ttu-id="e60c3-103">Propriété canonique PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="e60c3-103">PidTagMessageStatus Canonical Property</span></span>

  
  
<span data-ttu-id="e60c3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e60c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e60c3-105">Contient un masque binaire composé de 32 bits d’indicateurs qui définit l’état d’un message dans une table des matières.</span><span class="sxs-lookup"><span data-stu-id="e60c3-105">Contains a 32-bit bitmask of flags that defines the status of a message in a contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e60c3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e60c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e60c3-107">PR_MSG_STATUS</span><span class="sxs-lookup"><span data-stu-id="e60c3-107">PR_MSG_STATUS</span></span>  <br/> |
|<span data-ttu-id="e60c3-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="e60c3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e60c3-109">0x0E17</span><span class="sxs-lookup"><span data-stu-id="e60c3-109">0x0E17</span></span>  <br/> |
|<span data-ttu-id="e60c3-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e60c3-110">Data type:</span></span>  <br/> |<span data-ttu-id="e60c3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e60c3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e60c3-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e60c3-112">Area:</span></span>  <br/> |<span data-ttu-id="e60c3-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="e60c3-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e60c3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e60c3-114">Remarks</span></span>

<span data-ttu-id="e60c3-115">Un message peut exister dans une table des matières et dans une ou plusieurs tables de résultats de recherche, et chaque instance du message peut avoir un statut différent.</span><span class="sxs-lookup"><span data-stu-id="e60c3-115">A message can exist in a contents table and in one or more search-results tables, and each instance of the message can have a different status.</span></span> <span data-ttu-id="e60c3-116">Cette propriété n’est pas une propriété d’un message, mais une colonne dans une table des matières.</span><span class="sxs-lookup"><span data-stu-id="e60c3-116">This property should not be considered a property on a message but a column in a contents table.</span></span> 
  
<span data-ttu-id="e60c3-117">Une application cliente peut définir une ou plusieurs des indicateurs suivants dans cette propriété :</span><span class="sxs-lookup"><span data-stu-id="e60c3-117">A client application can set one or more of the following flags in this property:</span></span> 
  
<span data-ttu-id="e60c3-118">MSGSTATUS_ANSWERED</span><span class="sxs-lookup"><span data-stu-id="e60c3-118">MSGSTATUS_ANSWERED</span></span> 
  
> <span data-ttu-id="e60c3-119">Le message a été répondu à.</span><span class="sxs-lookup"><span data-stu-id="e60c3-119">The message has been replied to.</span></span> 
    
<span data-ttu-id="e60c3-120">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="e60c3-120">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="e60c3-121">Le message a été marqué pour suppression suivante.</span><span class="sxs-lookup"><span data-stu-id="e60c3-121">The message has been marked for subsequent deletion.</span></span> 
    
<span data-ttu-id="e60c3-122">MSGSTATUS_DRAFT</span><span class="sxs-lookup"><span data-stu-id="e60c3-122">MSGSTATUS_DRAFT</span></span> 
  
> <span data-ttu-id="e60c3-123">Le message est dans l’état de révision de brouillon.</span><span class="sxs-lookup"><span data-stu-id="e60c3-123">The message is in draft revision status.</span></span> 
    
<span data-ttu-id="e60c3-124">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="e60c3-124">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="e60c3-125">Le message doit être supprimé de l’affiche de dossier de destinataires.</span><span class="sxs-lookup"><span data-stu-id="e60c3-125">The message is to be suppressed from recipients' folder displays.</span></span> 
    
<span data-ttu-id="e60c3-126">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="e60c3-126">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="e60c3-127">Le message doit être mis en surbrillance dans les affichages de dossier de destinataires.</span><span class="sxs-lookup"><span data-stu-id="e60c3-127">The message is to be highlighted in recipients' folder displays.</span></span> 
    
<span data-ttu-id="e60c3-128">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="e60c3-128">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="e60c3-129">Le message a été marqué pour suppression au niveau de la banque de messages à distance sans télécharger sur le client local.</span><span class="sxs-lookup"><span data-stu-id="e60c3-129">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span> 
    
<span data-ttu-id="e60c3-130">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="e60c3-130">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="e60c3-131">Le message a été marqué pour téléchargement à partir de la banque de messages à distance au client local.</span><span class="sxs-lookup"><span data-stu-id="e60c3-131">The message has been marked for downloading from the remote message store to the local client.</span></span> 
    
<span data-ttu-id="e60c3-132">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="e60c3-132">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="e60c3-133">Le message a été marqué pour un usage défini par le client.</span><span class="sxs-lookup"><span data-stu-id="e60c3-133">The message has been tagged for a client-defined purpose.</span></span>
    
<span data-ttu-id="e60c3-134">Les indicateurs **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**et **MSGSTATUS_TAGGED** sont définis par le client.</span><span class="sxs-lookup"><span data-stu-id="e60c3-134">The **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**, and **MSGSTATUS_TAGGED** flags are defined by the client.</span></span> <span data-ttu-id="e60c3-135">Fournisseurs de transport et le magasin de transmettre ces bits sans aucune action.</span><span class="sxs-lookup"><span data-stu-id="e60c3-135">Transport and store providers pass these bits without any action.</span></span> 
  
<span data-ttu-id="e60c3-136">Les clients peuvent interpréter ces valeurs en aucune manière appropriée pour leurs applications.</span><span class="sxs-lookup"><span data-stu-id="e60c3-136">Clients can interpret these values in any way that is appropriate for their applications.</span></span> <span data-ttu-id="e60c3-137">Une façon que de nombreux clients utilisent cette propriété est pour afficher les messages marqués pour la suppression d’une icône représentant.</span><span class="sxs-lookup"><span data-stu-id="e60c3-137">One way that many clients use this property is to display messages marked for deletion with a representative icon.</span></span> 
  
<span data-ttu-id="e60c3-138">Un client distant visionneuse définir **MSGSTATUS_REMOTE_DELETE** ou **MSGSTATUS_REMOTE_DOWNLOAD** sur les messages dans le dossier en-tête présenté par le fournisseur de transport à distance.</span><span class="sxs-lookup"><span data-stu-id="e60c3-138">A remote viewer client can set **MSGSTATUS_REMOTE_DELETE** or **MSGSTATUS_REMOTE_DOWNLOAD** on messages in the header folder presented to it by the remote transport provider.</span></span> <span data-ttu-id="e60c3-139">L’application cliente peut examiner chaque en-tête du message dans ce dossier pour déterminer si le message doit être téléchargé ou supprimé dans la banque de messages à distance.</span><span class="sxs-lookup"><span data-stu-id="e60c3-139">The client application can examine each message header in this folder to determine whether the message should be downloaded or deleted at the remote message store.</span></span> <span data-ttu-id="e60c3-140">Il utilise ensuite la méthode [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) pour définir l’indicateur approprié.</span><span class="sxs-lookup"><span data-stu-id="e60c3-140">It then uses the [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) method to set the appropriate flag.</span></span> <span data-ttu-id="e60c3-141">**SetMessageStatus** est la seule façon de définir des indicateurs de cette propriété ; la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) ne peut pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="e60c3-141">**SetMessageStatus** is the only way to set any of the flags in this property; the [IMAPIProp::SetProps](imapiprop-setprops.md) method cannot be used.</span></span> <span data-ttu-id="e60c3-142">Pour récupérer cette propriété, les clients appeler [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) plutôt que [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="e60c3-142">To retrieve this property, clients call [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) rather than [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
  
<span data-ttu-id="e60c3-143">Bits 16 à 31 (0 x 10000 par le biais de 0 x 80000000) de cette propriété sont disponibles pour une utilisation par l’application cliente de message interpersonnel (IPM).</span><span class="sxs-lookup"><span data-stu-id="e60c3-143">Bits 16 through 31 (0x10000 through 0x80000000) of this property are available for use by the interpersonal message (IPM) client application.</span></span> <span data-ttu-id="e60c3-144">Tous les autres bits sont réservés pour une utilisation par MAPI ; les paramètres non définis dans le tableau précédent doivent initialement définies sur zéro et ne sera pas modifiés par la suite.</span><span class="sxs-lookup"><span data-stu-id="e60c3-144">All other bits are reserved for use by MAPI; those not defined in the preceding table should be initially set to zero and not altered subsequently.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e60c3-145">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e60c3-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e60c3-146">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="e60c3-146">Protocol specifications</span></span>

<span data-ttu-id="e60c3-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e60c3-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e60c3-148">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="e60c3-148">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e60c3-149">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e60c3-149">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e60c3-150">Gère la synchronisation des données de l’objet messagerie entre un serveur et un client.</span><span class="sxs-lookup"><span data-stu-id="e60c3-150">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e60c3-151">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e60c3-151">Header files</span></span>

<span data-ttu-id="e60c3-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e60c3-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="e60c3-153">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e60c3-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="e60c3-154">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="e60c3-154">Mapitags.h</span></span>
  
> <span data-ttu-id="e60c3-155">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="e60c3-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e60c3-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e60c3-156">See also</span></span>



[<span data-ttu-id="e60c3-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="e60c3-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)


[<span data-ttu-id="e60c3-158">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e60c3-158">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e60c3-159">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e60c3-159">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e60c3-160">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e60c3-160">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e60c3-161">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e60c3-161">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

