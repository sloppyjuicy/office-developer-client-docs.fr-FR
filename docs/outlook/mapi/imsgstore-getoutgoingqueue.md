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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 1b59071758aad9c71939eb9efc029005806b2a37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784255"
---
# <a name="imsgstoregetoutgoingqueue"></a><span data-ttu-id="c5c16-103">IMsgStore::GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="c5c16-103">IMsgStore::GetOutgoingQueue</span></span>

  
  
<span data-ttu-id="c5c16-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c5c16-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c5c16-105">Permet d’accéder à la table sortant de la file d’attente, une table qui comporte des informations sur tous les messages en file d’attente sortante de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="c5c16-105">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span> <span data-ttu-id="c5c16-106">Cette m�thode est appel�e uniquement par le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="c5c16-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT GetOutgoingQueue(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="c5c16-107">Param�tres</span><span class="sxs-lookup"><span data-stu-id="c5c16-107">Parameters</span></span>

 <span data-ttu-id="c5c16-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c5c16-108">_ulFlags_</span></span>
  
> <span data-ttu-id="c5c16-109">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="c5c16-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="c5c16-110">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="c5c16-110">_lppTable_</span></span>
  
> <span data-ttu-id="c5c16-111">[out] Pointeur vers un pointeur vers le tableau sortant de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="c5c16-111">[out] A pointer to a pointer to the outgoing queue table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c5c16-112">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="c5c16-112">Return value</span></span>

<span data-ttu-id="c5c16-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="c5c16-113">S_OK</span></span> 
  
> <span data-ttu-id="c5c16-114">Le tableau sortant de la file d’attente a été renvoyé avec succès.</span><span class="sxs-lookup"><span data-stu-id="c5c16-114">The outgoing queue table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c5c16-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="c5c16-115">Remarks</span></span>

<span data-ttu-id="c5c16-116">La méthode **IMsgStore::GetOutgoingQueue** fournit le spouleur MAPI d’accéder à la table qui affiche la file d’attente de la banque de messages de messages sortants.</span><span class="sxs-lookup"><span data-stu-id="c5c16-116">The **IMsgStore::GetOutgoingQueue** method provides the MAPI spooler with access to the table that shows the message store's queue of outgoing messages.</span></span> <span data-ttu-id="c5c16-117">En règle générale, les messages sont placés dans le tableau de file d’attente sortant après que leur méthode [IMessage::SubmitMessage](imessage-submitmessage.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="c5c16-117">Typically, messages are placed in the outgoing queue table after their [IMessage::SubmitMessage](imessage-submitmessage.md) method is called.</span></span> <span data-ttu-id="c5c16-118">Toutefois, étant donné que l’ordre de soumission affecte l’ordre d’envoi pour le fournisseur de transport et de prétraitement, certains messages qui ont été marquées pour l’envoi n’apparaîtront dans la table de file d’attente sortant immédiatement.</span><span class="sxs-lookup"><span data-stu-id="c5c16-118">However, because the order of submission affects the order of preprocessing and submission to the transport provider, some messages that have been marked for sending might not appear in the outgoing queue table immediately.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c5c16-119">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="c5c16-119">Notes to implementers</span></span>

<span data-ttu-id="c5c16-120">Pour obtenir la liste des propriétés qui doit être inclus en tant que colonnes dans votre tableau de file d’attente sortant, voir [Les Tables de file d’attente sortante](outgoing-queue-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c5c16-120">For a list of the properties that must be included as columns in your outgoing queue table, see [Outgoing Queue Tables](outgoing-queue-tables.md).</span></span> 
  
<span data-ttu-id="c5c16-121">Étant donné que le spouleur MAPI est conçu pour accepter les messages provenant d’une banque de messages dans l’ordre croissant de l’heure d’envoi, soit autoriser le spouleur MAPI trier le tableau sortant de la file d’attente pour correspondre à cette commande ou comme l’ordre de tri par défaut.</span><span class="sxs-lookup"><span data-stu-id="c5c16-121">Because the MAPI spooler is designed to accept messages from a message store in ascending order of submission time, either allow the MAPI spooler to sort the outgoing queue table to match this order or establish it as the default sort order.</span></span>
  
<span data-ttu-id="c5c16-122">À prendre en charge les notifications de la table de file d’attente de messages sortants, en vous assurant que le spouleur MAPI est averti lorsque le contenu de la file d’attente change.</span><span class="sxs-lookup"><span data-stu-id="c5c16-122">You must support notifications for the outgoing message queue table, ensuring that the MAPI spooler is notified when the contents of the queue change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c5c16-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5c16-123">See also</span></span>



[<span data-ttu-id="c5c16-124">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="c5c16-124">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="c5c16-125">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c5c16-125">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

