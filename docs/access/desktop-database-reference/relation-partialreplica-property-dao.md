---
title: Propriété Relation.PartialReplica (DAO)
TOCTitle: PartialReplica Property
ms:assetid: 3cb15639-371e-06e3-e2ba-30466ce09a72
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192692(v=office.15)
ms:contentKeyID: 48544324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053557
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 11f8017c01cec9af2da26bedaf689d69554e554c
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998186"
---
# <a name="relationpartialreplica-property-dao"></a><span data-ttu-id="52c88-102">Propriété Relation.PartialReplica (DAO)</span><span class="sxs-lookup"><span data-stu-id="52c88-102">Relation.PartialReplica property (DAO)</span></span>

<span data-ttu-id="52c88-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="52c88-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="52c88-p101">Définit ou renvoie une valeur sur une **Relation** indiquant si cette relation doit être prise en compte lors du remplissage d'un réplica partiel à partir d'un réplica complet. (Bases de données de moteur de base de données Microsoft Access uniquement). Type de données **Boolean** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="52c88-p101">Sets or returns a value on a **Relation** object indicating whether that relation should be considered when populating a partial replica from a full replica. (Microsoft Access database engine databases only). Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="52c88-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52c88-107">Syntax</span></span>

<span data-ttu-id="52c88-108">*expression* . PartialReplica</span><span class="sxs-lookup"><span data-stu-id="52c88-108">*expression* .PartialReplica</span></span>

<span data-ttu-id="52c88-109">*expression* Expression qui renvoie un objet **Relation** .</span><span class="sxs-lookup"><span data-stu-id="52c88-109">*expression* An expression that returns a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="52c88-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="52c88-110">Remarks</span></span>

<span data-ttu-id="52c88-111">Le paramètre ou la valeur de retour est une donnée de type booléen qui est **True** lorsque la relation doit être prise en compte lors de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="52c88-111">The setting or return value is a Boolean data type that is **True** when the relation should be enforced during synchronization.</span></span>

<span data-ttu-id="52c88-p102">Cette propriété vous permet de répliquer des données d'un réplica complet dans un réplica partiel en fonction des relations entre les tables. Vous pouvez utiliser la propriété **PartialReplica** lorsque la propriété **ReplicaFilter** seule ne suffit pas à spécifier avec précision les données à repliquer dans le réplica partiel. Supposez par exemple que vous avez une base de données dont la table Customers a une relation un-à-plusieurs avec la table Orders et que vous voulez configurer un réplica partiel qui réplique uniquement les commandes des clients de la région Californie (plutôt que toutes les commandes). Vous ne pouvez pas définir la propriété **ReplicaFilter** au niveau de la table Orders sur Region = 'CA' car le champ Region se trouve dans la table Customers, et non dans la table Orders.</span><span class="sxs-lookup"><span data-stu-id="52c88-p102">This property enables you to replicate data from the full replica to the partial replica based on relationships between tables. You can use the **PartialReplica** property when setting the **ReplicaFilter** property alone can't adequately specify what data should be replicated to the partial. For example, suppose you have a database in which the Customers table has a one-to-many relationship with the Orders table, and you want to configure a partial replica that only replicates orders from customers in the California region (instead of all orders). It is not possible to set the **ReplicaFilter** property on the Orders table to Region = 'CA' because the Region field is in the Customers table, not the Orders table.</span></span>

<span data-ttu-id="52c88-p103">Pour répliquer toutes les commandes de la région Californie, vous devez indiquer que la relation entre les tables Orders et Customers sera active lors de la réplication. Une fois le réplica partiel créé, les étapes suivantes le renseignent avec toutes les commandes de la région Californie :</span><span class="sxs-lookup"><span data-stu-id="52c88-p103">To replicate all orders from the California region, you must indicate that the relation between the Orders and Customers tables will be active during replication. Once you've created a partial replica, the following steps will populate it with all orders from the California region:</span></span>

