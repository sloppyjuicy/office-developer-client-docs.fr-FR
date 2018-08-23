---
title: IMessageGetAttachmentTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetAttachmentTable
api_type:
- COM
ms.assetid: e568917e-6085-4094-8728-89ba90a78c40
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bf100ed916080a91366062f45b9e3349516bdb98
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588516"
---
# <a name="imessagegetattachmenttable"></a><span data-ttu-id="d1245-103">IMessage::GetAttachmentTable</span><span class="sxs-lookup"><span data-stu-id="d1245-103">IMessage::GetAttachmentTable</span></span>

  
  
<span data-ttu-id="d1245-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1245-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1245-105">Renvoie un tableau de pièce jointe du message.</span><span class="sxs-lookup"><span data-stu-id="d1245-105">Returns the message's attachment table.</span></span>
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="d1245-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="d1245-106">Parameters</span></span>

 <span data-ttu-id="d1245-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d1245-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d1245-108">[in] Masque de bits d’indicateurs qui sont associées à la création de la table.</span><span class="sxs-lookup"><span data-stu-id="d1245-108">[in] Bitmask of flags that relate to the creation of the table.</span></span> <span data-ttu-id="d1245-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="d1245-109">The following flag can be set:</span></span> 
    
<span data-ttu-id="d1245-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d1245-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d1245-111">Les colonnes de type chaîne sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="d1245-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="d1245-112">Si l’indicateur MAPI_UNICODE n’est pas définie, les colonnes de type chaîne sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="d1245-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
<span data-ttu-id="d1245-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d1245-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="d1245-114">Permet de **GetAttachmentTable** renvoyer avec succès, éventuellement, avant de la table est totalement disponible au client appelant.</span><span class="sxs-lookup"><span data-stu-id="d1245-114">Allows **GetAttachmentTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="d1245-115">Si le tableau n’est pas disponible, vous appelez suivante lui peut provoquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="d1245-115">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
 <span data-ttu-id="d1245-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="d1245-116">_lppTable_</span></span>
  
> <span data-ttu-id="d1245-117">[out] Pointeur vers un pointeur vers la table des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="d1245-117">[out] Pointer to a pointer to the attachment table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d1245-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="d1245-118">Return value</span></span>

<span data-ttu-id="d1245-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="d1245-119">S_OK</span></span> 
  
> <span data-ttu-id="d1245-120">Le tableau de pièce jointe a été récupéré correctement.</span><span class="sxs-lookup"><span data-stu-id="d1245-120">The attachment table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d1245-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="d1245-121">Remarks</span></span>

<span data-ttu-id="d1245-122">La méthode **IMessage::GetAttachmentTable** retourne un pointeur vers la table de pièce jointe du message, qui consacrée des informations sur toutes les pièces jointes dans le message.</span><span class="sxs-lookup"><span data-stu-id="d1245-122">The **IMessage::GetAttachmentTable** method returns a pointer to the message's attachment table, which includes information about all of the attachments in the message.</span></span> <span data-ttu-id="d1245-123">Les clients peuvent accéder à une pièce jointe uniquement par le biais de la table des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="d1245-123">Clients can get access to an attachment only through the attachment table.</span></span> <span data-ttu-id="d1245-124">En récupérant le numéro d’une pièce jointe sa propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) un client peut utiliser plusieurs méthodes **IMessage** pour fonctionner avec la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="d1245-124">By retrieving an attachment's number its **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property a client can use several of the **IMessage** methods to work with the attachment.</span></span> 
  
<span data-ttu-id="d1245-125">Il existe une ligne pour chaque pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="d1245-125">There is one row for each attachment.</span></span> <span data-ttu-id="d1245-126">Pour obtenir une liste complète des colonnes dans une table des pièces jointes, voir les [Tables des pièces jointes](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="d1245-126">For a complete list of the columns in an attachment table, see [Attachment Tables](attachment-tables.md).</span></span>
  
<span data-ttu-id="d1245-127">Une pièce jointe n’apparaît généralement pas dans la table des pièces jointes jusqu'à ce que la pièce jointe et le message ont été enregistrés avec un appel à [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="d1245-127">An attachment usually does not appear in the attachment table until both the attachment and the message have been saved with a call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="d1245-128">Tables des pièces jointes sont dynamiques.</span><span class="sxs-lookup"><span data-stu-id="d1245-128">Attachment tables are dynamic.</span></span> <span data-ttu-id="d1245-129">Si un client crée une pièce jointe, supprime une pièce jointe existante ou modifie une ou plusieurs propriétés une fois que les appels **SaveChanges** ont été apportées sur la pièce jointe du message, la table des pièces jointes système mis à jour pour refléter les nouvelles informations.</span><span class="sxs-lookup"><span data-stu-id="d1245-129">If a client creates a new attachment, deletes an existing attachment, or changes one or more properties once the **SaveChanges** calls have been made on the attachment on the message, the attachment table will be updated to reflect the new information.</span></span> 
  
<span data-ttu-id="d1245-130">Certaines tables des pièces jointes prend en charge une grande variété de restrictions ; d’autres ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="d1245-130">Some attachment tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="d1245-131">Prise en charge des restrictions dépend de l’implémentation du fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="d1245-131">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="d1245-132">Ouverture à l’origine, tables des pièces jointes ne sont pas nécessairement triées selon un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="d1245-132">When initially opened, attachment tables are not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="d1245-133">Définition de l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte les appels suivants de la table des pièces jointes :</span><span class="sxs-lookup"><span data-stu-id="d1245-133">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the attachment table:</span></span> 
  
- <span data-ttu-id="d1245-134">[IMAPITable::QueryColumns](imapitable-querycolumns.md) pour extraire l’ensemble de colonnes.</span><span class="sxs-lookup"><span data-stu-id="d1245-134">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="d1245-135">[IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer des lignes.</span><span class="sxs-lookup"><span data-stu-id="d1245-135">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="d1245-136">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) pour récupérer l’ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="d1245-136">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="d1245-137">Si les demandes d’indicateur Unicode que les informations des colonnes de la chaîne retournée par ces appels au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="d1245-137">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="d1245-138">Toutefois, étant donné que tous les fournisseurs de banque de messages prennent en charge Unicode, définition de cet indicateur est uniquement une demande.</span><span class="sxs-lookup"><span data-stu-id="d1245-138">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d1245-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1245-139">See also</span></span>



[<span data-ttu-id="d1245-140">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="d1245-140">IMessage::CreateAttach</span></span>](imessage-createattach.md)
  
[<span data-ttu-id="d1245-141">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="d1245-141">IMessage::DeleteAttach</span></span>](imessage-deleteattach.md)
  
[<span data-ttu-id="d1245-142">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="d1245-142">IMessage::OpenAttach</span></span>](imessage-openattach.md)
  
[<span data-ttu-id="d1245-143">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d1245-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

