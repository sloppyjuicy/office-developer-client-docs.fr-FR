---
title: ITnefEncodeRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.EncodeRecips
api_type:
- COM
ms.assetid: b3ce4b0e-4f48-4a7e-a30c-c4754bccb12c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d8caa503e557d35e259db743505d39ea4809dbfd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437650"
---
# <a name="itnefencoderecips"></a><span data-ttu-id="19793-103">ITnef::EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="19793-103">ITnef::EncodeRecips</span></span>

  
  
<span data-ttu-id="19793-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19793-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19793-105">Encode une vue de la table des destinataires d’un message dans le flux de données Transport-Neutral Encapsulation Format (TNEF) du message.</span><span class="sxs-lookup"><span data-stu-id="19793-105">Encodes a view for a message's recipient table in the Transport-Neutral Encapsulation Format (TNEF) data stream for the message.</span></span>
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a><span data-ttu-id="19793-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="19793-106">Parameters</span></span>

 <span data-ttu-id="19793-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="19793-107">_ulFlags_</span></span>
  
> <span data-ttu-id="19793-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="19793-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="19793-109">_lpRecipientTable_</span><span class="sxs-lookup"><span data-stu-id="19793-109">_lpRecipientTable_</span></span>
  
> <span data-ttu-id="19793-110">[in] Pointeur vers la table des destinataires pour laquelle l’affichage est codé.</span><span class="sxs-lookup"><span data-stu-id="19793-110">[in] A pointer to the recipient table for which the view is encoded.</span></span> <span data-ttu-id="19793-111">Le  _paramètre lpRecipientTable_ peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="19793-111">The  _lpRecipientTable_ parameter can be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="19793-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="19793-112">Return value</span></span>

<span data-ttu-id="19793-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="19793-113">S_OK</span></span> 
  
> <span data-ttu-id="19793-114">L’appel a réussi et a renvoyé la ou les valeurs attendues.</span><span class="sxs-lookup"><span data-stu-id="19793-114">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="19793-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="19793-115">Remarks</span></span>

<span data-ttu-id="19793-116">Les fournisseurs de transport, les fournisseurs de magasins de messages et les passerelles appellent la méthode **ITnef::EncodeRecips** pour effectuer le codage TNEF pour un affichage de table de destinataires particulier.</span><span class="sxs-lookup"><span data-stu-id="19793-116">Transport providers, message store providers, and gateways call the **ITnef::EncodeRecips** method to perform TNEF encoding for a particular recipient table view.</span></span> <span data-ttu-id="19793-117">Le codage TNEF est utile, par exemple, si un fournisseur ou une passerelle requiert un ensemble de colonnes, un ordre de tri ou une restriction particuliers pour la table des destinataires.</span><span class="sxs-lookup"><span data-stu-id="19793-117">TNEF encoding is useful, for example, if a provider or gateway requires a particular column set, sort order, or restriction for the recipient table.</span></span> 
  
<span data-ttu-id="19793-118">Un fournisseur ou une passerelle transmet la vue de table à coder dans le paramètre _lpRecipientTable._</span><span class="sxs-lookup"><span data-stu-id="19793-118">A provider or gateway passes the table view to be encoded in the  _lpRecipientTable_ parameter.</span></span> <span data-ttu-id="19793-119">L’implémentation TNEF code la table des destinataires avec l’affichage donné, à l’aide du jeu de colonnes donné, de l’ordre de tri, de la restriction et de la position.</span><span class="sxs-lookup"><span data-stu-id="19793-119">The TNEF implementation encodes the recipient table with the given view, using the given column set, sort order, restriction, and position.</span></span> <span data-ttu-id="19793-120">Si un fournisseur ou une passerelle transmet la valeur NULL dans  _lpRecipientTable_, le TNEF obtient la table des destinataires à partir du message encodé à l’aide de la méthode [IMessage::GetRecipientTable](imessage-getrecipienttable.md) et traite chaque ligne de la table dans le flux TNEF à l’aide des paramètres actuels de la table.</span><span class="sxs-lookup"><span data-stu-id="19793-120">If a provider or gateway passes NULL in  _lpRecipientTable_, TNEF gets the recipient table from the message being encoded by using the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, and processes every row of the table into the TNEF stream by using the table's current settings.</span></span> 
  
<span data-ttu-id="19793-121">L’appel de **EncodeRecips** avec NULL dans _lpRecipientTable_ code donc tous les destinataires du message et équivaut à appeler la méthode [ITnef::AddProps](itnef-addprops.md) avec l’indicateur TNEF_PROP_INCLUDE dans son paramètre _ulFlags_ et la propriété **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) dans son paramètre _lpPropList._</span><span class="sxs-lookup"><span data-stu-id="19793-121">Calling **EncodeRecips** with NULL in  _lpRecipientTable_ thus encodes all message recipients and is equivalent to calling the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag in its  _ulFlags_ parameter and the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in its  _lpPropList_ parameter.</span></span> 
  
<span data-ttu-id="19793-122">Notez qu’il est rarement nécessaire d’appeler **EncodeRecips,** sauf s’il est nécessaire d’encoder un affichage de table de destinataires particulier.</span><span class="sxs-lookup"><span data-stu-id="19793-122">Note that it is rarely necessary to call **EncodeRecips** unless there is a requirement to encode a particular recipient table view.</span></span> <span data-ttu-id="19793-123">Les systèmes de messagerie étrangers ont presque toujours des installations pour la gestion des listes de destinataires qui sont suffisamment puissantes pour gérer les besoins courants de codage des listes de destinataires ; Par conséquent, ces systèmes ne nécessitent presque jamais le TNEF à cet effet.</span><span class="sxs-lookup"><span data-stu-id="19793-123">Foreign messaging systems almost always have facilities for handling recipient lists that are powerful enough to handle the common needs of encoding recipient lists; therefore, these systems almost never require TNEF for this purpose.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="19793-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19793-124">See also</span></span>



[<span data-ttu-id="19793-125">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="19793-125">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="19793-126">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="19793-126">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="19793-127">Propriété canonique PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="19793-127">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="19793-128">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="19793-128">ITnef : IUnknown</span></span>](itnefiunknown.md)

