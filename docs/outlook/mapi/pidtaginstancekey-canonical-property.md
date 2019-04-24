---
title: Propriété canonique PidTagInstanceKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInstanceKey
api_type:
- HeaderDef
ms.assetid: 14fc5571-acc0-4d75-8598-964aee5ba01c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c237149c305a80012d1f06ea4373b892d25daec1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358510"
---
# <a name="pidtaginstancekey-canonical-property"></a><span data-ttu-id="67e35-103">Propriété canonique PidTagInstanceKey</span><span class="sxs-lookup"><span data-stu-id="67e35-103">PidTagInstanceKey Canonical Property</span></span>

  
  
<span data-ttu-id="67e35-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67e35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67e35-105">Contient une valeur qui identifie de manière unique une ligne dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="67e35-105">Contains a value that uniquely identifies a row in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="67e35-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="67e35-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="67e35-107">PR_INSTANCE_KEY</span><span class="sxs-lookup"><span data-stu-id="67e35-107">PR_INSTANCE_KEY</span></span>  <br/> |
|<span data-ttu-id="67e35-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="67e35-108">Identifier:</span></span>  <br/> |<span data-ttu-id="67e35-109">0x0FF6</span><span class="sxs-lookup"><span data-stu-id="67e35-109">0x0FF6</span></span>  <br/> |
|<span data-ttu-id="67e35-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="67e35-110">Data type:</span></span>  <br/> |<span data-ttu-id="67e35-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="67e35-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="67e35-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="67e35-112">Area:</span></span>  <br/> |<span data-ttu-id="67e35-113">Table</span><span class="sxs-lookup"><span data-stu-id="67e35-113">Table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67e35-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="67e35-114">Remarks</span></span>

<span data-ttu-id="67e35-115">Cette propriété est une valeur binaire qui identifie de manière unique une ligne dans un affichage tableau.</span><span class="sxs-lookup"><span data-stu-id="67e35-115">This property is a binary value that uniquely identifies a row in a table view.</span></span> <span data-ttu-id="67e35-116">Il s'agit d'une colonne obligatoire dans la plupart des tables.</span><span class="sxs-lookup"><span data-stu-id="67e35-116">It is a required column in most tables.</span></span> <span data-ttu-id="67e35-117">Si une ligne est incluse dans deux vues, il existe deux clés d'instance différentes.</span><span class="sxs-lookup"><span data-stu-id="67e35-117">If a row is included in two views, there are two different instance keys.</span></span> <span data-ttu-id="67e35-118">La clé d'instance d'une ligne peut différer chaque fois que la table est ouverte, mais reste constante lorsque la table est ouverte.</span><span class="sxs-lookup"><span data-stu-id="67e35-118">The instance key of a row may differ each time the table is opened, but remains constant while the table is open.</span></span> <span data-ttu-id="67e35-119">Les lignes ajoutées alors qu'un tableau est en cours d'utilisation ne réutilisez pas une clé d'instance précédemment utilisée.</span><span class="sxs-lookup"><span data-stu-id="67e35-119">Rows added while a table is in use do not reuse an instance key that was previously used.</span></span> 
  
<span data-ttu-id="67e35-120">Utilisez les propriétés **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ou **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) pour corréler toutes les lignes d'une expansion.</span><span class="sxs-lookup"><span data-stu-id="67e35-120">Use the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) properties to correlate all the rows of an expansion.</span></span> <span data-ttu-id="67e35-121">Utilisez **PR_INSTANCE_KEY** pour rechercher une instance particulière au sein de l'expansion.</span><span class="sxs-lookup"><span data-stu-id="67e35-121">Use **PR_INSTANCE_KEY** to locate a particular instance within the expansion.</span></span> 
  
<span data-ttu-id="67e35-122">Lorsqu'une propriété à valeurs multiples est développée dans un tableau, une ligne est créée pour chaque instance de l'expansion, c'est-à-dire, pour chaque valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="67e35-122">When a multivalued property is expanded in a table, a row is created for each instance of the expansion, that is, for each value of that property.</span></span> <span data-ttu-id="67e35-123">Chaque ligne a une valeur unique pour la propriété **PR_INSTANCE_KEY** , tandis que toutes les autres colonnes conservent leurs valeurs d'origine tout au long de l'expansion.</span><span class="sxs-lookup"><span data-stu-id="67e35-123">Each row has a unique value for the **PR_INSTANCE_KEY** property, while all the other columns retain their original values throughout the expansion.</span></span> 
  
