---
title: IMAPITable IUnknown
description: IMAPITable IUnknown fournit une vue en lecture seule d’une table. IMAPITable est utilisé par les clients et les fournisseurs de services pour manipuler l’apparence d’une table.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable
api_type:
- COM
ms.assetid: f25be2b1-0f94-4a0c-b29d-d2201dc70ab7
ms.openlocfilehash: 70134c67e6ef4846433d0fabc1a089fbbac659dd
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827785"
---
# <a name="imapitable--iunknown"></a>IMAPITable : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit une vue en lecture seule d’une table. **IMAPITable** est utilisé par les clients et les fournisseurs de services pour manipuler l’apparence d’une table. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Objets de table  <br/> |
|Implémenté par :  <br/> |Fournisseurs de services et MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes, fournisseurs de services  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPITable  <br/> |
|Type de pointeur :  <br/> |LPMAPITABLE  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member |Description |
|:-----|:-----|
|[Getlasterror](imapitable-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) contenant des informations sur l’erreur précédente sur la table. |
|[Conseiller](imapitable-advise.md) <br/> |S’inscrit pour recevoir une notification des événements spécifiés affectant la table. |
|[Non-surveillance](imapitable-unadvise.md) <br/> |Annule l’envoi de notifications précédemment configurées avec un appel à la méthode **IMAPITable::Advise** . |
|[GetStatus](imapitable-getstatus.md) <br/> |Retourne l’état et le type de la table. |
|[SetColumns](imapitable-setcolumns.md) <br/> |Définit les propriétés particulières et l’ordre des propriétés à afficher sous forme de colonnes dans la table. |
|[QueryColumns](imapitable-querycolumns.md) <br/> |Retourne une liste de colonnes pour la table. |
|[GetRowCount](imapitable-getrowcount.md) <br/> |Retourne le nombre total de lignes dans la table. |
|[SeekRow](imapitable-seekrow.md) <br/> |Déplace le curseur vers une position spécifique dans la table. |
|[SeekRowApprox](imapitable-seekrowapprox.md) <br/> |Déplace le curseur vers une position fractionnaire approximative dans la table. |
|[QueryPosition](imapitable-queryposition.md) <br/> |Récupère la position de ligne de table actuelle du curseur, en fonction d’une valeur fractionnaire. |
|[FindRow](imapitable-findrow.md) <br/> |Recherche la ligne suivante dans un tableau qui correspond à des critères de recherche spécifiques. |
|[Restrict](imapitable-restrict.md) <br/> |Applique un filtre à une table, ce qui réduit l’ensemble de lignes aux seules lignes correspondant aux critères spécifiés. |
|[CreateBookmark](imapitable-createbookmark.md) <br/> |Marque la position actuelle de la table. |
|[FreeBookmark](imapitable-freebookmark.md) <br/> |Libère la mémoire associée à un signet. |
|[SortTable](imapitable-sorttable.md) <br/> |Commande les lignes de la table en fonction des critères de tri. |
|[QuerySortOrder](imapitable-querysortorder.md) <br/> |Récupère l’ordre de tri actuel d’une table. |
|[QueryRows](imapitable-queryrows.md) <br/> |Retourne une ou plusieurs lignes d’une table, en commençant à la position actuelle du curseur. |
|[Abandonner](imapitable-abort.md) <br/> |Arrête toutes les opérations asynchrones en cours pour la table. |
|[ExpandRow](imapitable-expandrow.md) <br/> |Développe une catégorie de table réduite, en ajoutant les lignes de feuille appartenant à la catégorie à la vue table. |
|[CollapseRow](imapitable-collapserow.md) <br/> |Réduit une catégorie de table développée, en supprimant les lignes de feuille appartenant à la catégorie de la vue table. |
|[WaitForCompletion](imapitable-waitforcompletion.md) <br/> |Suspend le traitement jusqu’à ce qu’une ou plusieurs opérations asynchrones en cours sur la table se terminent. |
|[GetCollapseState](imapitable-getcollapsestate.md) <br/> |Retourne les données nécessaires pour reconstruire l’état réduit ou développé actuel d’une table catégorisée. |
|[SetCollapseState](imapitable-setcollapsestate.md) <br/> |Reconstruit l’état actuel développé ou réduit d’une table catégorisée à l’aide de données enregistrées par un appel précédent à la méthode **IMAPITable::GetCollapseState** . |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

