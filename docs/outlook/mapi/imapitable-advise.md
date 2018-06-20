---
title: IMAPITableAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Advise
api_type:
- COM
ms.assetid: e8b5d21e-dc14-4b61-96b3-a51bcfa0d232
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 781146193748cdd9408a3320e90a73a070ced2af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784081"
---
# <a name="imapitableadvise"></a><span data-ttu-id="237bb-103">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="237bb-103">IMAPITable::Advise</span></span>

  
  
<span data-ttu-id="237bb-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="237bb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="237bb-105">Inscrit un objet de récepteur advise pour recevoir une notification d’événements spécifiés affectant la table.</span><span class="sxs-lookup"><span data-stu-id="237bb-105">Registers an advise sink object to receive notification of specified events affecting the table.</span></span>
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="237bb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="237bb-106">Parameters</span></span>

 <span data-ttu-id="237bb-107">_ulEventMask_</span><span class="sxs-lookup"><span data-stu-id="237bb-107">_ulEventMask_</span></span>
  
> <span data-ttu-id="237bb-108">[in] Valeur qui indique le type d’événement qui génère la notification.</span><span class="sxs-lookup"><span data-stu-id="237bb-108">[in] Value indicating the type of event that will generate the notification.</span></span> <span data-ttu-id="237bb-109">Uniquement la valeur suivante est valide :</span><span class="sxs-lookup"><span data-stu-id="237bb-109">Only the following value is valid:</span></span>
    
 `fnevTableModified`
  
 <span data-ttu-id="237bb-110">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="237bb-110">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="237bb-111">[in] Pointeur vers un objet de récepteur advise pour recevoir les notifications ultérieures.</span><span class="sxs-lookup"><span data-stu-id="237bb-111">[in] Pointer to an advise sink object to receive the subsequent notifications.</span></span> <span data-ttu-id="237bb-112">Cet objet de récepteur advise doit déjà affectée.</span><span class="sxs-lookup"><span data-stu-id="237bb-112">This advise sink object must have been already allocated.</span></span>
    
 <span data-ttu-id="237bb-113">_lpulConnection_</span><span class="sxs-lookup"><span data-stu-id="237bb-113">_lpulConnection_</span></span>
  
> <span data-ttu-id="237bb-114">[out] Pointeur vers une valeur différente de zéro qui représente l’enregistrement de notification réussie.</span><span class="sxs-lookup"><span data-stu-id="237bb-114">[out] Pointer to a nonzero value that represents the successful notification registration.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="237bb-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="237bb-115">Return value</span></span>

<span data-ttu-id="237bb-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="237bb-116">S_OK</span></span> 
  
> <span data-ttu-id="237bb-117">L’inscription de notification est terminée.</span><span class="sxs-lookup"><span data-stu-id="237bb-117">The notification registration successfully completed.</span></span>
    
<span data-ttu-id="237bb-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="237bb-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="237bb-119">L’implémentation de la table ne prend pas en charge les modifications apportées à ses lignes et colonnes ou ne prend pas en charge la notification.</span><span class="sxs-lookup"><span data-stu-id="237bb-119">The table implementation either does not support changes to its rows and columns or does not support notification.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="237bb-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="237bb-120">Remarks</span></span>

<span data-ttu-id="237bb-121">Utilisez la méthode **IMAPITable::Advise** pour inscrire un objet table implémenté dans le fournisseur pour les rappels de notification.</span><span class="sxs-lookup"><span data-stu-id="237bb-121">Use the **IMAPITable::Advise** method to register a table object implemented in the provider for notification callbacks.</span></span> <span data-ttu-id="237bb-122">Chaque fois qu’une modification est apportée à l’objet table, le fournisseur vérifie les bits de masque événement a été défini dans le paramètre _ulEventMask_ et donc le type de modification s’est produite.</span><span class="sxs-lookup"><span data-stu-id="237bb-122">Whenever a change occurs to the table object, the provider checks to see what event mask bit was set in the  _ulEventMask_ parameter and thus what type of change occurred.</span></span> <span data-ttu-id="237bb-123">Si un bit est défini, le fournisseur appelle la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour l’objet de récepteur advise indiqué par le paramètre _lpAdviseSink_ pour signaler l’événement.</span><span class="sxs-lookup"><span data-stu-id="237bb-123">If a bit is set, then the provider calls the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object indicated by the  _lpAdviseSink_ parameter to report the event.</span></span> <span data-ttu-id="237bb-124">Données transmises dans la structure de notification à la routine **OnNotify** décrivent l’événement.</span><span class="sxs-lookup"><span data-stu-id="237bb-124">Data passed in the notification structure to the **OnNotify** routine describes the event.</span></span> 
  
<span data-ttu-id="237bb-125">L’appel de **OnNotify** peut se produire lors de l’appel qui modifie l’objet, ou à tout moment suivante.</span><span class="sxs-lookup"><span data-stu-id="237bb-125">The call to **OnNotify** can occur during the call that changes the object, or at any following time.</span></span> <span data-ttu-id="237bb-126">Sur les systèmes qui prennent en charge plusieurs threads d’exécution, l’appel de **OnNotify** peut se produire sur n’importe quel thread.</span><span class="sxs-lookup"><span data-stu-id="237bb-126">On systems that support multiple threads of execution, the call to **OnNotify** can occur on any thread.</span></span> <span data-ttu-id="237bb-127">Pour activer un appel à **OnNotify** qui peut se produire à un moment peu opportuns en un seul qui est plus sûr de gérer un moyen, un fournisseur doit utiliser la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) .</span><span class="sxs-lookup"><span data-stu-id="237bb-127">For a way to turn a call to **OnNotify** that might happen at an inopportune time into one that is safer to handle, a provider should use the [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) function.</span></span> 
  