1.  <span data-ttu-id="52c88-118">Définir la propriété **ReplicaFilter** sur l’objet Customers **TableDef** à « Region = 'CA' ».</span><span class="sxs-lookup"><span data-stu-id="52c88-118">Set the **ReplicaFilter** property on the Customers **TableDef** object to "Region = 'CA'".</span></span>

2.  <span data-ttu-id="52c88-119">Définissez la valeur de la propriété **PartialReplica** sur **True** au niveau de l'objet **Relation** correspondant à la relation entre les tables Orders et Customers.</span><span class="sxs-lookup"><span data-stu-id="52c88-119">Set the value of the **PartialReplica** property to **True** on the **Relation** object corresponding to the relationship between Orders and Customers.</span></span>

3.  <span data-ttu-id="52c88-120">Invoquez la méthode **PopulatePartial**.</span><span class="sxs-lookup"><span data-stu-id="52c88-120">Invoke the **PopulatePartial** method.</span></span>
    

> [!NOTE]
> <span data-ttu-id="52c88-121">[!REMARQUE] Lorsque vous définissez un filtre ou une relation de réplica, notez que les enregistrements du réplica partiel ne répondant pas aux critères de restriction seront supprimés du réplica partiel mais pas du réplica complet.</span><span class="sxs-lookup"><span data-stu-id="52c88-121">When you set a replica filter or replica relation, be aware that records in the partial replica that don't satisfy the restriction criteria will be removed from the partial replica, but not from the full replica.</span></span> <span data-ttu-id="52c88-122">Par exemple, supposons que vous définissez la propriété **ReplicaFilter** sur les clients **TableDef** dans le réplica partiel à « Region = 'CA' » et vous puis remplir la base de données.</span><span class="sxs-lookup"><span data-stu-id="52c88-122">For example, suppose you set the **ReplicaFilter** property on the Customers **TableDef** in the partial replica to "Region = 'CA'" and you then repopulate the database.</span></span> <span data-ttu-id="52c88-123">Cette opération va entraîner l'ajout ou la mise à jour de tous les enregistrements relatifs aux clients basés en Californie.</span><span class="sxs-lookup"><span data-stu-id="52c88-123">This will insert or update all records for California-based customers.</span></span> 
> 
> <span data-ttu-id="52c88-124">Si vous rétablissez la propriété **ReplicaFilter** pour « Region = 'FL' » et remplir la base de données, tous les enregistrements de la région Californie du réplica partiel seront supprimées et tous les enregistrements de Floride seront insérées à partir du réplica complet.</span><span class="sxs-lookup"><span data-stu-id="52c88-124">If you then reset the **ReplicaFilter** property to "Region = 'FL'" and repopulate the database, all California region records in the partial replica will be removed, and all records from Florida-based customers will be inserted from the full replica.</span></span> <span data-ttu-id="52c88-125">Aucun enregistrement du réplica complet n'est supprimé.</span><span class="sxs-lookup"><span data-stu-id="52c88-125">No records in the full replica will be deleted.</span></span> 
>
> <span data-ttu-id="52c88-126">Avant de définir la propriété **ReplicaFilter** ou **PartialReplica**, il convient de synchroniser le réplica partiel dans lequel vous définissez ces propriétés avec le réplica complet.</span><span class="sxs-lookup"><span data-stu-id="52c88-126">Before setting either the **ReplicaFilter** or **PartialReplica** property, it's a good idea to synchronize the partial replica in which you are setting these properties with the full replica.</span></span> <span data-ttu-id="52c88-127">Vous garantissez ainsi que les modifications en cours du réplica partiel sont fusionnées dans ce dernier avant que tout enregistrement ne soit supprimé.</span><span class="sxs-lookup"><span data-stu-id="52c88-127">This will ensure that pending changes in the partial replica will be merged into the full replica before any records are removed in the partial replica.</span></span>


