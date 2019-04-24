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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 9a77d335f3c8980de29dab6e14079c83bd711b43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349272"
---
# <a name="imessagegetattachmenttable"></a><span data-ttu-id="ce2e6-103">IMessage::GetAttachmentTable</span><span class="sxs-lookup"><span data-stu-id="ce2e6-103">IMessage::GetAttachmentTable</span></span>

  
  
<span data-ttu-id="ce2e6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce2e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce2e6-105">Renvoie la table de pièces jointes du message.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-105">Returns the message's attachment table.</span></span>
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="ce2e6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce2e6-106">Parameters</span></span>

 <span data-ttu-id="ce2e6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ce2e6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ce2e6-108">dans Masque de des indicateurs liés à la création de la table.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-108">[in] Bitmask of flags that relate to the creation of the table.</span></span> <span data-ttu-id="ce2e6-109">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="ce2e6-109">The following flag can be set:</span></span> 
    
<span data-ttu-id="ce2e6-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ce2e6-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ce2e6-111">Les colonnes de chaîne sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="ce2e6-112">Si l'indicateur MAPI_UNICODE n'est pas défini, les colonnes de la chaîne sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
<span data-ttu-id="ce2e6-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ce2e6-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ce2e6-114">Permet à **GetAttachmentTable** de retourner correctement, éventuellement avant que la table soit entièrement disponible pour le client appelant.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-114">Allows **GetAttachmentTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="ce2e6-115">Si la table n'est pas disponible, un appel ultérieur de celle-ci peut entraîner une erreur.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-115">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
 <span data-ttu-id="ce2e6-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="ce2e6-116">_lppTable_</span></span>
  
> <span data-ttu-id="ce2e6-117">remarquer Pointeur vers un pointeur vers le tableau des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-117">[out] Pointer to a pointer to the attachment table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ce2e6-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ce2e6-118">Return value</span></span>

<span data-ttu-id="ce2e6-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="ce2e6-119">S_OK</span></span> 
  
> <span data-ttu-id="ce2e6-120">La table des pièces jointes a été récupérée avec succès.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-120">The attachment table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ce2e6-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="ce2e6-121">Remarks</span></span>

<span data-ttu-id="ce2e6-122">La méthode **IMessage:: GetAttachmentTable** renvoie un pointeur vers la table de pièces jointes du message, qui inclut des informations sur toutes les pièces jointes dans le message.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-122">The **IMessage::GetAttachmentTable** method returns a pointer to the message's attachment table, which includes information about all of the attachments in the message.</span></span> <span data-ttu-id="ce2e6-123">Les clients peuvent accéder à une pièce jointe uniquement par le biais de la table des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-123">Clients can get access to an attachment only through the attachment table.</span></span> <span data-ttu-id="ce2e6-124">En récupérant le numéro d'une pièce jointe à sa propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)), un client peut utiliser plusieurs méthodes **IMessage** pour fonctionner avec la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-124">By retrieving an attachment's number its **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property a client can use several of the **IMessage** methods to work with the attachment.</span></span> 
  
<span data-ttu-id="ce2e6-125">Il y a une ligne pour chaque pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-125">There is one row for each attachment.</span></span> <span data-ttu-id="ce2e6-126">Pour obtenir la liste complète des colonnes d'un tableau de pièces jointes, consultez la rubrique [tables des pièces jointes](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="ce2e6-126">For a complete list of the columns in an attachment table, see [Attachment Tables](attachment-tables.md).</span></span>
  
<span data-ttu-id="ce2e6-127">En règle générale, une pièce jointe n'apparaît pas dans la table des pièces jointes tant que la pièce jointe et le message n'ont pas été enregistrés avec un appel à [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="ce2e6-127">An attachment usually does not appear in the attachment table until both the attachment and the message have been saved with a call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="ce2e6-128">Les tables de pièces jointes sont dynamiques.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-128">Attachment tables are dynamic.</span></span> <span data-ttu-id="ce2e6-129">Si un client crée une nouvelle pièce jointe, supprime une pièce jointe existante ou modifie une ou plusieurs propriétés une fois que les appels de **SaveChanges** ont été faits sur la pièce jointe du message, la table des pièces jointes est mise à jour pour refléter les nouvelles informations.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-129">If a client creates a new attachment, deletes an existing attachment, or changes one or more properties once the **SaveChanges** calls have been made on the attachment on the message, the attachment table will be updated to reflect the new information.</span></span> 
  
<span data-ttu-id="ce2e6-130">Certaines tables de pièces jointes prennent en charge un large éventail de restrictions; d'autres non.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-130">Some attachment tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="ce2e6-131">La prise en charge des restrictions dépend de l'implémentation du fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-131">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="ce2e6-132">Lors de l'ouverture initiale, les tables de pièces jointes ne sont pas nécessairement triées dans un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-132">When initially opened, attachment tables are not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="ce2e6-133">La définition de l'indicateur MAPI_UNICODE dans le paramètre _ulFlags_ affecte les appels suivants au tableau des pièces jointes:</span><span class="sxs-lookup"><span data-stu-id="ce2e6-133">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the attachment table:</span></span> 
  
- <span data-ttu-id="ce2e6-134">[IMAPITable:: QueryColumns](imapitable-querycolumns.md) pour récupérer le jeu de colonnes.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-134">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="ce2e6-135">[IMAPITable:: QueryRows](imapitable-queryrows.md) pour extraire des lignes.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-135">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="ce2e6-136">[IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) pour récupérer l'ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-136">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="ce2e6-137">Définition des demandes d'indicateur Unicode pour que les informations de toutes les colonnes de chaînes renvoyées à partir de ces appels soient au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-137">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="ce2e6-138">Toutefois, étant donné que tous les fournisseurs de banques de messages ne prennent pas en charge Unicode, la définition de cet indicateur n'est qu'une requête.</span><span class="sxs-lookup"><span data-stu-id="ce2e6-138">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ce2e6-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce2e6-139">See also</span></span>



[<span data-ttu-id="ce2e6-140">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="ce2e6-140">IMessage::CreateAttach</span></span>](imessage-createattach.md)
  
[<span data-ttu-id="ce2e6-141">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="ce2e6-141">IMessage::DeleteAttach</span></span>](imessage-deleteattach.md)
  
[<span data-ttu-id="ce2e6-142">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="ce2e6-142">IMessage::OpenAttach</span></span>](imessage-openattach.md)
  
[<span data-ttu-id="ce2e6-143">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ce2e6-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

