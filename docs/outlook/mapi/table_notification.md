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
ms.openlocfilehash: fd77473ce728a51220a4c039f1d12d03d90e7f36
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787340"
---
# <a name="tablenotification"></a><span data-ttu-id="64781-103">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="64781-103">TABLE_NOTIFICATION</span></span>

<span data-ttu-id="64781-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="64781-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="64781-105">Décrit une ligne dans une table qui a été affectée à un type d’événement, comme une modification ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="64781-105">Describes a row in a table that has been affected by some type of event, such as a change or an error.</span></span> <span data-ttu-id="64781-106">Cela entraîne une notification de la table à générer.</span><span class="sxs-lookup"><span data-stu-id="64781-106">This causes a table notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="64781-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="64781-107">Header file:</span></span>  <br/> |<span data-ttu-id="64781-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="64781-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="64781-109">Membres</span><span class="sxs-lookup"><span data-stu-id="64781-109">Members</span></span>

<span data-ttu-id="64781-110">**ulTableEvent**</span><span class="sxs-lookup"><span data-stu-id="64781-110">**ulTableEvent**</span></span>
  
> <span data-ttu-id="64781-111">Masque de bits d’indicateurs utilisés pour représenter le type d’événement de table.</span><span class="sxs-lookup"><span data-stu-id="64781-111">Bitmask of flags used to represent the table event type.</span></span> <span data-ttu-id="64781-112">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="64781-112">The following flags can be set:</span></span>
    
<span data-ttu-id="64781-113">TABLE_CHANGED</span><span class="sxs-lookup"><span data-stu-id="64781-113">TABLE_CHANGED</span></span> 
  
> <span data-ttu-id="64781-114">Indique un haut niveau que des informations sur la table a changé.</span><span class="sxs-lookup"><span data-stu-id="64781-114">Indicates at a high level that something about the table has changed.</span></span> <span data-ttu-id="64781-115">État de la table est qu’il était avant l’événement.</span><span class="sxs-lookup"><span data-stu-id="64781-115">The table's state is as it was before the event.</span></span> <span data-ttu-id="64781-116">Cela signifie que toutes les propriétés **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), les signets, la position actuelle et les sélections pour l’interface utilisateur sont toujours valides.</span><span class="sxs-lookup"><span data-stu-id="64781-116">This means that all **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) properties, bookmarks, current positioning, and user interface selections are still valid.</span></span> <span data-ttu-id="64781-117">Gérez cet événement à relire la table.</span><span class="sxs-lookup"><span data-stu-id="64781-117">Handle this event by rereading the table.</span></span> <span data-ttu-id="64781-118">Fournisseurs de services qui ne souhaitent pas implémenter les notifications de table riche envoient les événements TABLE_CHANGED au lieu d’événements plus détaillés pour indiquer un type particulier de modification.</span><span class="sxs-lookup"><span data-stu-id="64781-118">Service providers that do not want to implement rich table notifications send TABLE_CHANGED events instead of more detailed events to indicate a particular type of change.</span></span> 
    
<span data-ttu-id="64781-119">TABLE_ERROR</span><span class="sxs-lookup"><span data-stu-id="64781-119">TABLE_ERROR</span></span> 
  