<span data-ttu-id="67e35-124">Dans un tri classé dans un tableau, les lignes qui ne correspondent pas aux données réelles peuvent être ajoutées au résultat du tri.</span><span class="sxs-lookup"><span data-stu-id="67e35-124">In a categorized sort of a table, rows not corresponding to actual data can be added to the result of the sort.</span></span> <span data-ttu-id="67e35-125">Chaque ligne de ce type, comme toutes les lignes de toutes les tables, possède sa propre clé d'instance unique.</span><span class="sxs-lookup"><span data-stu-id="67e35-125">Each such row, like all rows in all tables, has its own unique instance key.</span></span> 
  
 <span data-ttu-id="67e35-126">**PR_INSTANCE_KEY** est également utilisé dans les notifications d'événement de table.</span><span class="sxs-lookup"><span data-stu-id="67e35-126">**PR_INSTANCE_KEY** is also used in table event notifications.</span></span> <span data-ttu-id="67e35-127">Les membres **propIndex** et **propPrior** de la structure [TABLE_NOTIFICATION](table_notification.md) sont des structures [SPropValue](spropvalue.md) contenant des valeurs **PR_INSTANCE_KEY** .</span><span class="sxs-lookup"><span data-stu-id="67e35-127">The **propIndex** and **propPrior** members of the [TABLE_NOTIFICATION](table_notification.md) structure are [SPropValue](spropvalue.md) structures holding **PR_INSTANCE_KEY** values.</span></span> <span data-ttu-id="67e35-128">Le membre **propIndex** indique la ligne qui a été ajoutée ou modifiée.</span><span class="sxs-lookup"><span data-stu-id="67e35-128">The **propIndex** member indicates the row that was added or changed.</span></span> <span data-ttu-id="67e35-129">Le membre **propPrior** indique la ligne avant la ligne ajoutée ou modifiée (**PR_NULL** indique une modification apportée à la première ligne).</span><span class="sxs-lookup"><span data-stu-id="67e35-129">The **propPrior** member indicates the row before the added or changed row (**PR_NULL** indicates a change to the first row).</span></span> 
  
<span data-ttu-id="67e35-130">Cette valeur n'est pas copiée dans le cadre de la table d'affichage.</span><span class="sxs-lookup"><span data-stu-id="67e35-130">This value is not copied as part of the display table.</span></span> 
  
 <span data-ttu-id="67e35-131">**PR_INSTANCE_KEY** est une structure [MAPIUID](mapiuid.md) .</span><span class="sxs-lookup"><span data-stu-id="67e35-131">**PR_INSTANCE_KEY** is a [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="67e35-132">Toutes les clés d'instance peuvent être directement comparées en tant que valeurs binaires.</span><span class="sxs-lookup"><span data-stu-id="67e35-132">All instance keys can be directly compared as binary values.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="67e35-133">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="67e35-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="67e35-134">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="67e35-134">Protocol specifications</span></span>

<span data-ttu-id="67e35-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67e35-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67e35-136">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="67e35-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="67e35-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67e35-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67e35-138">Spécifie les propriétés et les opérations pour les listes d'utilisateurs, de contacts, de groupes et de ressources.</span><span class="sxs-lookup"><span data-stu-id="67e35-138">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="67e35-139">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="67e35-139">Header files</span></span>

<span data-ttu-id="67e35-140">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="67e35-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="67e35-141">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="67e35-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="67e35-142">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="67e35-142">Mapitags.h</span></span>
  
> <span data-ttu-id="67e35-143">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="67e35-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="67e35-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67e35-144">See also</span></span>



[<span data-ttu-id="67e35-145">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="67e35-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="67e35-146">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="67e35-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="67e35-147">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="67e35-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="67e35-148">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="67e35-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

