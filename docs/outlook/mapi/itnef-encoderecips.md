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
ms.openlocfilehash: 6324dcc567aee48f190f8568c6c94b5ee87c731f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584564"
---
# <a name="itnefencoderecips"></a><span data-ttu-id="6be99-103">ITnef::EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="6be99-103">ITnef::EncodeRecips</span></span>

  
  
<span data-ttu-id="6be99-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6be99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6be99-105">Encode un affichage pour la table des destinataires d’un message dans le flux de données de Transport-Neutral Encapsulation Format (TNEF) pour le message.</span><span class="sxs-lookup"><span data-stu-id="6be99-105">Encodes a view for a message's recipient table in the Transport-Neutral Encapsulation Format (TNEF) data stream for the message.</span></span>
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a><span data-ttu-id="6be99-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="6be99-106">Parameters</span></span>

 <span data-ttu-id="6be99-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6be99-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6be99-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="6be99-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="6be99-109">_lpRecipientTable_</span><span class="sxs-lookup"><span data-stu-id="6be99-109">_lpRecipientTable_</span></span>
  
> <span data-ttu-id="6be99-110">[in] Pointeur vers la table de destinataires pour lesquels l’affichage est codé.</span><span class="sxs-lookup"><span data-stu-id="6be99-110">[in] A pointer to the recipient table for which the view is encoded.</span></span> <span data-ttu-id="6be99-111">Le paramètre _lpRecipientTable_ peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="6be99-111">The  _lpRecipientTable_ parameter can be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6be99-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6be99-112">Return value</span></span>

<span data-ttu-id="6be99-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="6be99-113">S_OK</span></span> 
  
> <span data-ttu-id="6be99-114">L’appel a réussi et renvoyé la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="6be99-114">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6be99-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="6be99-115">Remarks</span></span>

<span data-ttu-id="6be99-116">Transport, fournisseurs de banque de message et passerelles appel la méthode **ITnef::EncodeRecips** pour effectuer le codage TNEF pour un affichage tableau destinataire particulier.</span><span class="sxs-lookup"><span data-stu-id="6be99-116">Transport providers, message store providers, and gateways call the **ITnef::EncodeRecips** method to perform TNEF encoding for a particular recipient table view.</span></span> <span data-ttu-id="6be99-117">Le codage TNEF est utile, par exemple, si un fournisseur ou une passerelle nécessite un ensemble de colonnes particulier, ordre de tri ou restriction pour la table de destinataires.</span><span class="sxs-lookup"><span data-stu-id="6be99-117">TNEF encoding is useful, for example, if a provider or gateway requires a particular column set, sort order, or restriction for the recipient table.</span></span> 
  
<span data-ttu-id="6be99-118">Un fournisseur ou une passerelle transmet l’affichage tableau doivent être codées dans le paramètre _lpRecipientTable_ .</span><span class="sxs-lookup"><span data-stu-id="6be99-118">A provider or gateway passes the table view to be encoded in the  _lpRecipientTable_ parameter.</span></span> <span data-ttu-id="6be99-119">L’implémentation TNEF encode la table de destinataires avec la vue spécifiée, à l’aide de la colonne donnée set, ordre de tri, les restrictions et position.</span><span class="sxs-lookup"><span data-stu-id="6be99-119">The TNEF implementation encodes the recipient table with the given view, using the given column set, sort order, restriction, and position.</span></span> <span data-ttu-id="6be99-120">Si un fournisseur ou une passerelle passe NULL _lpRecipientTable_, TNEF Obtient la table de destinataires du message encodé à l’aide de la méthode [IMessage::GetRecipientTable](imessage-getrecipienttable.md) , processus et chaque ligne du tableau dans le flux TNEF à l’aide de la paramètres actuels de la table.</span><span class="sxs-lookup"><span data-stu-id="6be99-120">If a provider or gateway passes NULL in  _lpRecipientTable_, TNEF gets the recipient table from the message being encoded by using the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, and processes every row of the table into the TNEF stream by using the table's current settings.</span></span> 
  
<span data-ttu-id="6be99-121">Appel **EncodeRecips** avec la valeur NULL dans _lpRecipientTable_ ainsi encode tous les destinataires du message et revient à appeler la méthode [ITnef::AddProps](itnef-addprops.md) avec l’indicateur TNEF_PROP_INCLUDE dans son paramètre _ulFlags_ et la **PR_ MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) propriété dans son paramètre _lpPropList_ .</span><span class="sxs-lookup"><span data-stu-id="6be99-121">Calling **EncodeRecips** with NULL in  _lpRecipientTable_ thus encodes all message recipients and is equivalent to calling the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag in its  _ulFlags_ parameter and the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in its  _lpPropList_ parameter.</span></span> 
  
<span data-ttu-id="6be99-122">Notez qu’il est rarement nécessaire d’appeler **EncodeRecips** sauf s’il existe une condition requise pour coder un affichage de tableau destinataire particulier.</span><span class="sxs-lookup"><span data-stu-id="6be99-122">Note that it is rarely necessary to call **EncodeRecips** unless there is a requirement to encode a particular recipient table view.</span></span> <span data-ttu-id="6be99-123">Systèmes de messagerie étrangers ont presque toujours des outils de gestion des listes de destinataires qui sont suffisamment puissants pour gérer les besoins courants de codage des listes de destinataires ; Par conséquent, ces systèmes nécessitent pratiquement jamais TNEF à cet effet.</span><span class="sxs-lookup"><span data-stu-id="6be99-123">Foreign messaging systems almost always have facilities for handling recipient lists that are powerful enough to handle the common needs of encoding recipient lists; therefore, these systems almost never require TNEF for this purpose.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6be99-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6be99-124">See also</span></span>



[<span data-ttu-id="6be99-125">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="6be99-125">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="6be99-126">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="6be99-126">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="6be99-127">Propriété canonique PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="6be99-127">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="6be99-128">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6be99-128">ITnef : IUnknown</span></span>](itnefiunknown.md)

