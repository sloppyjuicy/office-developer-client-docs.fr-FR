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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d6a13799da4ef9315f9c23317fa18853d71c72f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328797"
---
# <a name="imapitable--iunknown"></a>IMAPITable : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit une vue en lecture seule d'un tableau. La méthode **IMAPITable** est utilisée par les clients et les fournisseurs de services pour manipuler le mode d'affichage d'un tableau. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Exposé par:  <br/> |Objets de tableau  <br/> |
|Implémenté par :  <br/> |Fournisseurs de services et MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes, fournisseurs de services  <br/> |
|Identificateur de l'interface:  <br/> |IID_IMAPITable  <br/> |
|Type de pointeur:  <br/> |LPMAPITABLE  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Généré](imapitable-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) contenant des informations sur l'erreur précédente sur le tableau.  <br/> |
|[Recommander](imapitable-advise.md) <br/> |S'inscrit pour recevoir des notifications d'événements spécifiques affectant la table.  <br/> |
|[Unadvise](imapitable-unadvise.md) <br/> |Annule l'envoi des notifications précédemment configurées avec un appel à la méthode **IMAPITable:: Advise** .  <br/> |
|[GetStatus](imapitable-getstatus.md) <br/> |Renvoie l'État et le type de la table.  <br/> |
|[SetColumns](imapitable-setcolumns.md) <br/> |Définit les propriétés et l'ordre des propriétés spécifiques à afficher sous la forme de colonnes dans le tableau.  <br/> |
|[QueryColumns](imapitable-querycolumns.md) <br/> |Renvoie une liste de colonnes pour le tableau.  <br/> |
|[GetRowCount](imapitable-getrowcount.md) <br/> |Renvoie le nombre total de lignes dans le tableau.  <br/> |
|[SeekRow](imapitable-seekrow.md) <br/> |Déplace le curseur à une position spécifique dans le tableau.  <br/> |
|[SeekRowApprox](imapitable-seekrowapprox.md) <br/> |Place le curseur sur une position fractionnaire approximative dans le tableau.  <br/> |
|[QueryPosition](imapitable-queryposition.md) <br/> |Récupère la position de ligne de tableau actuelle du curseur, en fonction d'une valeur fractionnaire.  <br/> |
|[FindRow](imapitable-findrow.md) <br/> |Recherche la ligne suivante dans un tableau qui correspond aux critères de recherche spécifiques.  <br/> |
|[Restrict](imapitable-restrict.md) <br/> |Applique un filtre à un tableau, réduisant ainsi la valeur de la ligne sur les lignes correspondant aux critères spécifiés.  <br/> |
|[CreateBookmark](imapitable-createbookmark.md) <br/> |Marque la position actuelle du tableau.  <br/> |
|[FreeBookmark](imapitable-freebookmark.md) <br/> |Libère la mémoire associée à un signet.  <br/> |
|[SortTable](imapitable-sorttable.md) <br/> |Trie les lignes de la table en fonction des critères de tri.  <br/> |
|[QuerySortOrder](imapitable-querysortorder.md) <br/> |Récupère l'ordre de tri actuel d'une table.  <br/> |
|[QueryRows](imapitable-queryrows.md) <br/> |Renvoie une ou plusieurs lignes d'un tableau, en commençant à la position actuelle du curseur.  <br/> |
|[Abandonner](imapitable-abort.md) <br/> |Arrête toutes les opérations asynchrones en cours pour la table.  <br/> |
|[ExpandRow](imapitable-expandrow.md) <br/> |Développe une catégorie de table réduite, ajoutant les lignes de feuille appartenant à la catégorie à l'affichage tableau.  <br/> |
|[CollapseRow](imapitable-collapserow.md) <br/> |Réduit une catégorie de tableau étendue, en supprimant les lignes de feuille appartenant à la catégorie à partir de la vue de table.  <br/> |
|[WaitForCompletion](imapitable-waitforcompletion.md) <br/> |Interrompt le traitement jusqu'à ce qu'une ou plusieurs opérations asynchrones en cours sur la table soient terminées.  <br/> |
|[GetCollapseState](imapitable-getcollapsestate.md) <br/> |Renvoie les données nécessaires pour régénérer l'État réduit ou développé actuel d'une table catégorisée.  <br/> |
|[SetCollapseState](imapitable-setcollapsestate.md) <br/> |Reconstruit l'état développé ou réduit actuel d'une table catégorisée à l'aide des données qui ont été enregistrées par un appel antérieur à la méthode **IMAPITable:: GetCollapseState** .  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