<span data-ttu-id="237bb-128">Pour fournir des notifications, le fournisseur implémentation **Advise** doit conserver une copie du pointeur pour la _lpAdviseSink_ conseille objet récepteur ; Pour ce faire, il appelle la méthode **IUnknown::AddRef** pour le récepteur de notifications maintenir son pointeur de l’objet jusqu'à ce que l’inscription aux notifications est annulée par un appel à la méthode [IMAPITable::Unadvise](imapitable-unadvise.md) .</span><span class="sxs-lookup"><span data-stu-id="237bb-128">To provide notifications, the provider implementing **Advise** needs to keep a copy of the pointer to the  _lpAdviseSink_ advise sink object; to do so, it calls the **IUnknown::AddRef** method for the advise sink to maintain its object pointer until notification registration is canceled with a call to the [IMAPITable::Unadvise](imapitable-unadvise.md) method.</span></span> <span data-ttu-id="237bb-129">L’implémentation **Advise** doit affecter un numéro de connexion à l’enregistrement de notification et appelez **AddRef** sur ce numéro de connexion avant de la retourner dans le paramètre _lpulConnection_ .</span><span class="sxs-lookup"><span data-stu-id="237bb-129">The **Advise** implementation should assign a connection number to the notification registration and call **AddRef** on this connection number before returning it in the  _lpulConnection_ parameter.</span></span> <span data-ttu-id="237bb-130">Fournisseurs de services peuvent libérer l’objet de récepteur advise avant l’enregistrement est annulée, mais ils ne doivent libérer jusqu'à ce que le numéro de connexion ** Unadvise ** a été appelée.</span><span class="sxs-lookup"><span data-stu-id="237bb-130">Service providers can release the advise sink object before the registration is canceled, but they must not release the connection number until ** Unadvise ** has been called.</span></span> 
  
<span data-ttu-id="237bb-131">Après un appel à **Advise** a réussi et avant ** Unadvise ** a été appelée, les clients doivent être préparés pour l’objet de récepteur advise doit être publié.</span><span class="sxs-lookup"><span data-stu-id="237bb-131">After a call to **Advise** has succeeded and before ** Unadvise ** has been called, clients must be prepared for the advise sink object to be released.</span></span> <span data-ttu-id="237bb-132">Un client doit donc libérer son objet de récepteur advise après **Advise** renvoie à moins qu’une utilisation à long terme spécifique pour qu’il.</span><span class="sxs-lookup"><span data-stu-id="237bb-132">A client should therefore release its advise sink object after **Advise** returns unless it has a specific long-term use for it.</span></span> 
  
<span data-ttu-id="237bb-133">En raison du comportement de notification asynchrone, implémentations de modifier les paramètres de colonne de table peuvent recevoir des notifications avec des informations organisées dans un ordre de la colonne précédente.</span><span class="sxs-lookup"><span data-stu-id="237bb-133">Because of the asynchronous behavior of notification, implementations that change table column settings can receive notifications with information organized in a previous column order.</span></span> <span data-ttu-id="237bb-134">Par exemple, une ligne de tableau peut être retournée pour un message qui vient d’être supprimé du conteneur.</span><span class="sxs-lookup"><span data-stu-id="237bb-134">For instance, a table row might be returned for a message that has just been deleted from the container.</span></span> <span data-ttu-id="237bb-135">Une notification est envoyée lorsque la colonne paramètre a été modifié et informations envoyées, mais que l’affichage de tableau de notification n’a pas été mis à jour avec ces informations encore.</span><span class="sxs-lookup"><span data-stu-id="237bb-135">Such a notification is sent when the column setting change has been made and information about it sent but the notification table view has not been updated with that information yet.</span></span>
  
<span data-ttu-id="237bb-136">Pour plus d’informations sur le processus de notification, voir [Notification d’événement MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="237bb-136">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="237bb-137">Pour obtenir des informations spécifiques sur la notification de la table, voir [Sur les Notifications de Table](about-table-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="237bb-137">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="237bb-138">Pour plus d’informations sur l’utilisation des méthodes **IMAPISupport** pour prendre en charge la notification, voir [Prise en charge de Notification d’événement](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="237bb-138">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="237bb-139">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="237bb-139">MFCMAPI reference</span></span>

<span data-ttu-id="237bb-140">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="237bb-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="237bb-141">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="237bb-141">**File**</span></span>|<span data-ttu-id="237bb-142">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="237bb-142">**Function**</span></span>|<span data-ttu-id="237bb-143">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="237bb-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="237bb-144">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="237bb-144">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="237bb-145">CContestTableListCtrl::NotificationOn</span><span class="sxs-lookup"><span data-stu-id="237bb-145">CContestTableListCtrl::NotificationOn</span></span>  <br/> |<span data-ttu-id="237bb-146">MFCMAPI utilise la méthode **IMAPITable::Advise** pour enregistrer les notifications autoriser l’affichage tableau restent en cours.</span><span class="sxs-lookup"><span data-stu-id="237bb-146">MFCMAPI uses the **IMAPITable::Advise** method to register for notifications to allow the table view to stay current.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="237bb-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="237bb-147">See also</span></span>



[<span data-ttu-id="237bb-148">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="237bb-148">HrThisThreadAdviseSink</span></span>](hrthisthreadadvisesink.md)
  
[<span data-ttu-id="237bb-149">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="237bb-149">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="237bb-150">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="237bb-150">IMAPITable::Unadvise</span></span>](imapitable-unadvise.md)
  
[<span data-ttu-id="237bb-151">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="237bb-151">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="237bb-152">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="237bb-152">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="237bb-153">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="237bb-153">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

