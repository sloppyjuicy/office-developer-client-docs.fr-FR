---
title: Database.Synchronize Method (DAO)
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
ms.openlocfilehash: b25536c158c248695c9e537a0153922b2518058a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863289"
---
# <a name="databasesynchronize-method-dao"></a><span data-ttu-id="43cfe-102">Database.Synchronize Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="43cfe-102">Database.Synchronize Method (DAO)</span></span>


<span data-ttu-id="43cfe-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="43cfe-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="43cfe-p101">Synchronise deux réplicas. (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="43cfe-p101">Synchronizes two replicas. (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="43cfe-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43cfe-106">Syntax</span></span>

<span data-ttu-id="43cfe-107">*expression* . Synchroniser (***NomCheminBaseDeDonnées***, ***ExchangeType***)</span><span class="sxs-lookup"><span data-stu-id="43cfe-107">*expression* .Synchronize(***DbPathName***, ***ExchangeType***)</span></span>

<span data-ttu-id="43cfe-108">*expression* Variable qui représente un objet de **base de données** .</span><span class="sxs-lookup"><span data-stu-id="43cfe-108">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="43cfe-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43cfe-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43cfe-110">Name</span><span class="sxs-lookup"><span data-stu-id="43cfe-110">Name</span></span></p></th>
<th><p><span data-ttu-id="43cfe-111">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="43cfe-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="43cfe-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="43cfe-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="43cfe-113">Description</span><span class="sxs-lookup"><span data-stu-id="43cfe-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43cfe-114">NomCheminBaseDeDonnées</span><span class="sxs-lookup"><span data-stu-id="43cfe-114">DbPathName</span></span></p></td>
<td><p><span data-ttu-id="43cfe-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="43cfe-115">Required</span></span></p></td>
<td><p><span data-ttu-id="43cfe-116"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="43cfe-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="43cfe-117">Chemin d'accès au réplica cible, avec lequel la base de données est synchronisée.</span><span class="sxs-lookup"><span data-stu-id="43cfe-117">The path to the target replica with which database will be synchronized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43cfe-118">ExchangeType</span><span class="sxs-lookup"><span data-stu-id="43cfe-118">ExchangeType</span></span></p></td>
<td><p><span data-ttu-id="43cfe-119">Facultatif</span><span class="sxs-lookup"><span data-stu-id="43cfe-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="43cfe-120"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="43cfe-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="43cfe-121">Constante <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> indiquant la direction dans laquelle synchroniser les modifications entre deux bases de données.</span><span class="sxs-lookup"><span data-stu-id="43cfe-121">A <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> constant indicating which direction to synchronize changes between the two databases.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="43cfe-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="43cfe-122">Remarks</span></span>

<span data-ttu-id="43cfe-123">Vous utilisez **Synchronize** pour échanger des données et des modifications de conception entre deux bases de données.</span><span class="sxs-lookup"><span data-stu-id="43cfe-123">You use **Synchronize** to exchange data and design changes between two databases.</span></span> <span data-ttu-id="43cfe-124">Les modifications de conception ont toujours lieu en premier.</span><span class="sxs-lookup"><span data-stu-id="43cfe-124">Design changes always happen first.</span></span> <span data-ttu-id="43cfe-125">Les deux bases de données doivent se trouver au même niveau de conception avant de pouvoir échanger des données.</span><span class="sxs-lookup"><span data-stu-id="43cfe-125">Both databases must be at the same design level before they can exchange data.</span></span> <span data-ttu-id="43cfe-126">Par exemple, un échange de type **dbRepExportChanges** peut entraîner des modifications de conception au niveau d’un réplica même si les modifications de données uniquement à partir de la base de données vers NomCheminBaseDeDonnées.</span><span class="sxs-lookup"><span data-stu-id="43cfe-126">For example, an exchange of type **dbRepExportChanges** might cause design changes at a replica even though data changes flow only from the database to DbPathName.</span></span>

<span data-ttu-id="43cfe-127">Le réplica identifié dans NomCheminBaseDeDonnées doit faire partie du même jeu de réplicas.</span><span class="sxs-lookup"><span data-stu-id="43cfe-127">The replica identified in DbPathName must be part of the same replica set.</span></span> <span data-ttu-id="43cfe-128">Si les deux réplicas possèdent le même paramètre de propriété **ReplicaID** ou sont des réplicas-maîtres pour deux ensembles de réplicas différents, la synchronisation échoue.</span><span class="sxs-lookup"><span data-stu-id="43cfe-128">If both replicas have the same **ReplicaID** property setting or are Design Masters for two different replica sets, the synchronization fails.</span></span>

<span data-ttu-id="43cfe-129">Lorsque vous synchronisez deux réplicas sur Internet, vous devez utiliser la constante **dbRepSyncInternet**.</span><span class="sxs-lookup"><span data-stu-id="43cfe-129">When you synchronize two replicas over the Internet, you must use the **dbRepSyncInternet** constant.</span></span> <span data-ttu-id="43cfe-130">Dans ce cas, vous spécifiez une adresse URL Uniform Resource Locator () pour l’argument NomCheminBaseDeDonnées au lieu de spécifier un chemin d’accès réseau local.</span><span class="sxs-lookup"><span data-stu-id="43cfe-130">In this case, you specify a Uniform Resource Locator (URL) address for the DbPathName argument instead of specifying a local area network path.</span></span>


> [!NOTE]
> <span data-ttu-id="43cfe-p105">[!REMARQUE] Vous ne pouvez pas synchroniser des réplicas partiels avec d'autres réplicas partiels. Pour plus d'informations, reportez-vous à la méthode [PopulatePartial](database-populatepartial-method-dao.md).</span><span class="sxs-lookup"><span data-stu-id="43cfe-p105">You can't synchronize partial replicas with other partial replicas. See the [PopulatePartial](database-populatepartial-method-dao.md) method for more information.</span></span>


