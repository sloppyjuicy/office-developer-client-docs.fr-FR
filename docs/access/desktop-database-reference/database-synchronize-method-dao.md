---
title: Méthode Database.Synchronize (DAO)
TOCTitle: Synchronize Method
ms:assetid: 5e716a4a-2430-8106-5c34-a02dd28bc4f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194659(v=office.15)
ms:contentKeyID: 48545137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053357
f1_categories:
- Office.Version=v15
ms.openlocfilehash: dc32087ad924a81eea5290d84ffb63dc4ad5e1ff
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999049"
---
# <a name="databasesynchronize-method-dao"></a><span data-ttu-id="cfd42-102">Méthode Database.Synchronize (DAO)</span><span class="sxs-lookup"><span data-stu-id="cfd42-102">Database.Synchronize method (DAO)</span></span>


<span data-ttu-id="cfd42-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cfd42-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cfd42-p101">Synchronise deux réplicas. (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="cfd42-p101">Synchronizes two replicas. (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="cfd42-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cfd42-106">Syntax</span></span>

<span data-ttu-id="cfd42-107">*expression* . Synchroniser (***NomCheminBaseDeDonnées***, ***ExchangeType***)</span><span class="sxs-lookup"><span data-stu-id="cfd42-107">*expression* .Synchronize(***DbPathName***, ***ExchangeType***)</span></span>

<span data-ttu-id="cfd42-108">*expression* Variable qui représente un objet de **base de données** .</span><span class="sxs-lookup"><span data-stu-id="cfd42-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="cfd42-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cfd42-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cfd42-110">Name</span><span class="sxs-lookup"><span data-stu-id="cfd42-110">Name</span></span></p></th>
<th><p><span data-ttu-id="cfd42-111">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="cfd42-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="cfd42-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="cfd42-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="cfd42-113">Description</span><span class="sxs-lookup"><span data-stu-id="cfd42-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cfd42-114"><em>NomCheminBaseDeDonnées</em></span><span class="sxs-lookup"><span data-stu-id="cfd42-114"><em>DbPathName</em></span></span></p></td>
<td><p><span data-ttu-id="cfd42-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="cfd42-115">Required</span></span></p></td>
<td><p><span data-ttu-id="cfd42-116"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="cfd42-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="cfd42-117">Chemin d'accès au réplica cible, avec lequel la base de données est synchronisée.</span><span class="sxs-lookup"><span data-stu-id="cfd42-117">The path to the target replica with which database will be synchronized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfd42-118"><em>ExchangeType</em></span><span class="sxs-lookup"><span data-stu-id="cfd42-118"><em>ExchangeType</em></span></span></p></td>
<td><p><span data-ttu-id="cfd42-119">Facultatif</span><span class="sxs-lookup"><span data-stu-id="cfd42-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="cfd42-120"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="cfd42-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="cfd42-121">Constante <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> indiquant la direction dans laquelle synchroniser les modifications entre deux bases de données.</span><span class="sxs-lookup"><span data-stu-id="cfd42-121">A <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> constant indicating which direction to synchronize changes between the two databases.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="cfd42-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="cfd42-122">Remarks</span></span>

<span data-ttu-id="cfd42-123">Vous utilisez **Synchronize** pour échanger des données et des modifications de conception entre deux bases de données.</span><span class="sxs-lookup"><span data-stu-id="cfd42-123">You use **Synchronize** to exchange data and design changes between two databases.</span></span> <span data-ttu-id="cfd42-124">Les modifications de conception ont toujours lieu en premier.</span><span class="sxs-lookup"><span data-stu-id="cfd42-124">Design changes always happen first.</span></span> <span data-ttu-id="cfd42-125">Les deux bases de données doivent se trouver au même niveau de conception avant de pouvoir échanger des données.</span><span class="sxs-lookup"><span data-stu-id="cfd42-125">Both databases must be at the same design level before they can exchange data.</span></span> <span data-ttu-id="cfd42-126">Par exemple, un échange de type **dbRepExportChanges** peut entraîner des modifications de conception au niveau d’un réplica même si les modifications de données uniquement à partir de la base de données vers NomCheminBaseDeDonnées.</span><span class="sxs-lookup"><span data-stu-id="cfd42-126">For example, an exchange of type **dbRepExportChanges** might cause design changes at a replica even though data changes flow only from the database to DbPathName.</span></span>

<span data-ttu-id="cfd42-127">Le réplica identifié dans NomCheminBaseDeDonnées doit faire partie du même jeu de réplicas.</span><span class="sxs-lookup"><span data-stu-id="cfd42-127">The replica identified in DbPathName must be part of the same replica set.</span></span> <span data-ttu-id="cfd42-128">Si les deux réplicas possèdent le même paramètre de propriété **ReplicaID** ou sont des réplicas-maîtres pour deux ensembles de réplicas différents, la synchronisation échoue.</span><span class="sxs-lookup"><span data-stu-id="cfd42-128">If both replicas have the same **ReplicaID** property setting or are Design Masters for two different replica sets, the synchronization fails.</span></span>

<span data-ttu-id="cfd42-129">Lorsque vous synchronisez deux réplicas sur Internet, vous devez utiliser la constante **dbRepSyncInternet**.</span><span class="sxs-lookup"><span data-stu-id="cfd42-129">When you synchronize two replicas over the Internet, you must use the **dbRepSyncInternet** constant.</span></span> <span data-ttu-id="cfd42-130">Dans ce cas, vous spécifiez une adresse URL Uniform Resource Locator () pour l’argument NomCheminBaseDeDonnées au lieu de spécifier un chemin d’accès réseau local.</span><span class="sxs-lookup"><span data-stu-id="cfd42-130">In this case, you specify a Uniform Resource Locator (URL) address for the DbPathName argument instead of specifying a local area network path.</span></span>


> [!NOTE]
> <span data-ttu-id="cfd42-p105">[!REMARQUE] Vous ne pouvez pas synchroniser des réplicas partiels avec d'autres réplicas partiels. Pour plus d'informations, reportez-vous à la méthode [PopulatePartial](database-populatepartial-method-dao.md).</span><span class="sxs-lookup"><span data-stu-id="cfd42-p105">You can't synchronize partial replicas with other partial replicas. See the [PopulatePartial](database-populatepartial-method-dao.md) method for more information.</span></span>


