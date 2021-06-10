---
title: Database.Synchronize, méthode (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 411948f3c0ac4d6c353cd2722136dffb6a25fb17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294707"
---
# <a name="databasesynchronize-method-dao"></a><span data-ttu-id="7f079-102">Database.Synchronize, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="7f079-102">Database.Synchronize method (DAO)</span></span>


<span data-ttu-id="7f079-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f079-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7f079-p101">Synchronise deux réplicas. (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="7f079-p101">Synchronizes two replicas. (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f079-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f079-106">Syntax</span></span>

<span data-ttu-id="7f079-107">*.* Synchronize(***DbPathName***, ***ExchangeType***)</span><span class="sxs-lookup"><span data-stu-id="7f079-107">*expression* .Synchronize(***DbPathName***, ***ExchangeType***)</span></span>

<span data-ttu-id="7f079-108">*expression* Variable qui représente un objet **Database**.</span><span class="sxs-lookup"><span data-stu-id="7f079-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="7f079-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f079-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7f079-110">Nom</span><span class="sxs-lookup"><span data-stu-id="7f079-110">Name</span></span></p></th>
<th><p><span data-ttu-id="7f079-111">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="7f079-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="7f079-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="7f079-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="7f079-113">Description</span><span class="sxs-lookup"><span data-stu-id="7f079-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f079-114"><em>DbPathName</em></span><span class="sxs-lookup"><span data-stu-id="7f079-114"><em>DbPathName</em></span></span></p></td>
<td><p><span data-ttu-id="7f079-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7f079-115">Required</span></span></p></td>
<td><p><span data-ttu-id="7f079-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="7f079-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="7f079-117">Chemin d'accès au réplica cible, avec lequel la base de données est synchronisée.</span><span class="sxs-lookup"><span data-stu-id="7f079-117">The path to the target replica with which database will be synchronized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f079-118"><em>ExchangeType</em></span><span class="sxs-lookup"><span data-stu-id="7f079-118"><em>ExchangeType</em></span></span></p></td>
<td><p><span data-ttu-id="7f079-119">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7f079-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="7f079-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="7f079-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7f079-121">Constante <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> indiquant la direction de synchronisation des modifications entre les deux bases de données.</span><span class="sxs-lookup"><span data-stu-id="7f079-121">A <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> constant indicating which direction to synchronize changes between the two databases.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7f079-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="7f079-122">Remarks</span></span>

<span data-ttu-id="7f079-123">Vous utilisez **Synchronize** pour échanger des données et des modifications de conception entre deux bases de données.</span><span class="sxs-lookup"><span data-stu-id="7f079-123">You use **Synchronize** to exchange data and design changes between two databases.</span></span> <span data-ttu-id="7f079-124">Les modifications de conception ont toujours lieu en premier.</span><span class="sxs-lookup"><span data-stu-id="7f079-124">Design changes always happen first.</span></span> <span data-ttu-id="7f079-125">Les deux bases de données doivent se trouver au même niveau de conception avant de pouvoir échanger des données.</span><span class="sxs-lookup"><span data-stu-id="7f079-125">Both databases must be at the same design level before they can exchange data.</span></span> <span data-ttu-id="7f079-126">Par exemple, un échange de type **dbRepExportChanges** peut entraîner des modifications de conception au niveau d’un réplica, même si les modifications de données sont uniquement apportées de la base de données à DbPathName.</span><span class="sxs-lookup"><span data-stu-id="7f079-126">For example, an exchange of type **dbRepExportChanges** might cause design changes at a replica even though data changes flow only from the database to DbPathName.</span></span>

<span data-ttu-id="7f079-127">Le réplica identifié dans DbPathName doit faire partie du même jeu de réplicas.</span><span class="sxs-lookup"><span data-stu-id="7f079-127">The replica identified in DbPathName must be part of the same replica set.</span></span> <span data-ttu-id="7f079-128">Si les deux réplicas possèdent le même paramètre de propriété **ReplicaID** ou sont des réplicas-maîtres pour deux ensembles de réplicas différents, la synchronisation échoue.</span><span class="sxs-lookup"><span data-stu-id="7f079-128">If both replicas have the same **ReplicaID** property setting or are Design Masters for two different replica sets, the synchronization fails.</span></span>

<span data-ttu-id="7f079-129">Lorsque vous synchronisez deux réplicas sur Internet, vous devez utiliser la constante **dbRepSyncInternet**.</span><span class="sxs-lookup"><span data-stu-id="7f079-129">When you synchronize two replicas over the Internet, you must use the **dbRepSyncInternet** constant.</span></span> <span data-ttu-id="7f079-130">Dans ce cas, vous spécifiez une adresse URL (Uniform Resource Locator) pour l’argument DbPathName au lieu de spécifier un chemin d’accès au réseau local.</span><span class="sxs-lookup"><span data-stu-id="7f079-130">In this case, you specify a Uniform Resource Locator (URL) address for the DbPathName argument instead of specifying a local area network path.</span></span>


> [!NOTE]
> <span data-ttu-id="7f079-p105">[!REMARQUE] Vous ne pouvez pas synchroniser des réplicas partiels avec d'autres réplicas partiels. Pour plus d'informations, reportez-vous à la méthode [PopulatePartial](database-populatepartial-method-dao.md).</span><span class="sxs-lookup"><span data-stu-id="7f079-p105">You can't synchronize partial replicas with other partial replicas. See the [PopulatePartial](database-populatepartial-method-dao.md) method for more information.</span></span>


