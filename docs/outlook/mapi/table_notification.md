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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6c35220529fb88b470c563a0b004bfcf7e63ef76
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345646"
---
# <a name="tablenotification"></a><span data-ttu-id="68c45-103">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="68c45-103">TABLE_NOTIFICATION</span></span>

<span data-ttu-id="68c45-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68c45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68c45-105">Décrit une ligne d'un tableau qui a été affecté par un type d'événement, tel qu'une modification ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="68c45-105">Describes a row in a table that has been affected by some type of event, such as a change or an error.</span></span> <span data-ttu-id="68c45-106">Cela entraîne la génération d'une notification de table.</span><span class="sxs-lookup"><span data-stu-id="68c45-106">This causes a table notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="68c45-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="68c45-107">Header file:</span></span>  <br/> |<span data-ttu-id="68c45-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="68c45-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="68c45-109">Members</span><span class="sxs-lookup"><span data-stu-id="68c45-109">Members</span></span>

<span data-ttu-id="68c45-110">**ulTableEvent**</span><span class="sxs-lookup"><span data-stu-id="68c45-110">**ulTableEvent**</span></span>
  
> <span data-ttu-id="68c45-111">Masque de des indicateurs utilisé pour représenter le type d'événement de table.</span><span class="sxs-lookup"><span data-stu-id="68c45-111">Bitmask of flags used to represent the table event type.</span></span> <span data-ttu-id="68c45-112">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="68c45-112">The following flags can be set:</span></span>
    
<span data-ttu-id="68c45-113">TABLE_CHANGED</span><span class="sxs-lookup"><span data-stu-id="68c45-113">TABLE_CHANGED</span></span> 
  
> <span data-ttu-id="68c45-114">Indique à un niveau élevé que des informations sur la table ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="68c45-114">Indicates at a high level that something about the table has changed.</span></span> <span data-ttu-id="68c45-115">L'état du tableau est le même que celui de l'événement.</span><span class="sxs-lookup"><span data-stu-id="68c45-115">The table's state is as it was before the event.</span></span> <span data-ttu-id="68c45-116">Cela signifie que toutes les propriétés de **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), les signets, le positionnement actuel et les sélections de l'interface utilisateur sont toujours valides.</span><span class="sxs-lookup"><span data-stu-id="68c45-116">This means that all **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) properties, bookmarks, current positioning, and user interface selections are still valid.</span></span> <span data-ttu-id="68c45-117">Pour gérer cet événement, relisez le tableau.</span><span class="sxs-lookup"><span data-stu-id="68c45-117">Handle this event by rereading the table.</span></span> <span data-ttu-id="68c45-118">Les fournisseurs de services qui ne souhaitent pas implémenter les notifications de table enrichie envoient des événements TABLE_CHANGED au lieu d'événements plus détaillés pour indiquer un type particulier de modification.</span><span class="sxs-lookup"><span data-stu-id="68c45-118">Service providers that do not want to implement rich table notifications send TABLE_CHANGED events instead of more detailed events to indicate a particular type of change.</span></span> 
    
<span data-ttu-id="68c45-119">TABLE_ERROR</span><span class="sxs-lookup"><span data-stu-id="68c45-119">TABLE_ERROR</span></span> 
  
