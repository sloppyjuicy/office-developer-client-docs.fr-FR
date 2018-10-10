---
title: Relation.PartialReplica Property (DAO)
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
ms.openlocfilehash: 4b1768b61dcb6b14bc5d67e945379c5ebb5c399a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471599"
---
# <a name="relationpartialreplica-property-dao"></a><span data-ttu-id="6f769-102">Relation.PartialReplica Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="6f769-102">Relation.PartialReplica Property (DAO)</span></span>


<span data-ttu-id="6f769-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f769-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6f769-p101">Définit ou renvoie une valeur sur une **Relation** indiquant si cette relation doit être prise en compte lors du remplissage d'un réplica partiel à partir d'un réplica complet. (Bases de données de moteur de base de données Microsoft Access uniquement). Type de données **Boolean** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6f769-p101">Sets or returns a value on a **Relation** object indicating whether that relation should be considered when populating a partial replica from a full replica. (Microsoft Access database engine databases only). Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f769-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f769-107">Syntax</span></span>

<span data-ttu-id="6f769-108">*expression* . PartialReplica</span><span class="sxs-lookup"><span data-stu-id="6f769-108">*expression* .PartialReplica</span></span>

<span data-ttu-id="6f769-109">*expression* Expression qui renvoie un objet **Relation** .</span><span class="sxs-lookup"><span data-stu-id="6f769-109">*expression* An expression that returns a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f769-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="6f769-110">Remarks</span></span>

<span data-ttu-id="6f769-111">Le paramètre ou la valeur de retour est une donnée de type booléen qui est **True** lorsque la relation doit être prise en compte lors de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="6f769-111">The setting or return value is a Boolean data type that is **True** when the relation should be enforced during synchronization.</span></span>

<span data-ttu-id="6f769-p102">Cette propriété vous permet de répliquer des données d'un réplica complet dans un réplica partiel en fonction des relations entre les tables. Vous pouvez utiliser la propriété **PartialReplica** lorsque la propriété **ReplicaFilter** seule ne suffit pas à spécifier avec précision les données à repliquer dans le réplica partiel. Supposez par exemple que vous avez une base de données dont la table Customers a une relation un-à-plusieurs avec la table Orders et que vous voulez configurer un réplica partiel qui réplique uniquement les commandes des clients de la région Californie (plutôt que toutes les commandes). Vous ne pouvez pas définir la propriété **ReplicaFilter** au niveau de la table Orders sur Region = 'CA' car le champ Region se trouve dans la table Customers, et non dans la table Orders.</span><span class="sxs-lookup"><span data-stu-id="6f769-p102">This property enables you to replicate data from the full replica to the partial replica based on relationships between tables. You can use the **PartialReplica** property when setting the **ReplicaFilter** property alone can't adequately specify what data should be replicated to the partial. For example, suppose you have a database in which the Customers table has a one-to-many relationship with the Orders table, and you want to configure a partial replica that only replicates orders from customers in the California region (instead of all orders). It is not possible to set the **ReplicaFilter** property on the Orders table to Region = 'CA' because the Region field is in the Customers table, not the Orders table.</span></span>

<span data-ttu-id="6f769-p103">Pour répliquer toutes les commandes de la région Californie, vous devez indiquer que la relation entre les tables Orders et Customers sera active lors de la réplication. Une fois le réplica partiel créé, les étapes suivantes le renseignent avec toutes les commandes de la région Californie :</span><span class="sxs-lookup"><span data-stu-id="6f769-p103">To replicate all orders from the California region, you must indicate that the relation between the Orders and Customers tables will be active during replication. Once you've created a partial replica, the following steps will populate it with all orders from the California region:</span></span>

1.  <span data-ttu-id="6f769-118">Définir la propriété **ReplicaFilter** sur l’objet Customers **TableDef** à « Region = 'CA' ».</span><span class="sxs-lookup"><span data-stu-id="6f769-118">Set the **ReplicaFilter** property on the Customers **TableDef** object to "Region = 'CA'".</span></span>

2.  <span data-ttu-id="6f769-119">Définissez la valeur de la propriété **PartialReplica** sur **True** au niveau de l'objet **Relation** correspondant à la relation entre les tables Orders et Customers.</span><span class="sxs-lookup"><span data-stu-id="6f769-119">Set the value of the **PartialReplica** property to **True** on the **Relation** object corresponding to the relationship between Orders and Customers.</span></span>

3.  <span data-ttu-id="6f769-120">Invoquez la méthode **PopulatePartial**.</span><span class="sxs-lookup"><span data-stu-id="6f769-120">Invoke the **PopulatePartial** method.</span></span>
    

> [!NOTE]
> <P><span data-ttu-id="6f769-p104">Lorsque vous définissez un filtre ou une relation de réplica, notez que les enregistrements du réplica partiel ne répondant pas aux critères de restriction seront supprimés du réplica partiel mais pas du réplica complet. Supposez par exemple que vous définissez la propriété <STRONG>ReplicaFilter</STRONG> au niveau de l'objet <STRONG>TableDef</STRONG> Customers du réplica partiel sur "Region = 'CA'" et que vous remplissez une nouvelle fois la base de données. Cette opération va entraîner l'ajout ou la mise à jour de tous les enregistrements relatifs aux clients basés en Californie. Si vous redéfinissez ensuite la propriété <STRONG>ReplicaFilter</STRONG> sur "Region = 'FL'" et remplissez une nouvelle fois la base de données, tous les enregistrements de la région Californie du réplica partiel sont supprimés et tous ceux de la région Floride sont insérés à partir du réplica complet. Aucun enregistrement du réplica complet n'est supprimé. Avant de définir la propriété <STRONG>ReplicaFilter</STRONG> ou <STRONG>PartialReplica</STRONG>, il convient de synchroniser le réplica partiel dans lequel vous définissez ces propriétés avec le réplica complet. Vous garantissez ainsi que les modifications en cours du réplica partiel sont fusionnées dans ce dernier avant que tout enregistrement ne soit supprimé.</span><span class="sxs-lookup"><span data-stu-id="6f769-p104">When you set a replica filter or replica relation, be aware that records in the partial replica that don't satisfy the restriction criteria will be removed from the partial replica, but not from the full replica. For example, suppose you set the <STRONG>ReplicaFilter</STRONG> property on the Customers <STRONG>TableDef</STRONG> in the partial replica to "Region = 'CA'" and you then repopulate the database. This will insert or update all records for California-based customers. If you then reset the <STRONG>ReplicaFilter</STRONG> property to "Region = 'FL'" and repopulate the database, all California region records in the partial replica will be removed, and all records from Florida-based customers will be inserted from the full replica. No records in the full replica will be deleted. Before setting either the <STRONG>ReplicaFilter</STRONG> or <STRONG>PartialReplica</STRONG> property, it's a good idea to synchronize the partial replica in which you are setting these properties with the full replica. This will ensure that pending changes in the partial replica will be merged into the full replica before any records are removed in the partial replica.</span></span></P>


