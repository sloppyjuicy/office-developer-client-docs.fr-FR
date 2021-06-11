---
title: Extraction de données à partir de lignes de tableau
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2f389d26ec80b9af3ed28c5eb85b589c9cbb26c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405253"
---
# <a name="retrieving-data-from-table-rows"></a><span data-ttu-id="d6ba8-103">Extraction de données à partir de lignes de tableau</span><span class="sxs-lookup"><span data-stu-id="d6ba8-103">Retrieving Data from Table Rows</span></span>

  
  
<span data-ttu-id="d6ba8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6ba8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6ba8-105">La récupération de lignes à partir d’un tableau implique les opérations ci-après :</span><span class="sxs-lookup"><span data-stu-id="d6ba8-105">Retrieving rows from a table involves:</span></span>
  
- <span data-ttu-id="d6ba8-106">Obtention des valeurs de propriété pour toutes les colonnes.</span><span class="sxs-lookup"><span data-stu-id="d6ba8-106">Obtaining the property values for all the columns.</span></span>
    
- <span data-ttu-id="d6ba8-107">Modification de la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="d6ba8-107">Modifying the current position.</span></span>
    
<span data-ttu-id="d6ba8-108">L’une des colonnes requises dans la plupart des tableaux est un identificateur d’entrée ( propriété PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) qui peut être utilisé pour ouvrir l’objet qui **représente** la ligne.</span><span class="sxs-lookup"><span data-stu-id="d6ba8-108">One of the required columns in most tables is an entry identifier — the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property — that can be used to open the object that represents the row.</span></span> <span data-ttu-id="d6ba8-109">Cet identificateur d’entrée est généralement un identificateur d’entrée à court terme, qui ne persiste pas au-delà de la durée de vie du tableau.</span><span class="sxs-lookup"><span data-stu-id="d6ba8-109">This entry identifier is usually a short-term entry identifier, one that does not persist past the lifetime of the table.</span></span> <span data-ttu-id="d6ba8-110">Toutefois, il peut s’agit d’un identificateur à long terme si le fournisseur de services qui implémente la table ne prend en charge qu’un seul type d’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d6ba8-110">However, it can be a long-term identifier if the service provider implementing the table only supports one type of entry identifier.</span></span>
  
<span data-ttu-id="d6ba8-111">Les clients et les fournisseurs de services peuvent effectuer l’un des appels suivants pour récupérer des lignes :</span><span class="sxs-lookup"><span data-stu-id="d6ba8-111">Clients and service providers can make one of the following calls to retrieve rows:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="d6ba8-112">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="d6ba8-112">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="d6ba8-113">Extrait un nombre spécifié de lignes commençant par la ligne en cours dans une direction avant ou arrière.</span><span class="sxs-lookup"><span data-stu-id="d6ba8-113">Retrieves a specified number of rows starting with the current row in either a forward or backward direction.</span></span>  <br/> |
|[<span data-ttu-id="d6ba8-114">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="d6ba8-114">HrQueryAllRows</span></span>](hrqueryallrows.md) <br/> |<span data-ttu-id="d6ba8-115">Récupère toutes les lignes d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="d6ba8-115">Retrieves all of the rows in a table.</span></span>  <br/> |
|[<span data-ttu-id="d6ba8-116">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="d6ba8-116">ITableData::HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="d6ba8-117">Extrait une ligne d’un tableau en fonction de la valeur de sa colonne d’index.</span><span class="sxs-lookup"><span data-stu-id="d6ba8-117">Retrieves a row in a table according to the value of its index column.</span></span> <span data-ttu-id="d6ba8-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) est généralement la colonne d’index d’une table.</span><span class="sxs-lookup"><span data-stu-id="d6ba8-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) is usually the index column for a table.</span></span>  <br/> |
   
<span data-ttu-id="d6ba8-119">Lorsqu’une propriété facultative est incluse comme une des colonnes d’un tableau, certaines lignes peuvent avoir des valeurs valides pour la colonne, tandis que d’autres peuvent ne pas l’être.</span><span class="sxs-lookup"><span data-stu-id="d6ba8-119">When an optional property is included as one of the columns in a table, some of the rows might have valid values for the column while others might not.</span></span> <span data-ttu-id="d6ba8-120">L’existence d’une valeur valide pour une colonne varie selon que l’objet fournissant les informations de la ligne définit la propriété.</span><span class="sxs-lookup"><span data-stu-id="d6ba8-120">Whether a valid value exists for a column depends on whether the object providing the information for the row sets the property.</span></span> <span data-ttu-id="d6ba8-121">Selon l’implémentation de l’objet, une propriété inexistante peut être représentée dans la table sous la PR_NULL **(** [PidTagNull](pidtagnull-canonical-property.md)) ou une valeur arbitraire.</span><span class="sxs-lookup"><span data-stu-id="d6ba8-121">Depending on the implementation of the object, a non-existent property can be represented in the table as **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) or an arbitrary value.</span></span> <span data-ttu-id="d6ba8-122">Les utilisateurs de tables doivent faire la distinction entre les propriétés qui n’existent pas et qui ont des valeurs sans signification et qui existent et qui ont des valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="d6ba8-122">Users of tables must be careful to differentiate between properties that are nonexistent and have meaningless values and properties that do exist and have valid values.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d6ba8-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6ba8-123">See also</span></span>



[<span data-ttu-id="d6ba8-124">MAPI Tables</span><span class="sxs-lookup"><span data-stu-id="d6ba8-124">MAPI Tables</span></span>](mapi-tables.md)

