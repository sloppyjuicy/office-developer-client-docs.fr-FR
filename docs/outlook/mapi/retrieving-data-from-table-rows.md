---
title: Extraction de données à partir des lignes de tableau
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 91b1fa06fd47321e9c19d9751caac793e27e8f16
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787017"
---
# <a name="retrieving-data-from-table-rows"></a><span data-ttu-id="bb94e-103">Extraction de données à partir des lignes de tableau</span><span class="sxs-lookup"><span data-stu-id="bb94e-103">Retrieving Data from Table Rows</span></span>

  
  
<span data-ttu-id="bb94e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bb94e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bb94e-105">Récupérer des lignes d’une table implique :</span><span class="sxs-lookup"><span data-stu-id="bb94e-105">Retrieving rows from a table involves:</span></span>
  
- <span data-ttu-id="bb94e-106">Obtention de valeurs de propriété pour toutes les colonnes.</span><span class="sxs-lookup"><span data-stu-id="bb94e-106">Obtaining the property values for all the columns.</span></span>
    
- <span data-ttu-id="bb94e-107">Modification de la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="bb94e-107">Modifying the current position.</span></span>
    
<span data-ttu-id="bb94e-108">Une des colonnes dans la plupart des tables requis est un identificateur d’entrée, la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) — qui peut être utilisé pour ouvrir l’objet qui représente la ligne.</span><span class="sxs-lookup"><span data-stu-id="bb94e-108">One of the required columns in most tables is an entry identifier — the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property — that can be used to open the object that represents the row.</span></span> <span data-ttu-id="bb94e-109">Cet identificateur d’entrée est généralement un identificateur d’entrée à court terme, qui ne conserve pas au-delà de la durée de vie de la table.</span><span class="sxs-lookup"><span data-stu-id="bb94e-109">This entry identifier is usually a short-term entry identifier, one that does not persist past the lifetime of the table.</span></span> <span data-ttu-id="bb94e-110">Toutefois, il peut être un identificateur à long terme si l’implémentation de la table uniquement le fournisseur de services prend en charge un seul type d’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="bb94e-110">However, it can be a long-term identifier if the service provider implementing the table only supports one type of entry identifier.</span></span>
  
<span data-ttu-id="bb94e-111">Clients et fournisseurs de services peut-il un des appels pour récupérer des lignes suivantes :</span><span class="sxs-lookup"><span data-stu-id="bb94e-111">Clients and service providers can make one of the following calls to retrieve rows:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="bb94e-112">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="bb94e-112">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="bb94e-113">Récupère un nombre spécifié de lignes en commençant par la ligne active dans une direction avancer ou reculer.</span><span class="sxs-lookup"><span data-stu-id="bb94e-113">Retrieves a specified number of rows starting with the current row in either a forward or backward direction.</span></span>  <br/> |
|[<span data-ttu-id="bb94e-114">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="bb94e-114">HrQueryAllRows</span></span>](hrqueryallrows.md) <br/> |<span data-ttu-id="bb94e-115">Récupère toutes les lignes d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="bb94e-115">Retrieves all of the rows in a table.</span></span>  <br/> |
|[<span data-ttu-id="bb94e-116">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="bb94e-116">ITableData::HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="bb94e-117">Récupère une ligne dans une table en fonction de la valeur de sa colonne d’index.</span><span class="sxs-lookup"><span data-stu-id="bb94e-117">Retrieves a row in a table according to the value of its index column.</span></span> <span data-ttu-id="bb94e-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) est généralement la colonne d’index pour une table.</span><span class="sxs-lookup"><span data-stu-id="bb94e-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) is usually the index column for a table.</span></span>  <br/> |
   
<span data-ttu-id="bb94e-119">Lorsqu’une propriété facultative est incluse en tant qu’une des colonnes dans une table, certaines lignes peut-être les valeurs valides pour la colonne alors que d’autres personnes risque de ne pas.</span><span class="sxs-lookup"><span data-stu-id="bb94e-119">When an optional property is included as one of the columns in a table, some of the rows might have valid values for the column while others might not.</span></span> <span data-ttu-id="bb94e-120">Existence d’une valeur valide pour une colonne dépend de si l’objet qui fournit les informations de la ligne définit la propriété.</span><span class="sxs-lookup"><span data-stu-id="bb94e-120">Whether a valid value exists for a column depends on whether the object providing the information for the row sets the property.</span></span> <span data-ttu-id="bb94e-121">En fonction de l’implémentation de l’objet, une propriété inexistante peut être représentée dans la table en tant que **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) ou une valeur arbitraire.</span><span class="sxs-lookup"><span data-stu-id="bb94e-121">Depending on the implementation of the object, a non-existent property can be represented in the table as **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) or an arbitrary value.</span></span> <span data-ttu-id="bb94e-122">Les utilisateurs de tableaux doivent être prudent de faire la distinction entre les propriétés qui n’existent pas et ont des valeurs sans signification et des propriétés qui existent et ont des valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="bb94e-122">Users of tables must be careful to differentiate between properties that are nonexistent and have meaningless values and properties that do exist and have valid values.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bb94e-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb94e-123">See also</span></span>



[<span data-ttu-id="bb94e-124">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="bb94e-124">MAPI Tables</span></span>](mapi-tables.md)

