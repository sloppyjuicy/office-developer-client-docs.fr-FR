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
# <a name="tablenotification"></a>TABLE_NOTIFICATION

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une ligne d'un tableau qui a été affecté par un type d'événement, tel qu'une modification ou une erreur. Cela entraîne la génération d'une notification de table. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
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
  
> Masque de des indicateurs utilisé pour représenter le type d'événement de table. Les indicateurs suivants peuvent être définis:
    
TABLE_CHANGED 
  
> Indique à un niveau élevé que des informations sur la table ont été modifiées. L'état du tableau est le même que celui de l'événement. Cela signifie que toutes les propriétés de **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), les signets, le positionnement actuel et les sélections de l'interface utilisateur sont toujours valides. Pour gérer cet événement, relisez le tableau. Les fournisseurs de services qui ne souhaitent pas implémenter les notifications de table enrichie envoient des événements TABLE_CHANGED au lieu d'événements plus détaillés pour indiquer un type particulier de modification. 
    
TABLE_ERROR 
  
> Une erreur s'est produite, généralement lors du traitement d'une opération asynchrone. Les erreurs au cours du traitement des méthodes suivantes peuvent générer cet événement: 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md)
    
   - [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
   - [IMAPITable::Restrict](imapitable-restrict.md)
    
   Après la réception d'un événement TABLE_ERROR, un client ne peut pas compter sur la précision du contenu de la table. En outre, les notifications d'autres modifications en attente peuvent être perdues. La méthode [IMAPITable:: GetLastError](imapitable-getlasterror.md) peut ne pas fournir d'informations supplémentaires sur l'erreur car elle a été générée à un point antérieur, pas nécessairement depuis le dernier appel de la méthode. 
    
TABLE_RELOAD 
  
> Les données de la table doivent être rechargées. Les fournisseurs de services envoient TABLE_RELOAD lorsque, par exemple, les données sous-jacentes sont stockées dans une base de données et que la base de données est remplacée. Gérez cet événement en supposant qu'aucune information relative à la table n'est encore valide et qu'elle est relues. Tous les signets, les clés d'instance, les informations d'État et de positionnement ne sont pas valides.
    
TABLE_RESTRICT_DONE 
  
> Une opération de restriction lancée avec un appel de méthode **IMAPITable:: Restrict** a abouti. 
    
TABLE_ROW_ADDED 
  
> Une nouvelle ligne a été ajoutée à la table et l'objet correspondant est enregistré. Les événements TABLE_ROW_ADDED sont générés après un appel à la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . 
    
TABLE_ROW_DELETED 
  
> Une ligne a été supprimée du tableau. Le membre **propPrior** est défini sur null. 
    
TABLE_ROW_MODIFIED 
  
> Une ligne a été modifiée. Le membre de **ligne** contient les propriétés affectées de la ligne. Plusieurs événements TABLE_ROW_MODIFIED sont envoyés dans l'ordre dans lequel ils apparaissent dans l'affichage tableau. 
    
  Les événements TABLE_ROW_MODIFIED sont envoyés après que les modifications apportées à l'objet correspondant ont été validées avec un appel à la méthode **IMAPIProp:: SaveChanges** . Si la ligne modifiée est la première ligne du tableau, la valeur de la balise property dans le membre **propPrior** est **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).
    
TABLE_SETCOL_DONE 
  
> Une opération de définition de colonne a été initiée avec une méthode **IMAPITable:** l'appel de la méthode SetColumns est terminé. 
    
TABLE_SORT_DONE 
  
> Une opération de tri de tableau a été lancée avec un **IMAPITable:** l'appel de méthode SortTable est terminé. 
    
**hResult**
  
> Valeur HRESULT de l'erreur qui s'est produite, si le membre **ulTableEvent** est défini sur TABLE_ERROR. 
    
**propIndex**
  
> Structure [SPropValue](spropvalue.md) pour la propriété **PR_INSTANCE_KEY** de la ligne concernée. 
    
**propPrior**
  
> Structure **SPropValue** pour la propriété **PR_INSTANCE_KEY** de la ligne avant la ligne concernée. Si la ligne concernée est la première ligne du tableau, **propPrior** doit être défini sur **PR_NULL** et non sur zéro. Zéro n'est pas une balise de propriété valide. 
    
**colonne**
  
> Structure [SRow](srow.md) décrivant la ligne concernée. Cette structure est remplie pour tous les événements de notification de table. Pour les événements de notification de table qui ne passent pas de données de ligne, le membre **cValues** de la structure **SRow** est défini sur zéro et le membre **lpProps** est défini sur null. Étant donné que cette structure **SRow** est en lecture seule; les clients doivent en faire une copie s'ils souhaitent apporter des modifications. La fonction [ScDupPropset](scduppropset.md) peut être utilisée pour effectuer la copie. 
    
## <a name="remarks"></a>Remarques

La structure de **notification de\_table** est l'un des membres de l'Union des structures incluses dans le membre **info** de la structure de [notification](notification.md) . Le membre **info** inclut une structure de **notification de\_table** lorsque le membre **UlEventType** de la structure est défini sur _fnevTableModified_.
  
L'ordre et le type des colonnes dans le membre de ligne reflètent l'ordre et le type qui étaient appliqués lors de la génération de la notification. L'ordre et le type au moment de la génération de la notification ne sont pas nécessairement les mêmes que lors de la remise de la notification. 
  
Pour plus d'informations sur la notification, reportez-vous aux rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d'événement dans MAPI](event-notification-in-mapi.md) <br/> |Vue d'ensemble générale des événements de notification et de notification.  <br/> |
|[Gestion des notifications](handling-notifications.md) <br/> |Présentation de la façon dont les clients doivent gérer les notifications.  <br/> |
|[Notification d'événement de prise en charge](supporting-event-notification.md) <br/> |Présentation de la façon dont les fournisseurs de services peuvent utiliser la méthode **IMAPISupport** pour générer des notifications.  <br/> |
   
Étant donné que les notifications de table sont asynchrones, les clients peuvent recevoir la notification d'une ligne ajoutée après avoir appris l'ajout par le biais d'un autre moyen. Il est possible de recevoir un événement TABLE_ERROR lorsqu'il y a une erreur dans une erreur de **type IMAPITable:: sort**, **IMAPITable:: Restrict**, ou **IMAPITable:: SetColumns** , méthode ou lorsqu'un processus sous-jacent tente de mettre à jour une table avec, par exemple, New ou lignes modifiées. 
  
## <a name="see-also"></a>Voir aussi

- [Notification](notification.md) 
- [ScDupPropset](scduppropset.md)
- [SRow](srow.md)
- [SPropValue](spropvalue.md)
- [Structures MAPI](mapi-structures.md)