> <span data-ttu-id="68c45-120">Une erreur s'est produite, généralement lors du traitement d'une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="68c45-120">An error has occurred, usually during the processing of an asynchronous operation.</span></span> <span data-ttu-id="68c45-121">Les erreurs au cours du traitement des méthodes suivantes peuvent générer cet événement:</span><span class="sxs-lookup"><span data-stu-id="68c45-121">Errors during the processing of the following methods can generate this event:</span></span> 
    
   - [<span data-ttu-id="68c45-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="68c45-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
   - [<span data-ttu-id="68c45-123">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="68c45-123">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
   - [<span data-ttu-id="68c45-124">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="68c45-124">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
   <span data-ttu-id="68c45-125">Après la réception d'un événement TABLE_ERROR, un client ne peut pas compter sur la précision du contenu de la table.</span><span class="sxs-lookup"><span data-stu-id="68c45-125">After receiving a TABLE_ERROR event, a client cannot rely on the accuracy of the table contents.</span></span> <span data-ttu-id="68c45-126">En outre, les notifications d'autres modifications en attente peuvent être perdues.</span><span class="sxs-lookup"><span data-stu-id="68c45-126">Also, pending notifications about other changes might be lost.</span></span> <span data-ttu-id="68c45-127">La méthode [IMAPITable:: GetLastError](imapitable-getlasterror.md) peut ne pas fournir d'informations supplémentaires sur l'erreur car elle a été générée à un point antérieur, pas nécessairement depuis le dernier appel de la méthode.</span><span class="sxs-lookup"><span data-stu-id="68c45-127">The [IMAPITable::GetLastError](imapitable-getlasterror.md) method might not provide any additional information about the error because it was generated at some previous point, not necessarily from the last method call.</span></span> 
    
<span data-ttu-id="68c45-128">TABLE_RELOAD</span><span class="sxs-lookup"><span data-stu-id="68c45-128">TABLE_RELOAD</span></span> 
  
> <span data-ttu-id="68c45-129">Les données de la table doivent être rechargées.</span><span class="sxs-lookup"><span data-stu-id="68c45-129">The data in the table should be reloaded.</span></span> <span data-ttu-id="68c45-130">Les fournisseurs de services envoient TABLE_RELOAD lorsque, par exemple, les données sous-jacentes sont stockées dans une base de données et que la base de données est remplacée.</span><span class="sxs-lookup"><span data-stu-id="68c45-130">Service providers send TABLE_RELOAD when, for example, the underlying data is stored in a database and the database is replaced.</span></span> <span data-ttu-id="68c45-131">Gérez cet événement en supposant qu'aucune information relative à la table n'est encore valide et qu'elle est relues.</span><span class="sxs-lookup"><span data-stu-id="68c45-131">Handle this event by assuming that nothing about the table is still valid and by rereading the table.</span></span> <span data-ttu-id="68c45-132">Tous les signets, les clés d'instance, les informations d'État et de positionnement ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="68c45-132">All bookmarks, instance keys, status and positioning information are invalid.</span></span>
    
<span data-ttu-id="68c45-133">TABLE_RESTRICT_DONE</span><span class="sxs-lookup"><span data-stu-id="68c45-133">TABLE_RESTRICT_DONE</span></span> 
  
> <span data-ttu-id="68c45-134">Une opération de restriction lancée avec un appel de méthode **IMAPITable:: Restrict** a abouti.</span><span class="sxs-lookup"><span data-stu-id="68c45-134">A restriction operation initiated with an **IMAPITable::Restrict** method call has completed.</span></span> 
    
<span data-ttu-id="68c45-135">TABLE_ROW_ADDED</span><span class="sxs-lookup"><span data-stu-id="68c45-135">TABLE_ROW_ADDED</span></span> 
  
> <span data-ttu-id="68c45-136">Une nouvelle ligne a été ajoutée à la table et l'objet correspondant est enregistré.</span><span class="sxs-lookup"><span data-stu-id="68c45-136">A new row has been added to the table and the corresponding object saved.</span></span> <span data-ttu-id="68c45-137">Les événements TABLE_ROW_ADDED sont générés après un appel à la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="68c45-137">TABLE_ROW_ADDED events are generated after a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
<span data-ttu-id="68c45-138">TABLE_ROW_DELETED</span><span class="sxs-lookup"><span data-stu-id="68c45-138">TABLE_ROW_DELETED</span></span> 
  
> <span data-ttu-id="68c45-139">Une ligne a été supprimée du tableau.</span><span class="sxs-lookup"><span data-stu-id="68c45-139">A row has been removed from the table.</span></span> <span data-ttu-id="68c45-140">Le membre **propPrior** est défini sur null.</span><span class="sxs-lookup"><span data-stu-id="68c45-140">The **propPrior** member is set to NULL.</span></span> 
    
<span data-ttu-id="68c45-141">TABLE_ROW_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="68c45-141">TABLE_ROW_MODIFIED</span></span> 
  
> <span data-ttu-id="68c45-142">Une ligne a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="68c45-142">A row has been changed.</span></span> <span data-ttu-id="68c45-143">Le membre de **ligne** contient les propriétés affectées de la ligne.</span><span class="sxs-lookup"><span data-stu-id="68c45-143">The **row** member contains the affected properties for the row.</span></span> <span data-ttu-id="68c45-144">Plusieurs événements TABLE_ROW_MODIFIED sont envoyés dans l'ordre dans lequel ils apparaissent dans l'affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="68c45-144">Multiple TABLE_ROW_MODIFIED events are sent in the order that they appear in the table view.</span></span> 
    
  <span data-ttu-id="68c45-145">Les événements TABLE_ROW_MODIFIED sont envoyés après que les modifications apportées à l'objet correspondant ont été validées avec un appel à la méthode **IMAPIProp:: SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="68c45-145">TABLE_ROW_MODIFIED events are sent after changes to the corresponding object have been committed with a call to the **IMAPIProp::SaveChanges** method.</span></span> <span data-ttu-id="68c45-146">Si la ligne modifiée est la première ligne du tableau, la valeur de la balise property dans le membre **propPrior** est **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="68c45-146">If the modified row is now the first row in the table, the value of the property tag in the **propPrior** member is **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
    
<span data-ttu-id="68c45-147">TABLE_SETCOL_DONE</span><span class="sxs-lookup"><span data-stu-id="68c45-147">TABLE_SETCOL_DONE</span></span> 
  
> <span data-ttu-id="68c45-148">Une opération de définition de colonne a été initiée avec une méthode **IMAPITable:** l'appel de la méthode SetColumns est terminé.</span><span class="sxs-lookup"><span data-stu-id="68c45-148">A column setting operation initiated with an **IMAPITable::SetColumns** method call has completed.</span></span> 
    
<span data-ttu-id="68c45-149">TABLE_SORT_DONE</span><span class="sxs-lookup"><span data-stu-id="68c45-149">TABLE_SORT_DONE</span></span> 
  
> <span data-ttu-id="68c45-150">Une opération de tri de tableau a été lancée avec un **IMAPITable:** l'appel de méthode SortTable est terminé.</span><span class="sxs-lookup"><span data-stu-id="68c45-150">A table sorting operation initiated with an **IMAPITable::SortTable** method call has completed.</span></span> 
    
<span data-ttu-id="68c45-151">**hResult**</span><span class="sxs-lookup"><span data-stu-id="68c45-151">**hResult**</span></span>
  
> <span data-ttu-id="68c45-152">Valeur HRESULT de l'erreur qui s'est produite, si le membre **ulTableEvent** est défini sur TABLE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="68c45-152">HRESULT value for the error that has occurred, if the **ulTableEvent** member is set to TABLE_ERROR.</span></span> 
    
<span data-ttu-id="68c45-153">**propIndex**</span><span class="sxs-lookup"><span data-stu-id="68c45-153">**propIndex**</span></span>
  
> <span data-ttu-id="68c45-154">Structure [SPropValue](spropvalue.md) pour la propriété **PR_INSTANCE_KEY** de la ligne concernée.</span><span class="sxs-lookup"><span data-stu-id="68c45-154">[SPropValue](spropvalue.md) structure for the **PR_INSTANCE_KEY** property of the affected row.</span></span> 
    
<span data-ttu-id="68c45-155">**propPrior**</span><span class="sxs-lookup"><span data-stu-id="68c45-155">**propPrior**</span></span>
  
> <span data-ttu-id="68c45-156">Structure **SPropValue** pour la propriété **PR_INSTANCE_KEY** de la ligne avant la ligne concernée.</span><span class="sxs-lookup"><span data-stu-id="68c45-156">**SPropValue** structure for the **PR_INSTANCE_KEY** property of the row before the affected one.</span></span> <span data-ttu-id="68c45-157">Si la ligne concernée est la première ligne du tableau, **propPrior** doit être défini sur **PR_NULL** et non sur zéro.</span><span class="sxs-lookup"><span data-stu-id="68c45-157">If the affected row is the first row in the table, **propPrior** must be set to **PR_NULL** and not zero.</span></span> <span data-ttu-id="68c45-158">Zéro n'est pas une balise de propriété valide.</span><span class="sxs-lookup"><span data-stu-id="68c45-158">Zero is not a valid property tag.</span></span> 
    
<span data-ttu-id="68c45-159">**colonne**</span><span class="sxs-lookup"><span data-stu-id="68c45-159">**row**</span></span>
  
> <span data-ttu-id="68c45-160">Structure [SRow](srow.md) décrivant la ligne concernée.</span><span class="sxs-lookup"><span data-stu-id="68c45-160">[SRow](srow.md) structure describing the affected row.</span></span> <span data-ttu-id="68c45-161">Cette structure est remplie pour tous les événements de notification de table.</span><span class="sxs-lookup"><span data-stu-id="68c45-161">This structure is filled for all table notification events.</span></span> <span data-ttu-id="68c45-162">Pour les événements de notification de table qui ne passent pas de données de ligne, le membre **cValues** de la structure **SRow** est défini sur zéro et le membre **lpProps** est défini sur null.</span><span class="sxs-lookup"><span data-stu-id="68c45-162">For table notification events that do not pass row data, the **cValues** member of the **SRow** structure is set to zero and the **lpProps** member is set to NULL.</span></span> <span data-ttu-id="68c45-163">Étant donné que cette structure **SRow** est en lecture seule; les clients doivent en faire une copie s'ils souhaitent apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="68c45-163">Because this **SRow** structure is read-only; clients must make a copy of it if they want to make modifications.</span></span> <span data-ttu-id="68c45-164">La fonction [ScDupPropset](scduppropset.md) peut être utilisée pour effectuer la copie.</span><span class="sxs-lookup"><span data-stu-id="68c45-164">The [ScDupPropset](scduppropset.md) function can be used to make the copy.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="68c45-165">Remarques</span><span class="sxs-lookup"><span data-stu-id="68c45-165">Remarks</span></span>

<span data-ttu-id="68c45-166">La structure de **notification de\_table** est l'un des membres de l'Union des structures incluses dans le membre **info** de la structure de [notification](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="68c45-166">The **TABLE\_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="68c45-167">Le membre **info** inclut une structure de **notification de\_table** lorsque le membre **UlEventType** de la structure est défini sur _fnevTableModified_.</span><span class="sxs-lookup"><span data-stu-id="68c45-167">The **info** member includes a **TABLE\_NOTIFICATION** structure when the **ulEventType** member of the structure is set to  _fnevTableModified_.</span></span>
  
<span data-ttu-id="68c45-168">L'ordre et le type des colonnes dans le membre de ligne reflètent l'ordre et le type qui étaient appliqués lors de la génération de la notification.</span><span class="sxs-lookup"><span data-stu-id="68c45-168">The order and type of columns in the row member reflect the order and type that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="68c45-169">L'ordre et le type au moment de la génération de la notification ne sont pas nécessairement les mêmes que lors de la remise de la notification.</span><span class="sxs-lookup"><span data-stu-id="68c45-169">The order and type at the time that the notification was generated is not necessarily the same as when the notification was delivered.</span></span> 
  
<span data-ttu-id="68c45-170">Pour plus d'informations sur la notification, reportez-vous aux rubriques décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="68c45-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="68c45-171">**Rubrique**</span><span class="sxs-lookup"><span data-stu-id="68c45-171">**Topic**</span></span>|<span data-ttu-id="68c45-172">**Description**</span><span class="sxs-lookup"><span data-stu-id="68c45-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="68c45-173">Notification d'événement dans MAPI</span><span class="sxs-lookup"><span data-stu-id="68c45-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="68c45-174">Vue d'ensemble générale des événements de notification et de notification.</span><span class="sxs-lookup"><span data-stu-id="68c45-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="68c45-175">Gestion des notifications</span><span class="sxs-lookup"><span data-stu-id="68c45-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="68c45-176">Présentation de la façon dont les clients doivent gérer les notifications.</span><span class="sxs-lookup"><span data-stu-id="68c45-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="68c45-177">Notification d'événement de prise en charge</span><span class="sxs-lookup"><span data-stu-id="68c45-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="68c45-178">Présentation de la façon dont les fournisseurs de services peuvent utiliser la méthode **IMAPISupport** pour générer des notifications.</span><span class="sxs-lookup"><span data-stu-id="68c45-178">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
<span data-ttu-id="68c45-179">Étant donné que les notifications de table sont asynchrones, les clients peuvent recevoir la notification d'une ligne ajoutée après avoir appris l'ajout par le biais d'un autre moyen.</span><span class="sxs-lookup"><span data-stu-id="68c45-179">Because table notifications are asynchronous, clients can receive notification of an added row after learning about the addition through another means.</span></span> <span data-ttu-id="68c45-180">Il est possible de recevoir un événement TABLE_ERROR lorsqu'il y a une erreur dans une erreur de **type IMAPITable:: sort**, **IMAPITable:: Restrict**, ou **IMAPITable:: SetColumns** , méthode ou lorsqu'un processus sous-jacent tente de mettre à jour une table avec, par exemple, New ou lignes modifiées.</span><span class="sxs-lookup"><span data-stu-id="68c45-180">It is possible to receive a TABLE_ERROR event when there is an error in an **IMAPITable::Sort**, **IMAPITable::Restrict**, or **IMAPITable::SetColumns** method or when an underlying process attempts to update a table with, for example, new or modified rows.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="68c45-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68c45-181">See also</span></span>

- [<span data-ttu-id="68c45-182">Notification</span><span class="sxs-lookup"><span data-stu-id="68c45-182">NOTIFICATION</span></span>](notification.md) 
- [<span data-ttu-id="68c45-183">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="68c45-183">ScDupPropset</span></span>](scduppropset.md)
- [<span data-ttu-id="68c45-184">SRow</span><span class="sxs-lookup"><span data-stu-id="68c45-184">SRow</span></span>](srow.md)
- [<span data-ttu-id="68c45-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="68c45-185">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="68c45-186">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="68c45-186">MAPI Structures</span></span>](mapi-structures.md)

