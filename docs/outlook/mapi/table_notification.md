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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7f32145e0947411c48e1e6c3a941c9913a08709c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565843"
---
# <a name="tablenotification"></a>TABLE_NOTIFICATION

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décrit une ligne dans une table qui a été affectée à un type d’événement, comme une modification ou une erreur. Cela entraîne une notification de la table à générer. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
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

## <a name="members"></a>Members

**ulTableEvent**
  
> Masque de bits d’indicateurs utilisés pour représenter le type d’événement de table. Les indicateurs suivants peuvent être définis :
    
TABLE_CHANGED 
  
> Indique un haut niveau que des informations sur la table a changé. État de la table est qu’il était avant l’événement. Cela signifie que toutes les propriétés **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), les signets, la position actuelle et les sélections pour l’interface utilisateur sont toujours valides. Gérez cet événement à relire la table. Fournisseurs de services qui ne souhaitent pas implémenter les notifications de table riche envoient les événements TABLE_CHANGED au lieu d’événements plus détaillés pour indiquer un type particulier de modification. 
    
TABLE_ERROR 
  
> Une erreur s’est produite, généralement lors du traitement d’une opération asynchrone. Erreurs lors du traitement des méthodes suivantes peuvent générer cet événement : 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md)
    
   - [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
   - [IMAPITable::Restrict](imapitable-restrict.md)
    
   Après avoir reçu un événement TABLE_ERROR, un client ne peut pas s’appuient sur l’exactitude des table des matières. En outre, les notifications sur les autres modifications en attente risquent d’être perdues. La méthode [IMAPITable::GetLastError](imapitable-getlasterror.md) ne peut pas fournir des informations supplémentaires sur l’erreur, car il a été généré à un moment donné précédent, pas nécessairement à partir du dernier appel de méthode. 
    
TABLE_RELOAD 
  
> Les données dans le tableau doivent être rechargées. Fournisseurs de services envoient TABLE_RELOAD lorsque, par exemple, les données sous-jacentes sont stockées dans une base de données et la base de données est remplacée. Gérez cet événement à en supposant qu’aucune information sur la table est toujours valide et à relire la table. Tous les signets, clés de l’instance, état et les informations de positionnement ne sont pas valides.
    
TABLE_RESTRICT_DONE 
  
> Une opération de restriction lancée par un appel de méthode **IMAPITable** est terminée. 
    
TABLE_ROW_ADDED 
  
> Une nouvelle ligne a été ajoutée à la table et l’objet correspondant est enregistré. Événements TABLE_ROW_ADDED sont générés après un appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . 
    
TABLE_ROW_DELETED 
  
> Une ligne a été supprimée à partir de la table. Le membre **propPrior** est défini sur NULL. 
    
TABLE_ROW_MODIFIED 
  
> Une ligne a été modifiée. Le membre de **ligne** contient les propriétés affectées pour la ligne. Plusieurs événements TABLE_ROW_MODIFIED sont envoyées dans l’ordre dans lequel ils apparaissent dans l’affichage tableau. 
    
  Événements TABLE_ROW_MODIFIED sont envoyées une fois les modifications apportées à l’objet correspondant ont été validées par un appel à la méthode **IMAPIProp::SaveChanges** . Si la ligne modifiée est désormais la première ligne dans le tableau, la valeur de la balise de propriété dans le membre **propPrior** est **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).
    
TABLE_SETCOL_DONE 
  
> Une opération de définition de colonne initiée avec un appel de la méthode **IMAPITable::SetColumns** est terminée. 
    
TABLE_SORT_DONE 
  
> Opération lancée par un appel de méthode **IMAPITable::SortTable** de tri d’une table est terminée. 
    
**hResult**
  
> Valeur HRESULT de l’erreur s’est produite, si le membre **ulTableEvent** est défini sur TABLE_ERROR. 
    
**propIndex**
  
> Structure [SPropValue](spropvalue.md) pour la propriété **PR_INSTANCE_KEY** de la ligne concernée. 
    
**propPrior**
  
> Structure **SPropValue** pour la propriété **PR_INSTANCE_KEY** de la ligne avant celle concerné. Si la ligne concernée est la première ligne dans le tableau, **propPrior** doit être définie à **PR_NULL** et non nul. Zéro n’est pas une balise de propriété valide. 
    
**row**
  
> Structure [SRow](srow.md) décrivant la ligne concernée. Cette structure est remplie pour tous les événements de notification de tableau. Pour les événements de notification de table qui ne passent pas de données de ligne, le membre **cValues** de la structure **SRow** est défini sur zéro et le membre **lpProps** est défini sur NULL. Étant donné que cette structure **SRow** est en lecture seule ; les clients doivent effectuer une copie de celle-ci s’ils souhaitent apporter des modifications. La fonction [ScDupPropset](scduppropset.md) peut être utilisée pour effectuer la copie. 
    
## <a name="remarks"></a>Remarques

Le **tableau\_NOTIFICATION** structure est un des membres de l’union de structures inclus dans le membre **info** de la structure de [NOTIFICATION](notification.md) . Le membre **info** inclut un **tableau\_NOTIFICATION** structure lorsque le membre **ulEventType** de la structure est défini sur _fnevTableModified_.
  
L’ordre et le type des colonnes dans le membre de ligne reflètent l’ordre et le type qui était en vigueur au moment de la notification a été générée. L’ordre et le type au moment de la notification n’est pas nécessairement le même que lorsque la notification a été remise. 
  
Pour plus d’informations sur la notification, consultez les rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d’événement dans MAPI](event-notification-in-mapi.md) <br/> |Vue d’ensemble des notifications et les événements de notification.  <br/> |
|[Gestion des notifications](handling-notifications.md) <br/> |Étude de la façon dont les clients doivent gérer les notifications.  <br/> |
|[Prise en charge des notifications d’événements](supporting-event-notification.md) <br/> |Étude de comment les fournisseurs de services peuvent utiliser la méthode **IMAPISupport** pour générer des notifications.  <br/> |
   
Notifications de table étant asynchrones, les clients peuvent recevoir une notification d’une ligne ajoutée après en savoir plus sur l’ajout par un autre moyen. Il est possible de recevoir un événement TABLE_ERROR lorsqu’il existe une erreur dans une méthode **IMAPITable::Sort**, **IMAPITable::Restrict**ou **IMAPITable::SetColumns** ou lorsque sous-jacentes d’un processus tente de mettre à jour un tableau avec, par exemple, nouvelle ou les lignes modifiées. 
  
## <a name="see-also"></a>Voir aussi

- [Notification](notification.md) 
- [ScDupPropset](scduppropset.md)
- [SRow](srow.md)
- [SPropValue](spropvalue.md)
- [Structures MAPI](mapi-structures.md)

