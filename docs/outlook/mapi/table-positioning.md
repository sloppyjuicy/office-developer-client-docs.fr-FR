---
title: Positionnement des tableaux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0cbbc93-8074-4e86-b660-ee7bab910587
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 656f696c58e9b62e7e601d7f531870b8c385e862
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345653"
---
# <a name="table-positioning"></a><span data-ttu-id="1fd17-103">Positionnement des tableaux</span><span class="sxs-lookup"><span data-stu-id="1fd17-103">Table Positioning</span></span>

  
  
<span data-ttu-id="1fd17-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fd17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1fd17-105">La position actuelle dans un tableau est toujours indiquée par un curseur.</span><span class="sxs-lookup"><span data-stu-id="1fd17-105">The current position within a table is always indicated by a cursor.</span></span> <span data-ttu-id="1fd17-106">Il y a un curseur pour chaque vue d'un tableau; sa valeur est définie par l'implémenteur de la table.</span><span class="sxs-lookup"><span data-stu-id="1fd17-106">There is one cursor for each view of a table; its value is set by the table's implementer.</span></span> <span data-ttu-id="1fd17-107">Lorsqu'un client ou un fournisseur de services utilisant la table effectue un appel pour modifier la position de la table, la valeur du curseur est réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="1fd17-107">When a client or service provider using the table makes a call to change the position of the table, the value of the cursor is reset.</span></span> <span data-ttu-id="1fd17-108">La position d'une table peut être modifiée de la façon suivante:</span><span class="sxs-lookup"><span data-stu-id="1fd17-108">A table's position can be changed with:</span></span>
  
- <span data-ttu-id="1fd17-109">Signet.</span><span class="sxs-lookup"><span data-stu-id="1fd17-109">A bookmark.</span></span>
    
- <span data-ttu-id="1fd17-110">Fraction.</span><span class="sxs-lookup"><span data-stu-id="1fd17-110">A fractional value.</span></span>
    
- <span data-ttu-id="1fd17-111">Un filtre.</span><span class="sxs-lookup"><span data-stu-id="1fd17-111">A filter.</span></span>
    

