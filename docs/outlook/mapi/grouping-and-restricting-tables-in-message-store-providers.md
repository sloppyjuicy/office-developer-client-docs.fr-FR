---
title: Regroupement et restriction des tables dans les fournisseurs de magasins de messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8a45a9fd0d40c16d110fd52be1ac1117e1dd4d04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428983"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a><span data-ttu-id="b8f1d-103">Regroupement et restriction des tables dans les fournisseurs de magasins de messages</span><span class="sxs-lookup"><span data-stu-id="b8f1d-103">Grouping and Restricting Tables in Message Store Providers</span></span>

  
  
<span data-ttu-id="b8f1d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8f1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8f1d-105">Les applications clientes permettent fréquemment aux utilisateurs de contrôler l’affichage du contenu d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="b8f1d-105">Client applications frequently allow users some control over how the contents of a folder are displayed.</span></span> <span data-ttu-id="b8f1d-106">En règle générale, un utilisateur peut choisir de grouper des messages en fonction de la valeur d’une ou de plusieurs propriétés de message ou d’exclure les messages qui correspondent à certains critères.</span><span class="sxs-lookup"><span data-stu-id="b8f1d-106">Typically, a user can choose to have messages grouped according to the value of one or more message properties, or can choose to exclude messages that match certain criteria.</span></span> <span data-ttu-id="b8f1d-107">Pour ce faire, utilisez [l’interface IMAPITable : IUnknown.](imapitableiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="b8f1d-107">This is done by using the [IMAPITable : IUnknown](imapitableiunknown.md) interface.</span></span> <span data-ttu-id="b8f1d-108">Les applications clientes peuvent limiter les lignes renvoyées à partir du tableau à tous les critères spécifiés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b8f1d-108">Client applications can restrict the rows returned from the table to whatever criteria the user specifies.</span></span> <span data-ttu-id="b8f1d-109">Par conséquent, un fournisseur de magasin de messages doit implémenter les méthodes **IMAPITable** suivantes.</span><span class="sxs-lookup"><span data-stu-id="b8f1d-109">Therefore, a message store provider needs to implement the following **IMAPITable** methods.</span></span> 
  
|<span data-ttu-id="b8f1d-110">Méthode IMAPITable\*\* \*\*</span><span class="sxs-lookup"><span data-stu-id="b8f1d-110">\*\*\*\*IMAPITable\*\* method\*\*</span></span>|<span data-ttu-id="b8f1d-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="b8f1d-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8f1d-112">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="b8f1d-112">IMAPITable::FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="b8f1d-113">Renvoie les lignes de tableau qui correspondent aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="b8f1d-113">Returns table rows that match the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="b8f1d-114">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="b8f1d-114">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="b8f1d-115">Renvoie l’ensemble des colonnes d’un tableau ou l’ensemble des colonnes actuellement utilisées.</span><span class="sxs-lookup"><span data-stu-id="b8f1d-115">Returns the set of columns in a table or the set of currently used columns.</span></span>  <br/> |
|[<span data-ttu-id="b8f1d-116">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="b8f1d-116">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="b8f1d-117">Renvoie une ou plusieurs lignes d’un tableau, à partir d’une position donnée.</span><span class="sxs-lookup"><span data-stu-id="b8f1d-117">Returns one or more rows from a table, starting from a given position.</span></span>  <br/> |
|[<span data-ttu-id="b8f1d-118">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="b8f1d-118">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="b8f1d-119">Applique une restriction à une table afin que les appels ultérieurs à **FindRow** retournent uniquement les lignes qui correspondent à la restriction.</span><span class="sxs-lookup"><span data-stu-id="b8f1d-119">Applies a restriction to a table so that subsequent calls to **FindRow** return only rows that match the restriction.</span></span>  <br/> |
|[<span data-ttu-id="b8f1d-120">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="b8f1d-120">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="b8f1d-121">Spécifie les colonnes qui doivent être renvoyées lorsque des lignes sont extraites du tableau.</span><span class="sxs-lookup"><span data-stu-id="b8f1d-121">Specifies which columns should be returned when rows are retrieved from the table.</span></span>  <br/> |
   
<span data-ttu-id="b8f1d-122">Les restrictions peuvent être complexes à implémenter ; Pour plus d’informations, voir [à propos des restrictions.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="b8f1d-122">Restrictions can be complex to implement; for more information, see [About Restrictions](about-restrictions.md).</span></span> <span data-ttu-id="b8f1d-123">Pour plus d’informations sur l’implémentation de tableaux, voir [Tables MAPI](mapi-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b8f1d-123">For more information about implementing tables, see [MAPI Tables](mapi-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b8f1d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8f1d-124">See also</span></span>



[<span data-ttu-id="b8f1d-125">Fonctionnalit�s de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="b8f1d-125">Message Store Features</span></span>](message-store-features.md)

