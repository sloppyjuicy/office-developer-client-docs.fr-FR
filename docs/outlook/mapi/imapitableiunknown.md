---
title: IMAPITable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable
api_type:
- COM
ms.assetid: f25be2b1-0f94-4a0c-b29d-d2201dc70ab7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a5504711bdeac4ef94cbe47395ceb8163b60ad68
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584330"
---
# <a name="imapitable--iunknown"></a>IMAPITable : IUnknown

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Fournit une vue en lecture seule d’une table. **IMAPITable** est utilisée par les clients et les fournisseurs de services pour manipuler l’apparence d’un tableau. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposés par :  <br/> |Objets table  <br/> |
|Implémentée par :  <br/> |Fournisseurs de services et MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes, les fournisseurs de services  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPITable  <br/> |
|Type de pointeur :  <br/> |LPMAPITABLE  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[GetLastError](imapitable-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) contenant des informations sur l’erreur précédente dans le tableau.  <br/> |
|[Conseiller](imapitable-advise.md) <br/> |Enregistre pour recevoir une notification d’événements spécifiés affectant la table.  <br/> |
|[L’avertissement](imapitable-unadvise.md) <br/> |Annule l’envoi de notifications précédemment configurées avec un appel à la méthode **IMAPITable::Advise** .  <br/> |
|[GetStatus](imapitable-getstatus.md) <br/> |Renvoie l’état et le type de la table.  <br/> |
|[SetColumns](imapitable-setcolumns.md) <br/> |Définit les propriétés et l’ordre des propriétés apparaissent sous forme de colonnes dans le tableau.  <br/> |
|[QueryColumns](imapitable-querycolumns.md) <br/> |Renvoie une liste de colonnes pour la table.  <br/> |
|[GetRowCount](imapitable-getrowcount.md) <br/> |Renvoie le nombre total de lignes dans le tableau.  <br/> |
|[SeekRow](imapitable-seekrow.md) <br/> |Déplace le curseur à un emplacement spécifique dans le tableau.  <br/> |
|[SeekRowApprox](imapitable-seekrowapprox.md) <br/> |Déplace le curseur à une position en fraction approximative dans le tableau.  <br/> |
|[QueryPosition](imapitable-queryposition.md) <br/> |Extrait la position de ligne de tableau en cours du curseur, basée sur une valeur décimale.  <br/> |
|[FindRow](imapitable-findrow.md) <br/> |Trouve la ligne suivante dans une table qui répond aux critères de recherche spécifiques.  <br/> |
|[Restrict](imapitable-restrict.md) <br/> |Applique un filtre à une table, réduisant la ligne valeur uniquement les lignes correspondant aux critères spécifiés.  <br/> |
|[CreateBookmark](imapitable-createbookmark.md) <br/> |Marque la position actuelle de la table.  <br/> |
|[FreeBookmark](imapitable-freebookmark.md) <br/> |Libère la mémoire associée à un signet.  <br/> |
|[SortTable](imapitable-sorttable.md) <br/> |Trie les lignes de la table en fonction des critères de tri.  <br/> |
|[QuerySortOrder](imapitable-querysortorder.md) <br/> |Récupère l’ordre de tri en cours pour une table.  <br/> |
|[QueryRows](imapitable-queryrows.md) <br/> |Renvoie une ou plusieurs lignes d’une table, en commençant à l’emplacement du curseur.  <br/> |
|[Abandonner](imapitable-abort.md) <br/> |Arrête toutes les opérations asynchrones en cours pour la table.  <br/> |
|[ExpandRow](imapitable-expandrow.md) <br/> |Développe une catégorie de table réduite, ajouter les lignes de feuilles appartenant à la catégorie à l’affichage tableau.  <br/> |
|[CollapseRow](imapitable-collapserow.md) <br/> |Réduire une catégorie de table étendue, suppression des lignes feuille appartenant à la catégorie à partir de l’affichage tableau.  <br/> |
|[WaitForCompletion](imapitable-waitforcompletion.md) <br/> |Interrompt le traitement jusqu'à ce qu’un ou plusieurs asynchrones opérations en cours sur la table est terminé.  <br/> |
|[GetCollapseState](imapitable-getcollapsestate.md) <br/> |Retourne les données nécessaires à la recréation en cours réduit ou développé état d’une table, voir.  <br/> |
|[SetCollapseState](imapitable-setcollapsestate.md) <br/> |Reconstruit l’état actuel de développés ou réduit d’une table, voir l’aide de données qui a été enregistrées par un appel antérieur à la méthode **IMAPITable::GetCollapseState** .  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

