---
title: IMAPITable IUnknown
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8a7e5e2d599f64eeb8c9a33c45ba91e8820e2210
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556476"
---
# <a name="imapitable--iunknown"></a>IMAPITable : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit une vue en lecture seule d’un tableau. **IMAPITable est utilisé** par les clients et les fournisseurs de services pour manipuler la façon dont une table apparaît. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Objets Table  <br/> |
|Implémenté par :  <br/> |Fournisseurs de services et MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes, fournisseurs de services  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPITable  <br/> |
|Type de pointeur :  <br/> |LPMAPITABLE  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[GetLastError](imapitable-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) contenant des informations sur l’erreur précédente sur le tableau.  <br/> |
|[Conseiller](imapitable-advise.md) <br/> |S’inscrit pour recevoir une notification des événements spécifiés affectant la table.  <br/> |
|[Unadvise](imapitable-unadvise.md) <br/> |Annule l’envoi de notifications précédemment définies avec un appel à la **méthode IMAPITable::Advise.**  <br/> |
|[GetStatus](imapitable-getstatus.md) <br/> |Renvoie l’état et le type de la table.  <br/> |
|[SetColumns](imapitable-setcolumns.md) <br/> |Définit les propriétés et l’ordre particuliers des propriétés à voir apparaître sous la valeur de colonnes dans le tableau.  <br/> |
|[QueryColumns](imapitable-querycolumns.md) <br/> |Renvoie une liste de colonnes pour le tableau.  <br/> |
|[GetRowCount](imapitable-getrowcount.md) <br/> |Renvoie le nombre total de lignes dans le tableau.  <br/> |
|[SeekRow](imapitable-seekrow.md) <br/> |Déplace le curseur à une position spécifique dans le tableau.  <br/> |
|[SeekRowApprox](imapitable-seekrowapprox.md) <br/> |Déplace le curseur vers une position fractionnaire approximative dans le tableau.  <br/> |
|[QueryPosition](imapitable-queryposition.md) <br/> |Extrait la position de ligne de tableau actuelle du curseur, en fonction d’une valeur fractionnaire.  <br/> |
|[FindRow](imapitable-findrow.md) <br/> |Recherche la ligne suivante dans un tableau qui correspond à des critères de recherche spécifiques.  <br/> |
|[Restrict](imapitable-restrict.md) <br/> |Applique un filtre à un tableau, en réduisant le jeu de lignes uniquement aux lignes correspondant aux critères spécifiés.  <br/> |
|[CreateBookmark](imapitable-createbookmark.md) <br/> |Marque la position actuelle du tableau.  <br/> |
|[FreeBookmark](imapitable-freebookmark.md) <br/> |Libère la mémoire associée à un signet.  <br/> |
|[SortTable](imapitable-sorttable.md) <br/> |Trie les lignes du tableau en fonction des critères de tri.  <br/> |
|[QuerySortOrder](imapitable-querysortorder.md) <br/> |Extrait l’ordre de tri actuel d’un tableau.  <br/> |
|[QueryRows](imapitable-queryrows.md) <br/> |Renvoie une ou plusieurs lignes d’un tableau, en commençant à la position actuelle du curseur.  <br/> |
|[Abandonner](imapitable-abort.md) <br/> |Arrête toutes les opérations asynchrones en cours pour la table.  <br/> |
|[ExpandRow](imapitable-expandrow.md) <br/> |Développe une catégorie de tableaux réduire, en ajoutant les lignes de feuille appartenant à la catégorie à l’affichage tableau.  <br/> |
|[CollapseRow](imapitable-collapserow.md) <br/> |Cette propriété permet de réduire une catégorie de tableau étendu, en supprimant les lignes de feuille appartenant à la catégorie de l’affichage Tableau.  <br/> |
|[WaitForCompletion](imapitable-waitforcompletion.md) <br/> |Suspend le traitement jusqu’à ce qu’une ou plusieurs opérations asynchrones en cours sur la table soient terminées.  <br/> |
|[GetCollapseState](imapitable-getcollapsestate.md) <br/> |Renvoie les données nécessaires pour reconstruire l’état actuel, réduire ou développé, d’une table classée.  <br/> |
|[SetCollapseState](imapitable-setcollapsestate.md) <br/> |Reconstruit l’état étendu ou réduire actuel d’une table classée à l’aide de données enregistrées par un appel précédent à la méthode **IMAPITable::GetCollapseState.**  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

