---
title: TABLE_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.TABLE_NOTIFICATION
api_type:
- COM
ms.assetid: 48e478c4-6e9a-40ab-a7bb-e6219b743b08
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6c35220529fb88b470c563a0b004bfcf7e63ef76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415956"
---
# <a name="table_notification"></a><span data-ttu-id="d5c44-103">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d5c44-103">TABLE_NOTIFICATION</span></span>

<span data-ttu-id="d5c44-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5c44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5c44-105">Décrit une ligne d’un tableau qui a été affectée par un type d’événement, tel qu’une modification ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="d5c44-105">Describes a row in a table that has been affected by some type of event, such as a change or an error.</span></span> <span data-ttu-id="d5c44-106">Une notification de tableau est alors générée.</span><span class="sxs-lookup"><span data-stu-id="d5c44-106">This causes a table notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d5c44-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d5c44-107">Header file:</span></span>  <br/> |<span data-ttu-id="d5c44-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d5c44-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _TABLE_NOTIFICATION
{
  ULONG ulTableEvent;
  HRESULT hResult;
  SPropValue propIndex;
  SPropValue propPrior;
  SRow row;
} TABLE_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="d5c44-109">Members</span><span class="sxs-lookup"><span data-stu-id="d5c44-109">Members</span></span>

<span data-ttu-id="d5c44-110">**ulTableEvent**</span><span class="sxs-lookup"><span data-stu-id="d5c44-110">**ulTableEvent**</span></span>
  
> <span data-ttu-id="d5c44-111">Masque de bits d’indicateurs utilisés pour représenter le type d’événement de table.</span><span class="sxs-lookup"><span data-stu-id="d5c44-111">Bitmask of flags used to represent the table event type.</span></span> <span data-ttu-id="d5c44-112">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="d5c44-112">The following flags can be set:</span></span>
    
<span data-ttu-id="d5c44-113">TABLE_CHANGED</span><span class="sxs-lookup"><span data-stu-id="d5c44-113">TABLE_CHANGED</span></span> 
  
> <span data-ttu-id="d5c44-114">Indique à un niveau élevé que quelque chose a changé dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="d5c44-114">Indicates at a high level that something about the table has changed.</span></span> <span data-ttu-id="d5c44-115">L’état de la table est tel qu’il était avant l’événement.</span><span class="sxs-lookup"><span data-stu-id="d5c44-115">The table's state is as it was before the event.</span></span> <span data-ttu-id="d5c44-116">Cela signifie  que toutes les PR_INSTANCE_KEY[(PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), les signets, le positionnement actuel et les sélections de l’interface utilisateur sont toujours valides.</span><span class="sxs-lookup"><span data-stu-id="d5c44-116">This means that all **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) properties, bookmarks, current positioning, and user interface selections are still valid.</span></span> <span data-ttu-id="d5c44-117">Gérer cet événement en relisant le tableau.</span><span class="sxs-lookup"><span data-stu-id="d5c44-117">Handle this event by rereading the table.</span></span> <span data-ttu-id="d5c44-118">Les fournisseurs de services qui ne souhaitent pas implémenter de notifications de tableau enrichi envoient TABLE_CHANGED événements au lieu d’événements plus détaillés pour indiquer un type particulier de modification.</span><span class="sxs-lookup"><span data-stu-id="d5c44-118">Service providers that do not want to implement rich table notifications send TABLE_CHANGED events instead of more detailed events to indicate a particular type of change.</span></span> 
    
<span data-ttu-id="d5c44-119">TABLE_ERROR</span><span class="sxs-lookup"><span data-stu-id="d5c44-119">TABLE_ERROR</span></span> 
  
