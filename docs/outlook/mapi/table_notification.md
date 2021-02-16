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
# <a name="table_notification"></a>TABLE_NOTIFICATION

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une ligne d’un tableau qui a été affectée par un type d’événement, tel qu’une modification ou une erreur. Une notification de tableau est alors générée. 
  
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
  
> Masque de bits d’indicateurs utilisés pour représenter le type d’événement de table. Les indicateurs suivants peuvent être définies :
    
TABLE_CHANGED 
  
> Indique à un niveau élevé que quelque chose a changé dans le tableau. L’état de la table est tel qu’il était avant l’événement. Cela signifie  que toutes les PR_INSTANCE_KEY[(PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), les signets, le positionnement actuel et les sélections de l’interface utilisateur sont toujours valides. Gérer cet événement en relisant le tableau. Les fournisseurs de services qui ne souhaitent pas implémenter de notifications de tableau enrichi envoient TABLE_CHANGED événements au lieu d’événements plus détaillés pour indiquer un type particulier de modification. 
    
TABLE_ERROR 
  
> Une erreur s’est produite, généralement pendant le traitement d’une opération asynchrone. Les erreurs lors du traitement des méthodes suivantes peuvent générer cet événement : 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md)
    
   - [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
   - [IMAPITable::Restrict](imapitable-restrict.md)
    
   Après avoir reçu un TABLE_ERROR, un client ne peut pas compter sur la précision du contenu de la table. En outre, les notifications en attente concernant d’autres modifications peuvent être perdues. La [méthode IMAPITable::GetLastError](imapitable-getlasterror.md) peut ne pas fournir d’informations supplémentaires sur l’erreur, car elle a été générée à un moment donné précédent, pas nécessairement à partir du dernier appel de méthode. 
    
TABLE_RELOAD 
  
> Les données de la table doivent être rechargées. Les fournisseurs de services TABLE_RELOAD lorsque, par exemple, les données sous-jacentes sont stockées dans une base de données et que la base de données est remplacée. Gérer cet événement en supposant que rien sur la table n’est toujours valide et en relisant le tableau. Tous les signets, les clés d’instance, les informations d’état et de positionnement ne sont pas valides.
    
TABLE_RESTRICT_DONE 
  
> Une opération de restriction initiée avec un appel de méthode **IMAPITable::Restrict** est terminée. 
    
TABLE_ROW_ADDED 
  
> Une nouvelle ligne a été ajoutée au tableau et l’objet correspondant a été enregistré. TABLE_ROW_ADDED événements sont générés après un appel à la [méthode IMAPIProp::SaveChanges.](imapiprop-savechanges.md) 
    
TABLE_ROW_DELETED 
  
> Une ligne a été supprimée du tableau. Le **membre propPrior** est définie sur NULL. 
    
TABLE_ROW_MODIFIED 
  
> Une ligne a été modifiée. Le **membre de** ligne contient les propriétés affectées de la ligne. Plusieurs TABLE_ROW_MODIFIED sont envoyés dans l’ordre dans l’affichage Tableau. 
    
  TABLE_ROW_MODIFIED événements sont envoyés une fois que les modifications apportées à l’objet correspondant ont été engagés avec un appel à la méthode **IMAPIProp::SaveChanges.** Si la ligne modifiée est maintenant la première ligne du tableau, la valeur de la balise de propriété dans le membre **propPrior** **est PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).
    
TABLE_SETCOL_DONE 
  
> Une opération de paramètre de colonne initiée avec un appel de méthode **IMAPITable::SetColumns** est terminée. 
    
TABLE_SORT_DONE 
  
> Une opération de tri de tableau initiée avec un appel de méthode **IMAPITable::SortTable** est terminée. 
    
**hResult**
  
> Valeur HRESULT de l’erreur qui s’est produite, si le membre **ulTableEvent** est TABLE_ERROR. 
    
**propIndex**
  
> [Structure SPropValue](spropvalue.md) pour la **propriété PR_INSTANCE_KEY** de la ligne concernée. 
    
**propPrior**
  
> **Structure SPropValue** pour la **propriété PR_INSTANCE_KEY** de la ligne avant la ligne concernée. Si la ligne affectée est la première ligne du tableau, **propPrior** doit être définie sur **PR_NULL** et non sur zéro. Zéro n’est pas une balise de propriété valide. 
    
**row**
  
> [Structure SRow](srow.md) décrivant la ligne concernée. Cette structure est remplie pour tous les événements de notification de tableau. Pour les événements de notification de table qui ne passent pas de données de ligne, le membre **cValues** de la structure **SRow** est définie sur zéro et le membre **lpProps** sur NULL. Étant donné que cette structure **SRow** est en lecture seule ; les clients doivent en faire une copie s’ils souhaitent apporter des modifications. La [fonction ScDupPropset peut](scduppropset.md) être utilisée pour effectuer la copie. 
    
## <a name="remarks"></a>Remarques

La **structure \_ DE NOTIFICATION** TABLE est l’un des membres de l’union des structures incluses dans le membre **d’informations** de la structure [NOTIFICATION.](notification.md) Le **membre d’informations** inclut une structure **DE \_ NOTIFICATION DE TABLE** lorsque le membre **ulEventType** de la structure est définie sur  _fnevTableModified_.
  
L’ordre et le type des colonnes dans le membre de ligne reflètent l’ordre et le type en vigueur au moment où la notification a été générée. La commande et le type au moment où la notification a été générée ne sont pas nécessairement les mêmes que lors de la livraison de la notification. 
  
Pour plus d’informations sur la notification, voir les rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d’événement dans MAPI](event-notification-in-mapi.md) <br/> |Vue d’ensemble des événements de notification et de notification.  <br/> |
|[Gestion des notifications](handling-notifications.md) <br/> |Discussion sur la façon dont les clients doivent gérer les notifications.  <br/> |
|[Prise en charge des notifications d’événement](supporting-event-notification.md) <br/> |Discussion sur la façon dont les fournisseurs de services peuvent utiliser la méthode **IMAPISupport** pour générer des notifications.  <br/> |
   
Étant donné que les notifications de tableau sont asynchrones, les clients peuvent recevoir une notification d’une ligne ajoutée après avoir appris l’ajout par le biais d’un autre moyen. Il est possible de recevoir un événement TABLE_ERROR en cas d’erreur dans une méthode **IMAPITable::Sort,** **IMAPITable::Restrict** ou **IMAPITable::SetColumns,** ou lorsqu’un processus sous-jacent tente de mettre à jour une table avec, par exemple, des lignes nouvelles ou modifiées. 
  
## <a name="see-also"></a>Voir aussi

- [Notification](notification.md) 
- [ScDupPropset](scduppropset.md)
- [SRow](srow.md)
- [SPropValue](spropvalue.md)
- [Structures MAPI](mapi-structures.md)

