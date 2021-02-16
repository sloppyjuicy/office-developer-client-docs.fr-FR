---
title: IMsgStoreGetOutgoingQueue
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetOutgoingQueue
api_type:
- COM
ms.assetid: 8316ff89-104d-43fd-902b-476fe567e23b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8ccb732dd587b2e5107290b2db7c48e85d0145d4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434150"
---
# <a name="imsgstoregetoutgoingqueue"></a><span data-ttu-id="5048f-103">IMsgStore::GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="5048f-103">IMsgStore::GetOutgoingQueue</span></span>

  
  
<span data-ttu-id="5048f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5048f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5048f-105">Permet d’accéder à la table de files d’attente sortante, une table qui contient des informations sur tous les messages de la file d’attente sortante de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="5048f-105">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span> <span data-ttu-id="5048f-106">Cette m�thode est appel�e uniquement par le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="5048f-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="5048f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5048f-107">Parameters</span></span>

 <span data-ttu-id="5048f-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5048f-108">_ulFlags_</span></span>
  
> <span data-ttu-id="5048f-109">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="5048f-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="5048f-110">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="5048f-110">_lppTable_</span></span>
  
> <span data-ttu-id="5048f-111">[out] Pointeur vers un pointeur vers la table de file d’attente sortante.</span><span class="sxs-lookup"><span data-stu-id="5048f-111">[out] A pointer to a pointer to the outgoing queue table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5048f-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5048f-112">Return value</span></span>

<span data-ttu-id="5048f-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="5048f-113">S_OK</span></span> 
  
> <span data-ttu-id="5048f-114">La table des files d’attente sortantes a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="5048f-114">The outgoing queue table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5048f-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="5048f-115">Remarks</span></span>

<span data-ttu-id="5048f-116">La **méthode IMsgStore::GetOutgoingQueue** permet aupooler MAPI d’accéder à la table qui affiche la file d’attente des messages sortants de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="5048f-116">The **IMsgStore::GetOutgoingQueue** method provides the MAPI spooler with access to the table that shows the message store's queue of outgoing messages.</span></span> <span data-ttu-id="5048f-117">En règle générale, les messages sont placés dans la table des files d’attente sortantes après l’appel de leur méthode [IMessage::SubmitMessage.](imessage-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="5048f-117">Typically, messages are placed in the outgoing queue table after their [IMessage::SubmitMessage](imessage-submitmessage.md) method is called.</span></span> <span data-ttu-id="5048f-118">Toutefois, étant donné que l’ordre d’envoi affecte l’ordre de prétraitation et d’envoi au fournisseur de transport, certains messages marqués pour l’envoi peuvent ne pas apparaître immédiatement dans la table des files d’attente sortantes.</span><span class="sxs-lookup"><span data-stu-id="5048f-118">However, because the order of submission affects the order of preprocessing and submission to the transport provider, some messages that have been marked for sending might not appear in the outgoing queue table immediately.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5048f-119">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="5048f-119">Notes to implementers</span></span>

<span data-ttu-id="5048f-120">Pour obtenir la liste des propriétés qui doivent être incluses en tant que colonnes dans votre table de file d’attente sortante, voir Tables de files [d’attente sortantes.](outgoing-queue-tables.md)</span><span class="sxs-lookup"><span data-stu-id="5048f-120">For a list of the properties that must be included as columns in your outgoing queue table, see [Outgoing Queue Tables](outgoing-queue-tables.md).</span></span> 
  
<span data-ttu-id="5048f-121">Étant donné que lepooler MAPI est conçu pour accepter les messages provenant d’une boutique de messages dans l’ordre croissant du temps d’envoi, autorisez lepoolur MAPI à trier la table des files d’attente sortantes pour qu’elle corresponde à cet ordre ou établissez-la en tant qu’ordre de tri par défaut.</span><span class="sxs-lookup"><span data-stu-id="5048f-121">Because the MAPI spooler is designed to accept messages from a message store in ascending order of submission time, either allow the MAPI spooler to sort the outgoing queue table to match this order or establish it as the default sort order.</span></span>
  
<span data-ttu-id="5048f-122">Vous devez prendre en charge les notifications pour la table des files d’attente des messages sortants, en vous assurant que lepooler MAPI est averti lorsque le contenu de la file d’attente change.</span><span class="sxs-lookup"><span data-stu-id="5048f-122">You must support notifications for the outgoing message queue table, ensuring that the MAPI spooler is notified when the contents of the queue change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5048f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5048f-123">See also</span></span>



[<span data-ttu-id="5048f-124">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="5048f-124">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="5048f-125">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5048f-125">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