> <span data-ttu-id="d5c44-120">Une erreur s’est produite, généralement pendant le traitement d’une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="d5c44-120">An error has occurred, usually during the processing of an asynchronous operation.</span></span> <span data-ttu-id="d5c44-121">Les erreurs lors du traitement des méthodes suivantes peuvent générer cet événement :</span><span class="sxs-lookup"><span data-stu-id="d5c44-121">Errors during the processing of the following methods can generate this event:</span></span> 
    
   - [<span data-ttu-id="d5c44-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="d5c44-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
   - [<span data-ttu-id="d5c44-123">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="d5c44-123">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
   - [<span data-ttu-id="d5c44-124">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="d5c44-124">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
   <span data-ttu-id="d5c44-125">Après avoir reçu un TABLE_ERROR, un client ne peut pas compter sur la précision du contenu de la table.</span><span class="sxs-lookup"><span data-stu-id="d5c44-125">After receiving a TABLE_ERROR event, a client cannot rely on the accuracy of the table contents.</span></span> <span data-ttu-id="d5c44-126">En outre, les notifications en attente concernant d’autres modifications peuvent être perdues.</span><span class="sxs-lookup"><span data-stu-id="d5c44-126">Also, pending notifications about other changes might be lost.</span></span> <span data-ttu-id="d5c44-127">La [méthode IMAPITable::GetLastError](imapitable-getlasterror.md) peut ne pas fournir d’informations supplémentaires sur l’erreur, car elle a été générée à un moment donné précédent, pas nécessairement à partir du dernier appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="d5c44-127">The [IMAPITable::GetLastError](imapitable-getlasterror.md) method might not provide any additional information about the error because it was generated at some previous point, not necessarily from the last method call.</span></span> 
    
<span data-ttu-id="d5c44-128">TABLE_RELOAD</span><span class="sxs-lookup"><span data-stu-id="d5c44-128">TABLE_RELOAD</span></span> 
  
> <span data-ttu-id="d5c44-129">Les données de la table doivent être rechargées.</span><span class="sxs-lookup"><span data-stu-id="d5c44-129">The data in the table should be reloaded.</span></span> <span data-ttu-id="d5c44-130">Les fournisseurs de services TABLE_RELOAD lorsque, par exemple, les données sous-jacentes sont stockées dans une base de données et que la base de données est remplacée.</span><span class="sxs-lookup"><span data-stu-id="d5c44-130">Service providers send TABLE_RELOAD when, for example, the underlying data is stored in a database and the database is replaced.</span></span> <span data-ttu-id="d5c44-131">Gérer cet événement en supposant que rien sur la table n’est toujours valide et en relisant le tableau.</span><span class="sxs-lookup"><span data-stu-id="d5c44-131">Handle this event by assuming that nothing about the table is still valid and by rereading the table.</span></span> <span data-ttu-id="d5c44-132">Tous les signets, les clés d’instance, les informations d’état et de positionnement ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="d5c44-132">All bookmarks, instance keys, status and positioning information are invalid.</span></span>
    
<span data-ttu-id="d5c44-133">TABLE_RESTRICT_DONE</span><span class="sxs-lookup"><span data-stu-id="d5c44-133">TABLE_RESTRICT_DONE</span></span> 
  
> <span data-ttu-id="d5c44-134">Une opération de restriction initiée avec un appel de méthode **IMAPITable::Restrict** est terminée.</span><span class="sxs-lookup"><span data-stu-id="d5c44-134">A restriction operation initiated with an **IMAPITable::Restrict** method call has completed.</span></span> 
    
<span data-ttu-id="d5c44-135">TABLE_ROW_ADDED</span><span class="sxs-lookup"><span data-stu-id="d5c44-135">TABLE_ROW_ADDED</span></span> 
  
> <span data-ttu-id="d5c44-136">Une nouvelle ligne a été ajoutée au tableau et l’objet correspondant a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="d5c44-136">A new row has been added to the table and the corresponding object saved.</span></span> <span data-ttu-id="d5c44-137">TABLE_ROW_ADDED événements sont générés après un appel à la [méthode IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="d5c44-137">TABLE_ROW_ADDED events are generated after a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
<span data-ttu-id="d5c44-138">TABLE_ROW_DELETED</span><span class="sxs-lookup"><span data-stu-id="d5c44-138">TABLE_ROW_DELETED</span></span> 
  
> <span data-ttu-id="d5c44-139">Une ligne a été supprimée du tableau.</span><span class="sxs-lookup"><span data-stu-id="d5c44-139">A row has been removed from the table.</span></span> <span data-ttu-id="d5c44-140">Le **membre propPrior** est définie sur NULL.</span><span class="sxs-lookup"><span data-stu-id="d5c44-140">The **propPrior** member is set to NULL.</span></span> 
    
<span data-ttu-id="d5c44-141">TABLE_ROW_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="d5c44-141">TABLE_ROW_MODIFIED</span></span> 
  
> <span data-ttu-id="d5c44-142">Une ligne a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="d5c44-142">A row has been changed.</span></span> <span data-ttu-id="d5c44-143">Le **membre de** ligne contient les propriétés affectées de la ligne.</span><span class="sxs-lookup"><span data-stu-id="d5c44-143">The **row** member contains the affected properties for the row.</span></span> <span data-ttu-id="d5c44-144">Plusieurs TABLE_ROW_MODIFIED sont envoyés dans l’ordre dans l’affichage Tableau.</span><span class="sxs-lookup"><span data-stu-id="d5c44-144">Multiple TABLE_ROW_MODIFIED events are sent in the order that they appear in the table view.</span></span> 
    
  <span data-ttu-id="d5c44-145">TABLE_ROW_MODIFIED événements sont envoyés une fois que les modifications apportées à l’objet correspondant ont été engagés avec un appel à la méthode **IMAPIProp::SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="d5c44-145">TABLE_ROW_MODIFIED events are sent after changes to the corresponding object have been committed with a call to the **IMAPIProp::SaveChanges** method.</span></span> <span data-ttu-id="d5c44-146">Si la ligne modifiée est maintenant la première ligne du tableau, la valeur de la balise de propriété dans le membre **propPrior** **est PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d5c44-146">If the modified row is now the first row in the table, the value of the property tag in the **propPrior** member is **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
    
<span data-ttu-id="d5c44-147">TABLE_SETCOL_DONE</span><span class="sxs-lookup"><span data-stu-id="d5c44-147">TABLE_SETCOL_DONE</span></span> 
  
> <span data-ttu-id="d5c44-148">Une opération de paramètre de colonne initiée avec un appel de méthode **IMAPITable::SetColumns** est terminée.</span><span class="sxs-lookup"><span data-stu-id="d5c44-148">A column setting operation initiated with an **IMAPITable::SetColumns** method call has completed.</span></span> 
    
<span data-ttu-id="d5c44-149">TABLE_SORT_DONE</span><span class="sxs-lookup"><span data-stu-id="d5c44-149">TABLE_SORT_DONE</span></span> 
  
> <span data-ttu-id="d5c44-150">Une opération de tri de tableau initiée avec un appel de méthode **IMAPITable::SortTable** est terminée.</span><span class="sxs-lookup"><span data-stu-id="d5c44-150">A table sorting operation initiated with an **IMAPITable::SortTable** method call has completed.</span></span> 
    
<span data-ttu-id="d5c44-151">**hResult**</span><span class="sxs-lookup"><span data-stu-id="d5c44-151">**hResult**</span></span>
  
> <span data-ttu-id="d5c44-152">Valeur HRESULT de l’erreur qui s’est produite, si le membre **ulTableEvent** est TABLE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="d5c44-152">HRESULT value for the error that has occurred, if the **ulTableEvent** member is set to TABLE_ERROR.</span></span> 
    
<span data-ttu-id="d5c44-153">**propIndex**</span><span class="sxs-lookup"><span data-stu-id="d5c44-153">**propIndex**</span></span>
  
> <span data-ttu-id="d5c44-154">[Structure SPropValue](spropvalue.md) pour la **propriété PR_INSTANCE_KEY** de la ligne concernée.</span><span class="sxs-lookup"><span data-stu-id="d5c44-154">[SPropValue](spropvalue.md) structure for the **PR_INSTANCE_KEY** property of the affected row.</span></span> 
    
<span data-ttu-id="d5c44-155">**propPrior**</span><span class="sxs-lookup"><span data-stu-id="d5c44-155">**propPrior**</span></span>
  
> <span data-ttu-id="d5c44-156">**Structure SPropValue** pour la **propriété PR_INSTANCE_KEY** de la ligne avant la ligne concernée.</span><span class="sxs-lookup"><span data-stu-id="d5c44-156">**SPropValue** structure for the **PR_INSTANCE_KEY** property of the row before the affected one.</span></span> <span data-ttu-id="d5c44-157">Si la ligne affectée est la première ligne du tableau, **propPrior** doit être définie sur **PR_NULL** et non sur zéro.</span><span class="sxs-lookup"><span data-stu-id="d5c44-157">If the affected row is the first row in the table, **propPrior** must be set to **PR_NULL** and not zero.</span></span> <span data-ttu-id="d5c44-158">Zéro n’est pas une balise de propriété valide.</span><span class="sxs-lookup"><span data-stu-id="d5c44-158">Zero is not a valid property tag.</span></span> 
    
<span data-ttu-id="d5c44-159">**row**</span><span class="sxs-lookup"><span data-stu-id="d5c44-159">**row**</span></span>
  
> <span data-ttu-id="d5c44-160">[Structure SRow](srow.md) décrivant la ligne concernée.</span><span class="sxs-lookup"><span data-stu-id="d5c44-160">[SRow](srow.md) structure describing the affected row.</span></span> <span data-ttu-id="d5c44-161">Cette structure est remplie pour tous les événements de notification de tableau.</span><span class="sxs-lookup"><span data-stu-id="d5c44-161">This structure is filled for all table notification events.</span></span> <span data-ttu-id="d5c44-162">Pour les événements de notification de table qui ne passent pas de données de ligne, le membre **cValues** de la structure **SRow** est définie sur zéro et le membre **lpProps** sur NULL.</span><span class="sxs-lookup"><span data-stu-id="d5c44-162">For table notification events that do not pass row data, the **cValues** member of the **SRow** structure is set to zero and the **lpProps** member is set to NULL.</span></span> <span data-ttu-id="d5c44-163">Étant donné que cette structure **SRow** est en lecture seule ; les clients doivent en faire une copie s’ils souhaitent apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="d5c44-163">Because this **SRow** structure is read-only; clients must make a copy of it if they want to make modifications.</span></span> <span data-ttu-id="d5c44-164">La [fonction ScDupPropset peut](scduppropset.md) être utilisée pour effectuer la copie.</span><span class="sxs-lookup"><span data-stu-id="d5c44-164">The [ScDupPropset](scduppropset.md) function can be used to make the copy.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d5c44-165">Remarques</span><span class="sxs-lookup"><span data-stu-id="d5c44-165">Remarks</span></span>

<span data-ttu-id="d5c44-166">La **structure \_ DE NOTIFICATION** TABLE est l’un des membres de l’union des structures incluses dans le membre **d’informations** de la structure [NOTIFICATION.](notification.md)</span><span class="sxs-lookup"><span data-stu-id="d5c44-166">The **TABLE\_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="d5c44-167">Le **membre d’informations** inclut une structure **DE \_ NOTIFICATION DE TABLE** lorsque le membre **ulEventType** de la structure est définie sur  _fnevTableModified_.</span><span class="sxs-lookup"><span data-stu-id="d5c44-167">The **info** member includes a **TABLE\_NOTIFICATION** structure when the **ulEventType** member of the structure is set to  _fnevTableModified_.</span></span>
  
<span data-ttu-id="d5c44-168">L’ordre et le type des colonnes dans le membre de ligne reflètent l’ordre et le type en vigueur au moment où la notification a été générée.</span><span class="sxs-lookup"><span data-stu-id="d5c44-168">The order and type of columns in the row member reflect the order and type that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="d5c44-169">La commande et le type au moment où la notification a été générée ne sont pas nécessairement les mêmes que lors de la livraison de la notification.</span><span class="sxs-lookup"><span data-stu-id="d5c44-169">The order and type at the time that the notification was generated is not necessarily the same as when the notification was delivered.</span></span> 
  
<span data-ttu-id="d5c44-170">Pour plus d’informations sur la notification, voir les rubriques décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d5c44-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="d5c44-171">**Rubrique**</span><span class="sxs-lookup"><span data-stu-id="d5c44-171">**Topic**</span></span>|<span data-ttu-id="d5c44-172">**Description**</span><span class="sxs-lookup"><span data-stu-id="d5c44-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5c44-173">Notification d’événement dans MAPI</span><span class="sxs-lookup"><span data-stu-id="d5c44-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="d5c44-174">Vue d’ensemble des événements de notification et de notification.</span><span class="sxs-lookup"><span data-stu-id="d5c44-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="d5c44-175">Gestion des notifications</span><span class="sxs-lookup"><span data-stu-id="d5c44-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="d5c44-176">Discussion sur la façon dont les clients doivent gérer les notifications.</span><span class="sxs-lookup"><span data-stu-id="d5c44-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="d5c44-177">Prise en charge des notifications d’événement</span><span class="sxs-lookup"><span data-stu-id="d5c44-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="d5c44-178">Discussion sur la façon dont les fournisseurs de services peuvent utiliser la méthode **IMAPISupport** pour générer des notifications.</span><span class="sxs-lookup"><span data-stu-id="d5c44-178">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
<span data-ttu-id="d5c44-179">Étant donné que les notifications de tableau sont asynchrones, les clients peuvent recevoir une notification d’une ligne ajoutée après avoir appris l’ajout par le biais d’un autre moyen.</span><span class="sxs-lookup"><span data-stu-id="d5c44-179">Because table notifications are asynchronous, clients can receive notification of an added row after learning about the addition through another means.</span></span> <span data-ttu-id="d5c44-180">Il est possible de recevoir un événement TABLE_ERROR en cas d’erreur dans une méthode **IMAPITable::Sort,** **IMAPITable::Restrict** ou **IMAPITable::SetColumns,** ou lorsqu’un processus sous-jacent tente de mettre à jour une table avec, par exemple, des lignes nouvelles ou modifiées.</span><span class="sxs-lookup"><span data-stu-id="d5c44-180">It is possible to receive a TABLE_ERROR event when there is an error in an **IMAPITable::Sort**, **IMAPITable::Restrict**, or **IMAPITable::SetColumns** method or when an underlying process attempts to update a table with, for example, new or modified rows.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d5c44-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5c44-181">See also</span></span>

- [<span data-ttu-id="d5c44-182">Notification</span><span class="sxs-lookup"><span data-stu-id="d5c44-182">NOTIFICATION</span></span>](notification.md) 
- [<span data-ttu-id="d5c44-183">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="d5c44-183">ScDupPropset</span></span>](scduppropset.md)
- [<span data-ttu-id="d5c44-184">SRow</span><span class="sxs-lookup"><span data-stu-id="d5c44-184">SRow</span></span>](srow.md)
- [<span data-ttu-id="d5c44-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d5c44-185">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="d5c44-186">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="d5c44-186">MAPI Structures</span></span>](mapi-structures.md)

