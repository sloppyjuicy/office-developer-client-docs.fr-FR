---
title: Regroupement et de restriction des tableaux dans les fournisseurs de banque de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 33c76cdd0e7850f82949349ac2e5bb0dd4e056ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783418"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a><span data-ttu-id="792fa-103">Regroupement et de restriction des tableaux dans les fournisseurs de banque de messages</span><span class="sxs-lookup"><span data-stu-id="792fa-103">Grouping and Restricting Tables in Message Store Providers</span></span>

  
  
<span data-ttu-id="792fa-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="792fa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="792fa-105">Applications clientes permettent souvent aux utilisateurs contrôler comment le contenu d’un dossier s’affiche.</span><span class="sxs-lookup"><span data-stu-id="792fa-105">Client applications frequently allow users some control over how the contents of a folder are displayed.</span></span> <span data-ttu-id="792fa-106">En règle générale, un utilisateur peut choisir que les messages regroupés en fonction de la valeur d’une ou plusieurs propriétés de message, ou peut choisir d’exclure les messages qui correspondent à certains critères.</span><span class="sxs-lookup"><span data-stu-id="792fa-106">Typically, a user can choose to have messages grouped according to the value of one or more message properties, or can choose to exclude messages that match certain criteria.</span></span> <span data-ttu-id="792fa-107">Cette opération est effectuée à l’aide de la [IMAPITable : IUnknown](imapitableiunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="792fa-107">This is done by using the [IMAPITable : IUnknown](imapitableiunknown.md) interface.</span></span> <span data-ttu-id="792fa-108">Applications clientes peuvent restreindre les lignes renvoyées à partir de la table à l’utilisateur spécifie tous les critères.</span><span class="sxs-lookup"><span data-stu-id="792fa-108">Client applications can restrict the rows returned from the table to whatever criteria the user specifies.</span></span> <span data-ttu-id="792fa-109">Par conséquent, un message stocker fournisseur doit implémenter les méthodes **IMAPITable** suivantes.</span><span class="sxs-lookup"><span data-stu-id="792fa-109">Therefore, a message store provider needs to implement the following **IMAPITable** methods.</span></span> 
  
|<span data-ttu-id="792fa-110">Méthode IMAPITable ** **</span><span class="sxs-lookup"><span data-stu-id="792fa-110">****IMAPITable** method**</span></span>|<span data-ttu-id="792fa-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="792fa-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="792fa-112">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="792fa-112">IMAPITable::FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="792fa-113">Renvoie la table lignes qui correspondent aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="792fa-113">Returns table rows that match the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="792fa-114">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="792fa-114">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="792fa-115">Renvoie l’ensemble de colonnes dans une table ou de l’ensemble des colonnes actuellement utilisées.</span><span class="sxs-lookup"><span data-stu-id="792fa-115">Returns the set of columns in a table or the set of currently used columns.</span></span>  <br/> |
|[<span data-ttu-id="792fa-116">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="792fa-116">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="792fa-117">Renvoie une ou plusieurs lignes d’une table, à partir d’une position donnée.</span><span class="sxs-lookup"><span data-stu-id="792fa-117">Returns one or more rows from a table, starting from a given position.</span></span>  <br/> |
|[<span data-ttu-id="792fa-118">IMAPITable</span><span class="sxs-lookup"><span data-stu-id="792fa-118">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="792fa-119">Applique une restriction à une table de sorte que les appels suivants à **FindRow** retournent uniquement les lignes qui correspondent à la restriction.</span><span class="sxs-lookup"><span data-stu-id="792fa-119">Applies a restriction to a table so that subsequent calls to **FindRow** return only rows that match the restriction.</span></span>  <br/> |
|[<span data-ttu-id="792fa-120">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="792fa-120">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="792fa-121">Spécifie les colonnes qui doivent être retournés lorsque des lignes de la table.</span><span class="sxs-lookup"><span data-stu-id="792fa-121">Specifies which columns should be returned when rows are retrieved from the table.</span></span>  <br/> |
   
<span data-ttu-id="792fa-122">Restrictions peuvent être complexes à implémenter ; Pour plus d’informations, voir [à propos des Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="792fa-122">Restrictions can be complex to implement; for more information, see [About Restrictions](about-restrictions.md).</span></span> <span data-ttu-id="792fa-123">Pour plus d’informations sur l’implémentation de tables, voir [Tables de MAPI](mapi-tables.md).</span><span class="sxs-lookup"><span data-stu-id="792fa-123">For more information about implementing tables, see [MAPI Tables](mapi-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="792fa-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="792fa-124">See also</span></span>



[<span data-ttu-id="792fa-125">Fonctionnalit�s de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="792fa-125">Message Store Features</span></span>](message-store-features.md)