> <span data-ttu-id="64781-120">Une erreur s’est produite, généralement lors du traitement d’une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="64781-120">An error has occurred, usually during the processing of an asynchronous operation.</span></span> <span data-ttu-id="64781-121">Erreurs lors du traitement des méthodes suivantes peuvent générer cet événement :</span><span class="sxs-lookup"><span data-stu-id="64781-121">Errors during the processing of the following methods can generate this event:</span></span> 
    
   - [<span data-ttu-id="64781-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="64781-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
   - [<span data-ttu-id="64781-123">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="64781-123">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
   - [<span data-ttu-id="64781-124">IMAPITable</span><span class="sxs-lookup"><span data-stu-id="64781-124">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
   <span data-ttu-id="64781-125">Après avoir reçu un événement TABLE_ERROR, un client ne peut pas s’appuient sur l’exactitude des table des matières.</span><span class="sxs-lookup"><span data-stu-id="64781-125">After receiving a TABLE_ERROR event, a client cannot rely on the accuracy of the table contents.</span></span> <span data-ttu-id="64781-126">En outre, les notifications sur les autres modifications en attente risquent d’être perdues.</span><span class="sxs-lookup"><span data-stu-id="64781-126">Also, pending notifications about other changes might be lost.</span></span> <span data-ttu-id="64781-127">La méthode [IMAPITable::GetLastError](imapitable-getlasterror.md) ne peut pas fournir des informations supplémentaires sur l’erreur, car il a été généré à un moment donné précédent, pas nécessairement à partir du dernier appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="64781-127">The [IMAPITable::GetLastError](imapitable-getlasterror.md) method might not provide any additional information about the error because it was generated at some previous point, not necessarily from the last method call.</span></span> 
    
<span data-ttu-id="64781-128">TABLE_RELOAD</span><span class="sxs-lookup"><span data-stu-id="64781-128">TABLE_RELOAD</span></span> 
  
> <span data-ttu-id="64781-129">Les données dans le tableau doivent être rechargées.</span><span class="sxs-lookup"><span data-stu-id="64781-129">The data in the table should be reloaded.</span></span> <span data-ttu-id="64781-130">Fournisseurs de services envoient TABLE_RELOAD lorsque, par exemple, les données sous-jacentes sont stockées dans une base de données et la base de données est remplacée.</span><span class="sxs-lookup"><span data-stu-id="64781-130">Service providers send TABLE_RELOAD when, for example, the underlying data is stored in a database and the database is replaced.</span></span> <span data-ttu-id="64781-131">Gérez cet événement à en supposant qu’aucune information sur la table est toujours valide et à relire la table.</span><span class="sxs-lookup"><span data-stu-id="64781-131">Handle this event by assuming that nothing about the table is still valid and by rereading the table.</span></span> <span data-ttu-id="64781-132">Tous les signets, clés de l’instance, état et les informations de positionnement ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="64781-132">All bookmarks, instance keys, status and positioning information are invalid.</span></span>
    
<span data-ttu-id="64781-133">TABLE_RESTRICT_DONE</span><span class="sxs-lookup"><span data-stu-id="64781-133">TABLE_RESTRICT_DONE</span></span> 
  
> <span data-ttu-id="64781-134">Une opération de restriction lancée par un appel de méthode **IMAPITable** est terminée.</span><span class="sxs-lookup"><span data-stu-id="64781-134">A restriction operation initiated with an **IMAPITable::Restrict** method call has completed.</span></span> 
    
<span data-ttu-id="64781-135">TABLE_ROW_ADDED</span><span class="sxs-lookup"><span data-stu-id="64781-135">TABLE_ROW_ADDED</span></span> 
  
> <span data-ttu-id="64781-136">Une nouvelle ligne a été ajoutée à la table et l’objet correspondant est enregistré.</span><span class="sxs-lookup"><span data-stu-id="64781-136">A new row has been added to the table and the corresponding object saved.</span></span> <span data-ttu-id="64781-137">Événements TABLE_ROW_ADDED sont générés après un appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="64781-137">TABLE_ROW_ADDED events are generated after a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
<span data-ttu-id="64781-138">TABLE_ROW_DELETED</span><span class="sxs-lookup"><span data-stu-id="64781-138">TABLE_ROW_DELETED</span></span> 
  
> <span data-ttu-id="64781-139">Une ligne a été supprimée à partir de la table.</span><span class="sxs-lookup"><span data-stu-id="64781-139">A row has been removed from the table.</span></span> <span data-ttu-id="64781-140">Le membre **propPrior** est défini sur NULL.</span><span class="sxs-lookup"><span data-stu-id="64781-140">The **propPrior** member is set to NULL.</span></span> 
    
<span data-ttu-id="64781-141">TABLE_ROW_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="64781-141">TABLE_ROW_MODIFIED</span></span> 
  
> <span data-ttu-id="64781-142">Une ligne a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="64781-142">A row has been changed.</span></span> <span data-ttu-id="64781-143">Le membre de **ligne** contient les propriétés affectées pour la ligne.</span><span class="sxs-lookup"><span data-stu-id="64781-143">The **row** member contains the affected properties for the row.</span></span> <span data-ttu-id="64781-144">Plusieurs événements TABLE_ROW_MODIFIED sont envoyées dans l’ordre dans lequel ils apparaissent dans l’affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="64781-144">Multiple TABLE_ROW_MODIFIED events are sent in the order that they appear in the table view.</span></span> 
    
  <span data-ttu-id="64781-145">Événements TABLE_ROW_MODIFIED sont envoyées une fois les modifications apportées à l’objet correspondant ont été validées par un appel à la méthode **IMAPIProp::SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="64781-145">TABLE_ROW_MODIFIED events are sent after changes to the corresponding object have been committed with a call to the **IMAPIProp::SaveChanges** method.</span></span> <span data-ttu-id="64781-146">Si la ligne modifiée est désormais la première ligne dans le tableau, la valeur de la balise de propriété dans le membre **propPrior** est **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="64781-146">If the modified row is now the first row in the table, the value of the property tag in the **propPrior** member is **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
    
<span data-ttu-id="64781-147">TABLE_SETCOL_DONE</span><span class="sxs-lookup"><span data-stu-id="64781-147">TABLE_SETCOL_DONE</span></span> 
  
> <span data-ttu-id="64781-148">Une opération de définition de colonne initiée avec un appel de la méthode **IMAPITable::SetColumns** est terminée.</span><span class="sxs-lookup"><span data-stu-id="64781-148">A column setting operation initiated with an **IMAPITable::SetColumns** method call has completed.</span></span> 
    
<span data-ttu-id="64781-149">TABLE_SORT_DONE</span><span class="sxs-lookup"><span data-stu-id="64781-149">TABLE_SORT_DONE</span></span> 
  
> <span data-ttu-id="64781-150">Opération lancée par un appel de méthode **IMAPITable::SortTable** de tri d’une table est terminée.</span><span class="sxs-lookup"><span data-stu-id="64781-150">A table sorting operation initiated with an **IMAPITable::SortTable** method call has completed.</span></span> 
    
<span data-ttu-id="64781-151">**hResult**</span><span class="sxs-lookup"><span data-stu-id="64781-151">**hResult**</span></span>
  
> <span data-ttu-id="64781-152">Valeur HRESULT de l’erreur s’est produite, si le membre **ulTableEvent** est défini sur TABLE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="64781-152">HRESULT value for the error that has occurred, if the **ulTableEvent** member is set to TABLE_ERROR.</span></span> 
    
<span data-ttu-id="64781-153">**propIndex**</span><span class="sxs-lookup"><span data-stu-id="64781-153">**propIndex**</span></span>
  
> <span data-ttu-id="64781-154">Structure [SPropValue](spropvalue.md) pour la propriété **PR_INSTANCE_KEY** de la ligne concernée.</span><span class="sxs-lookup"><span data-stu-id="64781-154">[SPropValue](spropvalue.md) structure for the **PR_INSTANCE_KEY** property of the affected row.</span></span> 
    
<span data-ttu-id="64781-155">**propPrior**</span><span class="sxs-lookup"><span data-stu-id="64781-155">**propPrior**</span></span>
  
> <span data-ttu-id="64781-156">Structure **SPropValue** pour la propriété **PR_INSTANCE_KEY** de la ligne avant celle concerné.</span><span class="sxs-lookup"><span data-stu-id="64781-156">**SPropValue** structure for the **PR_INSTANCE_KEY** property of the row before the affected one.</span></span> <span data-ttu-id="64781-157">Si la ligne concernée est la première ligne dans le tableau, **propPrior** doit être définie à **PR_NULL** et non nul.</span><span class="sxs-lookup"><span data-stu-id="64781-157">If the affected row is the first row in the table, **propPrior** must be set to **PR_NULL** and not zero.</span></span> <span data-ttu-id="64781-158">Zéro n’est pas une balise de propriété valide.</span><span class="sxs-lookup"><span data-stu-id="64781-158">Zero is not a valid property tag.</span></span> 
    
<span data-ttu-id="64781-159">**ligne**</span><span class="sxs-lookup"><span data-stu-id="64781-159">**row**</span></span>
  
> <span data-ttu-id="64781-160">Structure [SRow](srow.md) décrivant la ligne concernée.</span><span class="sxs-lookup"><span data-stu-id="64781-160">[SRow](srow.md) structure describing the affected row.</span></span> <span data-ttu-id="64781-161">Cette structure est remplie pour tous les événements de notification de tableau.</span><span class="sxs-lookup"><span data-stu-id="64781-161">This structure is filled for all table notification events.</span></span> <span data-ttu-id="64781-162">Pour les événements de notification de table qui ne passent pas de données de ligne, le membre **cValues** de la structure **SRow** est défini sur zéro et le membre **lpProps** est défini sur NULL.</span><span class="sxs-lookup"><span data-stu-id="64781-162">For table notification events that do not pass row data, the **cValues** member of the **SRow** structure is set to zero and the **lpProps** member is set to NULL.</span></span> <span data-ttu-id="64781-163">Étant donné que cette structure **SRow** est en lecture seule ; les clients doivent effectuer une copie de celle-ci s’ils souhaitent apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="64781-163">Because this **SRow** structure is read-only; clients must make a copy of it if they want to make modifications.</span></span> <span data-ttu-id="64781-164">La fonction [ScDupPropset](scduppropset.md) peut être utilisée pour effectuer la copie.</span><span class="sxs-lookup"><span data-stu-id="64781-164">The [ScDupPropset](scduppropset.md) function can be used to make the copy.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="64781-165">Remarques</span><span class="sxs-lookup"><span data-stu-id="64781-165">Remarks</span></span>

<span data-ttu-id="64781-166">Le **tableau\_NOTIFICATION** structure est un des membres de l’union de structures inclus dans le membre **info** de la structure de [NOTIFICATION](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="64781-166">The **TABLE\_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="64781-167">Le membre **info** inclut un **tableau\_NOTIFICATION** structure lorsque le membre **ulEventType** de la structure est défini sur _fnevTableModified_.</span><span class="sxs-lookup"><span data-stu-id="64781-167">The **info** member includes a **TABLE\_NOTIFICATION** structure when the **ulEventType** member of the structure is set to  _fnevTableModified_.</span></span>
  
<span data-ttu-id="64781-168">L’ordre et le type des colonnes dans le membre de ligne reflètent l’ordre et le type qui était en vigueur au moment de la notification a été générée.</span><span class="sxs-lookup"><span data-stu-id="64781-168">The order and type of columns in the row member reflect the order and type that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="64781-169">L’ordre et le type au moment de la notification n’est pas nécessairement le même que lorsque la notification a été remise.</span><span class="sxs-lookup"><span data-stu-id="64781-169">The order and type at the time that the notification was generated is not necessarily the same as when the notification was delivered.</span></span> 
  
<span data-ttu-id="64781-170">Pour plus d’informations sur la notification, consultez les rubriques décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="64781-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="64781-171">**Rubrique**</span><span class="sxs-lookup"><span data-stu-id="64781-171">**Topic**</span></span>|<span data-ttu-id="64781-172">**Description**</span><span class="sxs-lookup"><span data-stu-id="64781-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="64781-173">Notification d’événement MAPI</span><span class="sxs-lookup"><span data-stu-id="64781-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="64781-174">Vue d’ensemble des notifications et les événements de notification.</span><span class="sxs-lookup"><span data-stu-id="64781-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="64781-175">Gérer les Notifications</span><span class="sxs-lookup"><span data-stu-id="64781-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="64781-176">Étude de la façon dont les clients doivent gérer les notifications.</span><span class="sxs-lookup"><span data-stu-id="64781-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="64781-177">Prise en charge de la Notification d’événement</span><span class="sxs-lookup"><span data-stu-id="64781-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="64781-178">Étude de comment les fournisseurs de services peuvent utiliser la méthode **IMAPISupport** pour générer des notifications.</span><span class="sxs-lookup"><span data-stu-id="64781-178">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
<span data-ttu-id="64781-179">Notifications de table étant asynchrones, les clients peuvent recevoir une notification d’une ligne ajoutée après en savoir plus sur l’ajout par un autre moyen.</span><span class="sxs-lookup"><span data-stu-id="64781-179">Because table notifications are asynchronous, clients can receive notification of an added row after learning about the addition through another means.</span></span> <span data-ttu-id="64781-180">Il est possible de recevoir un événement TABLE_ERROR lorsqu’il existe une erreur dans une méthode **IMAPITable::Sort**, **IMAPITable::Restrict**ou **IMAPITable::SetColumns** ou lorsque sous-jacentes d’un processus tente de mettre à jour un tableau avec, par exemple, nouvelle ou les lignes modifiées.</span><span class="sxs-lookup"><span data-stu-id="64781-180">It is possible to receive a TABLE_ERROR event when there is an error in an **IMAPITable::Sort**, **IMAPITable::Restrict**, or **IMAPITable::SetColumns** method or when an underlying process attempts to update a table with, for example, new or modified rows.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="64781-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64781-181">See also</span></span>

- [<span data-ttu-id="64781-182">Notification</span><span class="sxs-lookup"><span data-stu-id="64781-182">NOTIFICATION</span></span>](notification.md) 
- [<span data-ttu-id="64781-183">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="64781-183">ScDupPropset</span></span>](scduppropset.md)
- [<span data-ttu-id="64781-184">SRow</span><span class="sxs-lookup"><span data-stu-id="64781-184">SRow</span></span>](srow.md)
- [<span data-ttu-id="64781-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="64781-185">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="64781-186">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="64781-186">MAPI Structures</span></span>](mapi-structures.md)

